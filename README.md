# Binary String Matching Genetic Algorithm

A small Python command-line simulation that uses a genetic algorithm to evolve a population of binary strings toward a user-provided target.

## Requirements

- Python 3
- No third-party packages

## Run

From the project directory, run:

```powershell
python genetic_algo_implementation.py
```

If `python` is not recognized on your system, try `py` instead:

```powershell
py genetic_algo_implementation.py
```

## Usage

When prompted, enter a target binary sequence and an initial binary string of the same length. For example:

```text
Enter the target binary sequence (e.g., 10101010): 111111
Enter the initial binary string (must be same length as target): 101010
```

The program prints each generation's chromosomes, fitness scores, and fitness percentages. It also displays the selected parents and offspring before and after mutation. Because the algorithm uses random operations, results can vary between runs.

## How It Works

1. The initial population contains the user-provided string and four randomly generated strings.
2. Fitness is the number of bit positions that match the target.
3. The two highest-fitness chromosomes are selected as parents.
4. Single-point crossover is applied with probability `0.9`.
5. Each bit is independently flipped with probability `0.01`.
6. The next population contains five offspring. The algorithm stops if it finds the target or reaches 50 generations.

## Configuration

The main parameters are defined near the top of `genetic_algo_implementation.py`:

| Setting | Default |
|---|---:|
| Population size | 5 |
| Crossover probability | 0.9 |
| Per-bit mutation probability | 0.01 |
| Maximum generations | 50 |

## Project Files

- `binary_string_matching` - Genetic algorithm implementation.
- `README.md` - Project overview and run instructions.
