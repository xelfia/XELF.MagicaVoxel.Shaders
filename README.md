# 🆇🅴🅻🅵.MagicaVoxel.Shaders
* Shaders for [MagicaVoxel](https://ephtracy.github.io/)
  * Tested with MagicaVoxel 0.99.1a for Windows

## Basic Informations
MagicaVoxel shader is a processor of vox model object. Installed MagicaVoxel shader can use from the Console in MagicaVoxel.

## Installation

Install the shader by copying the file from the [📁`shader`](shader) directory in this project into the 📁`shader` directory of your MagicaVoxel installation.

## Groupable Blur
* [🗎`blur.txt`](shader/blur.txt): Shader file of the Groupable Blur
* This will assist you:
  * To make a gradient.
  * To add an antialiasing effect.
  * To add a rounded corner effect.
* Keeps it shape:
  * Empty voxel to empty voxel
  * Valid voxel to valid voxel
* Palette can group: 
  * Each group will not blur into each other.
  * Colors in the same group only will blur.
* Shader can only access voxels:
  * Needs preparation of a proper palette you want.

### Console Commands
* **xs blur `color group stride` `center weight bias`**
** `color group stride`: [1…256] (default: 1)
** `center weight bias`: [-1…256] (default: 0)

### Notes
* Empty voxels (color index: `0`) are grouped into `-1`.
* Other valid voxels (color index: `1`…`255`) are grouped into `0+`.

### Command Examples

* **xs blur 8**
  * Palette grasped `8`<sub>tones</sub> × `32`<sub>groups</sub>
  * Each row on the palette UI is an independent group 
* **xs blur 256**
  * Palette grasped `256`<sub>tones</sub> × `1`<sub>group</sub>
  * For a grayscale-like palette (255 tone levels + 1 empty)
* **xs blur 8 4**
  * a bit large `center weight bias`=`4` will work as an antialiasing effect / a rounded corner effect.
* **xs -n 3 blur 8**
  * In the following sample, by one time run, the original model will become into the result of step 3.

### Samples

* [`blur-sample.vox`](vox/blur-sample.vox): A sample vox file for the Groupable Blur 
  * `original`➡🔨`xs blur 8`➡`step 1`➡🔨`xs blur 8`➡`step 2`➡🔨`xs blur 8`➡`step 3`

|||
|---|---|
|![step 0](image/xs%20blur%208%20step%200.png)<br>original|![step 1](image/xs%20blur%208%20step%201.png)<br>step 1
|![step 2](image/xs%20blur%208%20step%202.png)<br>step 2|![step 3](image/xs%20blur%208%20step%203.png)<br>step 3|
