# Week-12-George-Arbache
Recovery Code VgbBOfi7jDObvH43pjgrYJQhabC96BjIAQ8FA7MyTyc
• Node 1: Custom Character Asset Pipeline
	• Core Task: Import rigged 3D character mesh and animations.
	• Optimization Trigger: Consolidate materials into a single texture atlas to minimize draw calls.
	• Next Step: Point to Node 2.
• Node 2: Level of Detail (LOD) & Budget Check
	• Core Task: Enforce a strict poly budget (<15,000 triangles) and generate a 3-tier LOD chain.
	• Logic Gate: If camera is close \(\rightarrow \) stream full-resolution maps. If camera is distant \(\rightarrow \) swap to low-poly mesh and downscaled textures.
	• Next Step: Point to Node 3.
• Node 3: Contract Registry & Spawning
	• Core Task: Player interacts with the Bounty Board to accept a target contract.
	• System Action: Read target metadata and dynamically instantiate the unique target character model at a designated map waypoint.
  • Node 4: Navigation & Spatial Tracking
	• Core Task: Calculate real-time vector distances between the player coordinates and the target coordinates.
	• UI Update: Feed distance data into a screen-space tracking compass indicator.
	• Next Step: Point to Node 5.
• Node 5: High-Performance Target AI
	• Core Task: Execute tactical pathfinding routines (flee vs. ambush states).
	• Performance Strategy: Restrict asynchronous path calculations to proximity thresholds so distant targets do not drain CPU cycles.
