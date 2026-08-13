---
layout: post
title:  "Game Design: Zelda Dungeon Recreation"
date:   2022-02-06 12:00:00 -0000
categories: project school
nextpost: "Game Design: Racing Game Creation"
nextposthref: "./project/school/2022/02/22/game-design-proj-2-racing.html"

---

EECS494

Game Design, University of Michigan

<h2> Task </h2>

![Screenshot of Zelda](/images/zelda_screenshot_1.png)

My team - Andriy Massamilla and I - were tasked with recreating one of the most beloved moments in video game history - the first ever Zelda dungeon.

The only items given are screenshots, video walkthroughs, and some basic sprites for the game. The rest was left to us. Everything from mapping the sprites to models with hitboxes, creating a movement and attack system, to even a final boss fight with hit effects.

Beyond the recreation of the dungeon, we were also tasked with creating a 'remix' of the dungeon, introducing our own elements to the game (as long as it is not a grappling hook like Fortnite, Apex Legends, or countless other games).

<h2> 'Remix'</h2>

![Screenshot of Zelda Remix mode](/images/zelda_screenshot_remix.png)

*Press '4' to enter remix mode!*

Andriy and I looked for a novel element that was fun, would not require substantial reworking of the dungeon, and would be easy for anyone to play. A few games came to mind: Super Hot - where time only advances when you move; Portal - where you can use a special tool to unlook portals to solve puzzles; and Crypt of the NecroDancer - where you must press on-beat to move around and attack enemies.   

Crpyt of the NecroDancer was extremely fun and did not require too much work to implement... Our 'remix' would involve moving and slashing to the beat of a song! Each movement on-beat would allow you to attack and move. But miss a beat and you lose your chance to move or attack for that beat! 

*Special thanks to Crpyto of the NecroDancer for the inspiration*

<h2> Gameplay </h2>

![Screenshot of Zelda](/images/zelda_screenshot_2.png)

*Press '1' to toggle infinite items*

*Press '2' to toggle god mode*

<h3> Movement </h3>
- Have you ever watched Zelda and realized when you move in one axis (i.e. vertical or horizontal), then try to move in the other axis, it will align you to the nearest block in an axis?
    - Every time the axis of movement changes, it realigns the player to the nearest block! (e.g. dungeon tiles or grass tiles)
    - Recreating this mechanic took a while to figure out until we realized we can introduce a state such that we track if their movement changed axis, then teleport the player to nearest full block 
- Enemies are pretty much 'on rails' (LERP-ing and SLERP-ing between points like the player and their starting point) or simple agents (e.g. go left five blocks, hold, turn right, ...; if player_dist < 5 blocks -> turn_to_player, move, ...)


<h3> Health / Inventory System</h3>
- Simple raycast around player for things that damage it 
- Health implementation is simply value where HP is a running value and a few lives. Plus some animations and stuff like `hp <= 0 -> death()` 
- Each item has a template of an item class then gets action called when keypress happens
    - Added fun animations and sounds for each instance like the bomb!
- Inventory is array and has way to add/discard
    - Keep it simple - one struct and three methods: add, remove, interact 


<h3> Enemies / Fighting System</h3>
- There are numerous enemies including the Dragon!
- Traps are quite challenging to get the movement right - I won't reveal my secrets as to not spoil others

![Screenshot of Zelda](/images/zelda_screenshot_4.png)

<h3> Remix System </h3>
- Move to the beat of the song! Try as hard as you can, otherwise you'll be dazed and miss a beat
    - *There are some slight bugs. But given only a few days and learning Unity only a few weeks prior, I am proud of it.*
- Using Royalty Free Music 


<h2>Download</h2>

![Screenshot of Zelda](/images/zelda_screenshot_3.png)

*Please extract before running*

[Download for Windows](/downloads/loz-remake-win.zip)

[Download for MacOS](/downloads/loz-remake-mac.zip)
