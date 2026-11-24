# marupeke-cv-solver
Solves Marupeke puzzles from a photo: it detects the grid, reads each cell, solves the puzzle and draws the solution on top of the original image.

Pipeline order:
 
```
photo/image_adquisition → image_preprocessing → grid_alignment → cell_classification → marupeke_solver → solution_visualization
```

## Board representation
The board is a 2D NumPy array of integers, using the following meanings:

| Value | Meaning  |
|-------|----------|
| 0     | `EMPTY`  |
| 1     | `O`      |
| 2     | `X`      |
| 3     | `BLACK`  |


## Setup

- **Python 3.13**
- Recommended: use a virtual environment (`.venv`) and install dependencies with `pip install -r requirements.txt`.
- New libraries go in `requirements.txt` as `package==version`.


## Project structure

- `src/`: all code files.
- `data/`: input images and puzzles, in subfolders by type (raw images, processed images, txt…).
- `results/`: solutions and output images.

Always save files with unique names (e.g. `name_date`) in the folder that matches their type or origin.

## Conventions

- Everything in English: code, comments and commit messages.
- `snake_case` for files, functions and variables.
- Pull before starting and remenber to commit and push changes.