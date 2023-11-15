<!DOCTYPE html>
<html>
<head>
    <title>Fashion Line</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            display: flex;
            flex-direction: column;
            justify-content: top;
            align-items: center;
            height: 100vh;
        }
        h1 {
            text-align: center;
        }
        table {
            width: 80%; /* Adjust the width as needed */
            border-collapse: collapse;
        }
        th, td {
            padding: 15px;
            text-align: center;
        }
        .blue-button {
            padding: 10px 20px;
            background-color: blue;
            color: white;
            border: none;
            cursor: pointer;
        }
        /* Modal Styles */
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.5);
        }
        .modal-content {
            background-color: white;
            padding: 20px;
            border-radius: 5px;
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
        }
        /* Close Button Style */
        .close {
            color: #888;
            float: right;
            font-size: 28px;
            font-weight: bold;
            cursor: pointer;
        }
        .close:hover,
        .close:focus {
            color: black;
            text-decoration: none;
            cursor: pointer;
        }
/* Modal Styles... */
        .footer {
            background-color: pink;
            color: black;
            text-align: center;
            padding: 20px;
            position: absolute;
            bottom: 0;
            width: 100%;
        }
        .footer h2 {
            margin: 0;
            font-size: 24px;
        }
        .footer p {
            margin: 5px 0;
        }
        /* Close Button Style... */
    </style>
</head>
<body>
    <h1>Fashion Line</h1>
    <table>
        <tr>
            <td>Home</td>
            <td>Search</td>
            <td>Dresses</td>
            <td>Shoes</td>
            <td>Pants</td>
            <td>Shirts & Tops</td>
            <td><button class="blue-button">Cart</button></td>
            <td><button class="blue-button" onclick="openModal()">Account</button></td>
        </tr>
    </table>

    <!-- Modal -->
    <div id="myModal" class="modal">
        <div class="modal-content">
            <span class="close" onclick="closeModal()">&times;</span>
            <!-- Login Form -->
            <div id="login-form">
                <h2>Login</h2>
                <input type="text" placeholder="Email">
                <input type="password" placeholder="Password">
                <button class="blue-button">Sign In</button>
                <p>Don't have an account? <a href="#" id="create-account-link">Create one</a></p>
                <p>Forgot your password? <a href="#" id="forgot-password-link">Reset it</a></p>
            </div>
            
            <!-- Create Account Form -->
            <div id="create-account-form" style="display: none;">
                <h2>Create Account</h2>
                <input type="text" placeholder="Email">
                <input type="password" placeholder="Password">
                <button class="blue-button">Create Account</button>
            </div>
            
            <!-- Forgot Password Form -->
            <div id="forgot-password-form" style="display: none;">
                <h2>Reset Password</h2>
                <input type="text" placeholder="Email">
                <button class="blue-button">Reset Password</button>
            </div>
        </div>
    </div>

    <!-- Additional content can go here -->

    <script>
        // Function to open the sign-in modal
        function openModal() {
            var modal = document.getElementById("myModal");
            modal.style.display = "block";
        }

        // Function to close the modal
        function closeModal() {
            var modal = document.getElementById("myModal");
            modal.style.display = "none";
        }

        // Show the login form by default
        var loginForm = document.getElementById("login-form");
        var createAccountForm = document.getElementById("create-account-form");
        var forgotPasswordForm = document.getElementById("forgot-password-form");

        // Function to switch to create account form
        document.getElementById("create-account-link").addEventListener("click", function() {
            loginForm.style.display = "none";
            createAccountForm.style.display = "block";
            forgotPasswordForm.style.display = "none";
        });

        // Function to switch to forgot password form
        document.getElementById("forgot-password-link").addEventListener("click", function() {
            loginForm.style.display = "none";
            createAccountForm.style.display = "none";
            forgotPasswordForm.style.display = "block";
        });
    </script>
  <!-- Footer -->
    <div class="footer">
        <h2>GROUP MEMBERS</h2>
        <p><strong>JOHN NYANG'AU KINYOSI</strong> BSSC/407J/2019</p>
        <p><strong>JOHN ALUMA</strong> BSSC/404J/2019</p>
         <p><strong>EDDY DULO</strong> BSSC/409J/2019</p>
          <p><strong>LINDSEY OMOTO</strong> BSSC/286J/2018</p>
        <p><strong>CATHERINE MUTESHI</strong> BSSC/356J/2019</p>
    </div>

</body>
</html>
