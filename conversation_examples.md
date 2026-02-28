# Conversation Examples

## New Patient – Appointment Booking

AI: Hello, thank you for calling the dental clinic. How may I assist you today?
Patient: I'd like to book a cleaning appointment.
AI: Are you a new or returning patient?
Patient: New.
AI: May I have your full name?
Patient: Sarah Williams.
AI: Please provide your phone number.
Patient: 9876543210
AI: What date works best for you?
Patient: March 15th.
AI: What time do you prefer?
Patient: Around 11 AM.
AI: Let me check availability. That slot is available. You are booking a dental cleaning on March 15th at 11:00 AM. Shall I confirm?
Patient: Yes.
AI: Your appointment is confirmed.

Structured Output:

{
  "intent": "book_appointment",
  "patient_status": "new",
  "patient_name": "Sarah Williams",
  "phone_number": "9876543210",
  "appointment_id": "",
  "appointment_date": "2025-03-15",
  "appointment_time": "11:00 AM",
  "procedure_type": "Dental Cleaning",
  "insurance_provider": "",
  "status": "confirmed",
  "escalation": false,
  "notes": ""
}


## Emergency Escalation

Patient: I'm bleeding heavily after a tooth extraction.
AI: This appears to be an emergency. I am transferring you to a clinic staff member immediately. Please stay on the line.

Structured Output:

{
  "intent": "emergency_request",
  "patient_status": "",
  "patient_name": "",
  "phone_number": "",
  "appointment_id": "",
  "appointment_date": "",
  "appointment_time": "",
  "procedure_type": "",
  "insurance_provider": "",
  "status": "escalated",
  "escalation": true,
  "notes": "Emergency call transferred"
}
