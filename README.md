# OpenArm robot module for [mc_rtc](https://jrl-umi3218.github.io/mc_rtc/)

This package contains a software representation, or a robot module, of the
[OpenArm](https://docs.openarm.dev/1.0/) bimanual robot platform. This robot
module is used by the [mc_rtc](https://jrl-umi3218.github.io/mc_rtc/)
framework to realize control of the OpenArm robot in simulation or in
experiments with the real platform.

> Both OpenArm hardware/URDF versions are supported, as separate module
> names: `OpenArmV1` and `OpenArmV2` (`OpenArm` is an alias of `OpenArmV1`).

## Required dependencies

- [mc_rtc](https://jrl-umi3218.github.io/mc_rtc/)
- [openarm_description](https://github.com/enactic/openarm_description)
- [xacro](https://github.com/ros/xacro) (`ros-<distro>-xacro`): the URDFs are
  generated from the xacro files of openarm_description at build time

## Build instructions

```
$ source /opt/ros/<distro>/setup.bash
$ source <path-to-openarm-ws>/install/setup.bash
$ cd mc_openarm
$ mkdir build
$ cd build
$ cmake ..
$ make
$ sudo make install
```

## Use

```yaml
Robots:
  openarm:
    module: OpenArmV12 # or OpenArm (alias of OpenArmV1)
```
