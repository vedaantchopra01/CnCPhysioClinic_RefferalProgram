<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CnC Physiotherapy Clinic Referral Program</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
            background-color: #f4f4f9;
            color: #333;
            text-align: center;
        }
        header {
            background-color: #4CAF50;
            color: white;
            padding: 20px 0;
            font-size: 1.5em;
        }
        header p {
            font-size: 1em;
            margin: 5px 0;
        }
        .container {
            max-width: 600px;
            margin: 20px auto;
            background: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        form {
            margin-top: 20px;
        }
        input, select, button {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        button {
            background-color: #4CAF50;
            color: white;
            border: none;
            cursor: pointer;
        }
        button:hover {
            background-color: #45a049;
        }
        .note {
            text-align: left;
            margin-bottom: 20px;
            font-size: 1em;
            color: #555;
        }
        .referral-code {
            margin-top: 20px;
            font-size: 1.2em;
            font-weight: bold;
            color: #4CAF50;
        }
    </style>
</head>
<body>
    <header>
        <h1>CnC Physiotherapy Clinic</h1>
        <p>"We Treat but He Cures"</p>
        <p>Landline: 0120-3137252</p>
        <p>Sector 122: D-127, Sector 122, Noida</p>
        <p>Sector 17: BHEL Dispensary, Sector 17, Noida</p>
    </header>

    <div class="container">
        <h2>Referral Program</h2>
        <p class="note">
            Refer your friend and get <strong>2 Dry Cupping Sessions</strong> or 
            <strong>1 Physiotherapy Session</strong> for free!<br>
            Your friend will get <strong>₹1000 off</strong> on our services.<br>
            Just fill out the form below and share the referral code with your family and friends via WhatsApp!
        </p>

        <form id="referralForm">
            <label for="name">Your Name:</label>
            <input type="text" id="name" name="name" placeholder="Enter your name" required>

            <label for="phone">Phone Number:</label>
            <input type="tel" id="phone" name="phone" placeholder="Enter your phone number" required>

            <label for="branch">Which CnC Physiotherapy branch did you visit?</label>
            <select id="branch" name="branch" required>
                <option value="" disabled selected>Select your branch</option>
                <option value="Sector 122">D-127, Sector 122, Noida</option>
                <option value="Sector 17">BHEL Dispensary, Sector 17, Noida</option>
            </select>

            <button type="submit">Generate Referral Code</button>
        </form>

        <div class="referral-code" id="referralCode"></div>
    </div>

    <script>
        document.getElementById("referralForm").addEventListener("submit", function(event) {
            event.preventDefault();

            // Get form values
            const name = document.getElementById("name").value.trim();
            const branch = document.getElementById("branch").value;

            // Generate referral code
            const referralCode = `CnC_122_Referral_${name.replace(/\s+/g, '_')}`;

            // Display referral code
            const referralCodeDiv = document.getElementById("referralCode");
            referralCodeDiv.innerHTML = `
                Your Referral Code:<br>
                <span>${referralCode}</span><br>
                Share this code with your family and friends!
            `;
        });
    </script>
</body>
</html>