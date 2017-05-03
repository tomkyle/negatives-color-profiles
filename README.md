
# Useful ICC profiles

**This repo is intended for making the profiles “available“ for image-related scripts, without “installing” them into the OS.**


## Elle Stone’s Well-Behaved ICC Profiles

Elle Stone's [Well-Behaved ICC Profiles](http://ninedegreesbelow.com/photography/lcms-make-icc-profiles.html) provide common ICC profiles for both color and gray images with gamma values ranging from 1.0 (linear) to 2.2 (typical).

> These profiles are for use with RGB images that have been converted to monotone gray (black and white). The main reason to convert from RGB to Gray is to save the file space needed to encode the image.

This repo is just a redistribution of Elle Stone's [Gray profiles](http://ninedegreesbelow.com/photography/lcms-make-icc-profiles.html#Gray), as of May 2017. Please also have a look on her official repo: [Elle's ICC profiles](https://github.com/ellelstone/elles_icc_profiles) on GitHub.



## sRGB v4 Appearance profile
This sRGB profile is provided by the ICC (International Color Consortium). See their page [sRGB Appearance profile](http://www.color.org/profiles/srgb_appearance.xalter) for more information. In short:

> This profile is a v4 replacement for commonly used sRGB v2 profiles. It gives better results in workflows that implement the ICC v4 specification, and is intended to be used in combination with other ICC v4 profiles.



## Usage


**Command parameters enable you to store profile paths in a bash variable, like so:**


```bash
#!/usr/bin/env bash
# myscript.sh

PROFILE_PATH=$(iccprofiles srgb-v4)
echo $PROFILE_PATH
```

### Available commands


**Profiles location:** The `directory` parameters will output the directory whery the ICC profiles are stored in local Homebrew ecosystem:

```bash
$ iccprofiles directory
# outputs:

/usr/local/opt/iccprofiles/profiles
```

**Linear gray profile with gamma 1.0:** the `gray-linear` parameters outputs the full path to a Linear Gray/Gamma 1.0 profile.

```bash
$ iccprofiles gray-linear
# outputs:

/usr/local/opt/iccprofiles/profiles/Gray-elle-V4-g10.icc
```


**sRGB v4 Appearance:** the `srgb-v4` parameters outputs the full path to the ICC's sRGB v4 Appearance profile.

```bash
$ iccprofiles srgb-v4
# outputs:

/usr/local/opt/iccprofiles/profiles/Gray-elle-V4-g10.icc
```

### No parameters: show summary

The script lists all profiles delivered with this package. Output looks like this:

```bash
$ iccprofiles
# outputs:

These ICC profiles came with Homebrew formula tomkyle/negatives/iccprofiles.
<https://github.com/tomkyle/negatives-iccprofiles>
------------------------------------------------------------
1. Gray profiles from Elle Stone's Well-Behaved ICC Profiles
<http://ninedegreesbelow.com/photography/lcms-make-icc-profiles.html#Gray>

/usr/local/opt/iccprofiles/profiles/Gray-elle-V4-g10.icc
/usr/local/opt/iccprofiles/profiles/Gray-elle-V4-g18.icc
/usr/local/opt/iccprofiles/profiles/Gray-elle-V4-g22.icc
------------------------------------------------------------
2. sRGB v4 Appearance profile
<http://www.color.org/profiles/srgb_appearance.xalter>

/usr/local/opt/iccprofiles/profiles/sRGB_ICC_v4_Appearance.icc
------------------------------------------------------------
```
