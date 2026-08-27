# Pujitha AI Portfolio Assistant

## Overview

Pujitha AI Portfolio Assistant is a personal AI assistant designed to help recruiters, employers, collaborators, and visitors learn about my professional background.

It answers questions about my education, machine learning projects, research, technical skills, internship experience, and portfolio.

The assistant provides an interactive alternative to browsing a traditional static portfolio.

## Who It Is For

The assistant is primarily designed for:

- Recruiters and hiring managers
- Potential employers
- University or research contacts
- Collaborators
- Visitors interested in my AI and Machine Learning work

## How to Use

Open the Pujitha AI Portfolio Assistant and ask a question about my professional background.

Example questions:

- Tell me about Pujitha's machine learning projects.
- What is Pujitha's master's thesis about?
- What technical skills does Pujitha have?
- Tell me about Pujitha's FlyRank internship.
- What kind of AI and Machine Learning work has Pujitha completed?

The assistant responds using the information provided about my education, projects, research, experience, and technical skills.

## Architecture

The assistant follows a simple portfolio-assistant architecture:

User
↓
Personal AI Portfolio Assistant
↓
Portfolio knowledge and instructions
↓
AI-generated response
↓
User

The system is designed to keep the assistant focused on information relevant to my professional portfolio.

## V2 Evaluation Results

The second version of the Personal AI Portfolio Assistant was evaluated using eight representative questions covering personal background, education, machine learning projects, master's thesis, internship experience, technical skills, portfolio links, and unknown information.

Each response was reviewed for relevance, accuracy, grounding in the available knowledge, and appropriate handling of information that was not available.

| Test Area | Result |
|---|---|
| Personal background | Pass |
| Educational background | Pass |
| Machine learning projects | Pass |
| Master's thesis | Pass |
| FlyRank internship | Pass |
| Technical skills | Pass |
| Portfolio and GitHub | Pass |
| Unknown information / hallucination test | Pass |

**Overall result: 8/8 test cases passed (100%).**

One important improvement was made during evaluation. The initial version failed to retrieve the master's thesis information even though the information was intended to be available. I improved the knowledge base by adding a clearer and more structured thesis section and then repeated the test. The updated version correctly identified the thesis title, research focus, federated learning approaches, probability calibration, explainability, and evaluation metrics.

The assistant also passed an unknown-information test. When asked about Pujitha's experience working at Google, it correctly stated that the available information did not mention Google experience instead of inventing employment or internship details.

These results are based on eight representative test cases and should not be interpreted as proof that the assistant will always produce correct answers.

## Limitations

The assistant has several limitations:

1. It depends on the information provided in its knowledge and instructions.
2. It does not automatically know when a new project, skill, or experience is added to my portfolio.
3. Information must therefore be updated when my professional profile changes.
4. The assistant should not be treated as a replacement for reviewing the original project documentation or CV.

## AI Transparency

I built and refined this portfolio assistant with the help of AI tools, including ChatGPT and Claude. AI was used to support planning, drafting, refinement, and development of the assistant. I reviewed the generated content and checked that the information presented about my background and projects was consistent with my actual portfolio.

## Future Improvements

Future versions could include:

- A structured portfolio knowledge base
- Automatic updates when new projects are added
- More systematic evaluation of answer accuracy
- Additional recruiter-focused questions
- Improved integration with the personal portfolio website
