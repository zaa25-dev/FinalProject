(To the Codepath grader, I asked the professor about the amount of app ideas, and since I'm doing this alone rather than in a group, I can go with 3 rather than 6.)

Top 3 app ideas:

1. 
**PotholeMapper** is an automated civic telemetry and hazard-detection platform that turns everyday commutes into passive road-quality audits. Mounted on a vehicle dashboard, or sitting in a cup holder, the app continuously samples device motion sensors to detect vertical G-force drops and pothole impacts without requiring manual driver interaction. Detected hazards are automatically geostamped and uploaded to a persistent community road roughness index and an infinite media stream where users can browse, verify, and track severe local road infrastructure failures.

App Evaluation
-Category: Automotive / Civic Tech / Navigation & Utility
-Mobile: Uniquely mobile experience utilizing five distinct hardware and platform capabilities: high-frequency inertial Sensors (Accelerometer and Gyroscope) for impact classification, Location (GPS) for speed gating and coordinates, vector Maps for road roughness visualization, Audio for hands-free hazard proximity warnings, and the Camera for capturing visual proof of road damage.
-Story: Commercial navigation tools like Waze require dangerous manual screen taps that vanish after 30 minutes. Current city issue-reporting apps such as SeeClickFix require human input to file reports. PotholeMapper provides hands-free passive sensing, creating an enduring public record of street conditions that can be compiled into municipal 311 repair dossiers to hold local public works departments accountable.
-Market: Daily automobile commuters, rideshare and delivery drivers, motorcyclists, cyclists, and municipal civil engineering teams seeking objective pavement condition data.
-Scope: The core technical scope centers on an isolated Z-axis impact detection algorithm (sqrt(x^2 + y^2 + z^2) - 1G) cross-referenced with GPS speed gating > 15mph to eliminate false positives from phone handling, followed by database synchronization and Mapbox/Google Maps rendering.

2. f

3. 


Final Idea (for now): PotholeMapper 
