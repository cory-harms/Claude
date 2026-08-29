# Bank It!

A phone-friendly scorekeeper for **BANK**, the push-your-luck party dice game.
One person keeps score while the table rolls two real dice — the app runs the
bank, the turn order, the banking, and the stats.

**▶ Play it live: https://cory-harms.github.io/Claude/**

**No installs, no dependencies.** It's a single `index.html` — open it in any
browser (or host it anywhere, e.g. GitHub Pages) and play.

## The rules it runs

- Players take turns rolling two dice; every roll feeds a shared pot — **the bank**.
- **Rolls 1–3 (safe):** every sum is added, and a **7 adds 70**. Doubles just add face value.
- **Roll 4 onward (danger):** **doubles double the whole bank**, and a **7 wipes the bank**
  and ends the round — anyone not banked scores nothing.
- Between rolls, any player can hit **BANK** to lock the current pot into their score
  and sit out the rest of the round.
- A round ends on a 7 or when everyone has banked. Highest total after the last
  round (5 / 10 / 15 / 20, your pick) wins.

## Features

- One-tap roll entry (2–12), with dedicated 7 and DOUBLES keys that switch
  behavior automatically between the safe and danger phases.
- **Live stats per player: how many doubles and how many 7s each player has
  rolled**, plus times banked and best single bank — shown on the player cards
  mid-game and in the final ledger.
- Tap-to-bank per player, automatic turn order that skips banked players,
  round-over and final-standings screens.
- Full **undo** (works even after a seven-out or from the final screen).
- Auto-saves to the device — close the tab mid-game and pick it back up.
- Rematch with the same table in one tap.

## Development

Game logic lives between the `__LOGIC_START__` / `__LOGIC_END__` markers in
`index.html` as pure functions, so it can be extracted and unit-tested in Node
without a browser.
