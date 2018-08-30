# 🆇🅴🅻🅵.MagicaVoxel.Shaders
* Shaders for MagicaVoxel
  * Tested with MagicaVoxel 0.99.1a for Windows

## Installation

Install the shader by copying the file from the [`shader`](shader) directory in this project into the `shader` directory of your MagicaVoxel installation.

## Groupable Blur
* [blur.txt](shader/blur.txt): Shader file of the Groupable Blur

### console commands
* xs blur `color group stride` `center weight bias`

### Example

* [`blur-sample.vox`](vox/blur-sample.vox): A sample vox file for the Groupable Blur 
  * `original`➡🔨`xs blur 8`➡`step 1`➡🔨`xs blur 8`➡`step 2`➡🔨`xs blur 8`➡`step 3`

|||
|---|---|
|![step 0](image/xs%20blur%208%20step%200.png)<br>original|![step 1](image/xs%20blur%208%20step%201.png)<br>step 1
|![step 2](image/xs%20blur%208%20step%202.png)<br>step 2|![step 3](image/xs%20blur%208%20step%203.png)<br>step 3|
