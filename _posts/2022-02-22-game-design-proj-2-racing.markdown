---
layout: post
title:  "Game Design: Drift Star"
date:   2022-02-22 12:00:00 -0400
categories: project school
lastpost: "Game Design: Zelda Dungeon Recreation"
lastposthref: "./project/school/2022/02/06/game-design-proj-1-zelda.html"
nextpost: "Game Design Capstone: Coconaut"
nextposthref: "./project/school/2022/04/19/game-design-proj-3-exploration.html"
---

EECS494

Game Design, University of Michigan

<h2>Task</h2>

![Screenshot of Drift Star](/images/drift_gif.gif)

For EECS494: Game Design at the University of Michigan, I was tasked with creating a game where the sky is the limit but must be completed within 2 weeks. The game must exemplify some game concepts including but not limited to:
- Interesting or unique gameplay mechanics - think Mirror's Edge
- Small or repetitive actions that build on eachother - think Angry Birds 
- World building - think region progession or narrative notes found in a game 

So I went to what I love most: cars, tires spinning, and lots of smoke.

<h2> Design </h2>

![Screenshot of Drift Star](/images/drift_screenshot_2.png)

The concept started simple as a drifting game. I had played quite a few indie drifting games and they're quite fun. But then I wanted to add something I love - like a lot - rally!

So thus the concept was born for Drift Star is a game where you are a boy racer in a classic, Group A Subaru; bending corners to get the highest points and hold the longest drift.

There are numerous stages included, each with a timer and high score.

<h2> Gameplay </h2>

![Screenshot of Drift Star](/images/drift_screenshot_1.png)

<h3> Car Physics </h3>

- Thankfully Unity makes a tidy built-in library for vehicles - even modeling torque and contact points on a tire
    - Use the tire 'slipage' calculation and then you can sense when a drift happens 
- Made global systems available for users

<h3> Scoring </h3>

- Design such that greater counter-steer angle = greater points
    - Usually means the driver is making very tight drifts (which are much harder than wide ones)
    - Chain has 1s debounce too!
- Go through the rings to advance forward! 
    - Miss one and you'll have to restart 

<h3> Stages </h3>

- All levels made with Unity terrain editor
    - Have to place assets at startup    
- Thanks to [ambientcg.com](https://ambientcg.com/) for textures
- Thanks to [Ada_King](https://marketplace.unity.com/packages/3d/vegetation/trees/free-trees-103208) for free trees!

<h3> Relaxing Mode </h3>

- No timer, score or checkpoint!

![Screenshot of relaxing mode](/images/drift_screenshot_4.png)


<h2> Download </h2>

![Screenshot of Drift Star](/images/drift_screenshot_3.png)

*Please extract before running*

[Download for Windows](/downloads/drift-star-win.zip)

[Download for MacOS](/downloads/drift-star-mac.zip)