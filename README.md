# Energy Consumption Monitor

A small C program that demonstrates statistical analysis of daily electricity consumption. It calculates the average and population standard deviation of a sample dataset, then flags readings that exceed a threshold defined as the average plus two standard deviations.

The dataset contains 31 fictional daily readings. The program is an educational statistical demonstration, not a trained artificial intelligence or machine-learning model.

## Requirements

- GCC or another C compiler that supports C11
- A terminal or command prompt

## Build and run

### Linux or macOS

1. Clone the repository:
   ```bash
   git clone https://github.com/lzakLP/energy-consumption-monitor-C.git
   cd energy-consumption-monitor-C
   ```
2. Compile the program:
   ```bash
   gcc -std=c11 -Wall -Wextra -pedantic main.c -o energy_monitor -lm
   ```
3. Run it:
   ```bash
   ./energy_monitor
   ```

### Windows with MinGW

1. Clone the repository and open its folder:
   ```bash
   git clone https://github.com/lzakLP/energy-consumption-monitor-C.git
   cd energy-consumption-monitor-C
   ```
2. Compile:
   ```bash
   gcc -std=c11 -Wall -Wextra -pedantic main.c -o energy_monitor.exe -lm
   ```
3. Run:
   ```bash
   energy_monitor.exe
   ```

## Test the program

When the program starts, use the menu:

- Enter `1` to calculate the average, standard deviation, and alert threshold, and review each day's status.
- Enter `2` to display the sample dataset.
- Enter `0` to exit.

The final sample reading is intentionally set to 150 kWh. It should be identified as unusually high by the threshold-based check.

## Run online

You can also test the source without installing a compiler:

1. Open [OnlineGDB](https://www.onlinegdb.com/online_c_compiler).
2. Select C as the language.
3. Paste the contents of `main.c` into the editor.
4. Select Run and enter one of the menu options in the console.

## Project files

- `main.c`: program source code
- `Makefile`: optional build commands for systems with make
- `.gitignore`: files excluded from version control
- `LICENSE`: MIT License

## Notes

All readings are fictional and intended for testing. The threshold is a simple statistical rule; it does not establish the cause of an unusual reading. Real-world monitoring would require actual meter data and additional context.

## License

Distributed under the MIT License. See [LICENSE](LICENSE).
