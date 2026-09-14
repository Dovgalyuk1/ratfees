# RAT — it runs the wallets and takes the fee

Static one-page site. No build step: `index.html` + `assets/`.

## The idea
The rat goes down the chain wallet by wallet looking for a fee left lying out. It takes one
crumb per wallet, carries it back to the hole, and everything that makes it home is split in
the same block: half to everyone holding $RAT, the rest burns. If a wallet looks up while the
rat is carrying, the crumb hits the floor and stays there — gone for everyone.

## The game — THE RUN
A stealth run, new mechanic for the series. Hold RUN to move, let go to freeze:
- The wallet's attention cycles on its own: **LOOKING AWAY** (green) → **TURNING…** (yellow,
  about a second) → **WATCHING YOU** (red). Moving when it goes red = caught, back to the hole,
  and any carried crumb is lost.
- Running makes **noise**; if the noise bar fills, the wallet turns early.
- Reach the crumb, pick it up (carrying is slower and noisier), carry it back through the hole.
- Eight wallets, each looking up more often and more suspicious than the last. Every wallet that
  gets through opens a page of TONIGHT'S HAUL.

## Assets
Cut from the one render Oleh sent: `assets/rat.webp` (the whole rat) and `assets/cheese.webp`
(the wedge in his paws, isolated by a yellow-only colour test — pink ears pass a naive
`R>180,G>110` test, so the mask also requires `G-B>55`).

## Sound
Paw patter, squeaks, a floorboard creak when the wallet starts to turn, a low alarm when caught,
a two-note chime coming home; music is a sneaky pizzicato walking bass with a plucked top line.

## Settings
```js
window.CONTRACT = "";   // contract address
window.TWITTER  = "";   // X link
window.BUY_URL  = "";   // buy link — BUY stays greyed out while empty
```
