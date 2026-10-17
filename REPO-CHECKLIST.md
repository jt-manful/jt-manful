# GitHub repository checklist

Based on what I could see publicly on 17 Oct 2026. GitHub blocked automated access to the full repository list, so I only saw the profile and the three pinned repos. Please go through your other 14 repos yourself using the "Other repositories" section.

## 1. Profile

- [ ] Create the public repo `jt-manful/jt-manful`, add `README.md` and `banner.png` from this folder.
- [ ] Profile settings: add a bio ("Software engineer moving into robotics | M.Sc. @ University of Bonn"), location "Bonn, Germany", and website `https://jt-manful.github.io`.
- [ ] Set your display name to "John Terence Manful" (it currently shows "John Terence").
- [ ] Pin up to 6 repos, in this order once they exist:
  1. VLA bimanual manipulation (new)
  2. Autonomous-Robot-and-AI-Platform
  3. ros2-mobile-robot
  4. SmartEnvSensorsNet
  5. F1 pit-stop predictor (new)
  6. One backend repo, if you have a public one you're proud of

## 2. Fix the three existing pinned repos

### Automous-Robot-and-AI-Platform
- [ ] Rename to `Autonomous-Robot-and-AI-Platform` (Settings, General, Repository name). GitHub redirects the old URL; then update the link in `index.html` and the profile README.
- [ ] README currently covers Docker setup only. Add: what it does, current status ("early stage"), which packages exist today (`detector_pkg`) versus planned (`tracking_pkg`, `navigation_pkg`, `manipulation_pkg`, `robot_bringup`), a screenshot or short GIF of detections, and a roadmap.
- [ ] Mention the OpenCV + ONNX Runtime pipeline and `vision_msgs` output, which is on your CV but not in the README.
- [ ] Add a LICENSE (MIT is a common choice; your decision).
- [ ] Topics: `ros2`, `ros2-jazzy`, `robotics`, `computer-vision`, `onnx-runtime`, `opencv`, `docker`, `cpp`.

### ros2-mobile-robot
- [ ] The description says "two-axis robotic arm, URDF/Xacro, Gazebo", while the README leads with SLAM Toolbox and Nav2. Pick one story or explain both clearly.
- [ ] The README's package tree lists only `my_robot_description` and `my_robot_bringup`. Check that the Nav2 and SLAM configuration and launch files are in the repo, or the README claims more than the repo shows.
- [ ] Fix the clone URL: it says `ros2-mobile_robot.git`; it should be `ros2-mobile-robot.git`.
- [ ] The arm command uses `positions: {0.0, 0.0}`. In YAML a list needs square brackets: `positions: [0.0, 0.0]`. Test the command after fixing it.
- [ ] Add the ROS 2 distro and Ubuntu version it was tested on.
- [ ] Topics: `ros2`, `nav2`, `slam-toolbox`, `gazebo`, `urdf`, `xacro`, `rviz2`, `robotics`.

### SmartEnvSensorsNet
- [ ] Add a description (for example: "ESP32 environmental monitoring with MQTT and REST ingestion, web portal and temperature forecasting").
- [ ] Add a README: architecture diagram, hardware list, how the nodes connect, how to run the server and `db.sql`, and what the notebook does.
- [ ] Check there are no Wi-Fi passwords, API keys or broker credentials in the code or history. Rotate any you find.
- [ ] Topics: `esp32`, `iot`, `mqtt`, `rest-api`, `sqlite`, `scikit-learn`, `arduino`.

## 3. New repos to publish

- [ ] **VLA bimanual manipulation**: README with task descriptions, the π0.5 vs X-VLA results table (90% brick placement, 20% bottle opening), the dataset conversion and policy server architecture, setup steps, and rollout videos. Check you may publish lab data, models and videos. Topics: `vision-language-action`, `robot-learning`, `lerobot`, `mujoco`, `openpi`, `bimanual-manipulation`, `fastapi`.
- [ ] **F1 pit-stop predictor**: README with screenshots of the dashboard, the data source and its licence, and model evaluation.
- [ ] Optional: the Django data-sharing platform (only if the institution allows it) and the fraud-detection thesis code.

## 4. README template for every project

```markdown
# Project name
One sentence: what it does and why.

![demo](docs/demo.gif)

**Status:** Completed | Ongoing | Prototype
**Stack:** ...

## What's in here
Short architecture description or diagram.

## Getting started
Prerequisites, install and run commands, tested environment.

## Results
Real numbers only, and how they were measured.

## Limitations and next steps

## License
```

## 5. Other repositories (the 14 I couldn't see)

- [ ] Archive or make private anything abandoned, empty or tutorial-only.
- [ ] Give every public repo a one-line description.
- [ ] Remove committed secrets, large binaries and generated files.

## 6. Connect everything

- [ ] Each project README ends with a "Portfolio: https://jt-manful.github.io" line.
- [ ] The site's project links match the repo URLs (search `index.html` for `TODO`).
- [ ] Repo names, dates, tech lists and status labels match your CV, the site and the profile README.
