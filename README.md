### User Side:

#### Login
- **Method:** POST
- **Endpoint:** `{baseUrl}/api/users/login`
- **Body:**
    ```
    {
        "email": "",
        "password": ""
    }
    ```

#### Sign Up
- **Method:** POST
- **Endpoint:** `{baseUrl}/api/users/signup`
- **Body:**
    ```
    {
        "fullName": "",
        "email": "",
        "password": "",
        "confirmpassword": ""
    }
    ```

#### Create Invitation Link
- **Method:** GET
- **Endpoint:** `{baseUrl}/api/users/create-invitation-link/{id}`

#### Sign Up for Invitation
- **Method:** POST
- **Endpoint:** `{baseUrl}/api/users/invitation-signup/{FullName}/{id}`
- **Body:**
    ```
    {
        "fullName": "",
        "email": "",
        "password": "",
        "confirmpassword": ""
    }
    ```

#### Update Password
- **Method:** POST
- **Endpoint:** `{baseUrl}/api/users/update-password`
- **Body:**
    ```
    {
        "userId": "",
        "oldPassword": "",
        "newPassword": ""
    }
    ```

#### Reset Password (Send OTP)
- **Method:** POST
- **Endpoint:** `{baseUrl}/api/users/reset-password`
- **Body:**
    ```
    {
        "gmail": ""
    }
    ```

#### OTP Check
- **Method:** POST
- **Endpoint:** `{baseUrl}/api/users/otp-check-user`
- **Body:**
    ```
    {
        "OTP": "5870",
        "gmail": "qasim@gmail.com"
    }
    ```

#### Reset Password
- **Method:** POST
- **Endpoint:** `{baseUrl}/api/users/after-otp-updatePassword/{id}`
- **Body:**
    ```
    {
        "newPassword": "1234"
    }
    ```

#### Get Referral
- **Method:** GET
- **Endpoint:** `{baseUrl}/api/users/referral-get-by-user/{id}`

#### Investment
- **Method:** POST
- **Endpoint:** `{baseUrl}/api/users/investment`
- **Body:**
    ```
    {
        "userId": "",
        "amount": "",
        "investmentTypeId": ""
    }
    ```

#### Get All Investment
- **Method:** GET
- **Endpoint:** `{baseUrl}/api/users/get-user-investment/{id}/{past/current}`

#### Edit User Detail
- **Method:** PUT
- **Endpoint:** `{baseUrl}/api/users/user-edit-details/{id}`
- **Body:**
    ```
    {
        "fullName": ""
    }
    ```

#### Upload User Profile
- **Method:** POST
- **Endpoint:** `/api/users/upload-profile-picture/{id}`
- **Body:**
    ```
    {
        "imagebase64": ""
    }
    ```

#### Update Profile Picture
- **Method:** POST
- **Endpoint:** `{baseUrl}/api/users/update-profile-pic`
- **Body:**
    ```
    {
        "profileImageBase64": ""
    }
    ```

#### Delete Profile Picture
- **Method:** DELETE
- **Endpoint:** `/api/users/delete-profile-picture/{id}`

#### Get User Withdrawal
- **Method:** GET
- **Endpoint:** `/api/users/get-user-all-withdraw/{id}/{pageNumber}?status={pending/approved/declined}`

#### User Withdrawal Request
- **Method:** POST
- **Endpoint:** `/api/users/user-withdraw/{id}?cancellation=false`

#### User Withdrawal Cancel Request
- **Method:** POST
- **Endpoint:** `/api/users/user-withdraw/{id}?cancellation=true&withDrawId={id}`

#### Get User Investment
- **Method:** GET
- **Endpoint:** `/api/users/get-user-investment/:id/:pageNumber/:tradeOption/:tradeId?`

#### Get User Withdrawal
- **Method:** GET
- **Endpoint:** `/api/users/user-withdraw/:id`

### Admin Side:

#### Admin Login
- **Method:** POST
- **Endpoint:** `/api/admin/login`
- **Body:**
    ```
    {
        "email": "",
        "password": ""
    }
    ```

#### Admin Sign Up
- **Method:** POST
- **Endpoint:** `/api/admin/signup`
- **Body:**
    ```
    {
        "email": "",
        "password": ""
    }
    ```

#### Admin Update Password
- **Method:** POST
- **Endpoint:** `/api/admin/update-password`
- **Body:**
    ```
    {
        "adminId": "",
        "oldPassword": "",
        "newPassword": ""
    }
    ```

#### User Delete by Admin
- **Method:** DELETE
- **Endpoint:** `/api/admin/user-delete/{id}`

#### Get All Users
- **Method:** GET
- **Endpoint:** `/api/admin/get-allusers/:pageNumber/:search?`

#### User Inactive
- **Method:** GET
- **Endpoint:** `/api/admin/user-inactive/:id`

#### User Active
- **Method:** GET
- **Endpoint:** `/api/admin/user-active/:id`

#### Get Specific User Details
- **Method:** GET
- **Endpoint:** `/api/admin/get-user/:id`

#### Get All User Investments
- **Method:** GET
- **Endpoint:** `/api/admin/all-investmnet/:pageNumber`

#### Get Current Users in Trade
- **Method:** GET
- **Endpoint:** `/api/admin/current-users-in-trade/:tradeName`

#### Get Past Users in Trade
- **Method:** GET
- **Endpoint:** `/api/admin/past-users-in-trade/:tradeName`

#### Get All Trade Options
- **Method:** GET
- **Endpoint:** `/api/admin/get-all-trade-options`

#### Profit Release to User
- **Method:** POST
- **Endpoint:** `/api/admin/profit-released-to-user`
- **Body:**
    ```
    {
        "userId": "",
        "profitPercentage": "",
        "investmentTypeId": "",
        "date": "",
        "amount": ""
    }
    ```

#### Get All Withdrawals
- **Method:** GET
- **Endpoint:** `/api/admin/get-all-withdraw/:pageNumber`

#### Update Withdrawal Status
- **Method:** GET
- **Endpoint:** `/api/admin/update-withdraw-status/:id?status={declined/approved}`
