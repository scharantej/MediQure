## Flask Application Design for Doctor Appointment Booking and Patient Data Storage System

### HTML Files

- **index.html:**
   - Main landing page of the application.
   - Contains a form to book doctor appointments.
   - Form includes fields for patient name, email, phone number, appointment date and time, and reason for visit.
- **patient_records.html:**
   - Table displaying a list of all registered patients and their details.
   - Includes fields for patient name, email, phone number, and medical history.

### Routes

- **@app.route('/'):**
   - Handles GET requests to the home page.
   - Renders the `index.html` file.
- **@app.route('/book_appointment', methods=['POST']):**
   - Handles POST requests to book a doctor's appointment.
   - Extracts patient data from the form in `index.html`.
   - Stores the appointment details in a database (not implemented in the design).
   - Redirects to the `index.html` file with a success message.
- **@app.route('/patient_records'):**
   - Handles GET requests to view patient records.
   - Queries the database to retrieve all patient records and displays them in `patient_records.html`.