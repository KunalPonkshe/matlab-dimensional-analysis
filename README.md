# Dimensional Analysis and Regression Modeling in MATLAB

A MATLAB coursework project exploring how dimensional analysis and
regression can be used to describe relationships between physical
variables and examine scale-model similarity.

The workflow constructs dimensionless groups using the Buckingham Pi
theorem, fits candidate regression models, compares their fit using
Akaike Information Criterion (AIC), and calculates parameter changes
that preserve the constructed dimensionless groups.

## Project overview

The original analysis uses 200 observations and nine selected physical
variables involving mass, volume, density, length, concentration,
pressure, and pressure gradients.

The workflow includes:

- Representing physical dimensions in a dimensional exponent matrix.
- Using reduced row echelon form to construct six dimensionless groups.
- Normalizing the groups for regression analysis.
- Fitting multivariable linear, exponential, and power-law models.
- Comparing candidate fits using AIC.
- Examining coefficient significance with a Bonferroni-adjusted threshold.
- Constructing a scaled parameter set and checking preservation of
  the dimensionless groups.

## Methods and tools

MATLAB · Linear algebra · Buckingham Pi theorem · Dimensional analysis ·
Linear and nonlinear regression · AIC · Multiple-testing correction ·
Dimensional similarity

The source uses `rref`, `fitlm`, and `fitnlm`.

## Repository contents

| File | Description |
|------|-------------|
| `dimensional_analysis.m` | Original MATLAB analysis script |
| `coursework_report.pdf` | Original published MATLAB report, including code and outputs |

## Requirements and data

The original report was generated using MATLAB R2024b. The regression
functions require Statistics and Machine Learning Toolbox.

The script currently expects a variable named `Project_data` to exist
in the MATLAB workspace, with the measurement table at
`Project_data{2,2}`.

The course-provided data generator is not included. This initial
release preserves the coursework analysis and is not yet a
self-contained, reproducible package.

## Current status

The original coursework is included as a baseline. Code cleanup and
technical review are in progress.

Planned updates include:

- Verify variable dimensions against the assignment definitions.
- Reconcile the scale-model assumptions with the calculated results.
- Correct coefficient transformations between normalized and
  unnormalized variables.
- Clarify that the linear equation fitted with `fitnlm` is a solver
  comparison rather than a separate model family.
- Add an explicit data-loading workflow and input validation.
- Add observed-versus-predicted and residual plots.
- Replace lengthy console output with concise results summaries.

The original report reflects the submitted coursework and has not
yet been updated to incorporate these revisions.

## Background

Developed as part of undergraduate biomedical engineering coursework
at Georgia Tech. The project demonstrates the connection between
physical reasoning, matrix methods, and computational modeling.
