---
layout: page
title: Syllabus
description: Listing of course modules and topics.
---

**Course Information:**

| Field | Details |
| --- | --- |
| Course | CSE 468/568: Robotics Algorithms |
| Term | Fall 2026 |
| Meetings | Tuesday/Thursday, 2:00–3:20 pm |
| Location | Knox 110 |
| Instructor | Karthik Dantu |
| Email | [kdantu@buffalo.edu](mailto:kdantu@buffalo.edu) |
| Phone | (716) 645-2670 |
| Website | <https://www.cse.buffalo.edu/faculty/kdantu> |
| Office | Davis 113F |
| Office hours | Monday, 2:00–3:00 pm; Wednesday, 4:00–5:00 pm |

**Course Description:** This course is intended to be a comprehensive
introduction to robotics algorithms for a senior
undergraduate/first-year graduate student. It is a Computer Science
course, and introduces the student to well-known algorithms in making a
simple robot autonomous.

**Course Format:** Sixteen weeks; two 90-minute meetings per week. A
standard meeting uses 15 minutes for retrieval and focused derivation,
60 minutes for guided and independent implementation, 10 minutes for a
demonstration or failure analysis, and 5 minutes for a commit and exit
note. The running platform is Linux, ROS 2, deterministic simulation,
recorded bags, and an F1TENTH-class vehicle when available.

**Prerequisite(s):** Data structures and algorithms; introductory
probability; linear algebra and calculus; programming in Python, C++,
or Java. Prior robotics is helpful, but not required.

**Credit Hours:** 3 (468)/ 3 (568)

**Textbooks and Readings**

There are no required textbooks for this class. Material is selected
from a collection of reference books. They include:

[*Introduction to Autonomous Mobile
Robots*](http://www.mobilerobots.ethz.ch/), 2^nd^ Edition<br>
**Author(s):** Ilah Nourbaksh, Ronald Seigward, Davide Scaramuzza<br>
ISBN-13: 978-0262015356

[*Probabilistic Robotics*](http://www.probabilistic-robotics.org/)<br>
**Author(s):** Sebastian Thrun, Wolfram Burgard, Dieter Fox<br>
ISBN-13: 978-0262201629

[*Introduction to Autonomous
Robots*](https://github.com/Introduction-to-Autonomous-Robots/Introduction-to-Autonomous-Robots)<br>
**Authors**: Correll, Nikolaus and Hayes, Bradley, and Heckman,
Christoffer, and Roncone, Alessandro<br>
Freely available online in the link provided.

[*Planning Algorithms*](http://lavalle.pl/planning/)<br>
**Authors**: Steve Lavelle<br>
Freely available online.

The primary text for the topic-by-topic readings below is
*Introduction to Autonomous Robots: Mechanisms, Sensors, Actuators, and
Algorithms*.

**Topic-by-Topic Course Readings:**

The readings identify the relevant chapter, section, subsection, and
page range in the primary text.

- **Autonomy systems and actuation**
  - Autonomy architecture and mobile-robot challenges — Ch. 1,
    §§1.3–1.4 (pp. 14–16).
  - ROS 2, simulation, bags, TF, logging, and reproducibility — course
    software material; Ch. 1, §1.3 provides autonomy-system context
    (pp. 14–15).
  - Reactive control — Ch. 11, §11.1 (pp. 193–196).
  - Finite-state machines, behavior trees, and mission planning — Ch.
    11, §§11.2–11.5.1 (pp. 197–207).
  - Electric motors, motor controllers, and actuator safety — Ch. 6,
    §§6.1–6.3 (pp. 105–112).
- **Robot geometry and motion**
  - Locomotion, stability, and degrees of freedom — Ch. 2, §§2.1–2.3
    (pp. 25–33).
  - Coordinate frames and homogeneous transformations — Ch. 2,
    §§2.4.1–2.4.3 (pp. 35–40).
  - Euler angles and quaternions — Ch. 2, §2.4.4 (pp. 40–42).
  - Differential-drive kinematics — Ch. 3, §3.3.2 (pp. 59–65).
  - Odometry — Ch. 3, §3.3.2, “From Forward Kinematics to Odometry”
    (pp. 65–66).
  - Car-like/Ackermann kinematics — Ch. 3, §3.3.3 (pp. 66–67).
- **Control, tracking, and learning**
  - Feedback control and PID — Ch. 3, §3.4.2 (p. 72); PID is developed
    in course material.
  - Trajectory tracking — Ch. 3, §3.4.2 (p. 72); Pure Pursuit and
    Stanley tracking are developed in course material.
  - LQR, MPC, trajectory optimization, and basic reinforcement learning
    — course material; neural-network foundations in Ch. 10,
    §§10.1–10.5 (pp. 170–182).
- **Sensors and robot perception**
  - Sensor terminology, error sources, and sensor classes — Ch. 7,
    §§7.1–7.1.1 (pp. 119–120).
  - Encoders, accelerometers, gyroscopes, and range sensing — Ch. 7,
    §§7.2–7.5.3 (pp. 121–130).
  - Image processing and camera-derived structure — Ch. 8, §§8.1–8.4
    (pp. 139–151).
  - LiDAR algorithms: line fitting and RANSAC — Ch. 9, §§9.3.1–9.3.3
    (pp. 157–161).
  - Feature descriptors and object recognition — Ch. 9, §§9.4–9.5
    (pp. 162–165).
  - Neural networks, CNNs, and recurrent networks — Ch. 10,
    §§10.1–10.7 (pp. 170–188).
  - Deep-learning perception, object detection, segmentation, and
    vision-language perception — course material; Ch. 10, §§10.3–10.7
    provides foundations (pp. 175–188).
  - ICP, voxel mapping, and RGB-D mapping — Ch. 12, §§12.2–12.4
    (pp. 214–219).
- **Probability, estimation, and localization**
  - Probability, uncertainty propagation, sensor fusion, and Kalman
    filtering — Ch. 15, §§15.1–15.3.1 (pp. 258–266) and Appendix C,
    §§C.1–C.5 (pp. 321–328).
  - Markov localization and Bayes filters — Ch. 16, §§16.2–16.3.1
    (pp. 271–281).
  - Particle filters and EKF localization — Ch. 16, §§16.4–16.5.1
    (pp. 281–287).
- **Mapping and SLAM**
  - Map representations and dense mapping — Ch. 12, §§12.1–12.4
    (pp. 213–219).
  - Landmark-based and graph-based SLAM — Ch. 17, §§17.1–17.4.2
    (pp. 292–303).
  - Learned SLAM, semantic maps, and visual-language-action systems —
    course material; graph-SLAM foundations in Ch. 17, §§17.3–17.4.2
    (pp. 295–303).
- **Planning and navigation**
  - Configuration spaces, Dijkstra’s algorithm, and A* — Ch. 13,
    §§13.1–13.2.2 (pp. 224–228).
  - Costmaps and diffusion-based planning — course material;
    map-representation foundations in Ch. 12, §12.1 (pp. 213–214).
  - RRT, planning at multiple scales, and coverage planning — Ch. 13,
    §§13.3–13.5 (pp. 228–235).
  - PRM/RRT*, kinodynamic planning, Dynamic Window, and trajectory
    rollout — course material; RRT foundations in Ch. 13, §13.3.1
    (pp. 229–233).
- **Deployment and responsibility**
  - Safety, privacy, cybersecurity, human interaction, sustainability,
    and responsible deployment — Ch. 6, §6.3 (p. 112) and Appendix C,
    §§C.5–C.5.4 (pp. 325–328), with course material on fault injection
    and safety monitors.

**Course Objectives:**

At the completion of this course, students will be able to:

1. **Kinematics.** Model and control a mobile robot by applying
   coordinate-frame reasoning, kinematics, feedback, trajectory
   tracking, and appropriate assumptions about sensing, timing, and
   actuation.
2. **Perception.** Design and evaluate robot-perception pipelines that
   combine range, inertial, camera, and learned visual information while
   accounting for calibration, uncertainty, and failure modes.
3. **Estimation.** Implement and assess probabilistic state-estimation,
   mapping, localization, and SLAM algorithms using quantitative
   evidence from deterministic simulation and recorded data.
4. **Planning.** Formulate and compare navigation and decision-making
   methods, including graph search, sampling-based planning, local
   planning, optimization, reinforcement learning, and learned autonomy
   components.
5. **ROS.** Architect, implement, test, and debug an integrated
   autonomy stack in ROS 2 with clear subsystem interfaces,
   reproducible experiments, safety monitors, and measured system
   behavior.
6. **Security and Ethics.** Exercise professional judgment in the
   deployment of autonomous robots by communicating results clearly and
   considering safety, security, privacy, ethics, human interaction,
   and societal impact.

While this is a reasonable outline, the instructor reserves the right to
change the syllabus as he sees fit. Please check the course site for the
latest changes.

**Grade Distribution:**

| Component | Weight | Grading basis |
| --- | ---: | --- |
| Programming assignments | 30% | Five cumulative assignments: PA1, PA2, PA3, and PA4 are 5% each; PA5 is 10%. Correctness, evidence, robustness, and explanation are evaluated. |
| Implementation activities | 20% | Approximately 12–14 low-stakes activities, each worth 2%. The ten highest activity scores count; the lowest two scores are dropped when 12 activities are offered, the lowest three when 13 are offered, and the lowest four when 14 are offered. Activities include traces, tests, and diagnostic artifacts and stop short of an assignment’s main integration. |
| Quizzes | 30% | Short quizzes assess conceptual understanding, derivation, code reading, prediction, debugging, and interpretation of results. |
| Midterm examinations | 20% | Midterm examination(s), collectively worth 20%, assess integrated understanding of robot models, algorithms, assumptions, and failure modes. |

Grades will be on a curve. From prior experience, I have seen different
performance from the undergraduate (468) and graduate (568) students.
Therefore, for fairness, I'll grade students on two separate curves, one
for graduate students and another for the undergraduate students.

**Course Policies:**

- **General:** **No makeup quizzes or in-class activities will be given
  unless discussed on a per case basis well in advance.**

- **Grades**

  - Graded on a curve with B+ roughly being the median.

  - Grades will be maintained in the myUB course system. Students are
    responsible for tracking their progress by referring to the online
    gradebook and reporting any discrepancies.

- **Labs and Assignments**

  - Students are expected to work **independently** unless an assignment
    expressly permits collaboration. **Offering** and **accepting**
    solutions from others outside of permitted collaboration is an act
    of **plagiarism**, which is a serious offense and **all involved
    parties** will be penalized according to the [Academic Honesty
    Policy](http://undergrad-catalog.buffalo.edu/policies/course/integrity.html).
    Discussion amongst students is encouraged, but when in doubt,
    direct your questions to the professor, teaching assistant, or
    graders.

  - Unless addressed with the professor well ahead of a deadline, late
    submissions will not be allowed.

- **Attendance and Absences**

  - Attendance is expected each class. Activities and quizzes are
    in-class. The professor will not entertain any grade changes toward
    the end of the course if the student has not participated during the
    semester.

  - If you have a medical reason for missing class, I will **require** a
    doctor's note. Without clear directions from a doctor asking time
    off for you, I will assume you are able to do the class work and
    attend class.

  - Students are responsible for all missed work, regardless of the
    reason for absence. It is also the absentee's responsibility to get
    all missing notes or materials.

**Plagiarism Policy:**

- This course has several programming assignments and in-class
  activities mostly based on the ROS 2 programming environment. We use
  **sophisticated code checkers** to check for code copied from
  assignments from this class as well as submissions from prior editions
  of the class. It is **very improbable** that you will be able to fool
  the code checker.

- Along the same lines, if you see someone else's code to understand the
  logic, it is probable that our code checker will flag this as
  plagiarized since your code will be influenced by what you saw and
  will look structurally similar.

- Discussing high-level programming ideas with other students is
  acceptable. However, this is a slippery slope, and the more detailed
  these discussions are and the more they tend toward actual code, the
  more likely the code checker will flag this as plagiarism.

- Copying snippets of code from online resources (such as StackOverflow,
  GitHub, etc.) is also considered plagiarism. When you are in doubt,
  please check with the professor for clarity.

- The AI-assisted programming workflow is described in **Operating
  Expectations** below. It does not override the individual-work,
  permitted-collaboration, or academic-integrity requirements above.

**Course Schedule:**

| Date | Topics | Activities | Assignments |
| --- | --- | --- | --- |
| Aug. 27 (Thu.) | Autonomy architecture and mobile-robot challenges | — | — |
| Sept. 1 (Tue.) | ROS 2, simulation, bags, TF, logging, and reproducibility | A01 assigned | — |
| Sept. 3 (Thu.) | Reactive control | A01 due; A02 assigned | — |
| Sept. 7 (Mon.) | *Labor Day holiday observed — no classes* | — | — |
| Sept. 8 (Tue.) | Coordinate frames and homogeneous transformations | A02 due; A03 assigned; A03 due Sept. 13 | — |
| Sept. 10 (Thu.) | Differential-drive kinematics; odometry; car-like/Ackermann kinematics | — | — |
| Sept. 15 (Tue.) | Feedback control and PID | A04 assigned; due Sept. 20 | PA1 assigned |
| Sept. 17 (Thu.) | Trajectory tracking | — | — |
| Sept. 22 (Tue.) | LQR, MPC, trajectory optimization, and basic reinforcement learning | A05 assigned; due Sept. 27 | — |
| Sept. 24 (Thu.) | Sensor terminology, error sources, and sensor classes; encoders, accelerometers, gyroscopes, and range sensing | — | — |
| Sept. 29 (Tue.) | LiDAR algorithms: line fitting and RANSAC | A06 assigned; due Oct. 4 | PA1 due; PA2 assigned |
| Oct. 1 (Thu.) | Image processing and camera-derived structure; feature descriptors and object recognition | A07 assigned; due Oct. 11 | — |
| Oct. 6 (Tue.) | Neural networks, CNNs, and recurrent networks | — | — |
| Oct. 8 (Thu.) | Deep-learning perception, object detection, segmentation, and vision-language perception | — | — |
| Oct. 12–13 | *Fall Break — no classes* | — | — |
| Oct. 15 (Thu.) | ICP, voxel mapping, and RGB-D mapping | — | PA2 due; PA3 assigned |
| Oct. 20 (Tue.) | Probability, uncertainty propagation, sensor fusion, and Kalman filtering | A08 assigned; due Oct. 25 | — |
| Oct. 22 (Thu.) | Markov localization and Bayes filters | A09 assigned; due Nov. 1 | — |
| Oct. 27 (Tue.) | Particle filters and EKF localization | — | — |
| Oct. 29 (Thu.) | Map representations and dense mapping | A10 assigned; due Nov. 8 | PA3 due |
| Nov. 3 (Tue.) | Landmark-based and graph-based SLAM | — | PA4 assigned |
| Nov. 5 (Thu.) | Learned SLAM, semantic maps, and visual-language-action systems | — | — |
| Nov. 10 (Tue.) | *CoRL travel day — no class* | — | — |
| Nov. 12 (Thu.) | *CoRL travel day — no class* | — | — |
| Nov. 17 (Tue.) | Configuration spaces, Dijkstra’s algorithm, and A* | A11 assigned; due Nov. 22 | PA4 due; PA5 assigned |
| Nov. 19 (Thu.) | Costmaps and diffusion-based planning | A12 assigned; due Dec. 1 | — |
| Nov. 24 (Tue.) | RRT, planning at multiple scales, and coverage planning | A13 assigned; due Dec. 3 | — |
| Nov. 25–28 | *Thanksgiving Break — no classes* | — | — |
| Dec. 1 (Tue.) | PRM/RRT*, kinodynamic planning, Dynamic Window, and trajectory rollout | A12 due; A14 assigned; due Dec. 3 | — |
| Dec. 3 (Thu.) | Safety, privacy, cybersecurity, human interaction, sustainability, and responsible deployment | A13 due; A14 due | — |
| Dec. 7 (Mon.) | *Official Race and Demo Day* | — | — |
| Dec. 8 (Tue.) | *Reading Day* | — | PA5 due |
| Dec. 9–16 | *Final examinations* | — | — |

**Programming Activities:**

These short implementation activities build individual components that
support the programming assignments. They adapt the course’s ROS,
control, perception, estimation, and planning exercises to the current
autonomy stack.

1. **A01 — ROS 2 Demo.** Run a minimal ROS 2 publisher/subscriber demo
   and identify the nodes, topics, and message flow.
2. **A02 — ROS 2 Basics 1.** Create a node that publishes, subscribes,
   and reports a robot-state value through the ROS 2 graph.
3. **A03 — ROS 2 Basics 2.** Use launch files, TF, and a recorded bag to
   reproduce and inspect a short autonomy run.
4. **A04 — Control Robot Goal Seek.** Implement a goal-seeking
   controller and document its position and heading error over a run.
5. **A05 — Car Pure Pursuit.** Tune a Pure Pursuit tracker for a
   car-like robot and compare tracking performance for two look-ahead
   choices.
6. **A06 — Laser Processing and TurtleBot RANSAC.** Filter a LiDAR
   scan, estimate a geometric line with RANSAC, and report inliers plus
   one failure case.
7. **A07 — Feature Matching and Alignment.** Detect, match, and
   visualize image features; identify a correspondence failure case.
8. **A08 — Bayesian Estimation.** Implement a prediction/correction
   update and interpret the effect of motion and sensor uncertainty.
9. **A09 — Point-Cloud Registration.** Register two point clouds or
   scans and report the estimated transform and residual error.
10. **A10 — Occupancy-Grid Map Representation.** Convert range
    observations and robot poses into an occupancy grid; visualize free,
    occupied, and unknown cells and explain one resolution or
    sensor-model tradeoff.
11. **A11 — Graph Planning — Forward Search.** Build a costmap-based
    forward search with Dijkstra’s algorithm or A*, then reconstruct the
    path and identify one infeasibility case.
12. **A12 — Nav2 Navigation Stack.** Configure and exercise Nav2 with a
    supplied map and robot model; inspect the global plan, local
    behavior, and one recovery or parameter-setting decision.
13. **A13 — Gap Follow and Local Recovery.** Implement a Follow-the-Gap
    or comparable local-recovery behavior and evaluate it in a
    constrained scene.
14. **A14 — Sampling Planner and Safety Watchdog.** Generate feasible
    sampled trajectories and add a simple confidence, collision, or
    watchdog gate before execution.

**Programming Assignments:**

The five programming assignments build a cumulative mobile-robot
autonomy stack.

1. **PA1 — Drive-by-Wire, Frames, and AEB.** ROS 2 bring-up, odometry,
   TF, logging, and a braking supervisor.
2. **PA2 — Reactive Driving: See, Follow, and Avoid.** LiDAR
   processing, PID wall following, Follow the Gap, and a compact visual
   cue.
3. **PA3 — Where Am I? Localization, Mapping, and SLAM.** Occupancy
   maps, Monte Carlo localization, and a measured SLAM study.
4. **PA4 — Plan the Line, Track the Line.** Costmaps, graph/sampling
   planning, tracking, replanning, and recovery.
5. **PA5 — Integrated Autonomy Challenge.** Monitored full-stack
   autonomy plus one advanced extension: learning, opponent perception,
   or advanced control.

PA5 pairs use named subsystem ownership, shared integration milestones,
and an individual checkoff.

Every assignment submission is code plus one short document: what was
built, how to run it, one design choice, evidence it works, and one
failure case with its likely cause. CSE 568 uses the same core with an
added derivation, research-grounded alternative, ablation,
consistency/complexity analysis, or statistical comparison.

**Operating Expectations:**

Every assignment submission is code plus one short document: what was
built, how to run it, one design choice, evidence it works, and one
failure case with its likely cause. Students use deterministic simulation
and recorded bags as the graded fallback. The simulator-to-hardware
safety gate remains mandatory for any hardware work. AI-assisted
programming is taught through specification, code reading, prediction,
testing, diagnosis, repair, and re-test; generated code is treated as
untrusted, and no separate AI-use statement is required.

**ABET Student Outcomes:**

This course supports the following ABET Computing Accreditation
Commission (CAC) Computer Science student outcomes.

1. **ABET CAC SO 1 — Analyze complex computing problems and apply
   principles of computing and other relevant disciplines to identify
   solutions.** *Direct contribution:* Students formulate sensing,
   estimation, planning, control, and integration problems; select
   representations, algorithms, and assumptions; and diagnose failures
   in deterministic replay and simulation.
2. **ABET CAC SO 2 — Design, implement, and evaluate a computing-based
   solution to meet a given set of computing requirements in the context
   of the program’s discipline.** *Direct contribution:* PA1–PA5
   require students to specify interfaces and constraints, implement
   robot-autonomy components, test them against scenario requirements,
   and evaluate the integrated solution with evidence.
3. **ABET CAC SO 3 — Communicate effectively in a variety of
   professional contexts.** *Reinforced contribution:* Each assignment
   requires a concise, reproducible technical document that states what
   was built, how to run it, one design choice, evidence it works, and
   one failure case with its likely cause; demonstrations and peer
   reproduction reinforce technical communication.
4. **ABET CAC SO 4 — Recognize professional responsibilities and make
   informed judgments in computing practice based on legal and ethical
   principles.** *Direct contribution:* Students evaluate safety,
   privacy, security, accessibility, environmental, and societal
   implications of autonomy-system design choices. The intended
   direct-assessment artifact is an individual written design-decision
   exercise scored on three performance indicators: recognition of
   professional responsibilities, informed judgment based on legal
   principles, and informed judgment based on ethical principles.
5. **ABET CAC SO 5 — Function effectively as a member or leader of a
   team engaged in activities appropriate to the program’s discipline.**
   *Reinforced contribution:* PA5 pairs use named subsystem ownership,
   shared integration milestones, and an individual checkoff; students
   plan tasks, coordinate interfaces, and meet common evaluation
   objectives.
6. **ABET Computer Science SO 6 — Apply computer science theory and
   software development fundamentals to produce computing-based
   solutions.** *Direct contribution:* Students implement and test
   algorithms for transforms, kinematics, filtering, mapping, planning,
   control, and learning; the course emphasizes modular software,
   algorithmic complexity, reproducibility, debugging, and regression
   tests.

**Assessment Evidence:** Candidate evidence includes assignment
repositories and tests, fixed-seed simulation results, bag-replay
traces, quantitative comparisons, concise technical documents,
individual safety/ethics decision exercises, and PA5 integration
demonstrations. CSE 568 students provide the same core evidence with an
added derivation, research-grounded alternative, ablation,
consistency/complexity analysis, or statistical comparison.
