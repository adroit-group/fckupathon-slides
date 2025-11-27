---
theme: apple-basic
title: "Fckupathon Game of Codes: Winter is encoding"
drawings:
  persist: false
transition: slide-up
mdc: true
layout: center
---

<img src="/meetup-logo.svg" width="582" height="90" />
Game of Codes: Winter is Encoding
<img src="/powered-by.svg" width="400" height="400" />

---
layout: two-cols
---

# We're Adroit.

A fully remote developer team based in Hungary, crafting beautiful and functional products, websites, and mobile apps.

<iframe src="https://giphy.com/embed/B4dt6rXq6nABilHTYM" width="380" height="382" style="" frameBorder="0" class="giphy-embed" />

::right::

Come work with us!
<QRCode value="https://adroitgroup.io/career" />

<!--
- We are a remote development company, we do everything from devopsy stuff through huge distributed systems to mobile apps.
- I'm me and these beautiful ppl are the team who helped build this so big shoutout to dem! <3
- If you are a devopsy or salesy person come talk to us if u looking for a new opportunity.
-->

---
layout: two-cols
---

# Agenda

<v-clicks>

- `1732724200` Introduction (\*pls add some cringe ahh meta joke, cuz we already in the middle of it)
- `2025-11-27T18:00:00.500000+01:00` Team forming and committing war crimes
- `2025-11-27T19:30:00` Pizza break
- `Thursday, 27-Nov-25 21:00:00 CET`

  We gather and we weep (and vote!)

</v-clicks>

::right::

<iframe src="https://giphy.com/embed/137TKgM3d2XQjK" width="471" height="480" style="" frameBorder="0" class="giphy-embed" />

<!--
- It's recommended to form 4-5 ppl teams and split up the tasks but we're not yo mama.
- Yes the pizza is free, we know that's why you guys are here anyways.
- It's crazy that you cannot commit war crimes anymore without it being an implicit political statement, but I did it anyways.
-->

---

# Tonight's task!

Since winter is coming...

<v-clicks>

- Write the most catastrophic data format with an encoder and a decoder, that a whole team can't debug before the holidays. _(What is dead may never die... just like your legacy code.)_
- You have ~~7 seasons~~ 3 hours to finish the task.
- You have to have at least a working encoder or a decoder.
- Don't write any documentation!!!!!! _(You know nothing, Jon Snow, and neither should your teammates.)_
- Tech stack is literally whatever. Python, Rust, carrier pigeons, we don't care.
- We recommend 4-5 people teams, but fr do whatever makes you happy.
- **The Walk of Shame**: 5 mins to flex your unhinged creation to the world
- Audience gonna vote on who cooked the hardest crime against humanity (in code form)

</v-clicks>

---
layout: two-cols
---

# Example Time

Here's the deal: we got an **input.json** with some complex data.

Right now it's boring JSON, but your job? Make it _absolutely unhinged_.

<QRCode size="200" value="https://adroit-group.github.io/fckupathon-slides/slides-11-27/input.json" />

[https://adroit-group.github.io/fckupathon-slides/slides-11-27/input.json](https://adroit-group.github.io/fckupathon-slides/slides-11-27/input.json)

::right::

```typescript {monaco-run} {height:'400px', showOutputAt:'+1'}
function encode(data: any): string {
  const encoded = Object.entries(data).map(([key, val]) => {
    const keyEncoded = key
      .split("")
      .map((c) => c.charCodeAt(0).toString(36))
      .join(".")

    const type =
      typeof val === "string" ? "S" : typeof val === "number" ? "N" : "O"

    const valEncoded = JSON.stringify(val)
      .split("")
      .map((c) => c.charCodeAt(0))
      .reverse()
      .join(".")

    return `${keyEncoded}🔥${type}🔥${valEncoded}💀`
  })

  // Winter is coming, after all
  return encoded.join("🌨️")
}

const lenny = {
  name: "Tyrion Lannister",
  age: 24,
  tldr: "Drinks and knows things",
}

console.log(encode(lenny))
```

<!--
- Lucky for me we don't have to center a div, cuz the dot breaks the word wrap in the eval loop, let's fix that really quick. (this is intentional)
- Without throwing shade the value encode comes from one of the biggest delivery company's public API docs, allegedly ofc.
-->

---
layout: center
---

# Voting

<QRCode value="https://strawpoll.com/kjn1DXoeeyQ" />

<!--
Todo: please be so kind to add the url for the voting good sir!-
-->

---
layout: end
---

# Thank you for your time!

You can find this presentation right here:
| | |
|--- | --- |
|[https://adroit-group.github.io/fckupathon-slides/slides-11-27](https://adroit-group.github.io/fckupathon-slides/slides-11-27) | <QRCode size="200" value="https://adroit-group.github.io/fckupathon-slides/slides-11-27" />|

<img src="/powered-by.svg" width="400" height="400" />
