# Energy Consumption Monitor

An educational project concept for analyzing daily electricity consumption with basic descriptive statistics in C.

The documented approach calculates the average and population standard deviation of a sample dataset, then uses the threshold

`average + 2 × standard deviation`

to flag unusually high readings.

> **Repository status:** The current repository contains this README only. The C source code, build files, and license referenced by the earlier documentation are not present in the `main` branch. The program therefore cannot currently be compiled or executed from this repository.

## Intended behavior

The planned demonstration uses 31 fictional daily electricity readings.

The intended program flow is:

1. Load or define the sample consumption readings.
2. Calculate the arithmetic mean.
3. Calculate the population standard deviation.
4. Compute the alert threshold as the mean plus two standard deviations.
5. Compare each daily reading with the threshold.
6. Display the dataset and identify readings above the threshold.

The previously documented sample includes a final reading of 150 kWh, intended to demonstrate the alert condition. This behavior cannot be verified until the source code is available.

## Statistical method

For (n) readings (x_1, x_2, ldots, x_n), the arithmetic mean is:

`mean = (x1 + x2 + ... + xn) / n`

The population standard deviation is:

`standard_deviation = sqrt(sum((xi - mean)^2) / n)`

The alert threshold is:

`threshold = mean + 2 * standard_deviation`

A reading above this threshold is flagged for review. This is a simple statistical rule and does not establish the cause of an unusual measurement.

## Planned technology

- C language.
- C11-compatible compiler.
- GCC or MinGW.
- Standard C library and math library.

## Planned build workflow

Build instructions will be provided after the source code and build files are added to the repository.

For reference, the intended GCC command is:

```bash
gcc -std=c11 -Wall -Wextra -pedantic main.c -o energy_monitor -lm
```

This command is not currently executable against the repository because `main.c` has not been committed.

## Planned project files

```text
energy-consumption-monitor-C/
├── main.c
├── Makefile
├── .gitignore
├── LICENSE
└── README.md
```

## Limitations

- The dataset is fictional and intended for educational use.
- The threshold is a basic statistical indicator, not a predictive model.
- A value above the threshold should be investigated with additional context.
- No real meter integration or automated data collection is included in the documented scope.

## Next steps

- [ ] Add the C source code to the repository.
- [ ] Add and verify the build instructions.
- [ ] Include the actual sample dataset and expected output.
- [ ] Add a license file if the project is intended for redistribution.
- [ ] Verify the program with a C11 compiler.
