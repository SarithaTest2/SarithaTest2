
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Customer Churn Prediction</title>

<h1 style="display: flex; align-items: center;">
        <img src="https://github.com/SarithaTest2/SarithaTest2/blob/main/Ranger%20Predict.png
)" alt="Ranger Predict" title="Ranger Predict" 
style="width: 50px; height: 50px; margin-right: 50px;"> 
<span style="color: red; margin-left: -30px;">Ranger Predict</span>
    </h1>

    <script>
        function fetchCustomerRecord() {
            // Predefined customer records
            const customerData = {
                "001": { Name: "Alice Johnson", Email: "alice@abc.com", Phone: "072-123-4567" },
                "002": { Name: "Bob Smith", Email: "bob@abc.com", Phone: "081-234-5555" },
                "003": { Name: "Charlie Brown", Email: "charlie@abc.com", Phone: "061-234-5678" }
            };

            // Get the entered Customer ID
            const customerID = document.getElementById("customerID").value;

            // Find the record and display it
            const resultDiv = document.getElementById("result");
            if (customerData[customerID]) {
                const record = customerData[customerID];
                resultDiv.innerHTML = `
                    <h3 style="color: lightcoral;text-decoration: underline">Customer Details:</h3>
                    <p><strong>Name:</strong> ${record.Name}</p>
                    <p><strong>Email:</strong> ${record.Email}</p>
                    <p><strong>Phone:</strong> ${record.Phone}</p>
                `;
            } else {
                resultDiv.innerHTML = "<p>No record found for the entered Customer ID.</p>";
            }
        }
    </script>
<style>
        body {
            background-color: black; /* Optional: Set background to black for contrast */
            color: white; /* Sets all text color to white */
        }
    </style>
</head>
<body>
    
<h1>
  Insights into Customer Churn Prediction
</h1>
    <p style="color: lightgreen;">Enter the Customer ID to access the predicted customer details:</p>
    <form onsubmit="event.preventDefault(); fetchCustomerRecord();">
        <label for="customerID">Customer ID:</label>
        <input type="text" id="customerID" required>
<br> <br>
        <button type="submit">
		<strong>Submit</strong>
	</button>
    </form>
    <div id="result" style="margin-top: 20px;"></div>
</body>
</html>
