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
* **Cities longitude latitude**: I search on Google for each city manually but after the plotting phase noticed that they need to be recalibrated -1 on each metric to achieve good result.

* **Student chose Science**: Each Student can choose only one Science category. So if in a student 'Biology' cell in empty then we conclude that he or she is on Social Science.

* **Population prediction**: Our original dataset only has a population of 1999, 2009, and 2019. To retreive population of 2022 for data relevancy we used Arima model and divided the gap year 2009 to 2019 in to one year gap like 2009, 2010, 2011,..., 2018, 2019 and the population go in a linear way and feed into my Arima with the step of 3 and retreive the result is population of 2022.

## Results
