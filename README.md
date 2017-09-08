# Simplified OpenColorIO with ACES for Blender

Simplified ACES  based OpenColorIO configuration for Blender based on the ACES OpenColorIO configuration from https://github.com/imageworks/OpenColorIO-Configs. Look-up tables copied from OpenColorIO-Configs. (sRGB/Rec709 default curves from blender original color management [blender-2.79 rc 1])

The intend is to have a simple configuration with alternative rendering primaries compared to common blender configurations with sRGB rendering primaries to allow wide gamut rendering.


# Why?

Offer simple base to experiment with wide gamut HDR rendering in Blender.


# What?

Config based on ACES AP1 (ACEScg) primaries for wide gamut rendering. Using the ACES RRT + ODT combination for now. Other gamut mapping may be added later.

Base intention is to use this config for quick preview and rendering. Export intention for me is mostly saving EXR files for later grading. So no focus on other ODTs for now.


# Warning

Color Picker is expecting RGB values in ACES AP1 (ACEScg) color space.


# Install

Just replace the `2.79/datafiles/colormanagement` in the blender application folder with this repository. Or set the environment variable `OCIO` to the config.ocio file.

    export OCIO=/path/to/config.ocio
