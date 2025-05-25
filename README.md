# jmeterTest

This project contains a JMeter test plan for automating HTTP POST and GET requests to [blazedemo.com](https://blazedemo.com), a demo flight booking site. The tests simulate selecting a flight from one city to another and purchasing a ticket, using both hardcoded and parameterized data.

## Project Structure

- `Test Plan.jmx`: The main JMeter test plan file.
- `jmetertest.csv`: CSV file with test data (fromPort and toPort values).
- `README.md`: Project documentation.

## How It Works

- The test plan uses a CSV Data Set Config to parameterize requests with data from `jmetertest.csv`.
- Three HTTP samplers are included:
  - **Reserva**: Selects a flight from city A to city B on blazedemo.com using hardcoded parameters.
  - **ReservaDesdeCSV**: Selects a flight from city A to city B using parameters from the CSV file.
  - **CompraDeTiquete**: Purchases a ticket for a selected flight, using hardcoded parameters (not from the CSV).

## Running the Test

1. Open `Test Plan.jmx` in JMeter.
2. Ensure the path to `jmetertest.csv` is correct.
3. Run the test plan.
4. View results in the "View Results Tree", "Aggregate Report", or "Summary Report" listeners.

## Requirements

- [Apache JMeter](https://jmeter.apache.org/) 5.6.3 or compatible.

## Notes

- The CSV file uses `;` as a delimiter.
- Update the CSV file to add more test cases as needed.