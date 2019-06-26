@title[what-do-you-see]

### What's the difference between these functions?

```
function getFirstName(person) {
    return person.fullName.firtName;
}
```

```
function getFirstName(person) {
    return (person && person.fullName)? person.fullName.firstName : null;
}
```

---

@title[whats-saying]

Is the first function wrong and second one correct?

@ul

It depends.

Note:
    There are a few question that need to be answer before we can get to a conclusion

@ulend

---

@title[let-us-think-about-it]

### Can we trust on the data?

@ul

- Where's the data coming from? Is it coming from outside? Is it coming from your code?


@ulend

---

@title[let-us-think-about-it-2]

### Are there null/optional values?

@ul

- Can person be `null`?

- Is `fullName` optional?

@ulend


---

@title[is-it-safer]

### Do you have an answer to this questions?

@ul

- Is it safer just to be defensive because you don't know the answer?

- Is it easier?

@ulend

---

@title[is-it-safer]

When this questions cannot be answered there's a lack of understanding on how this code that you're looking at works.

Note:
    It is fine if you don't know how it works, it is impossible to understand/remember everything in a system

---

@title[feel-comfortable]

### Feeling comfortable with your code is important

The way of feeling comfortable **is not** adding guards to avoid possible ugly situations.
The way of feeling comfortable **is** to understand how things work,

---

@title[take-time]

### Address the main issue

It is important to take time to understand the code and help yourself by improving the code's reasonability

Note:
    - Put a pin in the reasonability thing, I'll come back later to that.

---

@title[why-is-this-important]

### Why is this important?

'cause fear and uncertainty spreads rapidly. Our code will get overly defensive.

Note:
    - It is just going to be harder and harder to understand when things can be really null and when we are just adding things "just in case"
    - This thing snowballs

---

@title[bugs]

### This can also lead to bugs

Sure, the thing might not blow up but it can end up in unexpected behaviour.

Note:
    - When we try to ignore this conditions we might be in fact swallowing an error.
    - When we provide fallback values we might be injecting data in the system that might break in a different point, good luck finding debugging.
    - If the thing had blown up we would have caught the bug much easily, with a decent stack trace, for example.

---
@title[reasonability]

It is really important to be able to reason about your code. Understand what's doing and why is doing it like that.


---

@title[types]

# Types help to reason about your code.

Note:
    When you add types you're helping the compiler to catch errors, but you are also helping yourself to understand what are the expected inputs and what are the things that you can do safely and what are the things that you have to be careful about.

---


@title[takes-away]

### Takes away

@ul

- Don't check just in case.
- Understand what's happening.
- Help others by improving the reasonability

@ulend

Note:
    - Make sure you understand what you're doing, if you have a null check, I wanna be able to assume that it is there because the data is optional

---

@title[recap]

### By not being overly defensive we gain in:

* Knowledge about our system and the systems that we interact with.
* More expressive and self self-explanatory code that is easier to reason about.
* Cleaner and faster code.
* Better error reports/less bugs in production*

Note:
    - I added that asterisk over there because I wanted to go deeper in the topic and maybe find some statistics but I could not do it, maybe another talk.
