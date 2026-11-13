# 💡 Light Switch Dark Mode

Dark mode, but it's a real switch. Flip a wall switch with a satisfying click and the whole page lights up in warm amber. Flip it back and it's night again.

**Live demo:** https://codewithomesh.github.io/light-switch/

**Watch the video:** https://www.youtube.com/@CodeWithOmesh

## Features

- Realistic rocker switch with a tiny locator light so you can find it in the dark
- Two-part click sound (press + snap) made with the Web Audio API, no audio files
- Warm "lights on" flicker and smooth dark ↔ light theme swap with CSS variables
- Text changes with the mood: "Hello, night owl." → "Good morning."
- Keyboard accessible (a real `<button>` with `aria-pressed`)
- One file, no libraries, no build step

## Run it

Download `index.html` and open it in any browser.

## How it works

```js
switchEl.addEventListener("click", () => {
  const on = document.body.classList.toggle("lights-on");
  switchEl.setAttribute("aria-pressed", on);
  playClick(on);
});
```

Every colour on the page is a CSS variable. Adding the `lights-on` class to `<body>` swaps all of them at once, and CSS transitions do the fade.

---

Made by **Code with Omesh** · Follow for more satisfying things built with code.
