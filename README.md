## SODP_Team240

## Dataset folder

##Dataset folder contains the 7 csv files which we are using to create the statistical model

**-assessments.csv**

This file contains information about assessments in module-presentations. Usually, every presentation has a number of assessments followed by the final exam. CSV contains columns:
<ol>
  <li>code_module – identification code of the module, to which the assessment belongs.</li>
  <li>code_presentation - identification code of the presentation, to which the assessment belongs.</li>
  <li>id_assessment – identification number of the assessment.</li>
  <li>assessment_type – type of assessment. Three types of assessments exist: Tutor Marked Assessment (TMA), Computer Marked Assessment (CMA) and Final Exam (Exam).
  <li>date – information about the final submission date of the assessment calculated as the number of days since the start of the module-presentation. The starting date of the presentation has number 0 (zero).</li>
  <li>weight - weight of the assessment in %. Typically, Exams are treated separately and have the weight 100%; the sum of all other assessments is 100%.</li>
  If the information about the final exam date is missing, it is at the end of the last presentation week.
</ol>
  
**-courses.csv**

File contains the list of all available modules and their presentations. The columns are:
<ol>
  <li>code_module – code name of the module, which serves as the identifier.</li>
  <li>code_presentation – code name of the presentation. It consists of the year and “B” for the presentation starting in February and “J” for the presentation starting in October.</li>
  <li>length - length of the module-presentation in days.</li>
The structure of B and J presentations may differ and therefore it is good practice to analyse the B and J presentations separately. Nevertheless, for some presentations the corresponding previous B/J presentation do not exist and therefore the J presentation must be used to inform the B presentation or vice versa. In the dataset this is the case of CCC, EEE and GGG modules.
</ol>  

**-studentAssessment.csv**

This file contains the results of students’ assessments. If the student does not submit the assessment, no result is recorded. The final exam submissions is missing, if the result of the assessments is not stored in the system. This file contains the following columns:
<ol>
  <li>id_assessment – the identification number of the assessment.</li>
  <li>id_student – a unique identification number for the student.</li>
  <li>date_submitted – the date of student submission, measured as the number of days since the start of the module presentation.</li>
  <li>is_banked – a status flag indicating that the assessment result has been transferred from a previous presentation.</li>
  <li>score – the student’s score in this assessment. The range is from 0 to 100. The score lower than 40 is interpreted as Fail. The marks are in the range from 0 to 100.</li>
</ol>

**-studentInfo.csv**

This file contains demographic information about the students together with their results. File contains the following columns:
<ol>
  <li>code_module – an identification code for a module on which the student is registered.</li>
  <li>code_presentation - the identification code of the presentation during which the student is registered on the module.</li>
  <li>id_student – a unique identification number for the student.</li>
  <li>gender – the student’s gender.</li>
  <li>region – identifies the geographic region, where the student lived while taking the module-presentation.</li>
  <li>highest_education – highest student education level on entry to the module presentation.</li>
  <li>imd_band – specifies the Index of Multiple Depravation band of the place where the student lived during the module-presentation.</li>
  <li>age_band – band of the student’s age.</li>
  <li>num_of_prev_attempts – the number times the student has attempted this module.</li>
  <li>studied_credits – the total number of credits for the modules the student is currently studying.</li>
  <li>disability – indicates whether the student has declared a disability.</li>
  <li>final_result – student’s final result in the module-presentation.</li>
</ol>

**-studentRegistration.csv**
This file contains information about the time when the student registered for the module presentation. For students who unregistered the date of unregistration is also recorded. File contains five columns:
<ol>
  <li>code_module – an identification code for a module.</li>
  <li>code_presentation - the identification code of the presentation.</li>
  <li>id_student – a unique identification number for the student.</li>
  <li>date_registration – the date of student’s registration on the module presentation, this is the number of days measured relative to the start of the module-presentation (e.g. the negative value -30 means that the student registered to module presentation 30 days before it started).</li>
  <li>date_unregistration – date of student unregistration from the module presentation, this is the number of days measured relative to the start of the module-presentation. Students, who completed the course have this field empty. Students who unregistered have Withdrawal as the value of the final_result column in the studentInfo.csv file.</li>
</ol>

**-studentVle.csv**

The studentVle.csv file contains information about each student’s interactions with the materials in the VLE. This file contains the following columns:
<ol>
  <li>code_module – an identification code for a module.</li>
  <li>code_presentation - the identification code of the module presentation.</li>
  <li>id_student – a unique identification number for the student.</li>
  <li>id_site - an identification number for the VLE material.</li>
  <li>date – the date of student’s interaction with the material measured as the number of days since the start of the module-presentation.</li>
  <li>sum_click – the number of times a student interacts with the material in that day.</li>
</ol>

**-vle.csv**

The csv file contains information about the available materials in the VLE. Typically these are html pages, pdf files, etc. Students have access to these materials online and their interactions with the materials are recorded. The vle.csv file contains the following columns:
<ol>
  <li>id_site – an identification number of the material.</li>
  <li>code_module – an identification code for module.</li>
  <li>code_presentation - the identification code of presentation.</li>
  <li>activity_type – the role associated with the module material.</li>
  <li>week_from – the week from which the material is planned to be used.</li>
  <li>week_to – week until which the material is planned to be used.</li>
</ol>

## Dataset Citation
Kuzilek J., Hlosta M., Zdrahal Z. Open University Learning Analytics dataset Sci. Data 4:170171 doi: 10.1038/sdata.2017.171 (2017).
