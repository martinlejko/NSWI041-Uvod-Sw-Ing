# Test Cases

## Test Conditions: Use Case - Apply for Study

<table>
    <thead>
        <th>ID</th>
        <th>Name</th>
        <th>Description</th>
    </thead>
    <tr>
        <td>T_COND_01</td>
        <td>Sending of application</td>
        <td>Test whether the application gets sent correctly.</td>
    </tr>
    <tr>
        <td>T_COND_02</td>
        <td>Correct validation</td>
        <td>Test whether the application gets validated.</td>
    </tr>
    <tr>
        <td>T_COND_03</td>
        <td>Payment for registration processing</td>
        <td>Test whether application is processed only after the payment is assured.</td>
    </tr>
    <tr>
        <td>T_COND_04</td>
        <td>Application placement</td>
        <td>Test whether system correctly places the application into list of all applications.</td>
    </tr>
    <tr>
        <td>T_COND_05</td>
        <td>Application confirmation</td>
        <td>Test whether notification of correct application gets sent to student.</td>
    </tr>
</table>

## Test Cases

### Test Case 1

<table>
    <tr>
        <th>ID</th>
        <td colspan="2">T_CASE_01</td>
    </tr>
    <tr>
        <th>Title</th>
        <td colspan="2">Successful Application Submission</td>
    </tr>
    <tr>
        <th>Priority</th>
        <td colspan="2">High</td>
    </tr>
    <tr>
        <th>Preconditions</th>
        <td colspan="2">The user is logged into the system with a valid student or applicant account. The user is on the application submission page for UK.</td>
    </tr>
    <tr>
        <th>Postconditions</th>
        <td colspan="2">The application status is updated to "Submitted" in the user’s application dashboard and user is notified.</td>
    </tr>
    <tr>
        <th>Role</th>
        <td colspan="2">User</td>
    </tr>
    <tr>
        <th>Test Data</th>
        <td colspan="2">Valid application data including personal details, education history, and contact information.</td>
    </tr>
    <tr>
        <th>Covered Test Conditions</th>
        <td colspan="2">T_COND_01, T_COND_04, T_COND_05</td>
    </tr>
    <tr>
        <th>Test steps</th>
        <th>Action</th>
        <th>Expected result</th>
    </tr>
    <tr>
        <td>1.</td>
        <td>The user fills in all required fields in the application form (e.g., personal details, education history, contact information).</td>
        <td>All fields are filled out correctly with valid data.</td>
    </tr>
    <tr>
        <td>2.</td>
        <td>The user clicks the "Submit Application" button.</td>
        <td>The system accepts the submission and initiates validation.</td>
    </tr>
    <tr>
        <td>3.</td>
        <td>The system performs basic validation of the application.</td>
        <td>The system validates the data and finds no errors.</td>
    </tr>
    <tr>
        <td>4.</td>
        <td>The system displays a confirmation message indicating the application has been successfully submitted.</td>
        <td>The user sees a confirmation message indicating successful submission.</td>
    </tr>
    <tr>
        <td>5.</td>
        <td>The user checks the application status in the application overview.</td>
        <td>The application status is updated to "Submitted".</td>
    </tr>
</table>

### Test Case 2

<table>
    <tr>
        <th>ID</th>
        <td colspan="2">T_CASE_02</td>
    </tr>
    <tr>
        <th>Title</th>
        <td colspan="2">Basic Validation Error Handling</td>
    </tr>
    <tr>
        <th>Priority</th>
        <td colspan="2">High</td>
    </tr>
    <tr>
        <th>Preconditions</th>
        <td colspan="2">The user is logged into the system with a valid student or applicant account. The user is on the application submission page for UK.</td>
    </tr>
    <tr>
        <th>Postconditions</th>
        <td colspan="2">The application is not sent until all errors are resolved and re-validation is successful.</td>
    </tr>
    <tr>
        <th>Role</th>
        <td colspan="2">User</td>
    </tr>
    <tr>
        <th>Test Data</th>
        <td colspan="2">Application data with at least one invalid field (e.g., incorrect email format, missing address).</td>
    </tr>
    <tr>
        <th>Covered Test Conditions</th>
        <td colspan="2">T_COND_02, T_COND_05</td>
    </tr>
    <tr>
        <th>Test steps</th>
        <th>Action</th>
        <th>Expected result</th>
    </tr>
    <tr>
        <td>1.</td>
        <td>The user fills in the application with an error in at least one field (e.g., incorrect email format, missing address).</td>
        <td>The application contains invalid data in at least one field.</td>
    </tr>
    <tr>
        <td>2.</td>
        <td>The user clicks the "Submit Application" button.</td>
        <td>The system performs basic validation and detects errors.</td>
    </tr>
    <tr>
        <td>3.</td>
        <td>The system displays an error message specific to the validation error (e.g., "Invalid email format").</td>
        <td>The user sees an error message indicating the specific validation error.</td>
    </tr>
    <tr>
        <td>4.</td>
        <td>The user corrects the data with an error in the application.</td>
        <td>The user corrects the errors and updates the application data.</td>
    </tr>
    <tr>
        <td>5.</td>
        <td>The user clicks the "Submit Application" button again.</td>
        <td>The system re-validates the application and finds no errors.</td>
    </tr>
    <tr>
        <td>6.</td>
        <td>The system displays a confirmation message indicating the application has been successfully submitted.</td>
        <td>The user sees a confirmation message indicating successful submission.</td>
    </tr>
    <tr>
        <td>7.</td>
        <td>The user checks the application status in the application overview.</td>
        <td>The application status is updated to "Submitted".</td>
    </tr>
</table>