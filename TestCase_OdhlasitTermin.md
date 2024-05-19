Test Conditions
<table>
    <thead>
        <th>ID</th>
        <th>Name</th>
        <th>Description</th>
    </thead>
    <tr>
        <td>T_COND_01</td>
        <td>Login & Access</td>
        <td>Ensure the user can log in successfully. Ensure the user can access the exam scheduling dashboard.</td>
    </tr>
    <tr>
        <td>T_COND_02</td>
        <td>Display List of Terms</td>
        <td>Ensure the system displays a list of available exam terms for the user.</td>
    </tr>
    <tr>
        <td>T_COND_03</td>
        <td>Identify Registered Term</td>
        <td>Ensure the user can identify the term they are currently registered for.</td>
    </tr>
    <tr>
        <td>T_COND_04</td>
        <td>Unregister Button Display</td>
        <td>Ensure the "Unregister" button is displayed next to the term the user is registered for.</td>
    </tr>
    <tr>
        <td>T_COND_05</td>
        <td>Successful Unregistration</td>
        <td>Ensure the system successfully unregisters the user from the selected term upon clicking "Unregister".</td>
    </tr>
    <tr>
        <td>T_COND_06</td>
        <td>Prevent Unregistration within 24 Hours</td>
        <td>Ensure the system prevents unregistration if the term is within the next 24 hours.</td>
    </tr>
    <tr>
        <td>T_COND_07</td>
        <td>Confirmation of Unregistration</td>
        <td>Verify that the user receives a confirmation message after successfully unregistering from a term.</td>
    </tr>
    <tr>
        <td>T_COND_08</td>
        <td>No Remaining Registrations</td>
        <td>Ensure that after unregistration, the user is not registered for any other term.</td>
    </tr>
    <tr>
        <td>T_COND_09</td>
        <td>Error Message for 24-Hour Restriction</td>
        <td>Verify that the user receives an appropriate error message when attempting to unregister within 24 hours of the term.</td>
    </tr>
</table>

Test Case 1 (Use Case = Odhlášení z Termínu)
<table>
    <tr>
        <th>ID</th>
        <td colspan="2">T_CASE_01</td>
    </tr>
    <tr>
        <th>Title</th>
        <td colspan="2">User Unregistration from a Term</td>
    </tr>
    <tr>
        <th>Priority</th>
        <td colspan="2">High</td>
    </tr>
    <tr>
        <th>Preconditions</th>
        <td colspan="2">The user is already registered for a term.</td>
    </tr>
    <tr>
        <th>Postconditions</th>
        <td colspan="2">The user is unregistered from the selected term and receives a confirmation notification.</td>
    </tr>
    <tr>
        <th>Role</th>
        <td colspan="2">User</td>
    </tr>
    <tr>
        <th>Test Data</th>
        <td colspan="2">User account details, list of registered terms.</td>
    </tr>
    <tr>
        <th>Covered Test Conditions</th>
        <td colspan="2">T_COND_01, T_COND_02, T_COND_03, T_COND_04, T_COND_05</td>
    </tr>
    <tr>
        <th>Test steps</th>
        <th>Action</th>
        <th>Expected result</th>
    </tr>
    <tr>
        <td>1.</td>
        <td>Access the termín unregistration module on the website.</td>
        <td>The termín unregistration module is accessible.</td>
    </tr>
    <tr>
        <td>2.</td>
        <td>View the list of registered terms.</td>
        <td>The list of registered terms is displayed.</td>
    </tr>
    <tr>
        <td>3.</td>
        <td>Identify the term the user is registered for.</td>
        <td>The term is highlighted as the registered term.</td>
    </tr>
    <tr>
        <td>4.</td>
        <td>Click the "odhlásit se z termínu" button.</td>
        <td>The system unregisters the user from the selected term and displays a confirmation message.</td>
    </tr>
</table>
Test Case 2 (Use Case = Odhlášení z Termínu)
<table>
    <tr>
        <th>ID</th>
        <td colspan="2">T_CASE_02</td>
    </tr>
    <tr>
        <th>Title</th>
        <td colspan="2">Prevent Unregistration within 24 Hours</td>
    </tr>
    <tr>
        <th>Priority</th>
        <td colspan="2">High</td>
    </tr>
    <tr>
        <th>Preconditions</th>
        <td colspan="2">The user is already registered for a term. The term is scheduled within the next 24 hours.</td>
    </tr>
    <tr>
        <th>Postconditions</th>
        <td colspan="2">The user remains registered for the term and receives an error message.</td>
    </tr>
    <tr>
        <th>Role</th>
        <td colspan="2">User</td>
    </tr>
    <tr>
        <th>Test Data</th>
        <td colspan="2">User account details, list of registered terms.</td>
    </tr>
    <tr>
        <th>Covered Test Conditions</th>
        <td colspan="2">T_COND_06, T_COND_09</td>
    </tr>
    <tr>
        <th>Test steps</th>
        <th>Action</th>
        <th>Expected result</th>
    </tr>
    <tr>
        <td>1.</td>
        <td>Access the termín unregistration module on the website.</td>
        <td>The termín unregistration module is accessible.</td>
    </tr>
    <tr>
        <td>2.</td>
        <td>View the list of registered terms.</td>
        <td>The list of registered terms is displayed.</td>
    </tr>
    <tr>
        <td>3.</td>
        <td>Identify the term the user is registered for that is within the next 24 hours.</td>
        <td>The term is highlighted as the registered term within the next 24 hours.</td>
    </tr>
    <tr>
        <td>4.</td>
        <td>Click the "odhlásit se z termínu" button.</td>
        <td>The system prevents unregistration and displays an error message.</td>
    </tr>
</table>
Test Case 3 (Use Case = Odhlášení z Termínu)
<table>
    <tr>
        <th>ID</th>
        <td colspan="2">T_CASE_03</td>
    </tr>
    <tr>
        <th>Title</th>
        <td colspan="2">Confirmation of Unregistration</td>
    </tr>
    <tr>
        <th>Priority</th>
        <td colspan="2">Medium</td>
    </tr>
    <tr>
        <th>Preconditions</th>
        <td colspan="2">The user is already registered for a term.</td>
    </tr>
    <tr>
        <th>Postconditions</th>
        <td colspan="2">The user receives a confirmation message after successful unregistration.</td>
    </tr>
    <tr>
        <th>Role</th>
        <td colspan="2">User</td>
    </tr>
    <tr>
        <th>Test Data</th>
        <td colspan="2">User account details, list of registered terms.</td>
    </tr>
    <tr>
        <th>Covered Test Conditions</th>
        <td colspan="2">T_COND_07</td>
    </tr>
    <tr>
        <th>Test steps</th>
        <th>Action</th>
        <th>Expected result</th>
    </tr>
    <tr>
        <td>1.</td>
        <td>Access the termín unregistration module on the website.</td>
        <td>The termín unregistration module is accessible.</td>
    </tr>
    <tr>
        <td>2.</td>
        <td>View the list of registered terms.</td>
        <td>The list of registered terms is displayed.</td>
    </tr>
    <tr>
        <td>3.</td>
        <td>Identify the term the user is registered for.</td>
        <td>The term is highlighted as the registered term.</td>
    </tr>
    <tr>
        <td>4.</td>
        <td>Click the "odhlásit se z termínu" button.</td>
        <td>The system unregisters the user from the selected term and displays a confirmation message.</td>
    </tr>
    <tr>
        <td>5.</td>
        <td>Check for confirmation message.</td>
        <td>The user receives a confirmation message of unregistration.</td>
    </tr>
</table>







