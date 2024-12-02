# Geomagnetic Storm Prediction Dataset Preparation

This repository contains a program designed to prepare a dataset to aid the NOAA Space Weather Prediction Center in predicting Geomagnetic Storms (GSTs). The dataset combines Coronal Mass Ejection (CME) data and Geomagnetic Storm (GST) data from NASA's APIs and computes useful metrics for future machine learning applications.

---

## Features

1. **Data Extraction**: 
   - Fetches CME and GST data from NASA's APIs.
   
2. **Data Merging**: 
   - Combines the CME and GST datasets based on relevant criteria.

3. **Metric Computation**: 
   - Calculates the average time it takes for a CME to cause a GST.

4. **Data Preparation for Machine Learning**: 
   - Outputs a cleaned and enriched dataset for predictive modeling.

---

## Prerequisites

Before running the program, ensure you have the following:

- **Python 3.7+** installed.
- Dependencies listed in `requirements.txt`. Install them using:

  ```bash
  pip install -r requirements.txt
  ```

- Access to the NASA API. Obtain an API key from [NASA's API documentation](https://api.nasa.gov/).

---

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/saracmoujahed/data-sourcing-challenge.git
   cd data-sourcing-challenge
   ```

2. Set up your environment variables:
   - Create a `.env` file in the root directory.
   - Add your NASA API key:

     ```plaintext
     NASA_API_KEY=your_api_key_here
     ```

---

## Usage

Run the script using the command:

```bash
python retrieve_data.ipynb
```

### Workflow

1. **Data Fetching**:
   - The program fetches CME and GST data using the NASA API.
   
2. **Data Processing**:
   - Merges the data based on event timings.
   - Calculates the time delay between CME and GST occurrences.
   
3. **Output**:
   - Generates a CSV file containing the enriched dataset.

---

## Output

- **Processed Dataset**: The program produces a CSV file containing:
  - CME event details.
  - GST event details.
  - Computed delay time between CME and GST.

---

## Example Dataset Entry

| CME Event Time       | GST Event Time       | Delay (hours) | CME Details | GST Details |
|----------------------|----------------------|---------------|-------------|-------------|
| 2024-11-29 14:00:00 | 2024-11-30 06:00:00 | 16            | {...}       | {...}       |

---

## Future Work

This dataset can be utilized to train machine learning models to:

- Predict GSTs based on CME data.
- Improve early warning systems for power grids and GPS operators.

---

## Contributing

Contributions are welcome! Please fork this repository and submit a pull request for any enhancements or bug fixes.

---

## License

This project is licensed under the [MIT License](LICENSE).

---

## Acknowledgments

- NOAA Space Weather Prediction Center for inspiring this project.
- NASA for providing open access to CME and GST data.
- This project was developed with the assistance of ChatGPT, an AI language model created by OpenAI. The model helped in generating ideas, code snippets, and documentation to enhance the overall development process.

--- 

