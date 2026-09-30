Exploratory Testing

I spent around 30–45 minutes exploring the EchoChat Android app and Chrome Extension beyond the planned test cases. I focused on how the main features behave during normal use and also checked some edge cases to find usability issues or unexpected behavior.

### Areas Explored

- **AI conversations:** Tested normal questions and follow-up questions to check whether the AI could maintain conversation context. I also checked response actions such as Copy and Retry.
- **History:** Opened previous conversations from History and checked timestamps and whether response actions were still available after reopening a conversation.
- **Compare:** Tested the Compare feature with multiple AI models. I checked how the selected models responded and how model information was displayed.
- **Message quota:** Checked how the remaining message quota and reset information are shown. I compared the experience between Android and Chrome.
- **Registration and sign-in:** Tested the registration form and validation messages. I also checked email suggestions and sign-out behavior.
- **Attachments:** Tested the Screenshot/Scissors feature in the Chrome Extension and checked whether the captured screenshot could be processed.
- **UI and layout:** Reviewed the interface on Android, Samsung Galaxy Tab S6 and Chrome. I checked spacing, alignment, text visibility and the overall layout.
- **Cross-platform behavior:** Compared features that are available on both Android and Chrome to identify differences in how they work or are presented.

### Key Observations

- Some features behave differently between Android and Chrome. For example response actions and message quota information are not presented in the same way.
- Some controls do not give a clear visible response when selected which can make their purpose unclear.
- Some important information is not fully visible. For example model information can be cut off.
- The Compare feature does not clearly indicate whether an AI model is free or paid.
- Some screens could have better spacing and alignment especially on larger screens.
- The registration form showed a validation message for a field that was not visible on the form.
- The Screenshot/Scissors feature allowed a PNG screenshot to be attached but the file could not be processed.
- Testing multiple AI models in Compare also revealed cases where models remained stuck on "Waiting for response...".

### Recommendations

- Keep common features more consistent across Android and Chrome where possible.
- Give users clear feedback when they click or select a control.
- Make sure important messages and model information can be viewed completely.
- Clearly label AI models as free or paid before users select them.
- Improve spacing and alignment across different screen sizes.
- Make validation messages match the fields shown in the form.
- Clearly indicate supported file types when users attach files or screenshots.
- Review edge cases involving conversation history, multiple AI models, attachments, message quotas and registration.

The findings from exploratory testing are also documented in the test cases, bug reports and UI/UX review submitted with this assignment.
