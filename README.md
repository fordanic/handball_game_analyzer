
# Handball Game Analyzer

Handball Game Analyzer is a Python-based application designed to analyze handball game videos. The primary objectives of this project are to detect and track the lines of the pitch, the ball, and the players, and to identify various events within the game such as passes, shots, goals, free throws, yellow cards, suspensions, and penalty shots. The project is developed iteratively, starting with individual images and progressing to longer video sequences.

## Table of Contents

- [Handball Game Analyzer](#handball-game-analyzer)
  - [Table of Contents](#table-of-contents)
  - [Project Overview](#project-overview)
  - [Features](#features)
  - [Installation](#installation)
    - [Prerequisites](#prerequisites)
    - [Dependencies](#dependencies)
  - [Usage](#usage)
    - [Running the Analysis](#running-the-analysis)
    - [Generating Reports](#generating-reports)
    - [Jupyter Notebooks](#jupyter-notebooks)
  - [Project Structure](#project-structure)

## Project Overview

Handball Game Analyzer leverages computer vision and machine learning techniques to provide comprehensive analysis of handball game footage. The project focuses on speed and accuracy, making it suitable for both real-time analysis and post-processing.

## Features

- **Pitch Line Detection**: Automatically detect and track the lines of the handball pitch.
- **Ball Detection and Tracking**: Identify and track the ball throughout the game.
- **Player Detection and Tracking**: Recognize and follow players from both teams.
- **Event Detection**: Detect key events such as passes, shots, goals, free throws, yellow cards, suspensions, and penalty shots.
- **Visualization**: Annotate videos with detected events and objects, and project positions onto a 2D model of the pitch.

## Installation

### Prerequisites

- Python 3.7+
- pip (Python package installer)

### Dependencies

All required packages are listed in `requirements.txt`. To install them, run:

```bash
pip install -r requirements.txt
```

## Usage

### Running the Analysis

To run the analysis on a handball video, use the `run_analysis.py` script:

```bash
python scripts/run_analysis.py --input <path_to_video> --output <output_path>
```

### Generating Reports

To generate a detailed report, use the `generate_report.py` script:

```bash
python scripts/generate_report.py --input <analysis_output> --output <report_path>
```

### Jupyter Notebooks

For exploratory analysis and prototyping, use the Jupyter notebooks in the `notebooks` directory.

## Project Structure

```bash
handball_insight/
├── data/
│   ├── raw/                     # Raw video files and images
│   ├── processed/               # Processed video files and images
│   └── annotations/             # Annotation files for training/testing
├── notebooks/
│   └── exploratory_analysis.ipynb # Jupyter notebooks for initial exploration
├── src/
│   ├── __init__.py
│   ├── data_preprocessing.py    # Functions for data loading and preprocessing
│   ├── pitch_detection.py       # Functions for detecting pitch lines
│   ├── ball_tracking.py         # Functions for detecting and tracking the ball
│   ├── player_tracking.py       # Functions for detecting and tracking players
│   ├── event_detection.py       # Functions for detecting game events
│   └── utils.py                 # Utility functions
├── models/
│   ├── pretrained/              # Pretrained models
│   └── custom/                  # Custom trained models
├── tests/
│   ├── __init__.py
│   ├── test_data_preprocessing.py
│   ├── test_pitch_detection.py
│   ├── test_ball_tracking.py
│   ├── test_player_tracking.py
│   └── test_event_detection.py
├── scripts/
│   ├── run_analysis.py          # Script to run the entire analysis
│   └── generate_report.py       # Script to generate reports
├── requirements.txt             # Python package dependencies
├── README.md                    # Overall project documentation
├── TODO.md                      # Detailed to do list
└── .gitignore                   # Git ignore file
```
