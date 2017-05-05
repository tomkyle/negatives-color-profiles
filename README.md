
# Useful ICC profiles

**This repo is intended for making the profiles “available“ for image-related scripts, without “installing” them into the OS.**


## Elle Stone’s Well-Behaved ICC Profiles

Elle Stone's [Well-Behaved ICC Profiles](http://ninedegreesbelow.com/photography/lcms-make-icc-profiles.html) provide common ICC profiles for both color and gray images with gamma values ranging from 1.0 (linear) to 2.2 (typical).

> These profiles are for use with RGB images that have been converted to monotone gray (black and white). The main reason to convert from RGB to Gray is to save the file space needed to encode the image.

This repo just distributes some of Elle Stone's [Gray](http://ninedegreesbelow.com/photography/lcms-make-icc-profiles.html#Gray) and [sRGB v4](http://ninedegreesbelow.com/photography/lcms-make-icc-profiles.html#sRGB) profiles, as of May 2017. Please also have a look on her official repo: [Elle's ICC profiles](https://github.com/ellelstone/elles_icc_profiles) on GitHub.



## sRGB v4 Appearance profile
This sRGB profile is provided by the ICC (International Color Consortium). See their page [sRGB Appearance profile](http://www.color.org/profiles/srgb_appearance.xalter) for more information. In short:

> This profile is a v4 replacement for commonly used sRGB v2 profiles. It gives better results in workflows that implement the ICC v4 specification, and is intended to be used in combination with other ICC v4 profiles.

## Requirements

- Install [Homebrew](https://brew.sh/) on your Mac - [Installationsanleitung auf deutsch](https://brew.sh/index_de.html)


## Installation

This Homebrew formula is part of the [tomkyle/negatives Homebrew tap](https://github.com/tomkyle/homebrew-negatives). It is recommended to install the tap first:

```bash
$ brew tap tomkyle/negatives
$ brew install color-profiles
```

As “tapping” first is not neccessarily needed, you can install the formula directly:

```bash
$ brew install tomkyle/negatives/color-profiles
```




## Usage

### Without parameters: display short help


```bash
$ color-profiles
# outputs

1. Usage:
color-profiles [command]

2. Available commands:
directory     Display the directory where the ICC profiles are stored
gray-linear   Full path to profile 'Gray-elle-V4-g10.icc'
srgb-linear   Full path to profile 'sRGB-elle-V4-g10.icc'
srgb-v4       Full path to profile 'sRGB_ICC_v4_Appearance.icc'
summary       Display a summary of profiles coming with this package.
```


### Command parameters

Command parameters enable you to store profile paths in a bash variable, like so:


```bash
#!/usr/bin/env bash
# myscript.sh

PROFILE_PATH=$(color-profiles srgb-v4)
echo $PROFILE_PATH
```


#### directory
Show the directory where the ICC profiles are stored in local Homebrew ecosystem:

```bash
$ color-profiles directory
# outputs:

/usr/local/opt/color-profiles/profiles
```

#### gray-linear
Show the full path to a Elle Stone's Linear Gray/Gamma 1.0 profile:

```bash
$ color-profiles gray-linear
# outputs:

/usr/local/opt/color-profiles/profiles/Gray-elle-V4-g10.icc
```


#### srgb-linear
Show the full path to a Elle Stone's Linear sRGB v4 1.0 profile:

```bash
$ color-profiles srgb-linear
# outputs:

/usr/local/opt/color-profiles/profiles/sRGB-elle-V4-g10.icc
```



#### srgb-v4
Show the full path to the ICC's sRGB v4 Appearance profile:

```bash
$ color-profiles srgb-v4
# outputs:

/usr/local/opt/color-profiles/profiles/Gray-elle-V4-g10.icc
```

#### summary
List all profiles delivered with this package:

```bash
$ color-profiles summary
# outputs (shortened):

These ICC profiles came with Homebrew formula tomkyle/negatives/color-profiles.
<https://github.com/tomkyle/negatives-color-profiles>
------------------------------------------------------------
1. Gray profiles from Elle Stone's Well-Behaved ICC Profiles
<http://ninedegreesbelow.com/photography/lcms-make-icc-profiles.html#Gray>

/usr/local/opt/color-profiles/profiles/Gray-elle-V4-g10.icc
/usr/local/opt/color-profiles/profiles/Gray-elle-V4-g18.icc
/usr/local/opt/color-profiles/profiles/Gray-elle-V4-g22.icc
------------------------------------------------------------
2. sRGB v4 Appearance profile
<http://www.color.org/profiles/srgb_appearance.xalter>

/usr/local/opt/color-profiles/profiles/sRGB_ICC_v4_Appearance.icc
------------------------------------------------------------
```
