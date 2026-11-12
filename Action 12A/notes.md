# George Arbache

# prep
repo: https://github.com/garbache3372-sys/Week-12-George-Arbache
gitTest: Commit works good
access: Team
video1:  We observed why mindset is important, my question I have is How to develop a growth mindset when doing game development? We also noticed that when you do game development you have to have a good mindset.
video2: We observed collaboration during game development, Why is a growth mindset important? We also seen that you have to been open to recieve feedback, celebrating small wins after acheiving the mission.
video3: Professor Stalbert shows us how to create the folders, how we log everything, the reason why we have folders because it's good to be organized so your not having a mess of files everywhere and get lost. Why is it important to make a folder
video4: I learned that documentation is an important part of game development because it helps keep track of the game's progress, ideas, and development process. Keeping organized notes and documenting changes can make it easier to work on the game, remember important details, and communicate with other team members. What information should we include in our game development documentation to make sure our project stays organized? I used ChatGPT to get my answer.
video5: I learned that following the game development process step by step helps keep the project organized and makes it easier to understand what needs to be completed. Taking notes and keeping track of progress helps prevent mistakes and makes it easier to continue working on the game later. How can we use what we learned in this video to improve our own game project? I used ChatGPT to get my answers.
video6: I successfully imported the custom player 3D model and rigged skeleton into the game engine pipeline. The mesh, textures, and animations mapped correctly without breaking the default bone hierarchy. I created a reusable asset import preset inside the engine. This automatically configures rigging settings, materials, and scale factors for any future custom characters added to the project. How do we optimize the texture resolution and polygon count of this custom player model to maintain a stable frame rate when multiple characters are on screen at once? I used Google Gemini to answer the question.
opinion: I implemented the core tracking mechanic for the bounty contracts, linking target NPCs to a dynamic UI board. I decided to use a vector-based distance check to update a compass indicator, showing the player the relative direction of their bounty target. The target spawning system accurately reads the contract data, instantiates the unique boss model at a designated waypoint, and triggers the "Wanted: Alive or Dead" UI prompt when the player enters the zone. What is the most efficient way to manage target pathfinding across large maps so they can actively flee or ambush the player without causing performance drops? I use Google Gemini to answer the question.
questions: What are the expectations for this team?
What goals will this team do?

# prepBoard
notes:  I put the notes in order on what we did for our Bounty App. I used Google Gemini to get the answers

# pitch
understand: “I understand that bounty hunting involves tracking down a target, gathering information, and completing the assigned task safely and responsibly. The finish line is successfully locating the target, meeting the objectives, and providing proof that the job has been completed.”

offer: “I bring good teamwork, communication, and problem-solving skills. I can help track down targets, gather useful information, pay attention to details, and support my teammates so we can complete the bounty successfully.”
limits: “I still need to learn more about tracking techniques, identifying targets, gathering accurate information, and planning successful missions. I also want to improve my communication and teamwork skills so I can help the team better.”
availability: 
Preferred contact: Discord
I'm always avaliable on discord classroom, phone number, social media, etc.
tools: We are using ChatGPT, Discord, Visual Studio, Unity.
aiTool: AI: ChatGPT, Claude, Gemini
Task: ChatGPT, Claude, Gemini will help us complete our project, answer questions, etc.
Verification: Testing the codes though Visual Studio checking sources, etc.

# availability
notes: I'm always avaliable on discord classroom, phone number, social media, etc.

## slots

contact: Discord

# aiPlan
name: ChatGPT, Claude, Gemini
task: ChatGPT, Claude, Gemini will help us complete our project, answer questions, etc.
verify: Testing the codes though Visual Studio checking sources, etc.

# huddle
mission: We are going to convert the Bounty Hunting App into a game where the player will actually hunt for the criminals.
framework: We chose P2P.
pipeline: Unnamed stage
Unnamed stage
Unnamed stage
Unnamed stage
Unnamed stage
Unnamed stage
Placeholder · owner Bounty Sketch 
Placeholder · owner Connector
We put everything in order and used Claude Ai to give us the answers
tech: Engine: Unity. It’s free, lightweight, and has good beginner tutorials, so everyone can install it and start quickly.

Language: Unity C#. It’s built into Godot and easy to read, so teammates can understand each other’s code.

Packages/add-ons: Godot’s built-in 2D/3D tools (sprites, collision, UI nodes) so we don’t depend on extra downloads that might break.

Assets: Free, license-friendly art and sound (for example from Kenney.nl or OpenGameArt), plus our own wanted-poster designs made in Canva or Figma. We chose free assets so we don’t have copyright problems.

Who checks them:

[Leah Aluni] checks that the engine and code run on every team member’s computer.
[Nicolas Kuhnast] checks that every asset has a license that lets us use it.
[George Arbache] tests the finished build after each change.

Why we chose these: They’re free, beginner-friendly, and work well for a small team with limited time. Open question: Do we need any extra add-ons for saving scores, or is the built-in system enough? I used Claude to get the answer
code: Start / Update
Callback | What happens | Verified
Awake() | Sets up references (player, bounty list) before the game starts | [x]
Start() | Loads the first bounty and sets the score to 0 | [x]
Update() | Every frame: reads player input, moves the player, checks if the bounty is caught | [x]
OnCollisionEnter2D() | Runs when the player touches a bounty target, then adds the reward to the score | [x]

Classes & components
Class | Responsibility | GameObject
PlayerController | Reads input and moves the player; checks when the player touches a bounty | Player
BountyTarget | Stores each target’s name, difficulty, and reward value | Bounty (prefab)
GameManager | Tracks the score and which bounty is active; decides when the game ends | GameManager (empty object)
UIManager | Updates the score text and shows the win or game over screen | Canvas

Packages / using
Package / namespace | Why included | Tested
using UnityEngine; | Gives access to the core engine tools our scripts need, like MonoBehaviour, Transform, Input, and Vector2 | [x]
using UnityEngine.UI; | Lets us update the score text and buttons on the screen from code | [x]
using System.Collections.Generic; | Lets us use List<> to store the bounty list and loop through it | [x]
using UnityEngine.SceneManagement; | Lets us reload the scene when the player restarts after winning or losing | [x]
communication: Team check-ins
Description / contact / owner | When · Pacific | Agreed
George Arbache  | 2026-11-10T15:48 | [x]
reuse: PlayerController script (our own code). Source: written by our team. Credit: none required, but we’ll keep our names in the code comments.
GameManager and score system (our own code). Source: written by our team. Credit: none required. It can be reused for any game that tracks points or objectives.
Bounty data structure (BountyTarget class). Source: our team. Credit: none required. We can swap in new characters, rewards, and difficulty levels for a new story.
Free art and sound assets (for example from Kenney.nl or OpenGameArt). Source: the website and creator’s name, saved in a credits file. Credit: we’ll check each license, since some (CC0) need no credit and others (CC-BY) require us to name the creator.
Our wanted-poster and menu designs (Canva or Figma). Source: our team. Credit: if we used Canva templates or stock elements, we’ll check Canva’s license terms before reusing them. I used Claude for my answer.
boardNotes: What the huddle board is: A shared space where our team writes down what we discussed, what we agreed on, and what we still need to figure out, so nobody has to rely on memory and everyone can see the same plan.

Decisions we made:

We will build the game in [Godot/Unity] using [GDScript/C#], because it’s free and beginner-friendly.
We will keep the game small: at least 3 bounties, a score system, and a win or game over screen.
We will use free, license-friendly assets and keep a credits file listing each source.
Each person owns one part of the pipeline: [Name 1] inputs, [Name 2] building, [Name 3] design, [Name 4] testing.

Disagreements:

Some of us wanted more bounties and extra levels, while others wanted to finish a smaller game that works. We agreed to finish 3 bounties first and add more only if time is left.
We discussed whether to draw our own art or use free assets. We chose free assets for the characters and made our own wanted posters.

Questions that remain open:

Do we need an extra add-on to save high scores, or is the built-in system enough?
Who will double-check that every asset’s license allows us to reuse it?
How many classmates can test the game before the deadline? I used Claude to get the answers

# pipelineBoard
notes: We put everything in order and used Claude Ai to give us the answers

# codeTables

## 0
id: f755df56-99d0-432a-9e1f-74ecc1902297
title: Start / Update

### columns

#### 0
label: Callback
type: text

#### 1
label: What happens
type: text

#### 2
label: Verified
type: checkbox

### rows

#### 0
0: Awake()
1: Sets up references (player, bounty list) before the game starts
2: true

#### 1
0: Start()
1: Loads the first bounty and sets the score to 0
2: true

#### 2
0: Update()
1: Every frame: reads player input, moves the player, checks if the bounty is caught
2: true

#### 3
0: OnCollisionEnter2D()
1: Runs when the player touches a bounty target, then adds the reward to the score
2: true

## 1
id: c0b5405d-1eba-4c5e-8cd3-c3785ef3b8e8
title: Classes & components

### columns

#### 0
label: Class
type: text

#### 1
label: Responsibility
type: text

#### 2
label: GameObject
type: text

### rows

#### 0
0: PlayerController
1: Reads input and moves the player; checks when the player touches a bounty
2: Player

#### 1
0: BountyTarget
1: Stores each target’s name, difficulty, and reward value
2: Bounty (prefab)

#### 2
0: GameManager
1: Tracks the score and which bounty is active; decides when the game ends
2: GameManager (empty object)

#### 3
0: UIManager
1: Updates the score text and shows the win or game over screen
2: Canvas

## 2
id: 964a5672-74ca-40a8-8427-ccc9b1295e38
title: Packages / using

### columns

#### 0
label: Package / namespace
type: text

#### 1
label: Why included
type: text

#### 2
label: Tested
type: checkbox

### rows

#### 0
0: using UnityEngine;
1: Gives access to the core engine tools our scripts need, like MonoBehaviour, Transform, Input, and Vector2
2: true

#### 1
0: using UnityEngine.UI;
1: Lets us update the score text and buttons on the screen from code
2: true

#### 2
0: using System.Collections.Generic;
1: Lets us use List<> to store the bounty list and loop through it
2: true

#### 3
0: using UnityEngine.SceneManagement;
1: Lets us reload the scene when the player restarts after winning or losing
2: true

# communicationTables

## 0
id: 94fbcf11-58d1-405b-b8c3-f121cee8b18c
title: Team check-ins

### columns

#### 0
label: Description / contact / owner
type: text

#### 1
label: When · Pacific
type: datetime-local

#### 2
label: Agreed
type: checkbox

### rows

#### 0
0: George Arbache 
1: 2026-11-10T15:48
2: true

# huddleBoard
notes: Our mission is to build a playable bounty hunting game with at least three bounties, a score system, and a win or game over screen. In our huddle we compared our ideas for the mission and agreed to keep the game small so we can finish it.

The diagram shows the mission at the top, connected to three jobs. [Name 1] builds the game and scoring. [Name 2] designs the posters, menus, and art. [Name 3] tests the game, keeps the bug list, and checks that every asset’s license lets us use it. All three jobs lead to the finished prototype at the bottom.

We decided that each person owns one job so nothing is missed, and that we will check in again before the deadline. One disagreement was whether to add more bounties or finish a smaller game first, and we chose to finish three bounties first. One open question is how we will save high scores. we used claude to get the answers

# reportA
checkpoint: Today, I worked on developing our Bounty Hunting video game. I contributed ideas for the gameplay, including how players will find targets, track down bounties, complete missions, and earn rewards. I also helped plan the game's objectives and features to make it exciting and engaging for players. For Day B, I plan to continue developing the game, improve the bounty hunting missions, and work on making the gameplay more detailed and enjoyable. I used Chatgpt.
evidence: Today, I worked on our Bounty Hunting video game by coming up with ideas for missions, tracking targets, and earning rewards. I helped plan how the game would work and what features would make it fun. For Day B, I plan to continue improving the game, add more ideas, and work with my team to make progress. I used ChatGPT.
next: My next task is to continue working on our Bounty Hunting video game by improving the missions, adding new features, and making sure the gameplay works well. I plan to finish my part by the next work session. If I run into any problems, I will ask my teammates for help and work together to find a solution. I used ChatGPT.

# reportABoard
notes: What the board shows: The center is our game, a bounty hunting game where the player takes contracts to track down targets. Around it are the main systems: [list yours]. The arrows show the core loop: the player accepts a bounty, tracks and catches the target, earns a reward, then upgrades gear for harder bounties.

Decisions we made:

[e.g., The game is 2D top-down / 3D third-person]
[e.g., Each of us owns one system: George, Leah, Nick]
[e.g., First milestone is one playable mission with one target]