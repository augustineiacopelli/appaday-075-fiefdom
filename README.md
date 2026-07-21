# AppADay 075 — Fiefdom

**Live:** https://augustineiacopelli.github.io/appaday-075-fiefdom/
**Portfolio:** https://augustineiacopelli.github.io/appaday/

A deep strategy game of land and sea for one to six players, built as a single self-contained HTML file with no frameworks and no build step. It fuses the territorial conquest of Risk with a Monopoly-style resource economy, then adds fleets, feeding, and a nuclear endgame. Humans play hotseat on one device alongside any number of AI houses.

## The world

Every game generates a fresh world as a Voronoi map of roughly fifty to ninety filled territories with real borders, oceans, and channels. Water is crossable only by ship, and some territories are true islands reachable only by sea. Each house starts with a small connected home cluster seeded with a farm, a mill, and a refinery, and the rest of the map begins as neutral ground held by light garrisons.

## The three phases

Each turn moves through three phases. In **Court** you take your income and manage your realm: set each land you hold to one of three resources, muster your free reinforcements, hire troops for coin, build ships in the Shipyard, forge arms in the Arsenal, and sell surplus at the Market. In **March** you attack across land borders and across water, resolved with the familiar attacker-and-defender dice, single roll or blitz. In **Maneuver** you make one fortify move to consolidate.

## Economy and feeding

Income arrives at the start of your turn, harvest first and feeding second. Farms yield crops equal to your number of farms times four times a single die roll for the turn, mills yield two steel each, refineries yield ten gas each, and you collect one coin of tax per territory. Then every troop must eat one crop. If your harvest and stores cannot feed the whole army, the unfed troops each risk desertion at one in three, so a growing empire must keep its farms ahead of its soldiers.

## Fleets and invasion

Ships are a pooled fleet you build for steel while you hold at least one coastal land. Each ship carries up to ten troops, and a larger stack simply sails as more ships in one combined invasion, so a forty-troop army crosses as four ships. Crossing costs gas per ship, and ships spend for the turn and return to your pool next turn. The same fleet also ferries troops between your own coasts during Maneuver.

## The nuclear endgame

Launchers, interceptors, nukes, and rockets are forged from steel, with the first nuke and first rocket a coin-flip to complete. A launched nuke strikes an undefended target two times in three. The defender may answer with a salvo of rockets, declared all at once before anything is rolled, each intercepting at two in three, so committing more rockets sharply raises the odds of knocking the warhead down. A nuke that lands wipes everything on the site and leaves a permanent crater that no one can ever occupy or cross again. If more than five nukes ever detonate in a single game, nuclear winter ends the world and every house loses.

## Winning, conceding, and saving

Victory is simple: outlast every rival house and the realm is yours. A human player may concede at any time from the standings drawer, and an AI never will. Games save automatically and can be resumed later from the main menu, so a long campaign need not finish in one sitting.

## Technical notes

Single-file vanilla HTML, CSS, and JavaScript with Google Fonts as the only external dependency. The map generator, game engine, and AI are pure logic validated headlessly across six hundred full games with no crashes and no unresolved games, and the interface was smoke-tested through every phase and menu. The renderer is SVG rather than canvas, all modals are custom, and local storage is guarded, so the app runs cleanly inside sandboxed WebKit as well as everywhere else. Fully responsive from a 375px phone through desktop.

---

*Ship something every day. It compounds.*
