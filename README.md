# AppADay 075 — Fiefdom

**Live:** https://augustineiacopelli.github.io/appaday-075-fiefdom/
**Portfolio:** https://augustineiacopelli.github.io/appaday/

A deep strategy game of land and sea for one to six players, built as a single self-contained HTML file with no frameworks and no build step. It fuses the territorial conquest of Risk with a Monopoly-style resource economy, then adds fleets, feeding, a live commodity market, and a nuclear endgame. Humans play hotseat on one device alongside any number of AI houses.

## The world

Every game generates a fresh world as a Voronoi map of roughly fifty to ninety filled territories with real borders, oceans, and channels. Water is crossable only by ship, and some territories are true islands reachable only by sea. Each house starts with a small connected home cluster seeded with a farm, a mill, and a refinery, and the rest of the map begins as neutral ground held by light garrisons.

## The three phases

Each turn moves through three phases. In **Court** you take your income and manage your realm: set each land to a farm, mill, or refinery, muster and hire troops, build ships and arms, and trade at the market. In **March** you attack across land borders and across water, resolved with the familiar attacker-and-defender dice, single roll or blitz. In **Maneuver** you make one fortify move to consolidate.

## Economy and feeding

Income arrives at the start of your turn, harvest first and feeding second. Farms yield crops equal to your number of farms times four times a single die roll for the turn, mills yield two steel each, refineries yield ten gas each, and you collect one coin of tax per territory. Then every troop must eat one crop. If your harvest and stores cannot feed the whole army, the unfed troops each risk desertion at one in three, so a growing empire must keep its farms ahead of its soldiers.

## The market

The market trades both ways and its prices move with supply and demand on a single shared exchange that every house buys and sells against. Selling floods supply and drives a price down, buying creates demand and pushes it up, and a spread between the buy and sell price means round trips lose money, so there is no free arbitrage. Prices drift back toward their baseline over a few turns, so a crashed or spiked market recovers on its own. Crops are cheap and abundant, steel is scarce and swings hard, and gas sits in between. Because the AI sells its surplus into the same market, prices genuinely move over the course of a game.

## Fleets and invasion

Ships are a pooled fleet you build for steel while you hold at least one coastal land. Each ship carries up to ten troops, and a larger stack simply sails as more ships in one combined invasion, so a forty-troop army crosses as four ships. Crossing costs gas per ship, and ships spend for the turn and return to your pool next turn. The same fleet also ferries troops between your own coasts during Maneuver.

## The nuclear endgame

Launchers, interceptors, nukes, and rockets are forged from steel, with the first nuke and first rocket a coin-flip to complete. A launched nuke strikes an undefended target two times in three. The defender may answer with a salvo of rockets, declared all at once before anything is rolled, each intercepting at two in three, so committing more rockets sharply raises the odds of knocking the warhead down. A nuke that lands wipes everything on the site and leaves a permanent crater that no one can ever occupy or cross again. If more than five nukes ever detonate in a single game, nuclear winter ends the world and every house loses.

## The rival houses

AI opponents run their own economy, trade at the market, raise fleets, and press their own attacks at three levels of cunning. When a rival takes its turn, a panel narrates its moves step by step, what it built, whom it took land from, whether it sailed a fleet or launched a nuke, and the full account is kept in the Chronicle for review.

## Learning the game

New players can open a **How to Play** reference from the menu at any time, or start the built-in **Tutorial**, which walks you through your first full round with a coach that explains each phase as you reach it.

## Winning, conceding, and saving

Victory is simple: outlast every rival house and the realm is yours. A human player may concede at any time from the standings drawer, and an AI never will. Games save automatically and can be resumed later from the main menu, so a long campaign need not finish in one sitting.

## Technical notes

Single-file vanilla HTML, CSS, and JavaScript with Google Fonts as the only external dependency. The map generator, game engine, and AI are pure logic validated headlessly across six hundred full games with no crashes and no unresolved games, and the interface was smoke-tested through every phase, menu, the market, the tutorial, and the AI narrative. The renderer is SVG rather than canvas, all modals are custom, and local storage is guarded, so the app runs cleanly inside sandboxed WebKit as well as everywhere else. Fully responsive from a 375px phone through desktop.

---

*Ship something every day. It compounds.*
