# CO3102_CW2
I ran and tested everything using Android studio emulator on a Pixel 4 API 30 Device.

**Users**
New Users can create accounts by pressing Regiser button on the login screen which will take them to the UserActivity screen where they can pick questions and answer them.
Existing users can login simply by entering their credentials.
If user used the app before their email should be autofilled in the login box.
System does not track which options users have picked it only tracks what questions were answered in order to prevent users from going back and changinng their answers.

**Registration**
Users can register simply by filling out the required fields, all invalid inputs should be proptly marked when the register button is pressed to notify the user what was wrong.
Users can also use the Camera to scan QR codes to get SNI Number by pressing the camera Icon.

**Admins**
Admins can login through the same login page but instead they're taken to their own AdminActivity which has more control over the system.
** Creating a New Question**
Pressing the FAB (Floating Action Button) takes them to the addNewQuestionActivity which allows administrators create new questions.
FAB on the addNewQuestionActivity opens a bottomsheetdrawer where  administrators can input their option names and save by pressing Save button.
Pressing Finish Submits the question to the database and takes the admin back to the AdminActivity.

**Editing Existing Question**
Administrators can press on a existing question within the AdminActivity and it will open EditQuestion Activity or StatisticsActivity(Displays graph of votes) depending on 
whether users already voted. This is done to prevent editing/removing existing questions as outlined in the CW2 sheet.
On editingActivity Administrators can change question title, options and add new options if needed. Moreover, EditQuestionActivity Gives administrators ability to remove the question.

** Accounts **

Currently Created accounts used for testing Purposes

--Admins--
Username: admin@shangrila.gov.un
password: shangrila@2021$

--Users--
Usernames: user@test.com, test@user.com
Both users share the same password which is: password


**More Info**
The System uses Firebase NoSQL Approach to storing data.
Currently I have it loded in with default questions, there are no answers given to them yet.
The StatisticsActivity can only be seen by going into the "Dummy" and "How old are you?" Questions where I preloded random votes to showcase the horizontal bar graph.

**Known Bugs**
Due to personal circumstances or lack of time I was not able to fix a delay in editing Options, Options are edited and updated. However it requires administrators to manually
refresh the activity by pressing FAB and back button which causes the recyclerView to get reloaded.