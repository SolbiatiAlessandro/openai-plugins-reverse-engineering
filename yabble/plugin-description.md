The Yabble plugin is designed to assist users in generating and running marketing surveys. It provides a six-step process to create a survey, target specific demographics, generate personas, run the survey, fetch responses, and generate insights from the data.

The namespace `yabble` contains the following type definitions:

1. `createSurveyAndFetchQuestions`: This type is used to create a new survey and fetch the generated questions for the survey. The fields for this type are:
   - `survey_topic`: A string representing the topic of the survey. It must not be greater than 220 characters.
   - `additional_information`: An optional string providing additional information to help generate correct questions for the survey topic. It can be up to 255 characters.

2. `saveDemographicFilterAndRunPersonaGeneration`: This type is used to save demographic parameters for the audience to be surveyed and run persona generation. The fields for this type are:
   - `survey_id`: The ID of the survey returned from the `createSurveyAndFetchQuestions` request.
   - `gender`, `age`, `location`, `marital_status`, `employment`, `salary`, `children`, `other_demographic_parameters`: Optional strings representing different demographic parameters. Each can be up to 200 characters, except for `other_demographic_parameters` which can be up to 255 characters.
   - `number_of_people_to_survey`: An optional number representing the number of people to survey. The default is 50.

3. `runTheSurvey`: This type is used to run the selected survey and returns a list of new responses created. The field for this type is:
   - `survey_id`: The ID of the survey returned from the `createSurveyAndFetchQuestions` request.

4. `getQuestions`: This type is used to check the questions available for a survey. The field for this type is:
   - `survey_id`: The ID of the survey returned from the `createSurveyAndFetchQuestions` request.

5. `addQuestion`: This type is used to create a new question for a survey that has not been run yet. The fields for this type are:
   - `survey_id`: The ID of the survey returned from the `createSurveyAndFetchQuestions` request.
   - `question_title`: An optional string representing the title of the question. It can be up to 220 characters.

6. `updateQuestion`: This type is used to update a question for a survey that has not been run yet. The fields for this type are:
   - `survey_id`: The ID of the survey returned from the `createSurveyAndFetchQuestions` request.
   - `question_id`: The ID of a question for the given survey.
   - `question_title`: An optional string representing the title of the question. It can be up to 220 characters.

7. `removeQuestion`: This type is used to remove a question from a survey that has not been run yet. The fields for this type are:
   - `survey_id`: The ID of the survey returned from the `createSurveyAndFetchQuestions` request.
   - `question_id`: The ID of a question for the given survey.

8. `getPersonas`: This type is used to return a list of created personas to be surveyed. The field for this type is:
   - `survey_id`: The ID of the survey returned from the `createSurveyAndFetchQuestions` request.

9. `getResultingResponsesFromSurveyRun`: This type is used to fetch full data from the survey. The fields for this type are:
   - `survey_id`: The ID of the survey returned from the `createSurveyAndFetchQuestions` request.
   - `page`: An optional number representing the page of data

to fetch. The default is 1.

These types provide a way to interact with the Yabble plugin, allowing the user to create surveys, specify demographic parameters, run the surveys, and fetch the responses. The plugin is designed to provide marketing insights for board presentations, so the insights are formatted professionally and may include images, PowerPoint slides, and documents. The user is also encouraged to check out Yabble for more automated market research insights.
