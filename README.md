# Dashboard-3

<img width="1315" height="727" alt="image" src="https://github.com/user-attachments/assets/02e643b1-d6e0-43e1-97fe-855b48c52cef" />

**HR Analytics Dashboard | Power BI**

An interactive HR Analytics dashboard built in Microsoft Power BI to explore employee headcount, attrition (employee turnover), and how attrition varies by department, salary band, job role, satisfaction, gender, age, and tenure.
Project purpose: Turn HR data into a clear overview that can help stakeholders spot workforce patterns and decide where to investigate further. The dashboard describes patterns in the dataset; it does not, by itself, prove why employees leave.

**Dashboard overview**

The report brings together headline HR metrics, breakdowns of attrition, employee demographics, and filters for exploring specific groups.

**KPI cards**
| Visual | What it represents | How to read it |
|---|---|---|
| **Total Employees** | The total number of employee records counted by the report. | A high-level headcount for the dataset. Check the underlying measure and filters to confirm whether it represents unique employees. |
| **Active Employees** | Employees classified as still employed. In this report, the card uses `Attrition = NO` to identify active employees. | The number remaining after the active-employee filter is applied. |
| **Attrition Count** | The number of employees recorded as having left. | A count of departures, not a percentage. |
| **Attrition Rate %** | The percentage of employees who left, according to the report's attrition-rate measure. | Useful for understanding turnover relative to the employee population. Confirm the measure's denominator and filter context before comparing it with other reports. |
| **Average Age** | The average age of employees in the current filter context. | Gives a broad view of the workforce's age profile. |
| **Avg Experience** | The average value of `YearsAtCompany` used by the report. | This field reflects **years at the company (tenure)**, not necessarily total professional experience. Consider renaming the card to **Average Years at Company** for clarity. |


**Charts and other visuals**
| Visual | What it represents | How to read it |
|---|---|---|
| **Attrition by Department** — donut chart | How the attrition count is distributed across departments. | Compare the slices to see which departments account for more departures. A larger slice may reflect a larger department, so it does not automatically mean that department has the highest attrition rate. |
| **Attrition by Salary Slab** — clustered bar chart | Attrition split by salary band and attrition category. | Compare categories across salary bands. Use this to explore whether departures appear concentrated in particular pay bands; it does not establish that salary caused the departures. |
| **Attrition by Job Role & Satisfaction** — table/matrix | Attrition count broken down by job role and job-satisfaction level. | Helps identify role/satisfaction combinations with higher departure counts. Check the row and column labels and current filters when interpreting the values. |
| **Age Group Distribution** — column chart | Employee distribution across age groups. | Shows which age groups contain more employees. This is a workforce distribution visual, not necessarily an attrition comparison. |
| **Attrition by Gender** — pie chart | The attrition count split by gender. | Compares the share of recorded departures by gender. For a fair comparison of risk, compare gender-specific attrition rates as well as counts, since group sizes may differ. |
| **Attrition Trend by Experience** — area chart | Attrition count plotted against `TotalExperience(Years)`. | Shows how the count varies across total-experience values. The field is total experience, which differs from `YearsAtCompany`. If the chart uses summed attrition counts, confirm that summing is appropriate for the underlying data. |
| **Department-Wise Employee Count** — funnel chart | Employee count by department. | Compares department sizes. The funnel shape is a visual style; departments are categories, not necessarily sequential stages in a process. A bar chart may be easier for comparing departments. |
| **Department** — slicer | Filters the report to a selected department. | Selecting a department should update visuals that interact with this slicer. Clear the selection to return to all departments. |
| **AgeGroup** — slicer | Filters the report to a selected age group. | Use it to inspect the KPIs and charts for a particular age group. Clear the selection to return to all age groups. |

**Key business questions this dashboard can help explore**
- How many employees are in the dataset, and how many are still active?
- How many departures are recorded, and what is the measured attrition rate?
- Which departments account for the largest number of departures?
- How do departure counts vary across salary bands, job roles, satisfaction levels, gender, and experience?
- How does the workforce's age distribution look?
- Do the patterns change when filtering by department or age group?
These are exploratory questions. To compare attrition fairly across groups of different sizes, use attrition rates (departures divided by the relevant employee population), not departure counts alone.

**Interactivity**
- Use the Department slicer to focus on one department.
- Use the AgeGroup slicer to focus on an age range.
- Select a chart segment or bar to cross-filter other visuals where visual interactions are enabled.
- Clear selections to return to the overall view.

**Data and interpretation notes**
- The report uses fields such as EmpID, EmployeeCount, Attrition, AttritionCount, AttritionRate %, Age, AgeGroup, Department, Gender, SalarySlab, JobRole, JobSatisfaction, YearsAtCompany, and TotalExperience(Years).
- Attrition = YES generally indicates that an employee left; Attrition = NO generally indicates that the employee remains employed.
- Counts and rates answer different questions. Counts show the volume of departures; rates help compare groups of different sizes.
- A relationship shown in a chart does not establish causation. Further analysis is needed before making HR policy decisions.
- The exact figures shown depend on the data, measures, filters, and interactions in the Power BI report.
Tools and skills demonstrated
- Microsoft Power BI
- HR KPI reporting and dashboard layout
- Data visualisation (cards, donut, bar, column, pie, area, funnel, and matrix/table visuals)
- Filtering and cross-filtering with slicers
- Exploratory analysis of employee attrition and workforce demographics
