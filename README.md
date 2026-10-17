# Wish Lanterns

<a href="https://orbworlds.com/orb/wish-lanterns?utm_source=github&utm_medium=readme&utm_campaign=wish-lanterns"><img src="docs/screenshots/1.webp" alt="Wish Lanterns" width="100%"></a>

A quiet night sky over the water. Write a wish, let it go, and your lantern drifts up to join the ones everyone else has released. Tap any lantern to read what someone wished for. The wishes are shared, so the sky keeps filling up.

**[Play it on Orb](https://orbworlds.com/orb/wish-lanterns?utm_source=github&utm_medium=readme&utm_campaign=wish-lanterns)**. It runs in the browser on a computer, phone or tablet, and you
don't need an account.

<p>
  <img src="docs/screenshots/2.webp" alt="Wish Lanterns" width="100%">
</p>

## Controls

Drag to look around, tap a lantern to read its wish, and write your own in the box at the bottom.

## Run it yourself

```bash
git clone https://github.com/orbworlds/wish-lanterns
cd wish-lanterns
npm start
```

That opens it at http://127.0.0.1:4242 with the [Orb kit](https://github.com/orbworlds/kit),
which gives the game what it gets on Orb: other players (open a second tab, or press **+ Player**), saves and shared state.
You need Node 20 or newer, and nothing else.

The whole thing is `index.html`, 556 lines of HTML, CSS and JavaScript with
[three.js](https://threejs.org) from a CDN. Edit it and the page reloads.

What it uses from Orb's world SDK (`window.orb`, typed in [`orb-kit/orb.d.ts`](orb-kit/orb.d.ts)):

- `orb.room` for multiplayer (who is here, what they are doing, messages between players)
- `orb.store` for things everyone shares, like scores
- plain `localStorage` for progress, which Orb saves per player and brings along to their other devices

Outside Orb and the kit, `window.orb` isn't there and the game carries on without it.

## Make your own version

You can remix it on Orb without touching code: [open it there](https://orbworlds.com/orb/wish-lanterns?remix&utm_source=github&utm_medium=readme&utm_campaign=wish-lanterns), choose
**Make my own copy** and describe what you'd change. Orb's AI makes the changes in your copy.

Or fork this repository, make your changes and push them. `npm run share` then prints a link that
brings your fork into Orb as a world of your own, credited as a remix of this one, and it stays in
sync with your fork from then on.

## Contributing

Pull requests are welcome. GitHub checks each one by running the world in a headless browser, which has to go without errors,
and once a change is merged it's live on Orb within about 15 minutes. [CONTRIBUTING.md](CONTRIBUTING.md)
has the details.

## License

MIT, see [LICENSE](LICENSE). The Orb name and logo aren't covered by the license.
