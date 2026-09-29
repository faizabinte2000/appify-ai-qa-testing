# EchoGPT QA Testing

This repository contains the QA testing documentation for the **EchoGPT Multi AI Chat Chrome Extension** and **EchoChat Android App**.

The testing focused on functional behavior, usability, cross-platform differences, edge cases and unexpected behavior.

## Applications Tested

### Chrome Extension

**EchoGPT Multi AI Chat**

[Chrome Web Store](https://chromewebstore.google.com/detail/echogpt-multi-ai-chat-sid/negimdcamohmoheiifgecbjgjepkcfhj)

### Android Application

**EchoChat**

[Google Play Store](https://play.google.com/store/apps/details?id=com.echogpt.chatapp&hl=en)

## Project Structure

```text
EchoGPT-QA-Testing/
├── Test-Cases/
│   └── EchoGPT_Functional_Test_Cases.xlsx
│
├── Bug-Reports/
│   ├── BUG-001.md
│   ├── BUG-002.md
│   ├── BUG-003.md
│   └── ...
│
├── UI-UX-Review/
│   └── UI-UX-REVIEW.md
│
├── Exploratory-Testing/
│   └── Exploratory-Testing.md
│
├── Evidence/
│   ├── BUG-001-context-failure.jpeg
│   ├── BUG-002-history-time.jpeg
│   ├── BUG-003-missing-first-name-field.jpeg
│   └── ...
│
└── README.md
```
## Testing Scope

The following areas were covered during testing:

- Authentication and account management
- Email and Google sign-in
- OTP verification
- Account registration
- Session persistence and sign-out
- AI conversations and conversation context
- History and saved conversations
- AI model selection
- Compare feature
- Message quota
- Response actions
- New Chat and conversation management
- Attachments and file handling
- Voice input
- Camera and image input
- Write features
- Read features
- Translate features
- Image Studio
- Video Studio
- Settings and profile
- Subscription and upgrade flow
- Chrome Extension shortcuts
- Cross-platform behavior
- UI layout and usability

## Test Environment

### Android

- **Device:** realme 8 Pro
- **OS:** Android 12
- **App Version:** 1.0.8
- **Network:** Wi-Fi

Additional UI testing was performed on:

- **Device:** Samsung Galaxy Tab S6

### Chrome Extension

- **Platform:** macOS
- **Browser:** Google Chrome
- **Extension:** EchoGPT Multi AI Chat

## Test Cases

A total of **100 functional test cases** were documented.

The complete test case documentation includes:

- Test Case ID
- Feature
- Preconditions
- Test Steps
- Expected Result
- Actual Result
- Status
- Bug ID where applicable

The detailed test cases are available in:

**[EchoGPT Functional Test Cases](./Test-Cases/EchoGPT_Functional_Test_Cases.xlsx)**

### Test Summary

| Total Test Cases | Passed | Failed |
|---:|---:|---:|
| 100 | 74 | 17 |

Some test cases were also marked as **Not Run**, **Pass With Observation** or **Observed Difference** where applicable.

## Bug Reports

Bug reports were created for functional issues found during testing.

Each bug report includes relevant details such as:

- Bug ID
- Title
- Description
- Steps to Reproduce
- Expected Result
- Actual Result
- Severity
- Priority
- Environment
- Evidence

The evidence files are stored in the `Evidence/` folder.

## UI/UX Review

A separate UI/UX review was performed to document visual and usability observations that were better treated as improvement suggestions rather than functional defects.

The review includes observations related to:

- Responsive layout
- Spacing and alignment
- History
- Response actions
- Message quota visibility
- Shortcut commands
- Registration
- Email autocomplete
- Compare model selection
- Connectors
- Chat input
- Main screen layout
- Model information visibility

The complete review is available here:

**[UI/UX Review](./UI-UX-Review/UI-UX-REVIEW.md)**

## Exploratory Testing

Approximately **30–45 minutes** of exploratory testing was performed beyond the planned test cases.

The exploratory testing focused on:

- AI conversation behavior
- History
- Compare
- Message quota
- Registration and authentication
- Attachments
- Write features
- Read and Translate features
- UI and layout
- Cross-platform behavior
- Edge cases

The exploratory testing report is available here:

**[Exploratory Testing Report](./Exploratory-Testing/Exploratory-Testing.md)**

## Key Areas of Observation

During testing several types of issues were identified:

- Differences in behavior between Android and Chrome
- Conversation context issues
- Incorrect History timestamps
- Missing response actions in reopened conversations
- Differences in response actions between platforms
- Message quota visibility differences
- AI models remaining in a loading state
- Incorrect model attribution in saved Compare responses
- Registration validation mismatch
- Email autocomplete selection issue
- Screenshot processing failure
- UI spacing and alignment issues
- Incomplete or truncated information
- Missing free/paid labels for AI models

## Evidence

Screenshots and screen recordings collected during testing are stored in the `Evidence/` folder.

Evidence is linked from the relevant bug reports, UI/UX review and test case documentation.

## Testing Approach

The testing approach included:

1. Reviewing the available features and application flow.
2. Creating functional test cases for the main features.
3. Executing the test cases on Android and Chrome Extension.
4. Recording actual results and test status.
5. Re-testing unexpected behavior where possible.
6. Documenting reproducible functional issues as bug reports.
7. Comparing common features across Android and Chrome.
8. Performing exploratory testing to identify additional edge cases.
9. Reviewing visual and usability issues separately in the UI/UX review.
10. Attaching screenshots and recordings as supporting evidence.

## Deliverables

This repository contains the following QA deliverables:

- **100 Functional Test Cases**
- **Bug Reports**
- **UI/UX Review**
- **Exploratory Testing Report**
- **Screenshots and Screen Recordings**
- **Test Execution Results**

## Notes

The findings documented in this repository are based on the application behavior observed during the testing period and on the devices and environments listed above.
