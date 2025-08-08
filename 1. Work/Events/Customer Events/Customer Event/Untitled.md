# CloudBolt Converge 2025 - Airtable Survey Structure

## Form Introduction Text:

**CloudBolt Customer Event RSVP & Preferences Survey**

We're looking forward to hosting you for CloudBolt Converge 2025! Please take a few moments to complete this brief survey to help us plan for your arrival and ensure your experience is exceptional.

---

## Airtable Field Configuration:

### **Field 1: Attendee Status**

- **Field Type:** Single Select
- **Field Name:** `Attendee_Status`
- **Options:**
    - CloudBolt Staff
    - Customer
    - Prospective Customer
    - Partner

### **Field 2: Full Name**

- **Field Type:** Single Line Text
- **Field Name:** `Full_Name`
- **Required:** Yes

### **Field 3: Company Name**

- **Field Type:** Single Line Text
- **Field Name:** `Company_Name`
- **Required:** Yes

### **Field 4: Preferred Email**

- **Field Type:** Email
- **Field Name:** `Preferred_Email`
- **Required:** Yes

### **Field 5: Arrival Date**

- **Field Type:** Single Select
- **Field Name:** `Arrival_Date`
- **Options:**
    - Monday, September 15 (CloudBolt staff only)
    - Tuesday, September 16
    - Wednesday, September 17
    - Thursday, September 18

### **Field 6: Arrival Time**

- **Field Type:** Single Line Text
- **Field Name:** `Arrival_Time`
- **Description:** "Please specify your estimated arrival time (e.g., 2:00 PM)"

### **Field 7: Departure Date**

- **Field Type:** Single Select
- **Field Name:** `Departure_Date`
- **Options:**
    - Tuesday, September 16
    - Wednesday, September 17
    - Thursday, September 18
    - Friday, September 19
    - Saturday, September 20 (CloudBolt staff only)

### **Field 8: Departure Time**

- **Field Type:** Single Line Text
- **Field Name:** `Departure_Time`
- **Description:** "Please specify your estimated departure time (e.g., 6:00 PM)"

### **Field 9: Hotel Parking Pass**

- **Field Type:** Single Select
- **Field Name:** `Hotel_Parking_Pass`
- **Options:**
    - Yes
    - No

### **Field 10: Dietary Restrictions**

- **Field Type:** Long Text
- **Field Name:** `Dietary_Restrictions`
- **Description:** "Please list any dietary restrictions or preferences (e.g., vegetarian, gluten-free, food allergies)"

### **Field 11: Accessibility Needs**

- **Field Type:** Single Select
- **Field Name:** `Accessibility_Required`
- **Options:**
    - Yes
    - No

### **Field 12: Accessibility Details**

- **Field Type:** Long Text
- **Field Name:** `Accessibility_Details`
- **Description:** "Please describe any special accommodations needed"
- **Conditional:** Only show if Field 11 = "Yes"

### **Field 13: Porsche Driving Experience**

- **Field Type:** Single Select
- **Field Name:** `Porsche_Driving`
- **Options:**
    - Yes, I'd like to drive
    - No, I will not participate in the driving session
- **Description:** "Would you like to drive one of the Porsche vehicles during the driving experience (Wednesday, September 17, 12–2 PM)? Limited to 24 participants - first come, first served."

### **Field 14: Executive Meeting Request**

- **Field Type:** Single Select
- **Field Name:** `Executive_Meeting_Request`
- **Options:**
    - Yes
    - No

### **Field 15: Executive Meeting Details**

- **Field Type:** Single Line Text
- **Field Name:** `Executive_Meeting_With`
- **Description:** "Who would you like to meet with? (e.g., Account Manager, specific executive)"
- **Conditional:** Only show if Field 14 = "Yes"

### **Field 16: Additional Requests**

- **Field Type:** Long Text
- **Field Name:** `Additional_Requests`
- **Description:** "Do you have any additional requests, preferences, or questions?"

### **Field 17: Submission Date** (Auto-generated)

- **Field Type:** Created Time
- **Field Name:** `Submission_Date`

### **Field 18: Last Modified** (Auto-generated)

- **Field Type:** Last Modified Time
- **Field Name:** `Last_Modified`

---

## Form Settings:

### **Form Title:**

CloudBolt Converge 2025 - RSVP & Preferences

### **Form Description:**

Please refer to the [event agenda] for details on the program and conference schedule.

**Event Dates:**

- **Wednesday, September 17:** Porsche Experience Day (driving, cocktails, dinner)
- **Thursday, September 18:** Core Conference (8 AM - 3 PM)

### **Submit Button Text:**

"Submit RSVP"

### **Confirmation Message:**

"Thank you for your RSVP! We'll send confirmation details and any additional information to your preferred email address within 48 hours. Looking forward to seeing you in Atlanta!"

---

## Recommended Views for Internal Use:

### **View 1: All Responses**

- Show all fields
- Sort by submission date (newest first)

### **View 2: Porsche Drivers**

- Filter: Porsche_Driving = "Yes, I'd like to drive"
- Show: Full_Name, Company_Name, Attendee_Status, Submission_Date
- Sort by submission date (first come, first served)

### **View 3: Hotel Needs**

- Show: Full_Name, Company_Name, Arrival_Date, Departure_Date, Hotel_Parking_Pass
- Filter out "No" responses where possible

### **View 4: Special Requirements**

- Filter: Accessibility_Required = "Yes" OR Dietary_Restrictions is not empty
- Show: Full_Name, Dietary_Restrictions, Accessibility_Details

### **View 5: Executive Meetings**

- Filter: Executive_Meeting_Request = "Yes"
- Show: Full_Name, Company_Name, Executive_Meeting_With, Preferred_Email

---

## Form Logic Recommendations:

1. **Conditional Fields:** Set up Accessibility_Details to only appear when Accessibility_Required = "Yes"
2. **Conditional Fields:** Set up Executive_Meeting_With to only appear when Executive_Meeting_Request = "Yes"
3. **Validation:** Make Full_Name, Company_Name, and Preferred_Email required fields
4. **Date Logic:** Consider adding validation or help text about which dates are appropriate for different attendee types

---

## Next Steps:

1. Create the base in Airtable with these fields
2. Set up the form view
3. Configure conditional logic
4. Test the form internally
5. Share the form link with attendees
6. Set up automated email confirmations (if needed)
7. Create dashboard views for Elaine and the team to monitor responses