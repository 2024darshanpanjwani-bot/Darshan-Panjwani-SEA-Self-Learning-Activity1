# SEA – Self Learning Activity 1

**Student Name:** Darshan Panjwani  
**Roll Number:** 44  
**Topic:** Agile vs. DevOps in the Software Lifecycle

---

# 1. Agile vs. DevOps in the Software Lifecycle

Agile and DevOps support faster and more reliable software delivery, but they focus on different parts of the process. Agile emphasizes developing software in small, manageable iterations, collecting feedback, and adjusting to changing needs. DevOps connects development and operations so that testing, release, deployment, and monitoring can happen more smoothly and frequently.

DevOps combines team practices, processes, and tools to help organizations deliver software and services efficiently. It encourages teams to share responsibility, automate repetitive work, and improve applications continuously instead of treating development and operations as separate activities.

## Core Differences

| Dimension | Agile | DevOps |
|---|---|---|
| Primary focus | Iterative software development, product backlogs, and user stories. | The complete delivery process, including CI/CD, automation, monitoring, and operations. |
| Main goal | Deliver useful software in short cycles and respond to changing requirements. | Release changes regularly while maintaining reliability and stability. |
| Team structure | Common roles include developers, Product Owner, and Scrum Master, with stakeholder feedback during development. | Development, operations, QA, and security teams collaborate and share responsibility. |
| Feedback cycle | Feedback is commonly reviewed at the end of a sprint, often every one to several weeks. | Automated tests, logs, and monitoring can provide feedback within minutes or hours. |
| Common practices | Sprint planning, daily stand-ups, retrospectives, and backlog refinement. | CI/CD pipelines, automated testing, infrastructure as code, deployment automation, and monitoring. |

---

# 2. Managing the Workflow: Jira vs. Asana (SkillSwap Case Study)

For a MERN-stack platform such as **SkillSwap**, which helps students exchange skills with one another, project management involves both software development work and wider activities such as community building and launch planning.

## Jira – Managing Engineering Work

Jira is commonly used by software teams to plan and track work using Agile methods. For the core SkillSwap application, the development team can use Jira to organize features, bugs, and implementation tasks.

- **How it is used:** The team can divide development into sprints and group related tasks under epics, such as “User Authentication.” Story points can help estimate the effort needed for tasks such as implementing JWT-based login in Node.js or building responsive profile pages with React and Tailwind CSS.
- **Why it is useful:** Jira can integrate with GitHub, allowing related commits and pull requests to be associated with tickets. This makes it easier to follow a task from planning through implementation and review.

## Asana – Coordinating Cross-Functional Activities

Asana provides project planning features that help teams coordinate tasks, deadlines, dependencies, and responsibilities. It can be useful for activities that are not limited to coding.

- **How it is used:** The SkillSwap marketing or community team could use Asana to plan a beta launch, design campus promotional material, prepare terms of service, and schedule onboarding emails.
- **Why it is useful:** Its visual task boards and timelines can be easier for non-technical team members to use. It helps everyone understand ownership and deadlines without requiring them to follow software-development workflows.

---

# 3. Writing Effective User Stories and Acceptance Criteria

User stories describe a feature from the perspective of the person who will use it. They focus on the user's goal and the benefit of the feature rather than only describing technical implementation.

A commonly used format is:

**As a [type of user], I want to [perform an action] so that [I receive a benefit].**

## SkillSwap User Story Example

**User story:** As a registered student, I want to browse the available skills so that I can find another student who can help me learn a subject I find difficult.

## Acceptance Criteria (AC)

Acceptance criteria list the conditions that must be satisfied for a user story to be considered complete. They should be clear and possible to test.

### Checklist Format

- **AC1:** Only an authenticated user with a valid login session or JWT should be able to access the skill-browsing page.
- **AC2:** Skills should appear in a responsive grid that works on different screen sizes.
- **AC3:** Each skill card should display the provider's username, skill category, and proficiency level.

### Behavior-Driven Development (BDD) Format

- **Given** a student is logged in to SkillSwap and has opened another student's skill listing,
- **When** the student selects the **“Request Swap”** button,
- **Then** the system should save a pending request in the MongoDB database and notify the skill provider within the application.

---

# 4. Advanced Requirement Elicitation Techniques

Requirement elicitation is the process of discovering what users and stakeholders need from a system. For a peer-to-peer learning platform such as SkillSwap, using more than one technique can help reveal both expected features and problems users may not mention directly.

- **Structured interviews:** An analyst can speak individually with students to understand difficulties they face when arranging peer tutoring. These discussions may reveal a need for mutual ratings or reviews so that users can build trust when exchanging skills.
- **Ethnographic observation:** An analyst can observe how students currently find people to teach or learn a skill. For example, students may use multiple WhatsApp groups or campus noticeboards and may forget to follow up on requests. Observing this process can show why a central dashboard and automated reminders would be useful.
- **Prototyping:** The team can prepare simple wireframes of the React interface and ask students to try out a sample skill exchange. Their feedback can identify confusing screens or unnecessary steps before substantial backend development begins.

---

# 5. Requirement Traceability Matrix (RTM)

A **Requirement Traceability Matrix (RTM)** connects each requirement to its source, related system component, and test case. It helps the team confirm that requirements have been implemented and tested. It also makes it easier to identify missing work when a requirement changes.

## SkillSwap – Sample RTM

| Requirement ID | Requirement description | Source | Technical component | Test case ID | Status |
|---|---|---|---|---|---|
| REQ-001 | The system must authenticate users using JWT-based authentication. | Security specification | Node.js / Express authentication module | TC-Auth-01 | Verified |
| REQ-002 | Users must be able to create, view, update, and delete skill listings. | User story 4 | Skill and profile API routes with database access | TC-Skill-04 | Implemented |
| REQ-003 | The user interface must adjust to mobile screen sizes. | UI/UX guidelines | React and Tailwind CSS | TC-UI-09 | Tested |
| REQ-004 | The cloud database should support concurrent read requests. | Infrastructure specification | MongoDB Atlas cluster | TC-Perf-02 | Planned |

*Note: The entries and statuses above are illustrative examples for the SkillSwap case study.*

---

# 6. Tools for Requirement Management

Task-tracking applications help teams manage daily work, while requirement-management tools provide a structured way to document requirements, track changes, and connect requirements with design and testing.

## IBM DOORS

IBM DOORS (Dynamic Object-Oriented Requirements System) is a requirement-management solution designed for large and complex projects, including work in regulated fields such as aerospace, medical devices, and defence.

- **Strengths:** It supports traceability in both directions, controlled requirement changes, and audit records. When a requirement changes, teams can identify related design elements and test cases that may also need updating.
- **Limitations:** The software can take time to learn, its interface may feel less modern than lightweight collaboration tools, and licensing can be costly.

## Modern Alternatives for Web Projects

For a community-based MERN application such as SkillSwap, a large enterprise requirement-management system may be more than the project needs. Agile teams can instead consider tools that connect documentation, planning, and source code.

- **Jira + Confluence:** Confluence can store requirement documents and technical notes, while Jira tracks related tasks and development work. Links between issues and code changes help the team follow progress.
- **GitHub Projects:** This option keeps issues, project planning, and source code in the same environment. Teams can manage requirements alongside their repository and maintain documentation using Markdown files.

---

# Conclusion

Agile and DevOps address different but complementary needs in software delivery. Agile helps teams develop features iteratively and respond to feedback, while DevOps supports automation, collaboration, deployment, and ongoing monitoring. In a project such as SkillSwap, suitable workflow tools, well-written user stories, clear acceptance criteria, requirement elicitation, and an RTM can help the team plan and verify its work. Requirement-management tools further support documentation and change tracking throughout the software lifecycle.

## References

1. Amazon Web Services (AWS), **What is DevOps?** – https://aws.amazon.com/devops/what-is-devops/
2. Atlassian, **Agile** – https://www.atlassian.com/agile
3. Atlassian, **Jira** – https://www.atlassian.com/software/jira
4. Asana, **Project Management** – https://asana.com/
5. IBM, **Engineering Requirements Management DOORS** – https://www.ibm.com/products/requirements-management
6. GitHub Docs, **About Projects** – https://docs.github.com/en/issues/planning-and-tracking-with-projects/learning-about-projects/about-projects
