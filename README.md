# YieldCurveDislocationScanner

A Python-based tool that identifies relative value dislocations across the U.S. Treasury yield curve using historical z-scores. The scanner retrieves data from the FRED API and highlights barbell and butterfly spread structures that deviate from historical norms.

## Features

- Pulls historical daily yield data from FRED API
- Supports both US barbell and US butterfly structures
- Computes z-scores for each spread to identify dislocations
- Flags spreads exceeding a user-defined std. threshold

## Spread Structures

### Barbell
- 2s10s
- 5s30s
- 7s30s
- 1s30s

### Butterfly
- 2s5s10s
- 5s10s30s
- 3s7s20s
- 10s15s30s
- 1s3s5s

## Requirements

- fredapi
- pandas
- matplotlib
- scipy

## Usage

Run the script and enter a z-score threshold when prompted (e.g., `2`, `2.5`, or `3`).  
The tool will flag and plot any spread that exceeds ±σ based on its historical distribution since July 2023.
