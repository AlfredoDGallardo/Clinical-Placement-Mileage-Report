<p align="center">
<img src="https://profitbooks.net/wp-content/uploads/2024/04/Microsoft-Excel-Logo.png" height="40%" width="40%" alt="Microsoft Azure Logo"/>
</p>

<h1> Clinical-Placement-Mileage-Report </h1>
Excel-based clinical mileage tracking report with insights on student placement distances and forecasting future courses
</p>

## 📊 Overview
This report calculates the mileage between each student and their assigned clinical location along with courses student is projected to take within the next 3 terms, helping optimize placement decisions and identify outliers for travel support.

## 🛠 Tools Used
- Microsoft Excel (formulas, VLOOKUP, conditional formatting)
- Geocoding via manual inputs and mapping tools
- Data anonymized for privacy

## 🔍 Key Features
- Conditional Formatting : Conditional formatting helps visually highlight key data points in the report, making it easier to identify patterns, outliers, and areas that require further attention or action. 
  - Conditional formatting is used to highlight each student's mileage to the three closest cities-green for closest, yellow for the second closest, and blue for third closest.
  - Conditional formatting is applied to display student names in red font if their home address is in a state where the school is not authorized to enroll students. This serves as a key identifier for further investigation and address resolution.
- Formulas : 
  - The Haversine formula to calculate the straight-line distance between a student’s home ZIP code and each placement ZIP code. This trigonometry-based approach enables accurate zip-to-zip mileage comparisons, helping identify the nearest clinical sites.
    - Formula Used : 🧮```excel"=ACOS(SIN(RADIANS(Lat1)) * SIN(RADIANS(Lat2)) + COS(RADIANS(Lat1)) * COS(RADIANS(Lat2)) * COS(RADIANS(Lon2 - Lon1))) * 3958.8"```
  - The use of a dynamic array formula to retrieve and display each student’s projected future courses. The formula filters a list of planned courses from a separate sheet by matching the student ID, then transposes the results so the courses align horizontally with the student’s next three academic terms. This allows the report to dynamically reflect each student's upcoming coursework based on their academic roadmap
    - Formula Used : 🧮```excel =TRANSPOSE(FILTER(CourseListRange, StudentID = StudentIDRange))```

## 📁 Files
- (https://github.com/AlfredoDGallardo/Clinical-Placement-Mileage-Report/blob/main/Anonymizez_Sample_Student_Mileage_Report.xlsx) – Main Excel file
- `Screenshot.png` – Visual example of output

## 💼 Business Impact
Helped reduce student travel time by identifying closer placement options and increased transparency in placement decisions.
