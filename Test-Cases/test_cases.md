# EchoGPT Functional Test Cases

**Detailed Test Data:** The complete test case documentation, including test steps, actual results, and bug IDs, is available in the Excel file:

**[EchoGPT_Functional_Test_Cases.xlsx](./EchoGPT_Functional_Test_Cases.xlsx)**

## Test Summary

| Test Result | Number of Test Cases |
|---|---:|
| Passed | 74 |
| Failed | 17 |
| Pass With Observation | 3 |
| Not Run | 4 |
| Not Verified | 1 |
| Observed Difference | 1 |
| **Total** | **100** |

A total of 100 functional test cases were documented and evaluated. Of these, 74 passed and 17 failed. Three test cases passed with observations, four were not run, one could not be verified, and one recorded an observed difference. The detailed test cases, actual results, and associated bug IDs are available in the accompanying Excel file.

## Functional Test Cases

| ID | Test Case | Preconditions | Expected Result | Status |
|---|---|---|---|---|
| TC-001 | First Launch | Extension freshly installed, not signed in | Sidebar opens on the right with a sign-in / welcome screen and no errors in the console. | Pass |
| TC-002 | Keyboard Shortcut (macOS) | EchoGPT extension is installed on a macOS device | EchoGPT sidebar should open successfully. | Pass |
| TC-003 | (Android App)Sign In with Google — Valid Account | Valid Google account available | User should be authenticated successfully and redirected to the main chat screen without requiring OTP. | Pass |
| TC-004 | (Android App)Sign In with Email — Valid Email + OTP | Registered EchoGPT email account available; user has access to the email | User should be authenticated successfully and redirected to the main chat screen after successful OTP verification. | Pass |
| TC-005 | (Android App)Sign In with Email — Incorrect OTP | Registered EchoGPT email account available | User should not be authenticated and should receive an appropriate error message. | Pass |
| TC-006 | (Android App)Sign In with Email — OTP Required | Registered EchoGPT email account available | User should not be able to continue until the required OTP is fully entered. | Pass |
| TC-007 | (Android App)Sign In with Email — Invalid Email Format | App is on the email sign-in screen | App should validate the email format and prevent the OTP process from being initiated. | Pass |
| TC-008 | Sign Up with Email — New Email (Android App) | Email address has never been registered | User should receive a verification code at the new email address and be able to proceed with account creation. | Pass |
| TC-009 | Sign Up with Email — Existing Email (Android App) | Email address is already associated with an account | App should prevent duplicate account registration and inform the user that an account with the email already exists and they should sign in instead. | Pass |
| TC-010 | Sign Up with Email — Required Fields Validation (Android App) | Sign-up form is displayed | App should prevent submission when required fields are empty and indicate the missing required field(s). | Pass |
| TC-011 | Sign Up with Email — Invalid Email Format (Android App) | Sign-up form is displayed | App should reject the invalid email format and prevent the verification process from starting. | Pass |
| TC-012 | Sign Up with Google — Valid Account (Android App) | Valid Google account available | User should be authenticated successfully through Google and redirected to the main chat screen without requiring an OTP. | Pass |
| TC-013 | Authentication Session Persistence (Android App) | User has successfully signed in to the EchoGPT Android app | User should remain authenticated after reopening the app and should not be required to sign in again. | Pass |
| TC-014 | Logout (Android App) | User is successfully authenticated and on the main chat screen | User should be successfully logged out and redirected to the authentication screen. Protected account/chat functionality should not be accessible without signing in again. | Pass |
| TC-015 | Sign In with Google — Valid Account (Chrome Extension) | Valid Google account available | User should be authenticated successfully and redirected to the main chat screen without requiring an OTP. | Pass |
| TC-016 | Sign In with Email — Valid Email + OTP (Chrome Extension) | Registered EchoGPT email account available; user has access to the email | User should be authenticated successfully and redirected to the main chat screen after successful OTP verification. | Pass |
| TC-017 | Sign In with Email — Invalid Email (Chrome Extension) | Chrome Extension is on the email sign-in screen | App should validate the email address and prevent the verification process from proceeding with an invalid email. | Pass |
| TC-018 | Create New Account — Email Registration (Chrome Extension) | Chrome Extension is on the Create New Account screen | User should be able to initiate account registration using the information provided on the Create New Account form. | Fail |
| TC-019 | Create New Account — Invalid Email (Chrome Extension) | Chrome Extension is on the Create New Account screen | App should validate the email format and prevent the verification process from proceeding with an invalid email. | Pass |
| TC-020 | Email Autocomplete Selection (Chrome Extension) | Chrome Extension is on an email input field and email suggestions are displayed | User should be able to select a displayed email suggestion and populate the email field, if the displayed suggestions are intended to be selectable. | Fail |
| TC-021 | Authentication Session Persistence (Chrome Extension) | User is successfully signed in to the EchoGPT Chrome Extension | User should remain authenticated after reopening the browser and extension if persistent login is supported. | Pass |
| TC-022 | Sign Out (Chrome Extension) | User is successfully authenticated and on the main chat screen | User should be successfully signed out and required to authenticate again before accessing the main chat screen. | Fail |
| TC-023 | Suggested Prompts(Android App) | User is logged in and on the EchoChat home screen. | The selected prompt should be submitted and the AI should generate a response. | Pass |
| TC-024 | Ask Anything (Android App) | App is open and user is on the Ask Anything screen | The question should be sent successfully, a relevant response should appear, the counter should become 3 of 5, the Latest button should appear, and the response should be fully readable. | Pass |
| TC-025 | Ask Anything – Empty Input(Android App) | App is open and user is on the Ask Anything screen | The app should prevent submission of an empty message. | Pass |
| TC-026 | Ask Anything – Conversation Context(Android App) | User has sent a previous question and received a response in the same conversation | The app should understand that “the main types you mentioned” refers to the types of software testing in the previous response and provide a relevant answer. | Fail |
| TC-027 | Latest Button(Android App) | User is in a conversation and the Latest button is visible | Tapping Latest should navigate the user to the latest/end portion of the current conversation. | Pass |
| TC-028 | Network Error Handling(Android App) | User is on the Ask Anything screen with an active internet connection | The app should handle the loss of internet connection gracefully and inform the user that an internet connection is required when appropriate. | Pass |
| TC-029 | History – Conversation Timestamp (Android App) | User has an existing conversation and can access History | History should display the correct local date and time corresponding to when the conversation was created/updated. | Fail |
| TC-030 | History – Reopen Conversation | User has at least one existing conversation in History | The selected conversation should open successfully and display the previous messages completely and in the correct order. | Pass |
| TC-031 | AI Model Selection | User is on the Ask Anything screen | The model selector should open, allow the user to select an available model, and correctly display the newly selected model. | Pass |
| TC-032 | Ask Anything – Special Characters and Symbols | User is logged in and on the Ask Anything screen | The system should accept and correctly display the input containing special characters, symbols, numbers, and punctuation, and generate a response without errors or input corruption. | Pass |
| TC-033 | History – Response Actions in Reopened Conversation (Chrome Extension) | User has an existing conversation containing an AI response and can access History | Previously saved AI responses should retain the available response actions, including Copy and Retry, when the conversation is reopened from History. | Fail |
| TC-034 | Response Action Parity Across Platforms | User is signed in using the same account on Android App and Chrome Extension | Response actions should be consistent across supported platforms unless platform-specific functionality is defined. | Fail |
| TC-035 | Quota Indicator Visibility Before Limit Reached | User is signed in and has remaining message quota | The application should provide clear visibility of the remaining message quota and reset information before the usage limit is reached, and clearly communicate when the limit is reached. | Fail |
| TC-036 | Compare – Multiple AI Models Response (Chrome Extension) | User is signed in and the Compare feature is available | Each selected model should process the same prompt and return a response within a reasonable time. If a model cannot process the request, a clear error or failure message should be displayed instead of remaining indefinitely in a loading state. | Fail |
| TC-037 | History – Correct Model Attribution for Compare Responses | User have an existing Compare conversation containing responses from multiple AI models | Each saved Compare response should display the AI model that originally generated that response, regardless of the currently selected model. | Fail |
| TC-038 | Shortcut Commands Button (Chrome Extension) | User is signed in and the chat screen is displayed | The Shortcut Commands button should open or display the available shortcut commands. | Fail |
| TC-039 | Screenshot Attachment and Processing (Chrome Extension) | User is signed in and the chat screen is displayed | The screenshot captured by the Screenshot/Scissors feature should be successfully processed and made available to the AI for analysis. | Fail |
| TC-040 | Attachment/Document and Photo Access — Premium Restriction (Android App) | User is signed in with a non-Premium account | The application should restrict document/photo attachment functionality according to the Premium plan requirement and clearly communicate the restriction to the user. | Fail |
| TC-041 | Voice Input — Microphone Permission (Android App) | User is signed in and on a screen that supports voice input | The app should request microphone permission when needed and allow voice input after permission is granted. | Pass |
| TC-042 | Voice Input — Denied Microphone Permission (Android App) | User is signed in and microphone permission is denied | The app should handle denied microphone permission gracefully and provide appropriate guidance without crashing. | Pass |
| TC-043 | Camera/Image Input — Permission Handling (Android App) | User is signed in and a feature requiring camera/gallery access is selected | The app should request the required permission and proceed appropriately when permission is granted. | Pass |
| TC-044 | Copy AI Response (Android App) | User has received an AI response | Tapping Copy should copy the complete AI response to the device clipboard. | Pass |
| TC-045 | Retry AI Response (Android App) | User has received an AI response and Retry action is available | Tapping Retry should regenerate the response successfully. | Pass |
| TC-046 | Share AI Response (Android App) | User has received an AI response and Share action is available | Tapping Share should open the Android sharing interface with the AI response available to share. | Pass |
| TC-047 | Regenerate Response (Chrome Extension) | User has received an AI response | Regenerate/Retry should submit the request again and display a new response. | Pass |
| TC-048 | Stop Response Generation (Chrome Extension) | AI response generation is in progress | Stop should cancel the active response generation and prevent further tokens/content from being added. | Pass |
| TC-049 | New Chat | User is signed in and currently viewing a conversation | New Chat should start a fresh conversation without deleting previous conversations from History. | Pass |
| TC-050 | Delete Conversation | User has at least one saved conversation | Delete should remove the selected conversation after any required confirmation and it should no longer appear in History. | Pass |
| TC-051 | Clear Chat Input | User has typed text into the chat input field | The input field should be cleared successfully when the clear action is selected. | Pass |
| TC-052 | Long Message Input | User is signed in and chat input is available | The application should accept supported long input without crashing, freezing, or unexpectedly truncating the message. | Pass |
| TC-053 | Emoji Input | User is signed in and chat input is available | The application should accept and correctly display emoji in the input and conversation. | Pass |
| TC-054 | Multiple Attachments | User is signed in and attachment functionality is available | The application should handle multiple supported attachments according to the defined attachment limit and provide clear feedback if the limit is exceeded. | Pass |
| TC-055 | Unsupported Attachment Type | User is signed in and attachment functionality is available | The application should reject unsupported file types and provide a clear error message. | Pass |
| TC-056 | App/Extension Information Page | User is signed in and the application/extension menu is available | The About/Information option should open the EchoChat app installation or app information page. | Pass |
| TC-057 | Dark Mode Toggle (Android App) | User is signed in and the EchoChat Android App is open | The application should switch to Dark Mode when enabled and apply the dark theme consistently across the supported interface. Switching it off should restore the Light Mode appearance. | Pass |
| TC-058 | Image Studio — Paid Plan Requirement Disclosure (Chrome Extension) | User is signed in to the EchoGPT Chrome Extension with an account that does not have an active paid plan | The Image Studio interface should clearly communicate whether image generation requires a paid plan before the user submits a generation request. | Fail |
| TC-059 | Video Studio — Paid Plan Requirement Disclosure (Chrome Extension) | User is signed in to the EchoGPT Chrome Extension with an account that does not have an active paid plan | The Video Studio interface should clearly communicate whether video generation requires a paid plan before the user submits a generation request. | Fail |
| TC-060 | Image Studio — Empty Prompt Validation | User is signed in to the EchoGPT Chrome Extension and has access to Image Studio | The application should prevent image generation when the prompt field is empty and clearly inform the user that a prompt is required. | Pass |
| TC-061 | Video Studio — Empty Prompt Validation | User is signed in to the EchoGPT Chrome Extension and has access to Video Studio | The application should prevent video generation when the prompt field is empty and clearly inform the user that a prompt is required. | Pass |
| TC-062 | Write - Compose - Default State | User is signed in and the Chrome Extension is open | Write - Compose opens successfully with Topic, Format, Tone, Length, Output Language, AI model selection, and Generate button visible. | Pass |
| TC-063 | Write - Compose - Format Selection | User is on Write > Compose | The selected format should be visually indicated and applied to the generated content. | Pass |
| TC-064 | Write - Compose - Tone Selection | User is on Write > Compose | The selected tone should be visually indicated and applied to the generated content. | Pass |
| TC-065 | Write - Compose - Length Selection | User is on Write > Compose | The generated content length should correspond to the selected length option. | Pass |
| TC-066 | Write - Compose - Output Language | User is on Write > Compose | Content should be generated in the selected output language. | Pass |
| TC-067 | Write - Compose - Generate Content | User is on Write > Compose | The system should generate relevant content based on the entered topic and selected options. | Pass |
| TC-068 | Write - Compose - Empty Topic | User is on Write > Compose | The system should prevent generation and provide appropriate validation or guidance for the required Topic field. | Pass |
| TC-069 | Write - Reply - Default State | User is signed in and the Chrome Extension is open | Write - Reply should display Original Text, What to Reply, Format, Tone, Length, Output Language, AI model selection, and Generate button. | Pass |
| TC-070 | Write - Reply - Empty What to Reply | User is on Write > Reply | The system should handle an empty What to Reply field appropriately according to the feature design. | Pass |
| TC-071 | Write - Grammar - Default State | User is signed in and the Chrome Extension is open | Grammar mode should open with a text input area and Fix Grammar button. | Pass |
| TC-072 | Write - Grammar and Spelling Correction | User is on Write > Grammar | The system should identify and correct grammar and spelling errors while preserving the intended meaning. | Pass |
| TC-073 | Write - Reply - Empty Original Text | User is on Write > Reply | The system should prevent generation and prompt the user to enter the Original Text. | Pass |
| TC-074 | Write - Grammar - Empty Input | User is on Write > Grammar | The system should prevent processing and prompt the user to enter text. | Pass |
| TC-075 | Write - Generated Text Persistence Across Features | User is on Write and has successfully generated text | The generated text should behave consistently when navigating between features according to the intended session-state behavior. | Pass |
| TC-076 | AI Model Selection - Free and Advanced Models | User is signed in and the Chrome Extension is open | The system should allow the user to select available Free and Advanced models and generate a response successfully using the selected model. | Pass |
| TC-077 | Read - Valid Link | Signed in, Read tab open | The page content should be successfully fetched and made available for chat, with a loading state while fetching. | Pass |
| TC-078 | Read - Long Webpage Free Plan Limit | Signed in, Read tab open, Free plan | The system should handle webpages exceeding the Free-plan input limit by clearly informing the user that the extracted content is too long and indicating the applicable character limit. | Pass |
| TC-079 | Read - Invalid/Malformed URL | Read tab is open | The system should reject the invalid input and display a clear error or validation message without crashing. | Pass |
| TC-080 | Read - Unreachable/404 Link | Read tab is open | The system should display a clear error indicating that the page could not be accessed or found, instead of silently failing or crashing. | Pass |
| TC-081 | Read - Login-Gated Link | Read tab is open | The system should handle a login-gated page appropriately without fabricating unavailable account-specific content or crashing. | Pass |
| TC-082 | Read - Empty Link Field | Read tab is open | The system should prevent reading an empty link or display an appropriate validation message. | Pass |
| TC-083 | Read - File Upload (Supported Type) | Read tab is open | The file should upload successfully and the filename or preview should appear; its content should become available for chat. | Pass |
| TC-084 | Read - Unsupported File Type | Signed in, Read tab is open | The system should reject unsupported file types and display a clear error message identifying the unsupported type and supported file formats. | Pass |
| TC-085 | Read - Oversized File Upload | Signed in, Read tab is open | The system should either process the file successfully or clearly indicate if the file exceeds the allowed size/processing limit. | Not Run |
| TC-086 | Read - Link and File Behavior | Signed in, Read tab is open | The system should accept both supported webpage links and supported file uploads and make their content available for processing. | Not Run |
| TC-087 | Translate - Default State | Signed in, Translate tab open | Translate should open with Source Language set to Automatic, Target Language set to English, an empty text box, AI model selector, Translate button, and Swap button. | Pass |
| TC-088 | Translate - Auto-Detect Source Language | Translate tab is open | The system should automatically detect the source language and translate the text into the selected target language. | Pass |
| TC-089 | Translate - Explicit Source and Target Languages | Translate tab is open | The system should translate the text according to the explicitly selected source and target languages. | Pass |
| TC-090 | Translate - Swap Languages | Translate tab is open with Bengali as Source Language and Japanese as Target Language | The Source and Target language selections should swap correctly. | Fail |
| TC-091 | Translate - Empty Text Validation | Translate tab is open | The system should prevent translation of empty input and provide an appropriate validation message. | Pass |
| TC-092 | Translate - Long Text Handling | Translate tab is open | The system should process the long text without crashing, freezing, or silently losing a significant portion of the input. | Pass |
| TC-093 | Translate - Same Source and Target Language | Translate tab is open | The system should handle identical source and target languages without crashing or displaying an unexpected error. | Pass |
| TC-094 | Translate - Model Selection | Translate tab is open | The selected model should be applied to the translation request and the translation should be generated successfully. | Not Run |
| TC-095 | Translate - Special Characters and Emoji | Translate tab is open | The system should translate the text while preserving or appropriately handling numbers, symbols, and emoji. | Not Run |
| TC-096 | Upgrade Icon - Subscription Page Redirect | Signed in, EchoGPT extension open | The Upgrade option should redirect the user to the EchoGPT subscription page where available plans/upgrades can be viewed. | Pass |
| TC-097 | Settings and Profile Icon Navigation | User is signed in to the EchoGPT Chrome Extension | The Settings icon and profile/name icon should navigate to their intended settings or account interfaces. | Pass With Observation |
| TC-098 | Pin Extension Icon | Chrome browser open with EchoGPT extension installed | The extension should be pinned and its icon should appear in the Chrome browser toolbar. | Pass |
| TC-099 | Account Deletion Option - Platform Comparison | Signed in on Android app and Chrome extension | The availability of account management options should be consistent across platforms unless platform-specific behavior is intentionally defined. | Observed Difference |
| TC-100 | Re-registration Using Email From Deleted Account | An EchoGPT account has previously been deleted from the Android App | The application should clearly communicate whether an email address associated with a deleted account can be registered again. If re-registration is not permitted, the application should provide a clear user-facing explanation or recovery/support option. | Pass With Observation |

## Status Legend

- **Pass** — Actual result matched the expected result.
- **Fail** — Actual result did not match the expected result.
- **Pass With Observation** — The expected functionality was achieved, but an observation or minor difference was noted during testing.
- **Not Run** — The test case was documented but was not executed during the testing period.
- **Not Verified** — The expected behavior could not be conclusively verified during testing.
- **Observed Difference** — The behavior differed from the expected or comparable platform behavior and was recorded for further review.




