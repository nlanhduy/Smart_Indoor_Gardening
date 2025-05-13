# 🌱 Smart Indoor Gardening (SIG)

Smart Indoor Gardening (SIG) is a modern web-based system designed to remotely monitor and manage a smart indoor vegetable growing environment. The solution leverages IoT sensors and actuators to automate plant care, while the web application—built with **Next.js** and **React**—provides a responsive and user-friendly interface for real-time interaction and control.

## 🔧 Key Features of the SIG Model

The SIG system integrates several smart functionalities to create an optimized indoor gardening environment:

- **Automatic Watering**: Uses a soil moisture sensor to monitor current humidity levels in the growing medium. When the moisture drops below a defined threshold, a drip irrigation system is automatically activated.
  
- **Smart Lighting Control**: LED lights simulate sunlight to support healthy plant growth without excessive heat. An ambient light sensor adjusts the brightness of LEDs to match plant needs.
  
- **Temperature & Humidity Monitoring**: A DHT11 sensor collects temperature and humidity data, which is used to control exhaust fans and maintain optimal growing conditions.
  
- **Insect Detection**: A PIR sensor detects pest activity. When movement is detected, an alarm is triggered and a notification is sent to the system's web interface.

---

## 🌐 Web Application Features

The SIG web application serves as the primary interface for users to interact with the smart gardening system. Built using **Next.js** and styled with **Tailwind CSS**, it offers a fully responsive design and a seamless user experience.

### 🔗 Live Demo

You can explore the user interface of the SIG web application here:  
🌐 **[smart-indoor-gardening.vercel.app/dashboard](https://smart-indoor-gardening.vercel.app/dashboard)**  
> ⚠️ *Note: This link showcases the UI only. Backend and real-time sensor integration are not connected in this demo.*

### 🎯 Why Next.js?

We chose **Next.js** over tools like Node-RED due to its flexibility in building rich, customized user interfaces. While Node-RED is great for backend data flow and automation, its UI capabilities are limited. Next.js, combined with React, allows for:
- Enhanced performance through server-side rendering (SSR) and static site generation (SSG).
- Greater flexibility in design and UX customization.
- Improved SEO and faster load times.

---

### 🖥 Main Navigation Structure

The SIG web application is divided into five main sections, accessible via the top navigation bar:

1. **Home**  
   Displays a general overview of the system, real-time sensor data, and control toggles for various devices (e.g., water pump, LEDs). It also includes plant care guides for supported vegetables.

2. **Activities**  
   Logs and displays details from the cloud database, including sensor values, sensor names, device status, and timestamps. Useful for tracking real-time system activity.

3. **History**  
   Provides historical sensor data visualization to help users track environmental trends and plant health over time.

4. **More**  
   A section reserved for additional features or settings.

5. **Profile**  
   Allows users to manage personal account details, configure settings, and control access permissions.

---

### 📱 Responsive Design

All pages are fully responsive and optimized for various devices including smartphones, tablets, and desktops—ensuring a smooth user experience regardless of screen size.

---

### 🧠 System Architecture

The architecture of the Smart Indoor Gardening (SIG) system includes several key components working together:

![System Architecture](https://drive.google.com/uc?export=view&id=1odG7L7_rnb_-WH8y7Q2nrmqbaQo_XjJY)

- **System Sensors**: Sensors like temperature, humidity, CO2, and light sensors collect data from the environment and send it to the SIGSystem.  
- **SIGSystem (ESP8266)**: This is the main device, powered by an ESP8266 microcontroller. It collects data from sensors and controls devices like lights, fans, or motors.  
- **System Control Devices**: Devices such as lights, fans, and motors can be controlled based on sensor data or user commands.  
- **HiveMQ MQTT Broker**: Acts as a cloud-based messenger between the SIGSystem and user interface.  
- **Client Subscribers (Next.js)**: A Next.js-based web application that allows users to view real-time data and control the system.  
- **Database (PostgreSQL on Vercel)**: Stores all collected data and actions for analysis or history tracking.

## 📚 References

- [Full Report](https://drive.google.com/file/d/1ZdfNGHjne9qBcpgBSTBlaoTpUB1MI4Vb/view?usp=drive_link)
- [Real-world product demo](https://drive.google.com/file/d/1oM_r9B_gYfrpbZVRP1-5SZ-uNCY7VjmP/view?usp=drive_link)
- [Arduino Code](https://drive.google.com/drive/folders/1APSP88CiW3NUnQyNjGQj7Z38jQ3X8G1E?usp=drive_link)
- [3D Model](https://drive.google.com/drive/folders/1AagWFfdQDSvrGTecyDEt6CWE1MtJ36Ua?usp=drive_link)


## 🚀 Getting Started

To run the project locally:

```bash
npm install
npm run dev
# or
yarn dev
