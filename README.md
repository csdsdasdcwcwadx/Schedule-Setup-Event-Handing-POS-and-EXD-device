# Schedule Setup > Event Handling: POS and EXD Device  
work-portfolio (acti)  

## 1. Project Purpose  
### 1.1 **Configuring Event Trigger Time Range for POS and Extended Device**  
The primary goal of this project is to allow users to configure the event trigger time range for specific POS and Extended Device (EXD) systems. Events may include specific data formats triggered based on the current screen status on the monitoring side (e.g., motion, tamper detection, etc.). These configurations enable the system to automatically determine whether to respond to an event (e.g., pop-up notifications, sending emails, triggering beeping alerts, or pushing notifications to mobile devices) within the specified time range.  

- **Event**: The monitoring system sends specific data formats based on the current screen status (e.g., motion, tamper detection).  
- **POS and Extended Device**: Specific types of surveillance cameras.  

### 1.2 **Enhancing User Control**  
By allowing users to customize event trigger time ranges, this feature not only increases system flexibility but also enhances user control over device management. This functionality applies to various scenarios, such as automatically triggering alarms at night while only logging events without triggering alerts during working hours.  

## 2. Tasks  
### 2.1 **Frontend UI Development**  
A fully designed and implemented user interface ensures that users can intuitively configure and manage event trigger time ranges for POS and Extended Device systems. The frontend UI prioritizes a seamless user experience and supports multiple device data inputs and configurations.  

![image](https://github.com/user-attachments/assets/7153050d-9c19-44b0-ac22-2c9f293c4a98)  

### 2.2 **Event Trigger Configuration**  
Implemented specific event trigger logic, enabling the system to process camera data and execute corresponding actions based on user-defined rules. This involved leveraging ActiveX and API calls to ensure smooth data transmission between different system modules.  

![image](https://github.com/user-attachments/assets/658f5561-a006-43e9-af0d-dee481e6e5d4)  

## 3. Technologies Used  
### 3.1 **YUI.js Framework**  
Utilized the YUI.js framework to build and maintain the frontend UI. YUI.js offers a rich set of UI components and utilities, streamlining the development process.  

### 3.2 **Git Version Control**  
Employed Git for version control throughout the development process, ensuring that all modifications could be tracked and reverted. This was particularly beneficial for team collaboration, allowing clear documentation of contributions from each member.  

### 3.3 **ActiveX Data Integration**  
Implemented ActiveX technology to integrate data from hardware devices, ensuring real-time data reception from various devices and triggering corresponding events accordingly.  

### 3.4 **API Data Integration**  
Used RESTful APIs for communication with the backend, ensuring that the configuration data set by the frontend was correctly transmitted, stored, and processed.  

## 4. Challenges & Solutions  
### **Multi-Device Compatibility**  
POS and Extended Device systems come in various models with different configurations. The project needed to ensure system compatibility with multiple devices and correctly process different event formats. To address this, we designed a flexible data integration module that standardizes operations across different devices through an abstraction layer.  

## 5. System Architecture Diagram  
![image](https://github.com/user-attachments/assets/280daeb7-24f0-4a21-ae42-c2abce9006da)

