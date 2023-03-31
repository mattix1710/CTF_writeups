# hideme

![type_forensics](https://img.shields.io/badge/type-forensics-red)
![sub_type_steganography](https://img.shields.io/badge/sub_type-steganography-orange)
![level_easy](https://img.shields.io/badge/level-easy-green)
![points_100](https://img.shields.io/badge/points-100-blue)

## Intro
> Every file gets a flag.
> The SOC analyst saw one image been sent back and forth between two people. They decided to investigate and found out that there was more than what meets the eye [here](https://artifacts.picoctf.net/c/258/flag.png).

## Solution
The easiest way is to use `foremost <file>`. Next go into **output** folder, find ZIP archive, unpack it and read the flag from the picture.