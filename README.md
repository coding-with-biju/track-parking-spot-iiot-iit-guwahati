Track Parking Spot Project

Overview
The Track Parking Spot project uses four ultrasonic sensors to monitor parking spaces and track their availability. Additionally, the system captures environmental data such as temperature and humidity using a DHT11 sensor. The data is sent to a server and displayed on a dashboard for real-time tracking of parking spot status and environmental conditions.

 Features
1. Parking Spot Detection:
   - Monitors the availability of four parking spots using ultrasonic sensors.
   - Reports the status as "Available" or "Occupied."

2. Environmental Monitoring:
   - Captures temperature and humidity data using a DHT11 sensor.

3. Real-Time Data Processing:
   - Sends parking and environmental data to a Node.js server.
   - Stores data in a MySQL database.
   - Displays the data on a web-based dashboard.

Hardware Requirements
1. ESP8266 NodeMCU
2. DHT11 Sensor
3. 4 Ultrasonic Sensors (e.g., HC-SR04)
4. Jumper Wires
5. Breadboard
6. Power Supply

 Software Requirements
1. Arduino IDE (to program NodeMCU)
2. Node.js (server-side application)
3. MySQL (database)
4. PHP (for dashboard integration)
5. Web Browser (to view the dashboard)

 System Architecture
1. ESP8266 NodeMCU
   - Reads data from the ultrasonic sensors and DHT11.
   - Sends data to the Node.js server via HTTP POST.

2. Node.js Server
   - Receives and processes data from the ESP8266.
   - Stores data in the MySQL database.

3. MySQL Database
   - Stores parking statuses and environmental data.

4. Dashboard
   - Displays real-time parking and environmental data using PHP, HTML, CSS, and JavaScript.

How to Set Up
 Hardware Setup
1. Connect the DHT11 sensor to the ESP8266:
   - VCC -> 3.3V
   - GND -> GND
   - DATA -> D4

2. Connect each ultrasonic sensor to the ESP8266:
   - Trigger Pins: D1, D2, D5, D6
   - Echo Pins: D7, D8, D9, D10

3. Power the ESP8266 and sensors.

 Software Setup
1. Arduino IDE
   - Install required libraries (e.g., DHT, ESP8266WiFi).
   - Upload `esp8266_code.ino` to the NodeMCU.

2. Node.js Server
   - Install dependencies with `npm install`.
   - Start the server: `node server.js`.

3. MySQL Database
   - Create the database using `parking_system.sql`.

4. Dashboard
   - Place PHP files (`db_config.php`, `fetch_data.php`) in your web server’s directory.
   - Access the dashboard via your browser.

 Example Output
 Data Sent by ESP8266:

temperature=23.60
humidity=57.00
parking_status_1=Available
parking_status_2=Occupied
parking_status_3=Available
parking_status_4=Available

Dashboard:
- Temperature: 23.6 °C
- Humidity: 57.0 %
- Parking Spot 1: Available
- Parking Spot 2: Occupied
- Parking Spot 3: Available
- Parking Spot 4: Available

Future Improvements
1. Add SMS or email alerts for parking updates.
2. Use MQTT for faster and more efficient data communication.
3. Integrate with a mobile app for enhanced user experience.

Acknowledgments
- Inspired by IoT-based parking systems.
- Built for educational purposes to demonstrate IoT, Node.js, and web development integration.
