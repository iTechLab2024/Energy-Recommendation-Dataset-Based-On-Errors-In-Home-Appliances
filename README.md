###### Energy-Recommendation-Dataset-Based-On-Error-For-Home-Appliances  
<a href="https://doi.org/10.5281/zenodo.16279369"><img src="https://zenodo.org/badge/1023751746.svg" alt="DOI"></a>

A structured dataset of contextual energy-saving recommendations based on smart appliance error scenarios. Useful for training NLP models, smart home diagnostics, and energy-aware IoT systems.

# Energy Recommendation Dataset Based on Error for Home Appliances

## Overview
This repository contains a dataset of contextual, energy-saving recommendations generated in response to specific error scenarios from common household appliances. The dataset is designed for applications in intelligent energy systems, IoT analytics, and natural language processing (NLP) for smart environments.

## Table of Contents
- [Dataset Description](#dataset-description)
- [Data Fields](#data-fields)
- [Example Data](#example-data)
- [Use Case](#use-case)
- [Usage](#usage)
  - [Loading the Dataset](#loading-the-dataset)
  - [Preprocessing](#preprocessing)
  - [Filtering Examples](#filtering-examples)
- [Repository Structure](#repository-structure)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)
- [Acknowledgments](#acknowledgments)

## Dataset Description
This dataset links real-world appliance error scenarios (e.g., "Door open", "Compressor heating") to human-readable recommendations for improving energy efficiency or resolving system issues. Each row contains:
- A recommendation
- The device and error context
- The frequency of the issue (High, Medium, Low)

It is ideal for training NLP models, simulating intelligent energy systems, and powering rule-based or ML-based smart assistants.

### Data Fields
- `Recommendations`: Textual advice for resolving a condition or reducing energy consumption.
- `input_real`: Device type and error description (e.g., "Device: fridge, Error:Door open").
- `frequency`: How common the situation is — `High`, `Medium`, or `Low`.

### Example Data

| Recommendations                                         | input_real                                      | frequency |
|---------------------------------------------------------|--------------------------------------------------|-----------|
| Avoid leaving the door open for extended periods.       | Device: fridge, Error:Door open                 | High      |
| Do not overload the fridge or block air vents inside.   | Device: fridge,Error: major                     | High      |
| Schedule regular maintenance checks.                    | Device: fridge, Error:Sensor malfunction        | Medium    |
| Clean coils at the back to improve efficiency.          | Device: fridge, Error:Compressor heating        | Low       |

## Use Case
This dataset supports:
- Training or evaluating NLP models for energy-saving recommendations.
- Simulating smart assistant or chatbot behavior for appliance troubleshooting.
- Analyzing error-condition trends in home appliances.
- Developing rule-based or ML-based energy efficiency engines.

## Usage

### Loading the Dataset
```python
import pandas as pd

# Load the dataset
df = pd.read_csv('Final_Recommendations.csv', encoding='ISO-8859-1')
print(df.head())
```

### Preprocessing
```python
# Clean and normalize text
df.columns = df.columns.str.strip()
df['input_real'] = df['input_real'].str.strip()
df['frequency'] = df['frequency'].str.strip()
```

### Filtering Examples
```python
# Filter by device type or specific error
fridge_data = df[df['input_real'].str.contains('fridge', case=False)]
door_open_issues = df[df['input_real'].str.contains('Door open', case=False)]
```

## Repository Structure

    README.md: Project documentation.

    Energy-Recommendation-Dataset-Based-On-Errors-In-Home-Appliances.csv: Main dataset file.

    notebooks/: (Optional) Sample notebooks for data analysis or model development.

## Contributing

Contributions and suggestions are welcome! Feel free to open an issue or submit a pull request if you’d like to enhance this dataset or provide a use case.

## License

This project is licensed under the MIT License. See the LICENSE file for more details.

## Contact

For questions, feedback, or collaboration inquiries, please contact:
itechlab2024@gmail.com

## Acknowledgments

Thanks to the open-source and research community. Helpful tools and platforms:

 - **[pandas](https://pandas.pydata.org/)**
- **[scikit-learn](https://scikit-learn.org/)**
- **[Matplotlib](https://matplotlib.org/)**
- **[Stack Overflow](https://stackoverflow.com/)**
- **Open Source Community**
- **Online Courses and Tutorials**
