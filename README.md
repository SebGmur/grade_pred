# grade_pred
Student Grade Prediction - Kaggle Competition v01

Objective: Predict final grade (Feature Name: G3)

Information:<br><br>
This data approach student achievement in secondary education of two Portuguese schools. The data attributes include student grades, demographic, social and school-related features) and it was collected by using school reports and questionnaires. Two datasets are provided regarding the performance in two distinct subjects: Mathematics (mat) and Portuguese language (por). In [Cortez and Silva, 2008], the two datasets were modeled under binary/five-level classification and regression tasks. Important note: the target attribute G3 has a strong correlation with attributes G2 and G1. This occurs because G3 is the final year grade (issued at the 3rd period), while G1 and G2 correspond to the 1st and 2nd period grades. It is more difficult to predict G3 without G2 and G1, but such prediction is much more useful (see paper source for more details).


For reference check: <a href="https://www.kaggle.com/dipam7/student-grade-prediction">Kaggle</a>


<a href="https://www.kaggle.com/dipam7/student-grade-prediction/download"> Dataset </a>

<strong>Relevant Papers:</strong><br>
P. Cortez and A. Silva. Using Data Mining to Predict Secondary School Student Performance. In A. Brito and J. Teixeira Eds., Proceedings of 5th FUture BUsiness TEChnology Conference (FUBUTEC 2008) pp. 5-12, Porto, Portugal, April, 2008, EUROSIS, ISBN 978-9077381-39-7.<br>
Available at: <a href="http://www3.dsi.uminho.pt/pcortez/student.pdf">Web Link</a>
<br><br>
<html>
<head>
<style>
table {
  font-family: arial, sans-serif;
  border-collapse: collapse;
  width: 100%;
}

td, th {
  border: 1px solid #dddddd;
  text-align: left;
  padding: 8px;
}

tr:nth-child(even) {
  background-color: #dddddd;
}
</style>
</head>
<body>
<h3>Explanation of dimensions present in the dataset</h3>
<table>
  <tr>
    <th>Feature Name</th>
    <th>Description</th>
  </tr>
  <tr>
    <td colspan="2" style="align:right;"><strong>BINARY DATA:</strong></td>
  </tr>
  <tr>
    <td>school</td>
    <td>student's school (binary: 'GP' - Gabriel Pereira or 'MS' - Mousinho da Silveira)</td>
  </tr>
  <tr>
    <td>sex</td>
    <td>student's sex (binary: 'F' - female or 'M' - male)</td>
  </tr>
  <tr>
    <td>address</td>
    <td>student's home address type (binary: 'U' - urban or 'R' - rural)</td>
  </tr>
  <tr>
    <td>famsize</td>
    <td>family size (binary: 'LE3' - less or equal to 3 or 'GT3' - greater than 3)</td>
  </tr>
  <tr>
    <td>Pstatus</td>
    <td>parent's cohabitation status (binary: 'T' - living together or 'A' - apart)</td>
  </tr>
  <tr>
    <td>schoolsup</td>
    <td>extra educational support (binary: yes or no)</td>
  </tr>
  <tr>
    <td>famsup</td>
    <td>family educational support (binary: yes or no)</td>
  </tr>
  <tr>
    <td>paid</td>
    <td>extra paid classes within the course subject (Math or Portuguese) (binary: yes or no)</td>
  </tr>
  <tr>
    <td>activities</td>
    <td>extra-curricular activities (binary: yes or no)</td>
  </tr>
  <tr>
    <td>nursery</td>
    <td>attended nursery school (binary: yes or no)</td>
  </tr>
  <tr>
    <td>higher</td>
    <td>wants to take higher education (binary: yes or no)</td>
  </tr>
  <tr>
    <td>internet</td>
    <td>Internet access at home (binary: yes or no)</td>
  </tr>
  <tr>
    <td>romantic</td>
    <td>with a romantic relationship (binary: yes or no)</td>
  </tr>
  <tr>
    <td colspan="2" style="align:right;"><strong>NUMERIC DATA:</strong></td>
  </tr>
  <tr>
    <td>age</td>
    <td>student's age (numeric: from 15 to 22)</td>
  </tr>
  <tr>
    <td>Medu</td>
    <td>mother's education (numeric: 0 - none, 1 - primary education (4th grade), 2 at 5th to 9th grade, 3 at secondary education or 4 at higher education)</td>
  </tr>
  <tr>
    <td>Fedu</td>
    <td>father's education (numeric: 0 - none, 1 - primary education (4th grade), 2 at 5th to 9th grade, 3 at secondary education or 4 at higher education)</td>
  </tr>
  <tr>
    <td>traveltime</td>
    <td>home to school travel time (numeric: 1 - 1 hour)</td>
  </tr>
  <tr>
    <td>studytime</td>
    <td> weekly study time (numeric: 1 - 10 hours)</td>
  </tr>
  <tr>
    <td>failures</td>
    <td> number of past class failures (numeric: n if 1<=n<3, else 4)</td>
  </tr>
  <tr>
    <td>famrel</td>
    <td> quality of family relationships (numeric: from 1 - very bad to 5 - excellent)</td>
  </tr>
  <tr>
    <td>freetime</td>
    <td>free time after school (numeric: from 1 - very low to 5 - very high)</td>
  </tr>
  <tr>
    <td>goout</td>
    <td>going out with friends (numeric: from 1 - very low to 5 - very high)</td>
  </tr>
  <tr>
    <td>Dalc</td>
    <td>workday alcohol consumption (numeric: from 1 - very low to 5 - very high)</td>
  </tr>
  <tr>
    <td>Walc</td>
    <td>weekend alcohol consumption (numeric: from 1 - very low to 5 - very high)</td>
  </tr>  
  <tr>
    <td>health</td>
    <td>current health status (numeric: from 1 - very bad to 5 - very good)</td>
  </tr>  
  <tr>
    <td>absences</td>
    <td>number of school absences (numeric: from 0 to 93)</td>
  </tr>
  <tr>
    <td>G1</td>
    <td>first period grade (numeric: from 0 to 20)</td>
  </tr> 
  <tr>
    <td>G2</td>
    <td>second period grade (numeric: from 0 to 20)</td>
  </tr> 
  <tr>
    <td>G3</td>
    <td>final grade (numeric: from 0 to 20, output target)</td>
  </tr> 
  <tr>
    <td colspan="2" style="align:right;"><strong>NOMINAL DATA:</strong></td>
  </tr>
  <tr>
    <td>Mjob</td>
    <td>mother's job (nominal: 'teacher', 'health' care related, civil 'services' (e.g. administrative or police), 'at_home' or 'other')</td>
  </tr> 
  <tr>
    <td>Fjob</td>
    <td>father's job (nominal: 'teacher', 'health' care related, civil 'services' (e.g. administrative or police), 'at_home' or 'other')</td>
  </tr> 
  <tr>
    <td>reason</td>
    <td>reason to choose this school (nominal: close to 'home', school 'reputation', 'course' preference or 'other')</td>
  </tr> 
  <tr>
    <td>guardian</td>
    <td>student's guardian (nominal: 'mother', 'father' or 'other')</td>
  </tr> 
</table>

</body>
</html>
