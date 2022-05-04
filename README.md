<!--
WildFit Plus
-->
# WildFit Plus
![Swift](https://img.shields.io/badge/swift-5.5-brightgreen.svg) ![Xcode 13.2+](https://img.shields.io/badge/xcode-13.2%2B-blue.svg) ![iOS 15.0+](https://img.shields.io/badge/iOS-15.0%2B-blue.svg) ![watchOS 8.0+](https://img.shields.io/badge/watchOS-8.0%2B-blue.svg) ![CareKit 2.1+](https://img.shields.io/badge/CareKit-2.1%2B-red.svg) ![ci](https://github.com/netreconlab/CareKitSample-ParseCareKit/workflows/ci/badge.svg?branch=main)

## Description
<!--
This app leverages CareKit and HealthKit to deliver a day-by-day and week-by-weak health and wellness plan. 
It not only helps ones physical health, but also their mental health with daily stress, gratitude and happiness evaluations.
-->
An application of [CareKit](https://github.com/carekit-apple/CareKit)'s OCKSample synchronizing CareKit data to the Cloud via [ParseCareKit](https://github.com/netreconlab/ParseCareKit). It also leverages the [HealthKit](https://developer.apple.com/documentation/healthkit) framework. The app delivers a day-by-day and week-by-week health and wellness plan. It not only helps with physical health, but also mental health with daily stress, gratitude and happiness evaluations.

### Demo Video
<!--
Add the public link to your YouTube or video posted elsewhere.
-->
To learn more about this application, watch the video below:

<a href="http://www.youtube.com/watch?feature=player_embedded&v=mib_YioKAQQ
" target="_blank"><img src="http://img.youtube.com/vi/mib_YioKAQQ/0.jpg" 
alt="Sample demo video" width="240" height="180" border="10" /></a>

### Designed for the following users
<!--
Describe the types of users your app is designed for and who will benefit from your app.
-->
Men and Women between the ages of 18 and 60.
Beginner to Intermediate fitness level people.
Those who want better physical and mental wellness.

<!--
In addition, you can drop screenshots directly into your README file to add them to your README. Take these from your presentations.
-->
<img src="https://user-images.githubusercontent.com/8621344/101721031-06869500-3a75-11eb-9631-88927e9c8f00.png" width="300"> <img src="https://user-images.githubusercontent.com/8621344/101721111-33d34300-3a75-11eb-885e-4a6fc96dbd35.png" width="300"> <img src="https://user-images.githubusercontent.com/8621344/101721146-48afd680-3a75-11eb-955a-7848146a9d6f.png" width="300"><img src="https://user-images.githubusercontent.com/8621344/101721182-5cf3d380-3a75-11eb-99c9-bde40477acf3.png" width="300">

<!--
List all of the members who developed the project and
link to each members respective GitHub profile
-->
Developed by: 
- [Marshall Royce](https://github.com/mrro253) - University of Kentucky, Computer Science

ParseCareKit synchronizes the following entities to Parse tables/classes using [Parse-Swift](https://github.com/parse-community/Parse-Swift):

- [x] OCKTask <-> Task
- [x] OCKHealthKitTask <-> HealthKitTask 
- [x] OCKOutcome <-> Outcome
- [x] OCKRevisionRecord.KnowledgeVector <-> Clock
- [x] OCKPatient <-> Patient
- [x] OCKCarePlan <-> CarePlan
- [x] OCKContact <-> Contact

**Use at your own risk. There is no promise that this is HIPAA compliant and we are not responsible for any mishandling of your data**

<!--
What features were added by you, this should be descriptions of features added from the [Code](https://uk.instructure.com/courses/2030626/assignments/11151475) and [Demo](https://uk.instructure.com/courses/2030626/assignments/11151413) parts of the final. Feel free to add any figures that may help describe a feature. Note that there should be information here about how the OCKTask/OCKHealthTask's and OCKCarePlan's you added pertain to your app.
-->
## Contributions/Features
1. Steps counter --> OCKHealthKitTask with a goal of 5000 steps per day, this is visualized in insights. Shown as a NumericProgressTaskView.

2. Water intake tracker --> OCKHealthKitTask with a goal of 8 cups per day, this is visualized in insights. Shown as a NumericProgressTaskView.

3. Calisthenics exercises --> OCKTask that repeats every other day, has user do 50 push ups and crunches. The amount of these exercises completed is visualized in insights. Shown as an OCKGridTaskViewController.

4. Arm, legs, and chest Workouts --> OCKTask that repeats every 3 days in order to give users time to recover between workouts. The amount of completed workout exercises is visualized in insights. Shown as an OCKChecklistTaskViewController.

5. Wellness check-in --> ResearchKit survey that collects sleep, pain, happiness, and stress levels daily, this is visualized in insights. Shown as an OCKSurveyTaskViewController.

6. Gratitude log --> OCKTask. Studies have shown that by recognizing things you are grateful for throughout the day, self positivity and mental health are likely to increase. The number of logs is visualized in insights. Shown as an OCKButtonLogTaskViewController.

7. Vitamin/Supplement reminder --> OCKTask that Repeats daily. Shown as an OCKSimpleTaskViewController

8. Trending Workouts --> CustomFeaturedTaskView. Shown as an OCKFeaturedContentView

9. Visualized Data --> Charts task data as OCKCartesianChartViewController.
## Final Checklist
<!--
This is from the checkist from the final [Code](https://uk.instructure.com/courses/2030626/assignments/11151475). You should mark completed items with an x and leave non-completed items empty
-->
- [x] Signup/Login screen tailored to app
- [x] Signup/Login with email address
- [x] Custom app logo
- [ ] Custom styling
- [x] Add at least **5 new OCKTask/OCKHealthKitTasks** to your app
  - [x] Have a minimum of 7 OCKTask/OCKHealthKitTasks in your app
  - [x] 3/7 of OCKTasks should have different OCKSchedules than what's in the original app
- [x] Use at least 5/7 card below in your app
  - [ ] InstructionsTaskView - typically used with a OCKTask
  - [x] SimpleTaskView - typically used with a OCKTask
  - [x] Checklist - typically used with a OCKTask
  - [x] Button Log - typically used with a OCKTask
  - [x] GridTaskView - typically used with a OCKTask
  - [x] NumericProgressTaskView (SwiftUI) - typically used with a OCKHealthKitTask
  - [ ] LabeledValueTaskView (SwiftUI) - typically used with a OCKHealthKitTask
- [ ] Add the LinkView (SwiftUI) card to your app
- [x] Replace the current TipView with a class with CustomFeaturedContentView that subclasses OCKFeaturedContentView. This card should have an initializer which takes any link
- [x] Tailor the ResearchKit Onboarding to reflect your application
- [x] Add tailored check-in ResearchKit survey to your app
- [x] Add a new tab called "Insights" to MainTabView
- [x] Replace current ContactView with Searchable contact view
- [ ] Change the ProfileView to use a Form view
- [ ] Add at least two OCKCarePlan's and tie them to their respective OCKTask's and OCContact's 

## Wishlist features
<!--
Describe at least 3 features you want to add in the future before releasing your app in the app-store
-->
1. Log or track a run
2. Allow users to choose what kind of plan they want
3. Allow users to create their own workouts
4. Let users "Start exercise" and track data from it to log.

## Challenges faced while developing
<!--
Describe any challenges you faced with learning Swift, your baseline app, or adding features. You can describe how you overcame them.
-->
I had a lot of trouble implementing the calisthenics and workout tasks in terms of getting the schedule correct, as well as figuring out how to correctly display the workouts that I wanted to in a way I was okay with. Another big issue I faced was just a creative block, in terms of figuring out how to implement what I wanted into the app while also being able to conform to the requirements listed above.
Getting around the HealthKit documentation and figuring out how to get different HealthKit data took me a while to get used to as well, and even still I was unable to implement any HKWorkout tasks or samples.
## Setup Your Parse Server

### Heroku
The easiest way to setup your server is using the [one-button-click](https://github.com/netreconlab/parse-hipaa#heroku) deplyment method for [parse-hipaa](https://github.com/netreconlab/parse-hipaa).


## View your data in Parse Dashboard

### Heroku
The easiest way to setup your dashboard is using the [one-button-click](https://github.com/netreconlab/parse-hipaa-dashboard#heroku) deplyment method for [parse-hipaa-dashboard](https://github.com/netreconlab/parse-hipaa-dashboard).
