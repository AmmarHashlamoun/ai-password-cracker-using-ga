This project implements a Genetic Algorithm (GA) to perform cryptanalysis of text encrypted with a Vigenère cipher. It was developed as part of an undergraduate Artificial Intelligence course assignment.

## Overview
The genetic algorithm works by:
1. Creating a population of random potential keys
2. Evaluating each key's fitness based on how closely the decrypted text matches expected English letter frequencies
3. Using selection, crossover, and mutation to create a new generation of keys
4. Repeating until the maximum number of generations is reached or a satisfactory key is found

## Features
- Support for different key sizes (26 or 40 characters)
- Configurable genetic algorithm parameters:
    - Population size
    - Tournament selection size
    - Mutation rate
    - Elite carry-over size
    - Crossover rate

- Two crossover types:
    - Uniform crossover (0)
    - Single-point crossover (1)

- Performance tracking and logging:
    - Generation-by-generation logging in CSV format
    - Final results output with best key and fitness score

## Usage
1. Run the class `GeneticAlgorithm`
2. Enter the following parameters when prompted:
    - Run ID (for output file naming)
    - Key size (26 or 40)
    - Population size
    - Tournament size
    - Mutation rate (0.0-1.0)
    - Elite carry-over size
    - Crossover rate (0.0-1.0)
    - Crossover type (0 for uniform, 1 for single-point)
    - Maximum number of generations

## Output Files
For each run, the program generates:
1. `[RunID]_results.txt` - Contains the best key found, its fitness score, and all parameters used
2. `[RunID]_log.csv` - A CSV file tracking best, average, and worst fitness scores for each generation

## Project Structure
- - Main class implementing the genetic algorithm `GeneticAlgorithm.java`
- - Represents a single candidate solution (potential key) `Chromosome.java`
- - Contains methods for decryption and fitness evaluation `Evaluation.java`
- - Utility methods for statistical calculations `Calculations.java`

## Requirements
- Java (developed with JDK 22)
- Encrypted text file (default path: ) `A1-GeneticAlgorithmPasswordCracking/Data2.txt`

## Algorithm Details
The fitness function evaluates each key by:
1. Decrypting the encrypted text with the candidate key
2. Calculating the frequency distribution of letters in the decrypted text
3. Comparing this distribution to the expected frequency distribution of English text
4. Returning a score based on the total difference (lower scores are better)

The genetic algorithm uses tournament selection to choose parents for each new generation, applying crossover and mutation to create offspring with potentially better fitness.
