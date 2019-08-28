# <p align="right"><a class="github-button" aria-label="Download ntkme/github-buttons on GitHub" href="https://github.com/Balluff-BVS/halconscripts/raw/master/Filters/Noise/noise_filters.zip" data-icon="octicon-cloud-download">Download</a></p>

SALT PEPPER DISTRIBUTION
==========

## Example

Original Picture             | Filtered Picture
:-------------------------:|:-------------------------:
![Image error](https://github.com/Balluff-BVS/halconscripts/blob/master/Filters/Noise/SpDistribiution/original.png?raw=true)  |  ![Image error](https://github.com/Balluff-BVS/halconscripts/blob/master/Filters/Noise/SpDistribiution/sp_distribiution.png?raw=true)

Description
----------

Generates a noise distribution with the values 0 and 255. The parameters *PercentSalt* and *PercentPepper* determine the percentage of white and black noise pixels, respectively. The sum of these parameters must be smaller than 100.

Input Parameters
----------

**PercentSalt** - Percentage of salt (white noise pixels).

*Default value:* 5

*Suggested values:* 1.0, 2.0, 5.0, 7.0, 10.0, 15.0, 20.0, 30.0

*Restriction:* 0 <= PercentSalt <= 100

**PercentPepper** - Percentage of pepper (black noise pixels).

*Default value:* 5

*Suggested values:* 1.0, 2.0, 5.0, 7.0, 10.0, 15.0, 20.0, 30.0

*Restriction:* 0 <= PercentSalt <= 100
