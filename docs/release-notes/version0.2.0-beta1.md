# Release Notes

## Maple-Sim Beta 1: A New Start

It's been a month since we announced maple-sim alpha, a lot has happened this month.  We've got **a lot of** help from the community developers.  Compared to maple-sim a month ago, we are more stable, easier to use and had some features.

### Lots of new features for Beta!

#### 1. Simplified Swerve Simulation
> 🙏 Contributed by [@GearFox](https://github.com/GearBoxFox)

The new `SimplifiedSwerveSimulation` class manages and controls a `SwerveDriveSimulation`. Similar to how your user code operates the physical chassis, it runs closed loops on the virtual drive and steer motors in the simulated drivetrain, mimicking the behavior of a real swerve drive. This provides an easier way to simulate swerve drivetrains without the need for the hardware abstraction code structure.

Check out the [documentation](https://shenzhen-robotics-alliance.github.io/maple-sim/3.1_SWERVE_SIM_EZ_MODE.html) for more details.

#### 2. Motor Controller Closed Loops Simulation
> 🙏 Contributed by [@oh-yes-0-fps](https://github.com/oh-yes-0-fps)

The updated `MapleMotorSim` now includes a feature to simulate high-frequency closed loops running on motor controllers. This allows teams using different vendor APIs to more accurately simulate the behavior of their motor controllers during simulations.

#### 3. WPILib Units Library
> 🙏 Contributed by [@buwunny](https://github.com/buwunny)

The [New WPILib Units Library for 2025](https://docs.wpilib.org/pt/latest/docs/software/basic-programming/java-units.html) has been fully implemented across the project. This improves API readability and eliminates potential issues related to unit conversions.


#### 4. YAGSL, Officially Supported!
> 🙏 Thanks to @nstrike for making this possible!

With help from the developers of YAGSL, we have successfully integrated maple-sim with the amazing [Yet Another Generic Swerve Drive Library (2025-beta)](https://github.com/BroncBotz3481/YAGSL-Example/pull/251).   A preview version featuring realistic swerve simulation will be available soon. 

Please [follow YAGSL on Github](https://github.com/BroncBotz3481) to stay updated when it's released.

## More Stable Hosting
We are now using GitHub Pages to host the library and its documentation, providing a more reliable and stable experience than before.

You can download the vendordeps from this url:
```
https://shenzhen-robotics-alliance.github.io/maple-sim/vendordep/maple-sim.json
```
No additional configuration is needed in Gradle—simply drop the file into the `vendordeps/` directory, and the library will download automatically!

The online documentation is available [here](https://shenzhen-robotics-alliance.github.io/maple-sim/1_INSTALLING_MAPLE_SIM.html).

You can also access the online Javadocs [here](https://shenzhen-robotics-alliance.github.io/maple-sim/javadocs/).

## Full Changelog & Thanks
All the above couldn't have been possible without the help of the fellow community contributors. Deep and sincere thanks to:

??? "Contributors and Their Contributions"
      -   [@ArisaYamatogi](https://github.com/orgs/Shenzhen-Robotics-Alliance/people/ArisaYamatogi) from our team for:
         -   Illustrations and diagrams in the documents.
      -   [@buwunny](https://github.com/buwunny) from Team 3173 _"IgKnighters"_ for:
         -   Implementing WPILib units library across the project in [\[#24\]](https://github.com/Shenzhen-Robotics-Alliance/maple-sim/pull/24).
      -   [@cyocom](https://github.com/cyocom) for:
         -   Adding constants for WCP SwerveX modules in the swerve module factory in [\[#4\]](https://github.com/Shenzhen-Robotics-Alliance/maple-sim/pull/4) and [\[#5\]](https://github.com/Shenzhen-Robotics-Alliance/maple-sim/pull/5).
      -   [@Daniel1464](https://github.com/Daniel1464) from Team 5160 _"Chargers"_ for:
         -   Adding safety measures in [\[#33\]](https://github.com/Shenzhen-Robotics-Alliance/maple-sim/pull/33).
         -   Fixing links in documents in [\[#38\]](https://github.com/Shenzhen-Robotics-Alliance/maple-sim/pull/38).
      -   [@GearFox](https://github.com/GearBoxFox) from Team 4467 _"Titanium Titans"_, my mentor who guided me to FRC, for:
         -   Creating the [Simplified Swerve Simulation](https://shenzhen-robotics-alliance.github.io/maple-sim/3.1_SWERVE_SIM_EZ_MODE.html) in [\[#25\]](https://github.com/Shenzhen-Robotics-Alliance/maple-sim/pull/25).
         -   Proposing motor-controller closed-loop simulation.
      -   [@KfirNeuman](https://github.com/KfirNeuman) from Team 3075 _"Ha-Dream Team"_ for:
         -   Improving the readability of the DRIVE\_WHEEL\_TYPE enum in [\[#14\]](https://github.com/Shenzhen-Robotics-Alliance/maple-sim/pull/14).
      -   [@oh-yes-0-fps](https://github.com/oh-yes-0-fps) from Team 3173 _"IgKnighters"_ for:
         -   Improving intake simulation API in [\[#7\]](https://github.com/Shenzhen-Robotics-Alliance/maple-sim/pull/7).
         -   Removing redundant PPLib usage in [\[#11\]](https://github.com/Shenzhen-Robotics-Alliance/maple-sim/pull/11).
         -   Implementing motor-controller closed-loop and battery simulation in [\[#18\]](https://github.com/Shenzhen-Robotics-Alliance/maple-sim/pull/18).
         -   **(To be released)** Adding the SimRobot container, enhancing the gamepiece API, and more in [\[#26\]](https://github.com/Shenzhen-Robotics-Alliance/maple-sim/pull/26).
      -   [@Roman-Tech-Plus](https://github.com/Roman-Tech-Plus) from Team 5104 _"The Breakerbots"_ for:
         -   **(To be released)** Integrating maple-sim into CTRE's high-fidelity motor simulation in [\[#CTRE-simulation-support\]](https://github.com/Shenzhen-Robotics-Alliance/maple-sim/compare/CTRE-simulation-support...Roman-Tech-Plus:maple-sim:CTRE-simulation-support).
      -   [@thenetworkgrinch](https://github.com/thenetworkgrinch?tab=repositories) from [YAGSL](https://github.com/BroncBotz3481/YAGSL) and Team 3481 _"the BroncBotz"_ for:
         -   Setting up vendordeps publishing in [\[#2\]](https://github.com/Shenzhen-Robotics-Alliance/maple-sim/pull/2).
         -   Setting up documents on GitHub pages.
         -   Setting up Javadocs and Spotless formatting in [\[#3\]](https://github.com/Shenzhen-Robotics-Alliance/maple-sim/pull/3).
         -   Bringing [YAGSL beta with maple-sim](https://github.com/BroncBotz3481/YAGSL-Example/tree/beta) to life.

Thanks for kindly contributing to this project!


## What's Next?

As the title suggests, this is just the beginning for maple-sim. Our team, alongside contributors from the community, is actively working on exciting new features. We're planning to release **Beta 2** next month, which will include the following updates:

#### 1. SimRobot Container
A new `SimRobot` class that encapsulates simulation classes modeling your robot, providing a more readable and intuitive API.
(Contributed by [@oh-yes-0-fps](https://github.com/oh-yes-0-fps))

#### 2. New Gamepieces API
A new API for simulating gamepieces, enabling teams to model how their robot processes intaken gamepieces.
(Contributed by [@oh-yes-0-fps](https://github.com/oh-yes-0-fps))

#### 3. CTRE Simulation Support
Integration with [CTRE's high-fidelity motor simulation](https://v6.docs.ctr-electronics.com/en/stable/docs/api-reference/simulation/simulation-intro.html), allowing **maple-sim** to deliver enhanced physics simulation for teams using the [CTRE swerve API](https://v6.docs.ctr-electronics.com/en/stable/docs/api-reference/mechanisms/swerve/swerve-overview.html).
(Contributed by [@Roman-Tech-Plus](https://github.com/Roman-Tech-Plus) and inspired by [Team 5104 *"The Breakerbots"*'s Custom Library - BreakerLib](https://github.com/BreakerBots/BRICK/blob/main/2025-beta/src/main/java/frc/robot/BreakerLib/swerve/BreakerSimSwerveDrivetrain.java))

## Let's work together!

We warmly invite you to [report bugs, suggest for new features](https://github.com/Shenzhen-Robotics-Alliance/maple-sim/issues/new/choose) and [contribute to the project](https://shenzhen-robotics-alliance.github.io/maple-sim/CONTRIBUTION.html).

*We rely on the support of the community to grow and improve, and every contribution is deeply appreciated! Whether you're an experienced programmer or new to simulation, there are many ways to contribute. Not comfortable with coding? No problem! You can help by working on documentation or creating example projects.*

https://discord.com/invite/tWn45Qm6ub
