# IoT Smart Objects Monitoring and Control  

An IoT project featuring smart objects for monitoring and controlling environmental parameters such as temperature, humidity, and light intensity across multiple locations. The project includes ESP32 sketches, an MQTT subscriber script, a web backend for database integration, and a Jupyter notebook for predictive analytics

## Overview  
This project evaluates the ability to create smart objects, implement communication and application protocols, and perform data analytics. It includes:  
- Three smart devices for monitoring temperature, humidity, and light intensity in indoor and outdoor environments.  
- Real-time data collection, HTTP and MQTT-based data transmission, and database storage.  
- Web interfaces for browsing data, managing smart nodes, and controlling an AC fan.  
- Predictive analytics using a machine learning model to forecast temperature values based on sensor data.

## Features  
### Smart Objects  
- Collects temperature every 6 seconds, humidity every 3 seconds, and light intensity every 6 seconds.  
- Displays real-time data on an LCD screen.  
- Posts data to a database via HTTP or MQTT (user-selectable).  
- Includes a heartbeat LED with a double blink every 2 seconds.  

### Web Interface  
1. **Main Dashboard:**  
   - Displays current sensor values with 5-second updates.  
   - Buttons for manually starting/stopping the AC fan.  
   - Displays the last 15 LDR sensor readings from the database.  

2. **Configuration Page:**  
   - Allows assigning unique IDs/names to smart objects.  
   - Toggles between HTTP and MQTT for data transmission.  
   - Configures manual/auto fan control and sets the temperature trigger for automatic fan activation.  

3. **Historical Data Page:**  
   - Displays historical sensor data and filters by specific smart objects.  
   - Provides options to add and manage additional smart nodes.  

### Predictive Analytics  
- A machine learning model predicts temperature values using location, LDR value, humidity, and time of day.  
- Evaluates model performance with Mean Absolute Error (MAE).  
- Outputs predicted temperatures in a Jupyter notebook.  

## Technologies Used  
- **Hardware:** ESP32, sensors for temperature, humidity, and light intensity  
- **Backend:** Python, MQTT, HTTP, and a relational database  
- **Frontend:** HTML, CSS, JavaScript (Fetch API, AJAX)  
- **Analytics:** Python (pandas, scikit-learn)  

## Project Files  
- **ESP32 Sketch:** Code for the smart devices, including data collection, LED heartbeat, and HTTP/MQTT protocols.  
- **MQTT Subscriber Script:** Fetches MQTT-published data into the database.  
- **Web Backend:** Handles database interactions and serves web pages.  
- **Database Dump:** A sample database for quick setup.  
- **Jupyter Notebook:** Contains the predictive analytics model and results.  

