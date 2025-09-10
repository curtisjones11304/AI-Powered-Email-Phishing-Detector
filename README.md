# AI-Powered-Email-Phishing-Detector

|                                  |     |
| -------------------------------- | --- |
| Project Name                     | AI-Powered Email Phishing Detector |
| Team Members and Email Addresses | Elton Batista, *ebatista2022@my.fit.edu*<br/>Jordan Chelsey, *jordan.r.chelsey@gmail.com*<br/>Curtis Jones, *cjones2022@my.fit.edu*  |
| Faculty Advisor                  | Khaled Slhoub |

### First Semester

|                      |                                                                                                                                                                                                                                                                                                                                                                                     |
| -------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Plan (Sep 3)         | [Plan](https://github.com/curtisjones11304/AI-Powered-Email-Phishing-Detector/blob/main/Project%20Plan%20(1).pdf), [Presentation](https://github.com/curtisjones11304/AI-Powered-Email-Phishing-Detector/blob/main/AI-Powered%20Email%20Phishing%20Detector%20(1).pdf)                                                                                                                                                                                                                                      |
| Milestone 1 (Sep 29) | [Requirement](https://cs.fit.edu/~pkc/classes/seniorProjects/requirement.pdf), [Design](https://cs.fit.edu/~pkc/classes/seniorProjects/design.pdf), [Test](https://cs.fit.edu/~pkc/classes/seniorProjects/test.pdf), [Presentation](https://cs.fit.edu/~pkc/classes/seniorProjects/milestone1.pdf), [Progress Evaluation](https://cs.fit.edu/~pkc/classes/seniorProjects/eval1.pdf) |
| Milestone 2 (Oct 27) | [Presentation](https://cs.fit.edu/~pkc/classes/seniorProjects/milestone3.pdf), [Progress Evaluation](https://cs.fit.edu/~pkc/classes/seniorProjects/eval2.pdf)                                                                                                                                                                                                                      |
| Milestone 3 (Nov 24) | [Presentation](https://cs.fit.edu/~pkc/classes/seniorProjects/milestone3.pdf), [Progress Evaluation](https://cs.fit.edu/~pkc/classes/seniorProjects/eval3.pdf)                                                                                                                                                                                                                      |


### Second Semester

|                      |                                                                                                                                                                                                                                                                                                                                           |
| -------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Plan (Sep 3)         | [Plan](https://cs.fit.edu/~pkc/classes/seniorProjects/plan2.pdf), [Presentation](https://cs.fit.edu/~pkc/classes/seniorProjects/plan2Pres.pdf)                                                                                                                                                                                            |
| Milestone 4 (Sep 29) | [Presentation](https://cs.fit.edu/~pkc/classes/seniorProjects/milestone4.pdf), [Progress Evaluation](https://cs.fit.edu/~pkc/classes/seniorProjects/eval4.pdf)                                                                                                                                                                            |
| Milestone 5 (Oct 27) | [Poster](https://cs.fit.edu/~pkc/classes/seniorProjects/poster.pdf), [Presentation](https://cs.fit.edu/~pkc/classes/seniorProjects/milestone5.pdf), [Progress Evaluation](https://cs.fit.edu/~pkc/classes/seniorProjects/eval5.pdf)                                                                                                       |
| Milestone 6 (Nov 24) | [User and/or Developer Manual](https://cs.fit.edu/~pkc/classes/seniorProjects/userManual.pdf), [Demo Video](https://cs.fit.edu/~pkc/classes/seniorProjects/demoVideo.jpg), [Presentation](https://cs.fit.edu/~pkc/classes/seniorProjects/milestone6.pdf), [Progress Evaluation](https://cs.fit.edu/~pkc/classes/seniorProjects/eval6.pdf) |

### Example Demo UI
<img width="648" height="446" alt="image" src="https://github.com/user-attachments/assets/d447534d-fc8d-49a6-8f24-49e69aa8b7d7" />

### Functional Goals
**Analyze Emails in Detail**
- The system will check the subject, the sender, the body text, and any links.

  - Example: An email that says _“Your Netflix account has been suspended. Please click here to verify”_ and includes a link like http\://netf1ix-security.com. A normal spam filter might miss this because it looks like a regular email, but the system should be able to pick up on the strange domain and urgent tone.

**AI Model for Classification**
- A machine learning model (starting with Logistic Regression and Random Forest, then moving to transformer models like DistilBERT) will be trained on a dataset of phishing and legitimate emails.

  - Example: If the model sees _“Password Expiration Notice”_ from an address like support\@randomserver.ru, it should label it phishing, while the same subject line from it-support\@fit.edu should be legitimate.

**Keyword and Pattern Checks**
- On top of the AI, some rules will be built in. Things like:

  - Too many exclamation marks → “Update your account NOW!!!”

  - Links that don’t match the company name → “Chase Bank” email with a link going to cheap-deals.com.

  - Use of URL shorteners → bit.ly or tinyurl to hide the real link.

**Risk Score and Explanation**
- Instead of just saying “this is phishing,” the system will give a score and reasons.

  - Example Output: _Phishing (92% confidence). Reasons: suspicious domain, urgent call to action, mismatch between sender name and email address._

**Visual tools**
- By utilizing visual tools such as charts and diagrams, the system will allow users to see:

  - The percentage of emails within their inbox that are phishing emails

  - A scatter chart displaying the spread of confidence scores among emails within their inbox

**Gmail Integration**
- By utilizing Google’s Gmail API, the system will safely give users several options on what to do with flagged phishing emails without directly interacting with redirect links that could expose users to possible malware, including:

  - Delete emails above a certain confidence threshold

  - Reporting flagged emails directly to Gmail

  - Blocking senders with malicious intent

**Demo Interface**
- A small interface (likely a web app with Flask or FastAPI) will let a user paste in an email. The result will show:

  - Safe or phishing.

  - Confidence score.

  - Highlighted risky parts (like a bad URL or urgent language).

Short explanation in plain English, e.g., _“This email asks for personal details and comes from an untrusted domain.”_



