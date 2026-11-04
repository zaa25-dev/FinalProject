(To the Codepath grader, I asked the professor about the amount of app ideas, and since I'm doing this alone rather than in a group, I can go with 3 rather than 6.)

Top 3 app ideas:

1. 
**PotholeMapper** is an automated civic telemetry and hazard-detection platform that turns everyday commutes into passive road-quality audits. Mounted on a vehicle dashboard, or sitting in a cup holder, the app continuously samples device motion sensors to detect vertical G-force drops and pothole impacts without requiring manual driver interaction. Detected hazards are automatically geostamped and uploaded to a persistent community road roughness index and an infinite media stream where users can browse, verify, and track severe local road infrastructure failures.

App Evaluation

-Category: Automotive / Civic Tech / Navigation & Utility

-Mobile: Uniquely mobile experience utilizing five distinct hardware and platform capabilities: high-frequency inertial Sensors (Accelerometer and Gyroscope) for impact classification, Location (GPS) for speed gating and coordinates, vector Maps for road roughness visualization, Audio for hands-free hazard proximity warnings, and the Camera for capturing visual proof of road damage.

-Story: Commercial navigation tools like Waze require manual screen taps that vanish after 30 minutes. Current city issue-reporting apps such as SeeClickFix require human input to file reports, which often aren't always filed. PotholeMapper provides hands-free passive sensing, creating an enduring public record of street conditions that can be compiled into municipal 311 repair dossiers to hold local public works departments accountable.

-Market: Daily automobile commuters, rideshare and delivery drivers, motorcyclists, cyclists, and municipal civil engineering teams seeking objective pavement condition data.

-Scope: The core technical scope centers on an isolated Z-axis impact detection algorithm (sqrt(x^2 + y^2 + z^2) - 1G) cross-referenced with GPS speed gating > 15mph to eliminate false positives from phone handling, followed by database synchronization and Mapbox/Google Maps rendering.

2. 

**KineticDash:** Motion-Controlled Endless Runner
KineticDash is a high-speed, kinetic endless runner where the player’s physical smartphone acts as the direct flight stick and motion controller. Rather than swiping on glass, players tilt, whip, drop, and flick their device in real physical space to dodge obstacles, jump bottomless chasms, and bank through tight neon urban tracks. Every run records dynamic motion telemetry alongside near-miss highlights, which are published to a community leaderboard

App Evaluation

-Category: Mobile Gaming / Arcade & Motion Action

-Mobile: Uniquely mobile experience utilizing five distinct hardware and platform capabilities: high-rate inertial Sensors (Accelerometer and Gyroscope) for real-time device tilt steering and vertical flick detection, Audio for spatial engine audio, collision chimes, and speed-barrier sonic booms, Location (GPS) for localized regional leaderboard matchmaking

-Story: Traditional mobile runners rely on stale swipe-to-turn gestures that flatten the thrill of high-speed reflexes. KineticDash treats the physical phone as an authentic flight yoke—tilting left and right steers lanes with analog precision, snapping the phone upward jumps obstacles, and ducking the device slides under laser barriers, delivering an authentic physical arcade experience that cannot be replicated on a desktop or console controller without specialized peripherals.

-Market: Casual and competitive mobile gamers, endless runner fans (Subway Surfers, Temple Run), arcade enthusiasts, and players seeking engaging kinetic physical games that do not require outdoor travel.

-Scope: The core technical scope focuses on low-latency device orientation polling (Sensor.TYPE_ROTATION_VECTOR or paired Accelerometer/Gyroscope values) to map pitch and roll directly to avatar lateral velocity and jump triggers (deltaY > 1.8G). Run metrics and replay telemetry vectors are synchronized via Firebase Firestore, alongside Google Maps SDK integration for local neighborhood dojo nodes.


3.

**TiltMaze** is a physics-based arcade marble maze where the player's phone acts as a physical balance board. Instead of using virtual joysticks or swiping across glass, the user tilts the phone in real space to roll a ball through dynamic 3D obstacle courses, avoiding pit traps, hitting speed boosters, and managing momentum. It includes a level builder where players snap a photo of everyday objects on their desk (mugs, pens, books) to generate custom hazard courses.

-Category: Mobile Gaming / Physics & Arcade

-Mobile: Uses five device capabilities: inertial Sensors (Accelerometer and Gyroscope) to directly map physical device tilt angles to marble acceleration vectors; Audio for low-latency physical impact sounds (wood clacks, metal rail rolls, trap drops); the Camera to photograph physical tabletop setups as templates for custom levels; Location (GPS) for local community course discovery.

-Story: Most mobile maze and physics games rely on touch-screen joysticks that feel detached and clunky. Using raw hardware tilt turns the entire phone into a physical wooden labyrinth board, making hand stability, micro-adjustments, and physical balance the core mechanics. This can't be matched on a PC or console without specialized motion hardware.

-Market: Casual mobile gamers, puzzle and arcade fans, and players who prefer tactile, single-player physics challenges that can be picked up for quick sessions indoors.

-Scope: The core technical scope uses Android's SensorManager to read device pitch and roll angles (Sensor.TYPE_ROTATION_VECTOR), applying those angles directly as 2D force vectors on a simple physics circle within a custom Android Canvas (vx += roll * dt). Custom course layouts and high-score run times sync to Firebase Firestore, with local leaderboard coordinates rendered on Google Maps.


Final Idea (for now): PotholeMapper 
