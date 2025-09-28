# Ex03 Time Table
# Date:28/09/2025
# AIM
To write a html webpage page to display your slot timetable.

# ALGORITHM
## STEP 1
Create a Django-admin Interface.

## STEP 2
Create a static folder and inert HTML code.

## STEP 3
Create a simple table using `<table>` tag in html.

## STEP 4
Add header row using `<th>` tag.

## STEP 5
Add your timetable using `<td>` tag.

## STEP 6
Execute the program using runserver command.

# PROGRAM
'''<!doctype html>
<html lang="en">
<head>
  <style>
    body {
      margin:0;
      padding:0;
      font-family: "Segoe UI", Roboto, Arial, sans-serif;
      background:#f0f4f6;
      color:#222;
    }
    .banner {
      text-align:center;
      background:#000;
    }
    .banner img {
      max-width:100%;
      height:auto;
      display:block;
      margin:0 auto;
    }
    .container {
      max-width:980px;
      margin:20px auto;
      padding:0 15px;
    }
    /* keep the rest of the timetable styles you already had */
  </style>
</head>
<body>
  <!-- Banner Section -->
  <div class="banner">
    <img src="logo.png.jpeg" alt="Saveetha Engineering College Banner">
  </div>
  <!-- Content Section -->
  <div class="container">
    <h2 style="text-align:center;">SLOT TIME TABLE - THANZIL HUSSAIN A (25018773)
    <!-- Insert the timetable + subject legend tables here from previous code -->
  </div>
</body>
</html>
<!doctype html>
<html lang="en">
<head>
  <style>     
    :root{
      --yellow:#0db407;
      --teal:#fc9905; /* bright cyan/teal used for cells */
      --teal-dark:#f59300;
      --border:#444;
      --heading-bg:#f5f5f5;
      --card-bg:#ffffff;
      --muted:#666;
      font-family: "Segoe UI", Roboto, Arial, sans-serif;
    }

    body{
      margin:0;
      padding:24px;
      background:#f0f4f6;
      color:#222;
    }

    header{
      display:flex;
      align-items:center;
      gap:18px;
      margin-bottom:14px;
    }
    header .logo{
      width:92px;
      height:92px;
      background:linear-gradient(180deg,#0b84a5,#068a9c);
      border-radius:8px;
      display:flex;
      align-items:center;
      justify-content:center;
      color:#fff;
      font-weight:700;
      font-size:14px;
    }
    header h1{
      margin:0;
      font-size:20px;
      letter-spacing:0.6px;
    }
    header p { margin:0; color:var(--muted); font-size:13px; }

    .card{
      background:var(--card-bg);
      padding:14px;
      border-radius:6px;
      box-shadow:0 4px 14px rgba(0,0,0,0.06);
      border:3px solid #bfcfcf;
    }

    .timetable-title{
      text-align:center;
      font-weight:700;
      margin:6px 0 12px;
    }

    table.slot-table{
      width:100%;
      border-collapse:collapse;
      table-layout:fixed;
      font-size:15px;
    }

    table.slot-table th,
    table.slot-table td {
      border:4px solid var(--border);
      padding:10px 6px;
      text-align:center;
    }

    table.slot-table thead th {
      background:var(--yellow);
      font-weight:700;
    }

    table.slot-table tbody td {
      background:var(--teal);
      color:#003a3a;
      font-weight:700;
    }

    /* LUNCH row style */
    .lunch {
      background:transparent;
      text-align:center;
      font-weight:800;
      color:#0b4a4a;
      font-size:18px;
    }

    /* Subject code list table */
    .legend{
      margin-top:18px;
      width:100%;
      border-collapse:collapse;
      font-size:14px;
    }
    .legend th, .legend td {
      border:1px solid #999;
      padding:8px 10px;
      text-align:left;
      background:#fff;
    }
    .legend th{ background:var(--heading-bg); font-weight:700; }

    /* small screens */
    @media (max-width:700px){
      header{flex-direction:column;align-items:flex-start}
      table.slot-table th, table.slot-table td { padding:8px 4px; font-size:13px; }
    }
  </style>
</head>
<body>
      <table class="slot-table" aria-describedby="timetable-desc">
        <caption id="timetable-desc" style="text-align:left; caption-side:bottom; font-size:13px; color:var(--muted); padding-top:8px;">
        </caption>

        <thead>
          <tr>
            <th>Day/Time</th>
            <th>Monday</th>
            <th>Tuesday</th>
            <th>Wednesday</th>
            <th>Thursday</th>
            <th>Friday</th>
            <th>Saturday</th>
          </tr>
        </thead>

        <tbody>
          <tr>
            <td style="background:var(--yellow); font-weight:700;">8-10</td>
            <td>FWAD</td>
            <td>FREE SLOT</td>
            <td>FREE SLOT</td>
            <td>FREE SLOT</td>
            <td>FREE SLOT</td>
            <td>DS</td>
          </tr>

          <tr>
            <td style="background:var(--yellow); font-weight:700;">10-12</td>
            <td>PYTHON</td>
            <td>DS</td>
            <td>FWAD</td>
            <td>FREE SLOT</td>
            <td>FWAD</td>
            <td>FWAD</td>
          </tr>

          <tr>
            <td style="background:var(--yellow); font-weight:700;">12-1</td>
            <td class="lunch" colspan="6">L U N C H</td>
          </tr>

          <tr>
            <td style="background:var(--yellow); font-weight:700;">1-3</td>
            <td>PYTHON</td>
            <td>PYTHON</td>
            <td>FREE SLOT</td>
            <td>PYTHON</td>
            <td>DS</td>
            <td>FREE SLOT</td>
          </tr>

          <tr>
            <td style="background:var(--yellow); font-weight:700;">3-5</td>
            <td>FREE SLOT</td>
            <td>DS</td>
            <td>FREE SLOT</td>
            <td>PYTHON</td>
            <td>FREE SLOT</td>
            <td>DS</td>
          </tr>
        </tbody>
      </table>

      <!-- Subject legend -->
      <table class="legend" aria-label="Subject legend">
        <thead>
          <tr>
            <th style="width:6%;">S. No.</th>
            <th style="width:22%;">Subject Code</th>
            <th>Subject Name</th>
          </tr>
        </thead>
        <tbody>
          <tr><td>1.</td><td>19AI414</td><td>Fundamentals of Web Application Development (FWAD)</td></tr>
          <tr><td>2.</td><td>19AI301</td><td>PYTHON</td></tr>
          <tr><td>3.</td><td>19AI403</td><td>INTRODUCTION TO DATA SCIENCE</td></tr>
        </tbody>
      </table>

    </div>
  </div>
</body>
</html>
'''
# OUTPUT

<img>![{274951C3-F870-49BC-9ADB-800650FC41FB} png](https://github.com/user-attachments/assets/2e82bc28-b818-42b1-ad52-497f84cd855c)



# RESULT
The program for creating slot timetable using basic HTML tags is executed successfully.
