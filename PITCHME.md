@title[what-do-you-see]

### What's the difference between this functions?

```
function getFirstName(fullName) {
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

It depends

@ulend

---

@title[let-us-think-about-it]

### Can we trust on the data?

Where's the data coming from? Is it from outside? Is it coming from your code?

Do you need to program in a defensive way?

---

@title[let-us-think-about-it-2]

### Are there null/optional values?

Can person be null? Is fullName optional?

---

@title[is-it-safer]

Do you have an answer to this questions?
Is it safer just to be defensive because you don't know the answer?
Is it easier?

---

@title[is-it-safer]

If you cannot answer this questions shows a lack of understanding on how the code works, and that's okay.

---

@title[take-time]

It is important to take time to understand the code and help yourself by improving the code's reasonability*

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
    - When we try to ignore this conditions we might swallow an error.
    - When we provide fallback values we might be injecting data in the system that does not make sense and will break in a different point.
    - If the thing had blown up we would have catch the bug much easily, with a decent stack trace, for example.

---

@title[do-not-check-just-in-case]

* Don't check just in case.

Note:
    - Make sure you understand what you're doing, if you have a null check, I wanna be able to assume that it is there because the data is optional

---


@title[reasonability]

It is really important to be able to reason about your code. Understand what's doing, why is it doing it in a context.


---

@title[types]

# Types help to reason about your code.

Note:
    When you add types you're helping the compiler to catch errors, but you are also helping yourself to understand what to expected and what you can do safely.

---

@title[recap]

# By not being overly defensive we gain in:

* Knowledge about our system and the systems that we interact with.
* More reasonable code.
* Cleaner and faster code.
* Better error reports/less bugs in production*

Note:
    - When you add types you're helping the compiler to catch errors, but you are also helping yourself to understand what to expected and what you can do safely.
    - I added that asterisk over there because I wanted to go deeper in the topic and maybe find some statistics but I could not do it, maybe another talk.
