# HackThe6ix 2024 - Winner For Best Use Of MongoDB

# **DriveInsight**

DriveInsight is a cutting-edge system designed to enhance road safety by utilizing **AI**, **Computer Vision**, and **gyroscope data**. It offers meaningful insights and feedback on driving behavior, promoting better driving habits and safer roads.

## **Inspiration**

Road safety has become an escalating concern in recent years. According to Transport Canada, the number of collisions and casualties has been rising in the past three years. As **AI technology** grows exponentially, we identified a niche to leverage powerful AI to offer valuable advice and feedback to drivers of all levels, effectively promoting road safety.

## **What It Does**

DriveInsight collects and analyzes meaningful driving performance data using:

- **Computer Vision (CV):** Tracks behaviors such as shoulder checks and signs of drowsy driving.
- **Gyroscopes:** Measures driving dynamics and movements.

The collected data is analyzed by a **Large Language Model (LLM)** backend, which provides valuable insights and personalized advice to users. Potential use cases include:

- Supplementing driving lessons or exams for learners.
- Encouraging safe driving habits for concerned drivers.
- Providing objective evaluations for professional driving services.

## **Features**

- **Data Collection**: Uses CV algorithms and gyroscopes to monitor driving performance.
- **Real-Time Feedback**: Displays driving performance data in real time.
- **LLM Insights**: Analyzes driving behavior and offers personalized advice.
- **User Authentication**: Secure logins powered by **Auth0**.
- **Cloud Integration**: Stores driving videos and metadata securely in **Google Cloud Storage** and **MongoDB Atlas**.

## **How We Built It**

### **System Architecture**

1. **Data Collection Script**
   - **Language**: Python, React Native
   - **Functionality**:
     - Runs a CV algorithm using **Roboflow models**.
     - Streams video and gyroscope data to the frontend web app.

2. **Frontend Web App**
   - **Framework**: React
   - **Features**:
     - Displays driving performance data.
     - Allows users to review driving records and interact with the LLM.
     - Authenticates users using **Auth0**.

3. **Backend**
   - **Framework**: Flask
   - **Functionality**:
     - Connects to **Google Gemini** for LLM interactions.
     - Transfers data and LLM outputs between the frontend and database.
     - Uses **VectorSearch** to extract relevant driving records.

4. **Database**
   - **Service**: MongoDB Atlas
   - **Features**:
     - Stores metadata and analysis of each driving trip.
     - Configured for **VectorSearch**.

5. **Cloud Storage**
   - **Service**: Google Cloud Storage
   - **Purpose**: Hosts driving videos (large-sized media data).

## **Challenges We Faced**

- Setting up **WebSockets** for real-time data transfer between components.
- Configuring **Auth0** to integrate correctly within the React app.
- Deciding between storing videos as **BLOBs** in the database or using a cloud storage service.

## **Accomplishments**

- Successfully built components that perform key functionalities, including:
  - Identifying shoulder checks and signs of drowsy driving.
  - Interacting with the LLM to generate advice.
  - Querying the database using vectors.
- Overcame technical errors arising from using libraries and SDKs.

## **Technologies Used**

### **Frontend**
- **Framework**: React
- **Styling**: CSS
- **Authentication**: Auth0

### **Backend**
- **Framework**: Flask
- **LLM Integration**: Google Gemini
- **Real-Time Communication**: WebSockets, Socket.io

### **Database**
- **Service**: MongoDB Atlas
- **Search Technology**: VectorSearch

### **Cloud Storage**
- **Service**: Google Cloud Storage

### **Other**
- **Computer Vision Models**: Roboflow
- **Data Streaming**: Gyroscope and video processing

## **Future Enhancements**

- Improve LLM interactions for more contextual and actionable advice.
- Optimize real-time streaming of video and gyroscope data.
- Expand use cases to include advanced driver training programs.
- Develop a mobile application for easier data collection and interaction.

## **Contact**

If you have any questions or suggestions, feel free to reach out:

- **Email**: williamntlam@gmail.com
