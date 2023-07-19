# Analysis of Vietnam High School Graduation 2022 Exams


## Introduction
  The final examination from high school to university in Vietnam is a significant milestone that determines students' admission to higher education institutions. This project aims to analyze the examination process, exploring its structure, content, and impact on student's academic paths. By understanding this system, we can contribute to discussions on educational reform and student support, ultimately empowering Vietnamese students in their pursuit of academic success and personal growth.✨📚📊

## Dataset
We used two datasets for our research:

* **StudentGrade_2022**: This dataset contains approximately 1 million rows of data and serves as the primary dataset for our analysis and exploration.

* **Cities_Infomation**: The dataset used in our research contains the predicted population of Vietnam in 2022, derived from historical values such as 1999, 2009, and 2019. Additionally, it includes rankings that reflect the modernization level of cities, with tier 1 cities like Ha Noi and Ho Chi Minh City considered highly developed. The dataset also provides latitude and longitude coordinates for each city, enabling us to plot them on a world map for improved visualization.

## Hypothesis

* **Hypothesis 1**: Urban Students have better English grades than Rural Students:

  This is simple and easy to think of from a personal perspective but it will be a good first hypothesis to prove with our dataset before going deeper.
* **Hypothesis 2**: Students will tend to choose Social Science over Natural Science:

  Social Science is easy to understand, and results will be based on the student's memory power. Unlike in Natural Science where memory is not enough, applying logic and problem-solving is also essential. Students with weak and medium-weak academic will lean toward Social Science.
* **Hypothesis 3**: Above average math grade students will tend to choose Natural Science:

  This hypothesis examines the relationship between math grades and students' inclination toward Natural Science. It posits that students with stronger logical thinking skills, as demonstrated by their math performance, are more likely to opt for Natural Science.
* **Hypothesis 4**: Will a historic City (Ha Noi) and a modern city (Ho Chi Minh) affect student performance:

  This hypothesis investigates the potential impact of city characteristics on student performance. It focuses on the contrasting features of Ha Noi, with its rich history and culture, and Ho Chi Minh City, known for its technological advancements. The hypothesis explores whether these city attributes can affect student performance on exams.

## Methodology
* **Cities longitude latitude**: I search on Google for each city manually but after the plotting phase noticed that they need to be recalibrated -1 on each metric to achieve good results.

* **Student chose Science**: Each Student can choose only one Science category. So if a student's 'Biology' cell is empty then we conclude that he or she is in Social Science.

* **Population prediction**: Our original dataset only has a population of 1999, 2009, and 2019. To retrieve the population of 2022 for data relevancy we used Arima model and divided the gap year 2009 to 2019 into one-year gap like 2009, 2010, 2011,..., 2018 and 2019 and the population go in a linear way and feed into my Arima with the step of 3, retrieving the result for the population of 2022.

## Results
### **Hypothesis 1**: Urban Students have better English grades than Rural Students:
<p align="center">
  <img src="https://github.com/yung575451/Analysis-of-Vietnam-High-School-Graduation-2022-Exams/assets/90661245/676fe9ba-53cf-4e18-859d-03513afc27bf" alt="Description of the image">
  <p align="center">Picture 1.1 : Urban and Rural Average English Grade</p>
</p>

<p align="center">
  <img src="https://github.com/yung575451/Analysis-of-Vietnam-High-School-Graduation-2022-Exams/assets/90661245/c332ddc8-4e39-4d8e-bc20-b9a24ccdea8f">
  <p align="center">Picture 1.2 : English Grade Distribution in Percentage</p>
</p>

### **Discussion**: 
  As We can see from picture 1.1, the average grade of an urban student is higher than rural student. This is can be seen more clearly when looking at 1.2 where the chart shows clearly that the majority of the rural student is below average while the grade of urban student is spread evenly throughout. This suggests that the infrastructure and resource for approaching and learning new languages in the countryside is still limited.

### **Hypothesis 2**: Students will tend to choose Social Science over Natural Science:
<p align="center">
  <img src="https://github.com/yung575451/Analysis-of-Vietnam-High-School-Graduation-2022-Exams/assets/90661245/730a0518-bdf2-4ccd-868c-a454e2745fed">
  <p align="center">Picture 2.1 : 63 Cities Majority Subject</p>
</p>

### **Discussion**: 
It's pretty clear to see that the majority of 63 cities chose Social Science rather than Natural Science. This could have been skewed by the fact that Natural Science consists of many heavy subjects such as biology and physics while Social Science is a lot easier if you just want to graduate with subjects like history and Civic education. 

### **Hypothesis 3**: Above average math grade students will tend to choose Natural Science:
<p align="center">
  <img src="https://github.com/yung575451/Analysis-of-Vietnam-High-School-Graduation-2022-Exams/assets/90661245/4f0b93a5-0845-489d-ab76-cf9806983ed6">
  <p align="center">Picture 3.1 : 63 Cities Majority Subject</p>
</p>

### **Discussion**: 
This is the most surprising finding When filtering just the student above the mean of the national exam (>6.4). We get a clear difference between the North and South of VietNam in terms of choosing their Subject. It might come down to the different backgrounds of development. When the North is known for its rich history and culturists and the South for its improvement in technology.

### **Hypothesis 4**: Will a historic City (Ha Noi) and a modern city (Ho Chi Minh) affect student performance:
<p align="center">
  <img src="https://github.com/yung575451/Analysis-of-Vietnam-High-School-Graduation-2022-Exams/assets/90661245/eca8d255-dcea-4f5a-9549-db2ab5057936">
  <p align="center">Picture 4.1 : Literature point distribution</p>
</p>
<p align="center">
  <img src="https://github.com/yung575451/Analysis-of-Vietnam-High-School-Graduation-2022-Exams/assets/90661245/7ad2c0f2-47d0-4011-b6bb-30075419512a">
  <p align="center">Picture 4.2 : Math point distribution</p>
</p>
<p align="center">
  <img src="https://github.com/yung575451/Analysis-of-Vietnam-High-School-Graduation-2022-Exams/assets/90661245/a0a07900-25bf-4fdd-88f5-8c90218da65e">
  <p align="center">Picture 4.3 : English point distribution</p>
</p>
<p align="center">
  <img src="https://github.com/yung575451/Analysis-of-Vietnam-High-School-Graduation-2022-Exams/assets/90661245/fabf3ef8-ceac-40f7-b77f-451fcdba4090">
  <p align="center">Picture 4.4 : Natural Science point distribution</p>
</p>
<p align="center">
  <img src="https://github.com/yung575451/Analysis-of-Vietnam-High-School-Graduation-2022-Exams/assets/90661245/e1d9f209-7fc5-4ea8-841d-be672e03bad5">
  <p align="center">Picture 4.5 : Social Science point distribution</p>
</p>

### **Discussion**: 
While the differences between the two cities may not be apparent in the fields of Natural and Social Sciences, the characteristics of each city become more prominent when it comes to three major subjects: Math, English, and Literature.

In terms of Literature, Ha Noi's rich culture is reflected in its students, who exhibit a wide range of scores from 6.0 to 8.0. On the other hand, in Ho Chi Minh City, the majority of students achieve scores between 6.0 and 6.5.

When it comes to Math and English, the futuristic city of Ho Chi Minh City shines with its strong emphasis on these subjects. Although Ha Noi still maintains an advantage in the percentage of students scoring between 9.0 and 10.0, it can be attributed to the fact that Ha Noi has a higher number of outstanding students.

## **Conclusion**:
Analyzing the 2022 graduation exam results can provide valuable insights into the characteristics and educational backgrounds of students in different cities. This information can guide decisions on how to develop fields like science or literature, including when, where, and how to focus efforts. By understanding patterns and trends in exam performance, we can identify the strengths and weaknesses of each city, allowing for the allocation of resources and prioritization of specific subjects. This knowledge can inform educational strategies, curriculum development, and career pathways, leading to improved outcomes in various areas. In summary, analyzing exam results in relation to city characteristics helps make informed decisions for the development of science, literature, and other fields.
