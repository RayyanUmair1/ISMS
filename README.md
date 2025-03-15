*Quick Start Guide*

This guide will help you quickly set up and run the IoT Security Monitoring System (ISMS) on your local machine.

1. Clone the Repository

Download the project source code from GitHub:

git clone (https://github.com/RayyanUmair1/ISMS.git)
cd ISMS

2. Create a Virtual Environment

Setting up a virtual environment ensures dependencies remain isolated:

python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

3. Install Dependencies

Install all required Python libraries using the provided requirements file:

pip install -r requirements.txt

4. Setup the Database

Initialize and migrate the database using Flask-Migrate:

flask db init
flask db migrate -m "Initial migration"
flask db upgrade

5. Run the Application

Start the Flask development server:

flask run

Your application will now be running at http://127.0.0.1:5000/.


*User Guide*

This guide explains how to use different features of the IoT Security Monitoring System (ISMS).

1. Logging In & Registering

Visit /register to create a new account.

Enter a unique username and password, then click Register.

After registration, you will be redirected to the login page.

Log in with your credentials to access the Dashboard.


2. Accessing the Dashboard

After login, you will be directed to /dashboard.

The dashboard provides real-time insights into connected IoT devices.


3. Viewing IoT Risk Assessment

Navigate to /risk_assessment to assess the security risks of IoT devices.

Each connected device will have:

Latency (ms)

Response Time (ms)

Data Integrity Status (Pass/Fail)

Success Rate (%)

Overall Risk Score (Low, Medium, High)


4. Monitoring Audit Logs

Visit /audit_logs to review security logs.

This feature logs:

User logins/logouts

Profile edits

Access history of secured pages

Helps track suspicious activity in the system.


5. Viewing Connected Devices

Go to /connected_devices to see all connected IoT devices.

Each device entry includes:

Device Name

Status (Active/Inactive)

Last Active Timestamp


6. Live Video Streaming

Access /video_feed to stream live security camera footage.

This feature helps monitor real-time activities.


7. Editing Profile

Navigate to /edit_profile to update your username and password.

Updating the profile will be logged in the Audit Log.


8. Logging Out

Click the Logout button or visit /logout.

You will be redirected to the homepage.

Configuration

Database: Default is SQLite (sqlite:///site.db). Switch to PostgreSQL/MySQL for production.

Security:

Change app.secret_key in app.py

Use environment variables for sensitive keys

AWS IoT Core:

Replace your-aws-iot-endpoint in app.py

Provide device certificates

*Feature*

Integrate AWS IoT Core for real device monitoring

Automated security alerts (Twilio SMS, Email Notifications)

AI-based anomaly detection for IoT risk assessment

License

MIT License – You are free to use and modify this project.

Contributors

Rayyan Umair - Project Lead & Developer
