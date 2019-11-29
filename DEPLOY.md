# Deployment scripts
# Acceptance tests

User Interaction:
To check whether the bot is running
Type “Hi Guerdon” 
Bot will respond:

"Hi I am Guerdon. Here is what I can do for you: -
Train my classifier ; <G-drive link
Test the classifier ; <G-drive link> ;  <input text> 
Classify my test ; <input text>
Find top <N> members" 

Use Case 1: Train your text classifier
- Upload an excel containing training data to google drive with access permission to all.
- Enter a message in the following format in mattermost: "Train my classifier ; <G-drive link>"
- Bot will reply with training status to user.
- Once model is trained, bot uploads the trained model to G-drive and provides link back to the user.
Note: If the provided link is not accessible or no data is found, bot would return an error.
  
Use Case 2: Provide trained classifier and input data to test the classifier.
- Upload trained model to G-drive and make the link accessible to all.
- Enter a message in the following format in Mattermost: "Test the classifier ; <G-drive link> ;  <input text> "
- Bot responds with the result once classification is complete. 
 Note: If the provided link is not accessible or no model is found or Input text is not provided, bot would return error.
    
Use Case 3: Test our Bot classifier.
- Enter a message in the following format: "Classify my test ; <input text>"
- Bot would update user with the result once classification is complete.
Note: If input text is not provided, bot would return error.

Use Case 4: Mattermost top N users using our AI bot.
- Enter a message in the following format: "Find top <N> members"
Note: If bot is not able to fetch user data from Mattermost, it would return error.
  
# Continuous Integration (CI) Server
# Screencast
