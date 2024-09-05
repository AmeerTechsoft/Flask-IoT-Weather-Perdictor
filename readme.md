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

1. Clone the repository
```bash
   git clone https://github.com/AmeerTechsoft/Flask-IoT-Weather-Perdictor.git
   ```

2. Navigate to the project directory:
```bash
   cd project_directory
```
3. Install the required dependencies:
```bash
   pip install -r requirements.txt
```
4. Set up the SQLite database:
```bash
   sqlite3 predicted_data.db
```
   Run the following SQL command to create the necessary table:
```bash
   CREATE TABLE IF NOT EXISTS predicted_data (
       datetime TEXT,
       temperature REAL,
       humidity REAL
   );
```
5. Create a `predicted/predictions.csv` file with the necessary data for temperature and humidity predictions.

## Usage

1. Run the Flask application:
```bash
   python app.py
```
2. Open your browser and navigate to `http://127.0.0.1:5000/` to view the web interface.

3. Use the `/thingspeak_feed` endpoint to fetch the latest ThingSpeak data and `/chart_data` to visualize the stored predictions.

## API Endpoints

- **`/`**: Home page that displays the visualization of the temperature and humidity data.
- **`/thingspeak_feed`**: Fetches the latest data from ThingSpeak.
- **`/chart_data`**: Returns the chart data in JSON format for visualization.

## Video Demonstration


https://github.com/user-attachments/assets/1f1e4967-1d26-4ed7-91c4-f0ef3ef0e665

---

## Contributing

Feel free to fork this repository and submit pull requests. Any contributions are welcome!

## License

This project is licensed under the MIT License.

