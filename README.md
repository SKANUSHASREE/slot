# Ex03 Time Table
## Date: 13-05-2025

## AIM
To write a html webpage page to display your slot timetable.

## ALGORITHM
### STEP 1
Create a Django-admin Interface.

### STEP 2
Create a static folder and inert HTML code.

### STEP 3
Create a simple table using ```<table>``` tag in html.

### STEP 4
Add header row using ```<th>``` tag.

### STEP 5
Add your timetable using ```<td>``` tag.

### STEP 6
Execute the program using runserver command.

## PROGRAM
```
<html>
<head>
    <title>TIMETABLE</title>
    <style>
      :root {
        --primary-color: #6a1b9a;       
        --secondary-color: #f3e5f5;    
        --text-color: #2e2e2e;         
        --bg-color: #fff6f6;           
        --border-color: #3f1c1c;        
        --header-bg: #8e24aa;          
        --header-text: white;          
        --highlight-bg: #683174;              
        --highlight-text: white;
     }
     body {
       font-family: 'Poppins', sans-serif;
       background: var(--bg-color);         
       color: var(--text-color);          
       padding: 30px;
     }

     .container {
       max-width: 1000px;
       margin: auto;
       background: var(--secondary-color); 
       padding: 40px;
       border-radius: 10px;
       box-shadow: 0 6px 20px rgba(211, 47, 47, 0.15); 
       border: 2px solid var(--border-color);         
      }
      .header {
            text-align: center;
            margin-bottom: 10px;
        }

        .header img {
            max-width: 500px;
            height: auto;
            display: block;
            margin: 0 auto;
        }

        h1 {
            font-size: 35px;
            margin-top: 10px;
            color: var(--primary-color); 
            letter-spacing: 1px;
            font-weight: 600;
            text-transform: uppercase;
        }
        .info {
          text-align: center;
          font-size: 22px;              
          margin-bottom: 20px;          
          font-weight: 600;              
          padding: 10px;                 
          background-color: var(--secondary-color);  
        }
        table {
          width: 100%;
          border-collapse: collapse;
          margin-bottom: 30px;
          border-radius: 10px;         
        }

        th,td {
          border: 2px solid var(--border-color);
          padding: 15px;                
          text-align: center;
          font-size: 16px;   
        } 
        
        th {
          background-color: var(--header-bg);  
          color: var(--header-text);          
          font-weight: 600;                   
        }

        td {
          background-color: #fff;           
          color: var(--text-color);           
         }

         td.day {
           background-color: var(--highlight-bg);  
           color: var(--highlight-text);           
           font-weight: bold;
         }

         td.lunch {
           background-color: var(--secondary-color); 
           color: var(--text-color);               
           font-weight: bold;
         }

         tr:nth-child(even) {
           background-color: var(--secondary-color); 
         }
          .subject-title {
            font-size: 26px;
            text-align: center;
            font-weight: 600;
            margin-bottom: 15px;
            color: var(--primary-color); /* Matching primary color for titles */
        }

        .subject-table th {
            background-color: var(--header-bg); /* Dark purple header for subject table */
            color: var(--header-text);           /* White text */
        }

        footer {
            text-align: center;
            margin-top: 20px;
            color: var(--primary-color);  /* Primary color for footer text */
        }
    </style>
</head>
<body>

<div class="container">
    <div class="header">
        <img src="/static/logo.png" alt="Saveetha Logo">
        <h1>TIMETABLE</h1>
    </div>

    <div class="info">
        <strong>NAME:</strong> S KANUSHA SREE &nbsp; | &nbsp;
        <strong>REG NO:</strong> 212224040149
    </div>

    <table>
        <thead>
            <tr>
                <th>DAY</th>
                <th>8:00 - 10:00</th>
                <th>10:00 - 12:00</th>
                <th>12:00 - 13:00</th>
                <th>13:00 - 15:00</th>
                <th>15:00 - 17:00</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td class="day">MONDAY</td>
                <td></td>
                <td>EDM</td>
                <td class="lunch">LUNCH</td>
                <td>Human Values</td>
                <td></td>
            </tr>
            <tr>
                <td class="day">TUESDAY</td>
                <td>Advanced C Programming</td>
                <td>Physics</td>
                <td class="lunch">LUNCH</td>
                <td>EDM</td>
                <td>Web App Development</td>
            </tr>
            <tr>
                <td class="day">WEDNESDAY</td>
                <td></td>
                <td></td>
                <td class="lunch">LUNCH</td>
                <td>Mentor Meet</td>
                <td></td>
            </tr>
            <tr>
                <td class="day">THURSDAY</td>
                <td>Calculus & Matrix</td>
                <td>Advanced C Programming</td>
                <td class="lunch">LUNCH</td>
                <td></td>
                <td></td>
            </tr>
            <tr>
                <td class="day">FRIDAY</td>
                <td>Web App Development</td>
                <td>Calculus & Matrix</td>
                <td class="lunch">LUNCH</td>
                <td></td>
                <td></td>
            </tr>
            <tr>
                <td class="day">SATURDAY</td>
                <td></td>
                <td>Career Dev</td>
                <td class="lunch">LUNCH</td>
                <td>Physics</td>
                <td></td>
            </tr>
        </tbody>
    </table>

    <div class="Subject-Title">Subject Details</div>
    <table class="Subject-Table">
        <thead>
            <tr>
                <th>S.No</th>
                <th>Subject Code</th>
                <th>Subject Name</th>
            </tr>
        </thead>
        <tbody>
            <tr><td>1</td><td>19AI304</td><td>Advanced C Programming</td></tr>
            <tr><td>2</td><td>19AI414</td><td>Web Application Development</td></tr>
            <tr><td>3</td><td>SH6708</td><td>Career Development</td></tr>
            <tr><td>4</td><td>19AI302</td><td>Engineering Design and Modelling</td></tr>
            <tr><td>5</td><td>SH3214</td><td>Physics for Quantum Computing</td></tr>
            <tr><td>5</td><td>SH7801</td><td>Human Values and Professional Ethics</td></tr>
            <tr><td>5</td><td>SH2201</td><td>Calculus and Matrix Algebra</td></tr>

        </tbody>
    </table>
    <footer>
         ©2025 Saveetha Engineering College
    </footer>
</div>

</body>
</html>
```

## OUTPUT
![alt text](<Screenshot 2025-05-13 212927.png>)

## RESULT
The program for creating slot timetable using basic HTML tags is executed successfully.
