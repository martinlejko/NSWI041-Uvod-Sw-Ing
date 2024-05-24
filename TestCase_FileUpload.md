

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
            <td>File Upload Access</td>
            <td>Test whether the user can access the file upload functionality.</td>
        </tr>
        <tr>
            <td>TC2</td>
            <td>Successful File Upload</td>
            <td>Test whether the user can successfully upload a valid file.</td>
        </tr>
        <tr>
            <td>TC3</td>
            <td>File Validation Error</td>
            <td>Test whether the system properly handles invalid files.</td>
        </tr>
        <tr>
            <td>TC4</td>
            <td>View Uploaded Files</td>
            <td>Test whether the user can view the list of uploaded files.</td>
        </tr>
        <tr>
            <td>TC5</td>
            <td>Maximum File Upload Limit</td>
            <td>Test whether the system enforces the maximum number of files that can be uploaded.</td>
        </tr>
        <tr>
            <td>TC6</td>
            <td>File Upload Security</td>
            <td>Test whether the system performs security checks on uploaded files.</td>
        </tr>
    </tbody>
</table>

# Test Cases

## Test Case 1 (Use Case = File Upload)

<table>
    <tr>
        <th>ID</th>
        <td colspan="2">T_CASE_01</td>
    </tr>
    <tr>
        <th>Title</th>
        <td colspan="2">Access File Upload Functionality</td>
    </tr>
    <tr>
        <th>Priority</th>
        <td colspan="2">High</td>
    </tr>
    <tr>
        <th>Preconditions</th>
        <td colspan="2">The user is logged into the system and has an existing application.</td>
    </tr>
    <tr>
        <th>Postconditions</th>
        <td colspan="2">The user can see the file upload options in the application details page.</td>
    </tr>
    <tr>
        <th>Role</th>
        <td colspan="2">User</td>
    </tr>
    <tr>
        <th>Test Data</th>
        <td colspan="2">User account details, existing application.</td>
    </tr>
    <tr>
        <th>Covered Test Conditions</th>
        <td colspan="2">TC1</td>
    </tr>
    <tr>
        <th>Test steps</th>
        <th>Action</th>
        <th>Expected result</th>
    </tr>
    <tr>
        <td>1.</td>
        <td>Log in to the system.</td>
        <td>User is logged in.</td>
    </tr>
    <tr>
        <td>2.</td>
        <td>Open the details of an existing application.</td>
        <td>Application details page is displayed.</td>
    </tr>
    <tr>
        <td>3.</td>
        <td>Identify and click the option to add files.</td>
        <td>File upload options are displayed.</td>
    </tr>
</table>

## Test Case 2 (Use Case = File Upload)

<table>
    <tr>
        <th>ID</th>
        <td colspan="2">T_CASE_02</td>
    </tr>
    <tr>
        <th>Title</th>
        <td colspan="2">Successful File Upload</td>
    </tr>
    <tr>
        <th>Priority</th>
        <td colspan="2">High</td>
    </tr>
    <tr>
        <th>Preconditions</th>
        <td colspan="2">The user is logged into the system and has an existing application.</td>
    </tr>
    <tr>
        <th>Postconditions</th>
        <td colspan="2">The file is successfully uploaded and listed under the application.</td>
    </tr>
    <tr>
        <th>Role</th>
        <td colspan="2">User</td>
    </tr>
    <tr>
        <th>Test Data</th>
        <td colspan="2">User account details, existing application, valid file for upload.</td>
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
        <td>Log in to the system.</td>
        <td>User is logged in.</td>
    </tr>
    <tr>
        <td>2.</td>
        <td>Open the details of an existing application.</td>
        <td>Application details page is displayed.</td>
    </tr>
    <tr>
        <td>3.</td>
        <td>Click the option to add files.</td>
        <td>File upload options are displayed.</td>
    </tr>
    <tr>
        <td>4.</td>
        <td>Select a valid file from the computer and click "Open".</td>
        <td>The file is uploaded successfully, and a confirmation message is displayed.</td>
    </tr>
</table>

## Test Case 3 (Use Case = File Upload)

<table>
    <tr>
        <th>ID</th>
        <td colspan="2">T_CASE_03</td>
    </tr>
    <tr>
        <th>Title</th>
        <td colspan="2">File Validation Error</td>
    </tr>
    <tr>
        <th>Priority</th>
        <td colspan="2">High</td>
    </tr>
    <tr>
        <th>Preconditions</th>
        <td colspan="2">The user is logged into the system and has an existing application.</td>
    </tr>
    <tr>
        <th>Postconditions</th>
        <td colspan="2">The user is informed about the invalid file, and the file is not uploaded.</td>
    </tr>
    <tr>
        <th>Role</th>
        <td colspan="2">User</td>
    </tr>
    <tr>
        <th>Test Data</th>
        <td colspan="2">User account details, existing application, invalid file for upload.</td>
    </tr>
    <tr>
        <th>Covered Test Conditions</th>
        <td colspan="2">TC3</td>
    </tr>
    <tr>
        <th>Test steps</th>
        <th>Action</th>
        <th>Expected result</th>
    </tr>
    <tr>
        <td>1.</td>
        <td>Log in to the system.</td>
        <td>User is logged in.</td>
    </tr>
    <tr>
        <td>2.</td>
        <td>Open the details of an existing application.</td>
        <td>Application details page is displayed.</td>
    </tr>
    <tr>
        <td>3.</td>
        <td>Click the option to add files.</td>
        <td>File upload options are displayed.</td>
    </tr>
    <tr>
        <td>4.</td>
        <td>Select an invalid file from the computer and click "Open".</td>
        <td>The system displays an error message indicating why the file is invalid.</td>
    </tr>
</table>

## Test Case 4 (Use Case = File Upload)

<table>
    <tr>
        <th>ID</th>
        <td colspan="2">T_CASE_04</td>
    </tr>
    <tr>
        <th>Title</th>
        <td colspan="2">View Uploaded Files</td>
    </tr>
    <tr>
        <th>Priority</th>
        <td colspan="2">Medium</td>
    </tr>
    <tr>
        <th>Preconditions</th>
        <td colspan="2">The user is logged into the system and has an existing application with uploaded files.</td>
    </tr>
    <tr>
        <th>Postconditions</th>
        <td colspan="2">The user can see the list of all uploaded files for the application.</td>
    </tr>
    <tr>
        <th>Role</th>
        <td colspan="2">User</td>
    </tr>
    <tr>
        <th>Test Data</th>
        <td colspan="2">User account details, existing application with uploaded files.</td>
    </tr>
    <tr>
        <th>Covered Test Conditions</th>
        <td colspan="2">TC4</td>
    </tr>
    <tr>
        <th>Test steps</th>
        <th>Action</th>
        <th>Expected result</th>
    </tr>
    <tr>
        <td>1.</





