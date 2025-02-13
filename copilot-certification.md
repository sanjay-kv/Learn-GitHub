# GitHub Copilot Exam Preparation Study Guide

Get ready for the **GitHub Copilot Certification Exam** with this comprehensive study guide. It contains essential resources, learning objectives, and best practices to help you succeed.

Small documentation on tips and tricks of GitHub Copilot
![2024-11-04_0-10-07](https://github.com/user-attachments/assets/34db8182-e864-49a5-b7cb-43702e87e657)


## Objective Domains

The exam covers specific domains that assess your understanding and skills in using GitHub Copilot effectively. Each domain focuses on different aspects of GitHub Copilot, and the breakdown of exam coverage is as follows:

## Domain Breakdown

| Domain                                         | Exam Percentages |
|------------------------------------------------|-------------------|
| Domain 1: Responsible AI                       | 7%               |
| Domain 2: GitHub Copilot plans and features    | 31%              |
| Domain 3: How GitHub Copilot works and handles data | 15%      |
| Domain 4: Prompt crafting and Prompt engineering | 9%           |
| Domain 5: Developer use cases for AI           | 14%              |
| Domain 6: Testing with GitHub Copilot          | 9%               |
| Domain 7: Privacy fundamentals and context exclusions | 15%     |

Each domain includes a set of topics and learning objectives designed to prepare you for the exam.

## Audience Profile

This certification is ideal for professionals in software development, such as developers, administrators, and project managers, who use GitHub and have foundational knowledge of GitHub Copilot's capabilities. It is recommended to have hands-on experience with GitHub Copilot to enhance your understanding of exam topics.

## Recommendations and Best Practices

To increase your chances of passing the exam:
- Familiarize yourself with GitHub and GitHub Copilot features.
- Follow the recommended learning paths and complete hands-on exercises.
- Use the assessment questions provided to test your knowledge.

## Study Resources

These resources offer a structured path for learning GitHub Copilot's functionalities and preparing for the exam:

### Microsoft Learn
Microsoft Learn provides comprehensive modules for mastering GitHub Copilot:
- **[GitHub Copilot Fundamentals](https://learn.microsoft.com/en-us/training/paths/copilot/)**: Understand the basics of AI-powered assistance in coding.
- **[Accelerate App Development by Using GitHub Copilot](https://learn.microsoft.com/en-us/training/paths/accelerate-app-development-using-github-copilot/)**: Learn how to integrate GitHub Copilot into your development workflows.

### LinkedIn Learning
(Coming soon) A video-based learning path on LinkedIn Learning will provide additional resources to enhance your coding efficiency and knowledge of GitHub Copilot.

## Domain Summaries
# GitHub Copilot Certification Study Guide

## Domain 1: Responsible AI

### Explain responsible usage of AI
| Topic | Description |
|-------|-------------|
| Describe the risks associated with using AI | Understand the potential risks in AI usage |
| Explain the limitations of using generative AI tools | Explore issues like data depth, model bias, and data source limitations |
| Explain the need to validate the output of AI tools | Understand why it is important to verify AI outputs |
| Identify how to operate a responsible AI | Learn practices to use AI responsibly |
| Identify the potential harms of generative AI | Address concerns such as bias, secure code, fairness, privacy, and transparency |
| Explain how to mitigate the occurrence of potential harms | Discuss strategies to minimize AI-related risks |
| Explain ethical AI | Understand and apply ethical principles in AI usage |

---

## Domain 2: GitHub Copilot Plans and Features

### Identify the different GitHub Copilot plans
| Topic | Description |
|-------|-------------|
| Understand the differences between Copilot plans | Differentiate between Copilot Individual, Business, Enterprise, and Business for non-GHE |
| Understand Copilot for non-GitHub customers | Explore the options available for non-GitHub users |
| Define GitHub Copilot in the IDE | Understand how Copilot integrates within IDEs |
| Define GitHub Copilot Chat in the IDE | Learn about the Copilot Chat feature in the IDE |
| Describe ways to trigger GitHub Copilot | Explore triggers like chat, inline chat, suggestions, and CLI |

### Identify the main features with GitHub Copilot Individual
| Topic | Description |
|-------|-------------|
| Explain differences between GitHub Copilot Individual and Business | Learn about data exclusions, IP indemnity, billing, etc. |
| Understand the available features in the IDE for Copilot Individual | Explore specific features offered in the IDE for individual users |

# GitHub Copilot Features Overview

## GitHub Copilot Business

| Feature                                       | Description |
|-----------------------------------------------|-------------|
| **Exclude Specific Files**                    | Demonstrate how to exclude specific files from GitHub Copilot. |
| **Organization-Wide Policy Management**       | Demonstrate how to establish organization-wide policy management. |
| **Organization Audit Logs**                   | Describe the purpose of organization audit logs for GitHub Copilot Business. |
| **Audit Log Event Search**                    | Explain how to search audit log events for GitHub Copilot Business. |
| **Subscription Management via REST API**      | Explain how to manage GitHub Copilot Business subscriptions via the REST API. |

---

## GitHub Copilot Enterprise

| Feature                                       | Description |
|-----------------------------------------------|-------------|
| **Benefits of GitHub Copilot Chat on GitHub.com** | Explain the benefits of using GitHub Copilot Chat on GitHub.com. |
| **Pull Request Summaries**                    | Explain GitHub Copilot pull request summaries. |
| **Knowledge Base Configuration and Usage**    | Explain how to configure and use Knowledge Bases within GitHub Copilot Enterprise. |
| **Types of Knowledge in Knowledge Bases**     | Describe the different types of knowledge that can be stored in a Knowledge Base (e.g., code snippets, best practices, design patterns). |
| **Benefits of Knowledge Bases for Code Review** | Explain the benefits of using Knowledge Bases for code completion and review (e.g., improve code quality, consistency, and efficiency). |
| **Knowledge Base Management Instructions**    | Describe instructions for creating, managing, and searching Knowledge Bases within GitHub Copilot Enterprise, including details on indexing and other relevant configuration steps. |
| **Custom Models**                             | Explain the benefits of using custom models. |

---

## GitHub Copilot Chat

| Feature                                       | Description |
|-----------------------------------------------|-------------|
| **Effective Use Cases**                       | Identify the use cases where GitHub Copilot Chat is most effective. |
| **Performance Improvement**                   | Explain how to improve performance for GitHub Copilot Chat. |
| **Limitations**                               | Identify the limitations of using GitHub Copilot Chat. |
| **Code Suggestion Options**                   | Identify the available options for using code suggestions from GitHub Copilot Chat. |
| **Feedback Submission**                       | Explain how to share feedback about GitHub Copilot Chat. |
| **Best Practices**                            | Identify the common best practices for using GitHub Copilot Chat. |
| **Slash Commands**                            | Identify the available slash commands when using GitHub Copilot Chat. |


# Domain 3: How GitHub Copilot Works and Handles Data

## GitHub Copilot Data Handling

| Feature                                       | Description |
|-----------------------------------------------|-------------|
| **Data Usage and Sharing**                    | Describe how the data in GitHub Copilot individual is used and shared. |
| **Data Flow for Code Completion**             | Explain the data flow for GitHub Copilot code completion. |
| **Data Flow for GitHub Copilot Chat**         | Explain the data flow for GitHub Copilot Chat. |
| **Input Processing for GitHub Copilot Chat**  | Describe the different types of input processing for GitHub Copilot Chat (types of prompts it was designed for). |

---

## Data Pipeline Lifecycle of GitHub Copilot Code Suggestions in the IDE

| Feature                                       | Description |
|-----------------------------------------------|-------------|
| **Code Suggestion Lifecycle Visualization**   | Visualize the lifecycle of a GitHub Copilot code suggestion. |
| **Context Gathering**                         | Explain how GitHub Copilot gathers context. |
| **Prompt Building**                           | Explain how GitHub Copilot builds a prompt. |
| **Proxy Service and Filters**                 | Describe the proxy service and the filters each prompt goes through. |
| **Model Response Production**                 | Describe how the large language model produces its response. |
| **Post-Processing**                           | Explain the post-processing of GitHub Copilot’s responses through the proxy server. |
| **Code Matching Identification**              | Identify how GitHub Copilot identifies matching code. |

---

## Limitations of GitHub Copilot (and LLMs in General)

| Feature                                       | Description |
|-----------------------------------------------|-------------|
| **Effect of Seen Examples**                   | Describe the effect of most seen examples on the source data. |
| **Age of Code Suggestions**                   | Describe the age of code suggestions (how old and relevant the data is). |
| **Reasoning and Context vs. Calculations**    | Describe the nature of GitHub Copilot providing reasoning and context from a prompt vs. calculations. |
| **Limited Context Windows**                   | Describe limited context windows. |

# GitHub Copilot: Prompt Crafting, Engineering, and Developer Use Cases

## Fundamentals of Prompt Crafting

| Feature                                       | Description |
|-----------------------------------------------|-------------|
| **Context Determination**                     | Describe how the context for the prompt is determined. |
| **Language Options**                          | Describe the language options for prompting GitHub Copilot. |
| **Prompt Structure**                          | Describe the different parts of a prompt. |
| **Role of Prompting**                         | Describe the role of prompting. |
| **Zero-Shot vs. Few-Shot Prompting**          | Describe the difference between zero-shot and few-shot prompting. |
| **Chat History Usage**                        | Describe the way chat history is used with GitHub Copilot. |
| **Best Practices for Prompt Crafting**        | Identify prompt crafting best practices when using GitHub Copilot. |

---

## Fundamentals of Prompt Engineering

| Feature                                       | Description |
|-----------------------------------------------|-------------|
| **Prompt Engineering Principles**             | Explain prompt engineering principles, training methods, and best practices. |
| **Prompt Process Flow**                       | Describe the prompt process flow. |

---

# Domain 5: Developer Use Cases for AI

## Improve Developer Productivity

| Feature                                       | Description |
|-----------------------------------------------|-------------|
| **AI for Developer Productivity**             | Describe how AI can improve common use cases for developer productivity, such as: <ul><li>Learning new programming languages and frameworks</li><li>Language translation</li><li>Context switching</li><li>Writing documentation</li><li>Personalized context-aware responses</li><li>Generating sample data</li><li>Modernizing legacy applications</li><li>Debugging code</li><li>Data science</li><li>Code refactoring</li></ul> |
| **SDLC Management**                           | Discuss how GitHub Copilot can help with SDLC (Software Development Lifecycle) management. |
| **Limitations of GitHub Copilot**             | Describe the limitations of using GitHub Copilot. |
| **Productivity API**                          | Describe how to use the productivity API to see how GitHub Copilot impacts coding. |

# Domain 6: Testing with GitHub Copilot

| Topic | Description |
|-------|-------------|
| **Describe the options for generating testing for your code** | |
| Describe how GitHub Copilot can be used to add unit tests, integration tests, and other test types to your code | |
| Explain how GitHub Copilot can assist in identifying edge cases and suggesting tests to address them | |
| **Enhance code quality through testing** | |
| Describe how to improve the effectiveness of existing tests with GitHub Copilot’s suggestions | |
| Describe how to generate boilerplate code for various test types using GitHub Copilot | |
| Explain how GitHub Copilot can help write assertions for different testing scenarios | |
| **Leverage GitHub Copilot for security and performance** | |
| Describe how GitHub Copilot can learn from existing tests to suggest improvements and identify potential issues in the code | |
| Explain how to use GitHub Copilot Enterprise for collaborative code reviews, leveraging security best practices, and performance considerations | |
| Explain how GitHub Copilot can identify potential security vulnerabilities in your code | |
| Describe how GitHub Copilot can suggest code optimizations for improved performance | |

# Domain 7: Privacy fundamentals and context exclusions

| Topic | Description |
|-------|-------------|
| **Describe the different SKUs for GitHub Copilot** | |
| Describe the different SKUs and the privacy considerations for GitHub Copilot | |
| Describe the different code suggestion configuration options on the organization level | |
| Describe the GitHub Copilot Editor config file | |
