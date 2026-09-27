# UI/UX Review

This review documents visual and usability observations identified during testing of the EchoChat application and extension. These observations are provided as improvement suggestions rather than functional defects.

| ID | Screen / Area | UI/UX Observation | Recommendation | Evidence |
|---|---|---|---|---|
| UX-001 | Sign-in | Layout could be better optimized for the larger Samsung Tab S6 screen. | Improve responsive spacing and alignment on larger screens. | [UX-001.png](../Evidence/UX-001.png) |
| UX-002 | History | History timestamps could be displayed using the correct local time to help users identify conversations accurately. | Ensure conversation timestamps consistently reflect the user's local time. | [UX-002.png](../Evidence/UX-002.png) |
| UX-003 | Settings / Profile | The Settings icon and profile/name control currently open the same popup, which may make their purposes less distinct. | Differentiate the navigation or functions of these controls. | [UX-003.png](../Evidence/UX-003.png) |
| UX-004 | History / Response Actions | Response actions such as Copy and Retry could remain available when users reopen a saved conversation from History. | Maintain consistent response actions for saved conversations where applicable. | [UX-004.png](../Evidence/UX-004.png) |
| UX-005 | Response Actions | Available response actions differ between Android and Chrome, which may result in an inconsistent user experience. | Maintain consistent response-action options across supported platforms where applicable. | [UX-005.png](../Evidence/UX-005.png) |
| UX-006 | Message Quota | The remaining message quota is more visible on Android than in the Chrome Extension. | Display remaining quota and reset information clearly across platforms. | [UX-006.png](../Evidence/UX-006.png) |
| UX-007 | Offline State | The message input and Send control remain available while offline, which may cause uncertainty about whether a message can be sent. | Provide clearer offline-state feedback and indicate when sending is unavailable. | [UX-007.png](../Evidence/UX-007.png) |
| UX-008 | Shortcut Commands | The Shortcut Commands control does not provide visible feedback when selected, which may make its purpose unclear. | Display the available shortcut commands or provide clear feedback when the control is activated. | [UX-008.png](../Evidence/UX-008.png) |
| UX-009 | Screenshot Attachment | The attachment interface allows a PNG screenshot to be selected before the format restriction becomes apparent. | Clearly indicate supported attachment formats before or during file selection. | [UX-009.png](../Evidence/UX-009.png) |
| UX-010 | Registration | The message “First name is required” does not correspond to a visible First Name field in the registration form. | Align validation messages with the fields presented in the form. | [UX-010.png](../Evidence/UX-010.png) |
| UX-011 | Email Autocomplete | Email suggestions are displayed but cannot be selected directly, reducing the usefulness of the autocomplete feature. | Allow users to select a displayed suggestion directly. | [UX-011.png](../Evidence/UX-011.png) |
