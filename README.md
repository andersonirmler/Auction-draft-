# Auction Draft

A loud, fast party game for **1 host + 2 players**. Players bid out loud on mystery items. The host enters who won each item and what they paid. When both rosters are full, the judge scores both lineups.

**Play:** https://andersonirmler.github.io/Auction-draft-/

## How to play
1. Pick a mode: **Build the Perfect ___** or **Draft the Best ___** (50 categories each).
2. Enter the two player names. Adjust money ($20), items (10), and match length (best of 3) if you like.
3. Each round: category reveal → coin flip for who goes first → items appear one at a time. Turns alternate each item.
4. The host taps the winner and enters the price ($0 is allowed). **No bids** gives the item to the player whose turn it is, for $0. Once a roster is full, the other player gets the remaining items for $0.
5. Tap **Determine Who Won**. The judge scores every item. The higher total wins the round; ties go to the best single item, then synergy.
6. First to 2 round wins is the champion.

The host menu (☰) has sound on/off, undo, skip category and new game.

## Editing categories
All categories live in the `CATEGORIES` list near the top of the `<script>` in `index.html`:

```js
{ name: "Build the Perfect Face", items: [ /* 10 items: first 5 good, last 5 bad */ ] }
```

The first 5 items are the good ones and the last 5 are the bad ones. The judge uses that order to score, and the game shuffles items before revealing them.

## Notes
- Single file, no build step, no dependencies.
- The category deck order, saved game, and sound setting are kept in the browser's local storage. A category isn't repeated until every other category in that mode has been played.
