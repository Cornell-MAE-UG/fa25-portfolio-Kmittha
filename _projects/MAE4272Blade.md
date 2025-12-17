---
layout: project
title: MAE 4272 Blade Design Project
description:   The MAE 4272 blade design report presents the full development process for a small-scale wind turbine operating under a Weibull wind distribution. It details geometric constraints, selecting operating speed, aerodynamic reasoning, CAD modeling, and perfomance metrics, along with a preliminary testing protocol designed to evaluate efficiency, structural reliational, and alignment with project requirements. 
technologies: [Autodesk Fusion, MatLab, LabView VI, Big Blue Wind Tunnel]
image: /assets/images/BladeRender2.png 
---

The goal of this project was to design, fabricate, and test a small-scale wind turbine blade capable of maximizing power output in a controlled wind-tunnel environment. Our team, Group 24, was asked to create a blade that met strict geometric and material constraints - maximum 6 in. radius, maximum 2 in. chord length, and safe operation below allowable torque and stress limit - while optimizing performance at a fixed operating speed of 1200 RPM. The broader purpose was to translate theoretical aerodynamic modeling into a physical prototype and evaluate how closely real performance aligned with Betz-limit predictions. 

Figure 1: Chord/Pitch Angle/Twist Angle Distribution Along Blade
![Chord/Pitch/Twist Distribution Along Blade]({{ "/assets/images/DistributionAlongBlade.png" | relative_url }}){: style="width: 400px; display: block; margin: 0 auto;"}

Our design process centered on developng a blade geometry using Betz-limit blade element theory under idealized assumptions: no wake rotation, isentropic material behavior, and a Weibull-distributed wind speed profile. We selected the NACA 6412 airfoil base geometry for its high lift-to-drag ratio at low Reynolds numbers and used MATLAB to compute chord, pitch, and twist distributions along the blade span. Structural checks were performed by integrating bending moments along the radial elements and comparing to the 58 MPa allowable limit. The final geometry (5 in radius, 1.3 inch max chord) satisfied all constraints and passed structural verification with a maximum predicted stress of 0.239 MPa. 

Figure 2: Experimental Power v. RPM at 6-10 Hz
![Experimental Power v. RPM at 6-10 Hz]({{ "/assets/images/PowerversusRPM.png" | relative_url }}){: style="width: 400px; display: block; margin: 0 auto;"}

Testing was conducted in the Cornell wind tunnel across fan frequencies from 6-10 Hz. At each wind speed, torque was incrementally increased using a torque brake untill stall, then decreased to account for hysteresis. Using DAQ-collected torque and RPM data, we generated power curves for each wind speed and cmopared peak performance to theoretical predictions. While the blade operated safely and data collection was consistent, experimental power output (0.048 W) feel significantly below the theoretical 1.528 W, highlighting mechanical losses, aerodynamic inefficiencies, and non-ideal flow behavior not captured in the simplified model.

Figure 3: Autodesk Fusion 360 Render of NACA 6412 Optimized Blade
![Experimental v. Theoretical Power Output at 1200 RPM]({{ "/assets/images/ExversusThPower.png" | relative_url }}){: style="width: 400px; display: block; margin: 0 auto;"}

