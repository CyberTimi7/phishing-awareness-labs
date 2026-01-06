# Findings

During the phishing campaign simulation, most test emails failed to reach the target inbox. This outcome highlighted the effectiveness of modern email security controls in detecting and blocking suspicious or unauthenticated messages.

Several defensive mechanisms influenced email delivery, including spam filtering, sender reputation checks, and email authentication requirements such as SPF, DKIM, and DMARC. Emails sent from a locally configured mail server without proper domain authentication were either rejected outright or silently dropped before reaching the inbox.

The testing environment demonstrated that simply sending a phishing-style email is insufficient in real-world scenarios, as modern email clients apply multiple layers of protection before accepting a message. This reinforces the importance of email authentication, proper server configuration, and reputation management in preventing phishing attacks.

These findings emphasize that effective phishing defense relies on layered security controls rather than a single protective mechanism. Even basic configurations can significantly reduce the likelihood of successful phishing delivery.
