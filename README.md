<!DOCTYPE html>
<html>
<head>
  <title>BMI Calculator</title>
  <script type="text/javascript">
    function calculateBMI() {
      var weight = parseFloat(document.getElementById('weight').value);
      var height = parseFloat(document.getElementById('height').value);
      var result = document.getElementById('result');

      if (isNaN(weight) || isNaN(height) || weight <= 0 || height <= 0) {
        result.textContent = 'Please enter valid values for weight and height.';
        return;
      }

      var bmi = weight / (height * height);
      bmi = bmi.toFixed(2); // Round to 2 decimal places
      result.textContent = 'Your BMI is ' + bmi;
    }
  </script>
</head>
<body>
  <h1>BMI Calculator</h1>
  <label for="weight">Weight (kg):</label>
  <input type="text" id="weight">
  <br>
  <label for="height">Height (m):</label>
  <input type="text" id="height">
  <br>
  <button onclick="calculateBMI()">Calculate</button>
  <p id="result"></p>
</body>
</html>
