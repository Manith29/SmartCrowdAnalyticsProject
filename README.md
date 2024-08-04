

# Smart Crowd Analytics Project

This project aims to develop a real-time crowd monitoring system using IR sensors to detect human entry and exit at a venue. The system uses Firebase for data storage and visualization and employs fog and edge computing concepts for efficient data processing.

## Features

- **Real-time Monitoring:** Tracks the number of people entering and exiting a location.
- **Data Visualization:** Displays crowd data over time using matplotlib.
- **Cloud Storage:** Utilizes Firebase for storing and retrieving crowd data.
- **Edge Computing:** Processes data locally to enhance efficiency.

## Setup Instructions

### Prerequisites

- Python 3.x
- Pyrebase library
- Matplotlib library
- PySerial library
- Arduino with IR sensors

### Installation

1. **Clone the Repository:**

   ```bash
   git clone <repository-url>
   cd smart-crowd-analytics
   ```

2. **Install Required Libraries:**

   ```bash
   pip install pyrebase
   pip install matplotlib
   pip install pyserial
   ```

3. **Configure Firebase:**

   - Update the `config` dictionary in the code with your Firebase project's configuration details.

### Running the Project

1. **Run the Data Collection Script:**

   Connect your Arduino to the system and execute the script to collect data from the IR sensors.

   ```bash
   python data_collection.py
   ```

   This script will read data from the Arduino, detect entries and exits, and push the data to Firebase.

2. **Run the Data Visualization Script:**

   To visualize the data, execute the visualization script:

   ```bash
   python data_visualization.py
   ```

   This will generate a plot showing crowd data over time.

## Code Explanation

### Data Collection

The data collection script reads data from an Arduino connected to IR sensors. When someone enters or exits, it updates the counter and pushes the data to Firebase along with a timestamp.

### Data Visualization

The data visualization script retrieves data from Firebase, parses timestamps, and plots the crowd count over time using `matplotlib`.

## Hardware Requirements

- Arduino Board
- IR Sensors
- USB Cable for Arduino Connection

## License

Feel free to use this as a part of your project.

