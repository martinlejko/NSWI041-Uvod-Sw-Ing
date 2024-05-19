# Test Cases

## Test Conditions

<table>
    <thead>
        <tr>
            <th>ID</th>
            <th>Name</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>TC1</td>
            <td>Display Termin List</td>
            <td>Test whether the user can view the list of available terms.</td>
        </tr>
        <tr>
            <td>TC2</td>
            <td>User Registration to Termin</td>
            <td>Test whether the user can successfully register for an available term.</td>
        </tr>
        <tr>
            <td>TC3</td>
            <td>User Re-registration</td>
            <td>Test whether the system handles re-registration correctly.</td>
        </tr>
        <tr>
            <td>TC4</td>
            <td>Termin Modification Notification</td>
            <td>Test whether the user receives notification if a term is modified.</td>
        </tr>
        <tr>
            <td>TC5</td>
            <td>Prevent Last-Minute Change</td>
            <td>Test whether the system prevents changes within 24 hours of a term.</td>
        </tr>
    </tbody>
</table>

## Test Cases

### Test Case 1 (Use Case = Prihlaseni na Termin)

<table>
    <tr>
        <th>ID</th>
        <td colspan="2">T_CASE_01</td>
    </tr>
    <tr>
        <th>Title</th>
        <td colspan="2">User Registration for a Termín</td>
    </tr>
    <tr>
        <th>Priority</th>
        <td colspan="2">High</td>
    </tr>
    <tr>
        <th>Preconditions</th>
        <td colspan="2">The user has completed the application process and all documents are verified. At least one term has been created by the teacher.</td>
    </tr>
    <tr>
        <th>Postconditions</th>
        <td colspan="2">The user is registered for the selected term and receives a confirmation notification.</td>
    </tr>
    <tr>
        <th>Role</th>
        <td colspan="2">User</td>
    </tr>
    <tr>
        <th>Test Data</th>
        <td colspan="2">User account details, list of available terms.</td>
    </tr>
    <tr>
        <th>Covered Test Conditions</th>
        <td colspan="2">TC1, TC2</td>
    </tr>
    <tr>
        <th>Test steps</th>
        <th>Action</th>
        <th>Expected result</th>
    </tr>
    <tr>
        <td>1.</td>
        <td>Access the termín registration module on the website.</td>
        <td>The termín registration module is accessible.</td>
    </tr>
    <tr>
        <td>2.</td>
        <td>View the list of available terms.</td>
        <td>The list of available terms is displayed.</td>
    </tr>
    <tr>
        <td>3.</td>
        <td>Select a preferred term from the list.</td>
        <td>The term is highlighted as selected.</td>
    </tr>
    <tr>
        <td>4.</td>
        <td>Click the "přihlásit se na termín" button.</td>
        <td>The system registers the user for the selected term and displays a confirmation message.</td>
    </tr>
</table>

### Test Case 2 (Use Case = Prihlaseni na Termin)

<table>
    <tr>
        <th>ID</th>
        <td colspan="2">T_CASE_02</td>
    </tr>
    <tr>
        <th>Title</th>
        <td colspan="2">User Re-registration for a New Termin</td>
    </tr>
    <tr>
        <th>Priority</th>
        <td colspan="2">High</td>
    </tr>
    <tr>
        <th>Preconditions</th>
        <td colspan="2">The user has completed the application process and all documents are verified. The user is already registered for a term. At least one other term is available for registration.</td>
    </tr>
    <tr>
        <th>Postconditions</th>
        <td colspan="2">The user is unregistered from the previous term and registered for the new selected term. The user receives a confirmation notification. The system does not allow re-registration within 24 hours of the term.</td>
    </tr>
    <tr>
        <th>Role</th>
        <td colspan="2">User</td>
    </tr>
    <tr>
        <th>Test Data</th>
        <td colspan="2">User account details, list of available terms.</td>
    </tr>
    <tr>
        <th>Covered Test Conditions</th>
        <td colspan="2">TC1, TC3, TC5</td>
    </tr>
    <tr>
        <th>Test steps</th>
        <th>Action</th>
        <th>Expected result</th>
    </tr>
    <tr>
        <td>1.</td>
        <td>Access the termín registration module on the website.</td>
        <td>The termín registration module is accessible.</td>
    </tr>
    <tr>
        <td>2.</td>
        <td>View the list of available terms.</td>
        <td>The list of available terms is displayed.</td>
    </tr>
    <tr>
        <td>3.</td>
        <td>Select a new preferred term from the list.</td>
        <td>The new term is highlighted as selected.</td>
    </tr>
    <tr>
        <td>4.</td>
        <td>Click the "přihlásit se na termín" button for the new term.</td>
        <td>The system unregisters the user from the previous term and registers them for the new selected term, displaying a confirmation message.</td>
    </tr>
</table>
