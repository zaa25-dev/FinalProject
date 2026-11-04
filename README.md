# Milestone 1 - PotholeMapper (Unit 7)

## Table of Contents


---

## Overview

### Description

PotholeMapper is an automated civic telemetry and hazard-detection platform that turns everyday commutes into passive road-quality audits. 
Mounted on a vehicle dashboard, or sitting in a cup holder, the app continuously samples device motion sensors to detect vertical G-force drops and pothole impacts without requiring manual driver interaction. 
Detected hazards are automatically geostamped and uploaded to a persistent community road roughness index and an infinite media stream where users can browse, verify, and track severe local road infrastructure failures.

### App Evaluation

Category: Automotive / Civic Tech / Navigation & Utility

Mobile: Uniquely mobile experience utilizing five distinct hardware and platform capabilities: high-frequency inertial Sensors (Accelerometer and Gyroscope) for impact classification, 
Location (GPS) for speed gating and coordinates,
vector Maps for road roughness visualization, 
Audio for hands-free hazard proximity warnings, and the 
Camera for capturing visual proof of road damage.

Story: Commercial navigation tools like Waze require manual screen taps that vanish after 30 minutes. Current city issue-reporting apps such as SeeClickFix require human input to file reports. 
PotholeMapper provides hands-free passive sensing, creating an enduring public record of street conditions that can be compiled into municipal 311 repair dossiers to hold local public works departments accountable.

Market: Daily automobile commuters, rideshare and delivery drivers, motorcyclists, cyclists, and municipal civil engineering teams seeking objective pavement condition data.

Scope: The core technical scope centers on an isolated Z-axis impact detection algorithm (`sqrt(x^2 + y^2 + z^2) - 1G`) cross-referenced with GPS speed gating > 15mph to eliminate false positives from phone handling, followed by database synchronization and Mapbox/Google Maps rendering.

---

## Product Spec

### 1. User Features (Required and Optional)

#### Required Features

* **Automated Impact Detection & Telemetry Logging:** Passively records vertical G-force spikes, timestamp, vehicle transit speed, and exact GPS coordinates when a pothole is struck.
* **Surface Roughness Map:** Interactive vector map displaying road segments color-coded by road smoothness alongside discrete high-impact hazard pins.
* **Drive HUD / Sensor Dashboard:** Live real-time dashboard displaying current transit speed, live G-meter accelerometer deflection, and trip logging controls.

#### Optional Features

* **Camera Capture:** Those who want can snap a picture of the road to share how the road looks in reality. 
* **Auditory Proximity Alerts:** Spoken audio warning chime when approaching a verified high-impact hazard cluster within 200 feet.

---

### 2. Screen Archetypes

* **Stream Screen (HUD / Drive Mode)**
* *Associated Required Feature:* Automated Impact Detection & Telemetry Logging, Drive HUD / Sensor Dashboard — displays active sensor meters and logs impacts in real time during transit. In this menu, you can enable or disable mapping. 


* **Detail Screen (Hazard Inspection)**
* *Associated Required Feature:* Community Hazard Stream — displays detailed sensor telemetry (peak G-force, road type, transit speed), full-resolution photo proof, and community verification history. We're going to need to create an easy-to-understand score with this information. 


* **Map Screen (Roughness & Hazard Heatmap)**
* *Associated Required Feature:* Surface Roughness Map — A heatmap, with darker colors highlighting more damaged roads.


* **Creation Screen (Manual Report / Photo Submission)**
* *Associated Required Feature:* Camera Capture — allows users to add photos, descriptions, and road notes to an auto-detected impact event. Providing extra context to other users. This can apply to roads they or other users have mapped. 


* **Profile Screen (User Stats & Gear)**
* *Associated Required Feature:* Drive HUD / Sensor Dashboard — displays user's total audited miles, detected pothole/uneven road count, community karma score, and vehicle profile.



---

### 3. Navigation

#### Tab Navigation (Tab to Screen)

* **Tab 1 (Home):** Enable and Disable recording at any time
* **Tab 2 (Map):** Roughness Heatmap (Full-screen interactive map with color-coded road quality layers)
* **Tab 3 (Profile):** User Stats & History (Audited miles, logged impacts, vehicle settings)

#### Flow Navigation (Screen to Screen)

* **Community Feed (Stream Screen)**
* $\rightarrow$ Tap Hazard Card $\rightarrow$ **Hazard Detail Screen**


* **Hazard Detail Screen**
* $\rightarrow$ Tap Back Button $\rightarrow$ **Community Feed (Stream Screen)**
* $\rightarrow$ Tap Location Pin $\rightarrow$ **Roughness Heatmap (Map Screen)** centered on coordinates


* **Live Sensor HUD (Stream Screen)**
* $\rightarrow$ Tap "Add Photo" / Auto-Trigger $\rightarrow$ **Creation Screen (Camera / Report Confirmation)**
* $\rightarrow$ Tap "Stop Drive" $\rightarrow$ **Trip Summary Modal / Screen**


* **Roughness Heatmap (Map Screen)**
* $\rightarrow$ Tap Map Marker $\rightarrow$ **Hazard Detail Screen**


* **Profile Screen**
* $\rightarrow$ Tap "My Reports" $\rightarrow$ Filtered **Community Feed (Stream Screen)**



---

## Wireframes

### Hand-Sketched Low-Fidelity Wireframes

*(Embed your photographed wireframe sketches below using your GitHub relative repository path)*

```markdown

```

---
