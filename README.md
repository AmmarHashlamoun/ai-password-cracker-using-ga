# Genetic Algorithm Cryptanalysis: Vigenère Cipher Decryption

This project implements a Genetic Algorithm (GA) to perform cryptanalysis of text encrypted with a Vigenère cipher.

## Objective

Break encrypted text (ciphertext) without knowing the original key, using Genetic Algorithm techniques such as:
- Fitness evaluation
- Selection
- Crossover
- Mutation

## Core Features

- Dynamically sized population and key length
- Chromosome-based key encoding
- Decryption and fitness scoring using n-gram frequency analysis
- Multi-run support to compare configurations

## Project Structure

decryptga/
│
├── GeneticAlgorithm.java     # Main GA engine: initialization, loop, evolution
├── Chromosome.java           # Represents an individual (candidate key)
├── Evaluation.java           # Fitness, decryption, and helper methods
├── Data1.txt / Data2.txt     # Ciphertexts to decrypt
└── README.md                 # Project overview (this file)

## How to Run

1. Compile the project:
```bash
javac decryptga/*.java

	2.	Run the main class:

java decryptga.GeneticAlgorithm

	3.	Follow prompts to enter:

	•	Key size (26 or 40)
	•	Population size
	•	Number of generations

## Output

The algorithm prints:
	•	Best key per generation
	•	Decrypted output from best key
	•	Fitness scores of the final population


