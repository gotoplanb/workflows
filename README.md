# GitHub Actions Workflow Examples

This repository contains several example GitHub Actions workflows demonstrating different features and patterns.

## Individual Workflows

### Hello World (`hello-world.yml`)
A simple workflow that demonstrates input handling with a greeting.
- **Input**: `name` (optional string)
- **Output**: Logs "Hello {name}" if name is provided, otherwise "Hello World"
- **Usage**: Run manually and optionally provide a name

### Add Numbers (`add.yml`)
A workflow that demonstrates basic arithmetic operations.
- **Inputs**: 
  - `number1` (required number)
  - `number2` (required number)
- **Output**: Logs the sum of the two numbers
- **Usage**: Run manually and provide two numbers to add

### Random Number Generator (`random.yml`)
Generates a random number within a specified range.
- **Input**: `max_number` (required number, default: 100)
- **Output**: A random number between 1 and max_number
- **Usage**: 
  - Run manually with a maximum number
  - Can be called by other workflows

### Square Number (`square.yml`)
Squares a given number.
- **Input**: `number` (required number)
- **Output**: The square of the input number
- **Usage**: Run manually with a number to square

### Analyze Number (`analyze.yml`)
Determines if a number is even or odd.
- **Input**: `number` (required number)
- **Output**: Logs whether the number is even or odd
- **Usage**: 
  - Run manually with a number to analyze
  - Can be called by other workflows

## Chained Workflows

### Chain Workflow (`chain.yml`)
Demonstrates workflow composition by chaining multiple workflows together.
- **Input**: `max_number` (required number, default: 100)
- **Process**:
  1. Generates a random number using the `random` workflow
  2. Passes that number to the `analyze` workflow
  3. Shows if the random number was even or odd
- **Usage**: Run manually with a maximum number

## How to Run Workflows

1. Go to the "Actions" tab in the GitHub repository
2. Select the desired workflow from the left sidebar
3. Click "Run workflow"
4. Provide the required inputs
5. Click "Run workflow" to execute

## Features Demonstrated

- Workflow dispatch triggers
- Input parameters
- Job outputs
- Step outputs
- Workflow composition
- Conditional execution
- Shell scripting in workflows
- Data passing between workflows