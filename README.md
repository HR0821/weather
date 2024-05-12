# Scheduled Weather Data Grabbing Job
This is a Python script that performs scheduled data grabbing of weather data for Hong Kong. It makes use of the HKO (Hong Kong Observatory) API to fetch the weather forecast and logs the extracted data to a CSV file.

## Prerequisites
Before running the script, make sure you have the following dependencies installed:

`Python 3.7`

requests library: You can install it using pip with the following command:

`pip install requests`

schedule library: You can install it using pip with the following command:

`pip install schedule`

## Setup and Usage
1. Clone or download the repository to your local machine.
2. In the terminal, navigate to the project directory.
3. Find the `weather data_grabber.py` file to open and run or run the script using the following command:

`python weather data_grabber.py`
This will start the scheduled job that grabs weather data from the HKO API and logs it to the `weather_data.csv file`.

4. The script will run indefinitely and fetch weather data every day. You can stop the script by pressing `Ctrl+C` in the terminal.

## Output
The weather data will be logged to a CSV file named weather_data.csv. The file will be created in the same directory as the script if it doesn't exist. Each row in the CSV file represents a weather data entry, including the date, maximum temperature, minimum temperature, maximum relative humidity, minimum relative humidity, wind information, and weather description.

## Testing
To test the scheduled job and ensure it runs as expected, you can manually check the weather_data.csv file after running the script for a few days. Verify that new weather data entries are added to the file each day at the specified intervals. Additionally, you can check the console output for any error messages.

If it is difficult to check that the code is correct because the time interval is daily, we can change the code from 

`schedule.every().day.do(job)`

to

`schedule.every().minute.do(job)`

to help us test the code correctly quickly.

In the compressed file, `weather_data.csv` already has the correct weather data that I tested.

If you encounter any issues or errors during the setup or usage of the script, please refer to the Issues section of the repository to see if a similar problem has been reported. If not, feel free to open a new issue with relevant details, including the error message and steps to reproduce the issue.
