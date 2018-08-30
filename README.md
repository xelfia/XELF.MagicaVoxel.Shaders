# 🆇🅴🅻🅵.MagicaVoxel.Shaders
* Shaders for MagicaVoxel
  * Tested with MagicaVoxel 0.99.1a for Windows

## Installation

Install the shader by copying the file from the `shader` directory in this project into the `shader` directory of your MagicaVoxel installation.

## Groupable Blur

* xs blur `color group stride` `center weight bias`

### Example

* `original`➡🔨`xs blur 8`➡`step 1`➡🔨`xs blur 8`➡`step 2`➡🔨`xs blur 8`➡`step 3`

|||
|---|---|
|![step 0](image/xs%20blur%208%20step%200.png)<br>original|![step 1](image/xs%20blur%208%20step%201.png)<br>step 1
|![step 2](image/xs%20blur%208%20step%202.png)<br>step 2|![step 3](image/xs%20blur%208%20step%203.png)<br>step 3|
