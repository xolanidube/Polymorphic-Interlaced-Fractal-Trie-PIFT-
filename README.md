# Polymorphic Interlaced Fractal Trie (PIFT)

## Overview

The PIFT is a theoretical, breakthrough-level data structure designed in the Data Structures domain. 
It uses a fractal mapping to store keys in a trie-like structure, hypothesized to offer 
improved theoretical lookup complexities.

## Mathematical Background

Each key symbol s is mapped to an integer code, then expanded into multiple coordinates 
via a fractal mapping function:

$$
f(\text{symbol\_code}) \rightarrow (\text{coord}_1, \text{coord}_2, \ldots)
$$

In this prototype, we just produce two coordinates by repeatedly dividing by the branch_factor.

## Hypothesized Complexity

We conjecture improved complexity:

$$
\text{Lookup complexity} \sim O\left(\frac{\log n}{\log(\log n)}\right)
$$

This is a theoretical claim, not proven here.

## Implementation Details

- `insert(key, value)`: Insert a key by fractally distributing each symbol.
- `search(key)`: Search for a key by following fractal coordinates.
- `delete(key)`: Remove a key if present (basic lazy delete).

## Validation and Testing

We perform academic testing: insert a few keys, search them, and confirm correctness.
No performance guarantees are validated here—it's a conceptual prototype.

## Potential Real-World Applications

- High-speed lookups in enormous, complex key-spaces.
- Advanced indexing for genomic or large dataset searches.
- Innovative routing tables in large-scale networking scenarios.

## Usage

Just run the script to see a basic test. For real use, integrate into a Python environment and experiment.
