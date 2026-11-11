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

Why we chose these: They’re free, beginner-friendly, and work well for a small team with limited time. Open question: Do we need any extra add-ons for saving scores, or is the built-in system enough?
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
communication: 

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
