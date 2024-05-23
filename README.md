# Colstats 📊

Colstats is a powerful command-line utility designed for efficient data processing and analysis of columnar data files. Developed in Go, this tool provides high performance and ease of use, making it a perfect choice for developers, data scientists, and system administrators.

## Features 🚀

- **High Performance**: Optimized for speed and low memory usage.
- **Concurrency**: Leverages Go's concurrency model to process multiple files simultaneously.
- **Cross-Platform**: Runs on Windows, macOS, and Linux.
- **Flexible Input**: Supports various input formats like CSV, TSV, and more.
- **Basic Operations**: Supports sum and average operations on specified CSV columns.

## Installation 🛠️

### Prerequisites

- [Go](https://golang.org/doc/install) 1.16 or higher

### Build from Source

1. Clone the repository:

```sh
git clone https://github.com/theakhandpatel/Colstats.git
cd Colstats
```

2. Build the binary:

```sh
go build -o colstats
```

3. Move the binary to your PATH:

```sh
mv colstats /usr/local/bin/
```

## Usage 📝

### Basic Usage

To compute sum or average of a specific column in a CSV file:

```sh
colstats -op sum -col 1 data.csv
```

#### Concurrent Processing

Process multiple files concurrently to improve performance:

```sh
colstats -op sum -col 1 -c file1.csv file2.csv file3.csv
```

### Help ℹ️

For a complete list of options and usage instructions:

```sh
colstats --help
```

## Examples 🌟

### Compute Sum for a CSV File

```sh
colstats -op sum -col 1 example.csv
```

Output:

```
Sum of Column 1: 100
```

### Compute Average for a TSV File

```sh
colstats -op avg -col 2 -d '\t' example.tsv
```

Output:

```
Average of Column 2: 25.5
```

### Process Multiple Files

```sh
colstats -op sum -col 1 file1.csv file2.csv file3.csv
```

Output:

```
2.47427856e+08
```

## Development 🛠️

### Running Tests

To run the test suite:

```sh
go test ./...
```

### Benchmarking

To benchmark the tool:

```sh
go test -bench=.
```

### Profiling

To profile the tool for performance analysis:

```sh
go test -cpuprofile=cpu.prof -memprofile=mem.prof
```

## Contributing 🤝

Contributions are welcome! For bug reports, feature requests, or other questions, please open an issue on GitHub. To contribute code, submit a pull request with your changes.

## License 📜

This project is licensed under the MIT License. See the [LICENSE](https://github.com/theakhandpatel/Colstats/blob/main/LICENSE) file for details.

## Acknowledgments 🙏

This project is inspired by the book "Powerful Command-Line Applications in Go" by Ricardo Gerardi. Special thanks to the Go community for their contributions and support.

---

This version of the README incorporates emojis to give it a more vibrant and engaging character.