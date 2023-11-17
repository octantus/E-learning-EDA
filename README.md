# training_projects

The first one:
Product Manager has asked to analyze completed lessons and answer the following questions:

How many students successfully passed only one course? (Successful completion is defined as passing the course in the exam)
Identify the most difficult and the easiest exam: find courses and exams within the course that have the lowest and highest completion rates*.
Determine the average time to pass exams for each subject (consider the last successful exam completion by the student).
Identify the most popular subjects (TOP-3) based on the number of registrations. Also, identify subjects with the highest dropout rates (TOP-3).
Using pandas, identify the semester with the lowest course completion rates and the longest average completion times for courses from the beginning of 2013 to the end of 2014.
Often, for qualitative audience analysis, segmentation-based approaches are used. Using Python, build adapted RFM clusters of students to assess the audience qualitatively. In the adapted clustering, you can choose the following metrics: R - average time to pass one exam, F - course completion rate, M - average score obtained in exams. Describe in detail how you created the clusters. For each RFM segment, establish boundaries for recency, frequency, and monetary metrics for interpreting these clusters. The approach description can be found here.

# Files:
# assessments.csv — this file contains information about test assessments. Typically, each subject in a semester includes a series of tests with grades, followed by a final exam.
code_module — subject identification code.
code_presentation — semester (Identification code).
id_assessment — test (Identification number of the assessment).
assessment_type — type of test. There are three types of assessments: tutor-marked assessment (TMA), computer-marked assessment (CMA), course exam (Exam).
date — information about the final date of the test. Calculated as the number of days from the start of the semester. The start date of the semester has the number 0 (zero).
weight — test weight in % of the course grade. Exams are usually considered separately and have a weight of 100%; the sum of all other grades is 100%.

# courses.csv — the file contains a list of subjects by semester.
code_module — subject (identification code).
code_presentation — semester (identification code).
module_presentation_length — semester duration in days.

# studentAssessment.csv — this file contains students' test results. If a student does not submit an assignment for assessment, the result is not recorded in the table.
id_assessment — test (identification number).
id_student — student identification number.
date_submitted — date of submission of the test by the student, measured as the number of days from the start of the semester.
is_banked — the fact of transferring the test from the previous semester (sometimes courses are credited to students who have returned from academic leave).
score — student's grade on this test. The range is from 0 to 100. A grade below 40 is a failed test.

# studentRegistration.csv — this file contains information about the time when a student registered for the course in the semester.
code_module — subject (identification code).
code_presentation — semester (identification code).
id_student — student identification number.
date_registration — date of student registration. This is the number of days measured from the start of the semester (for example, a negative value of -30 means that the student registered for the course 30 days before its start).
date_unregistration — date of cancellation of student registration for the subject. For students who have completed the course, this field remains empty.
