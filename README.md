# vslam for humans: A complete system for all your Visual (Inertial) SLAM needs

## Goal

This repo is meant to eventually contain everything one might need to run vslam (with an emphasis on visual inertial algorithms) using one or more cameras. This includes at a minimum:

- [ ] Easy to use camera and camera to IMU calibration tooling (derive either from Kalibr or VINS Fusion, may be April Tags based).
- [ ] At least one reference implementation of a V(I)O algorithm (likely derived from VINS Fusion) with a design that allows for a drop in replacement. This should have settings to switch between a 6DOF and 3DOF mode (and maybe customization of motion model?).
- [ ] At least one reference implementation of a loop detection/closure algorithm (also VINS Fusion)
- [ ] Saving/loading/user manipulation of maps (e.g. fix a bad loop closure), ability to resume with user intervention for relocalization (a.la AMCL)
- [ ] A setting to run in constant memory localization mode (a.la cartographer)
- [ ] Catastrophic failure recognition (including localization mode), reset/recovery and ability to communicate this to a user.
- [ ] Kidnap detection/recovery
- [ ] Place recognition and loading of appropriate map (a.la Oculus Quest but of course with more user control)

## Guiding principles

- Be compatible with ROS but don't depend on it.
- Make Python interfaces first class citizens (kind of like Kalibr but ... more decipherable).
- Focus on easy to achieve efficiency (e.g. use cuda if available). The primary targeted platform is a Jetson Nano.
- Painless installation (build ros, apt, pip packages and possibly snaps/flatpaks).
- Anyone with enough skill to set up gmapping with AMCL should be able to easily set this up as well. Guide users through setup and debugging to get the best performance out of their system.

## Relevant giants with stable looking shoulders

- VINS Fusion
- SVO
- Kalibr
- Camcodal
- Cartographer
- Karto
- Really anything put out by someone at ETH
- Orb Slam
- Rovio
