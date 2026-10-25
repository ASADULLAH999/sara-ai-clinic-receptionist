## Description: <br>
Read and send email via IMAP/SMTP. Check for new/unread messages, fetch content, search mailboxes, mark as read/unread, and send emails with attachments. Supports multiple accounts. Works with any IMAP/SMTP server including Gmail, Outlook, 163.com, vip.163.com, 126.com, vip.126.com, 188.com, and vip.188.com. <br>

This skill is ready for commercial/non-commercial use. <br>

## Publisher: <br>
[gzlicanyi](https://clawhub.ai/user/gzlicanyi) <br>

### License/Terms of Use: <br>
MIT-0 <br>


## Use Case: <br>
Developers and agent users use this skill to configure mailbox access, inspect and manage IMAP messages, download allowed attachments, and send SMTP email from one or more configured accounts. <br>

### Deployment Geography for Use: <br>
Global <br>

## Known Risks and Mitigations: <br>
Risk: The skill requires credentials for the selected email account and can access mailbox contents. <br>
Mitigation: Use app passwords or authorization codes where supported, keep credentials scoped to the intended account, and install only when mailbox access is acceptable. <br>
Risk: SMTP send and test commands can send real email. <br>
Mitigation: Verify recipients, subject, body, attachments, and selected account before running send or test commands. <br>
Risk: Attachment download and file attachment features can read or write local files. <br>
Mitigation: Keep ALLOWED_READ_DIRS and ALLOWED_WRITE_DIRS narrow and confirm attachment paths before running commands that move file data. <br>
Risk: IMAP mark-read and mark-unread commands change mailbox state. <br>
Mitigation: Confirm mailbox names and message UIDs before running state-changing IMAP commands. <br>


## Reference(s): <br>
- [ClawHub skill page](https://clawhub.ai/gzlicanyi/imap-smtp-email) <br>
- [Google App Passwords](https://myaccount.google.com/apppasswords) <br>
- [Related caldav-sync skill](https://clawhub.ai/gzlicanyi/caldav-sync) <br>


## Skill Output: <br>
**Output Type(s):** [text, markdown, code, shell commands, configuration, guidance] <br>
**Output Format:** [Markdown guidance with inline shell commands and JSON command results from the Node.js scripts] <br>
**Output Parameters:** [1D] <br>
**Other Properties Related to Output:** [May read mailbox data, write downloaded attachments to allowlisted directories, and send real email through the configured SMTP account.] <br>

## Skill Version(s): <br>
0.0.15 (source: server release evidence) <br>

## Ethical Considerations: <br>
Users should evaluate whether this skill is appropriate for their environment, review any generated or modified files before relying on them, and apply their organization's safety, security, and compliance requirements before deployment. <br>
