
# Useful ICC profiles

**This repo is intended for making the profiles “installable“ as a Homebrew formula.**

## Elle Stone’s Well-Behaved ICC Profiles

Elle Stone's [Well-Behaved ICC Profiles](http://ninedegreesbelow.com/photography/lcms-make-icc-profiles.html) provide common ICC profiles for both color and gray images with gamma values ranging from 1.0 (linear) to 2.2 (typical).

> These profiles are for use with RGB images that have been converted to monotone gray (black and white). The main reason to convert from RGB to Gray is to save the file space needed to encode the image.

This repo is just a redistribution of Elle Stone's [Gray profiles](http://ninedegreesbelow.com/photography/lcms-make-icc-profiles.html#Gray), as of May 2017. Please also have a look on her official repo: [Elle's ICC profiles](https://github.com/ellelstone/elles_icc_profiles) on GitHub.



## sRGB v4 Appearance profile
This sRGB profile is provided by the ICC (International Color Consortium). See their page [sRGB Appearance profile](http://www.color.org/profiles/srgb_appearance.xalter) for more information. In short:

> This profile is a v4 replacement for commonly used sRGB v2 profiles. It gives better results in workflows that implement the ICC v4 specification, and is intended to be used in combination with other ICC v4 profiles.

## Usage


### Show profiles directory

The `directory` command will output the directory whery the ICC profiles are located in local Homebrew ecosystem:

```bash
$ iccprofiles directory
# outputs:
/usr/local/opt/iccprofiles/profiles
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
