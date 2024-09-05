# Project Title

Flask Application for IoT Data Visualization

## Description

This project is a Flask-based web application that interacts with a ThingSpeak IoT channel  where data was sent from an Arduino Wemos module and to retrieve and visualize sensor data (temperature and humidity). The data is fetched using the ThingSpeak API and displayed on a chart. Additionally, predicted data is stored in an SQLite database and rendered as a line chart.

## Features

- Fetches real-time data from a ThingSpeak channel.
- Stores predicted temperature and humidity data in an SQLite database.
- Visualizes the data in a web interface using charts (temperature and humidity).

## Requirements

- Python 3.x
- Flask
- Pandas
- SQLite3
- Requests

## Installation

1. Clone the repository:

   git clone <repository_url>

2. Navigate to the project directory:

   cd project_directory

3. Install the required dependencies:

   pip install -r requirements.txt

4. Set up the SQLite database:

   sqlite3 predicted_data.db

   Run the following SQL command to create the necessary table:

   CREATE TABLE IF NOT EXISTS predicted_data (
       datetime TEXT,
       temperature REAL,
       humidity REAL
   );

5. Create a `predicted/predictions.csv` file with the necessary data for temperature and humidity predictions.

## Usage

1. Run the Flask application:

   python app.py

2. Open your browser and navigate to `http://127.0.0.1:5000/` to view the web interface.

3. Use the `/thingspeak_feed` endpoint to fetch the latest ThingSpeak data and `/chart_data` to visualize the stored predictions.

## API Endpoints

- **`/`**: Home page that displays the visualization of the temperature and humidity data.
- **`/thingspeak_feed`**: Fetches the latest data from ThingSpeak.
- **`/chart_data`**: Returns the chart data in JSON format for visualization.

## Video Demonstration

<video controls src="IoT_temp_and_humidity_prediction.mp4" title="IOT video Temp"></video>
---

## Contributing

Feel free to fork this repository and submit pull requests. Any contributions are welcome!

## License

This project is licensed under the MIT License.

