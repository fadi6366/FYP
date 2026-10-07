
# 1. Project Overview

The Assistant will help users to perform their tasks. It will monitor the desktop screen while the user works. The AI model will identify the window and the task being performed and give suggestions to the user or point out any mistakes.

The assistant will include conversational interaction, personalized memory, reminders ,and an interactive desktop avatar.

# 2. Idea

The system will:

- Provide suggestions while the user is performing supported tasks.
- Monitor only a user-selected application/window.
- Detect which supported application is being used.
- Identify relevant task information from the selected application.
- Use a validation method before sending relevant information to the AI model.
- Point out detected mistakes or issues.
- Provide explanations and suggestions through the AI assistant.
- Display an interactive avatar when activated.
- Allow users to select/add different avatars.
- Allow users to chat with the assistant.
- Remember information provided by the user.
- Create one-time and recurring reminders.
- Provide a playful mode that can make occasional jokes about clear mistakes.
- Allow the user to adjust the assistant's tone.
- Allow the assistant to remain silent when it is uncertain.

## 3. Scope

### Initial Scope

The project will support a limited number of selected applications rather than attempting to support every application on a computer.

**Applications to be finalized:**

1.   
    
    Vs Code
    
2.   
    
    Microsoft word/excel/powerpoint
    
3.   
    
    ---
    

**Supported tasks to be finalized:**

1.   
    
    ---
    
2.   
    
    ---
    
3.   
    
    ---
    

The final application list and supported tasks will be selected based on technical feasibility, available validation methods, and the project's evaluation requirements.



## 4. Screen Monitoring

- The user selects a specific application/window to monitor.
- The system monitors only the selected window via screen recording.
- The system periodically captures relevant visual information from the selected window.
- The system identifies the application being used.
- Relevant information is extracted from the captured content.
- The information is passed through a validation/detection mechanism.
- Only validated/relevant information is provided to the AI model.
- Monitoring can be started or stopped by the user.

---

## 5. Validation Mechanism

A validation layer will be introduced between screen monitoring and the AI model.

### Basic Flow

User-selected application  
↓  
Screen capture  
↓  
Application/task detection  
↓  
Validation mechanism  
↓  
Validated information  
↓  
AI model  
↓  
Suggestion/explanation

The purpose of the validation layer is to reduce incorrect AI suggestions and provide measurable system performance.

**Validation method:** To be researched and finalized based on the selected applications and tasks.

---

## 6. AI Assistant

The AI assistant will:

- Understand validated task information.
- Explain detected problems.
- Provide suggestions.
- Answer user questions.
- Communicate through chat.
- Generate appropriate responses based on the user's task context.
- Stay silent when the system is not sufficiently confident.

---

## 7. Avatar System

- Avatar appears when the assistant is activated.
- Avatar can remain on the desktop while the user works.
- Avatar may have different states/animations such as sitting, standing, and walking.
- Users can select different avatars.
- Additional avatars may be added in the future.
- Avatar can display assistant messages or notifications.

---

## 8. Memory System

The assistant will have personalized memory.

Examples:

- Information the user explicitly asks it to remember.
- User preferences.
- Useful task-related information.

Memory must be separated between different user accounts.

---

## 9. Reminder System

The assistant will allow users to create:

- One-time reminders.
- Daily reminders.
- Recurring reminders.

Example:

"Remind me every day at 8 PM to study."

The reminder system will trigger a desktop notification at the appropriate time.

---

## 10. User Accounts

The system will include:

- Account creation.
- Login.
- Logout.
- Credential recovery/forgotten password functionality.
- Separate user accounts.
- Separate memory for each user.
- Separate reminders for each user.
- User-specific settings.

---

## 11. API Key

API will be added in backend. 

---

## 12. Playful Mode (Optional/maybe in future)

The assistant may have an optional playful mode.

When enabled:

- It can make occasional jokes about obvious mistakes.
- It should not make jokes when the system is uncertain.
- The user can adjust the assistant's tone.
- The user can disable playful responses.

---

## 13. Proposed Technology Stack

### Frontend / Desktop Application

- Electron.js
- React.js
- Tailwind CSS
- JavaScript

### Backend

- Node.js
- SQLite

### AI

- AI API

### Other Technologies

To be finalized after selecting the supported applications and validation methods.

---

## 14. Main System Flow

User  
↓  
Login  
↓  
Select application/window  
↓  
Start monitoring  
↓  
Application/task detection  
↓  
Validation  
↓  
AI analysis  
↓  
Suggestion / explanation  
↓  
Avatar / notification / chat

---

## 15. Research Component

The project will investigate how effectively an AI assistant can provide task assistance when AI responses are based on application-specific validated information rather than raw screen information alone.

The research component will focus on:

- Application/task detection
- Validation methods
- AI-assisted task guidance
- Error/mistake detection
- Reliability of AI suggestions
- System performance

---

## 16. Evaluation / Benchmarking

The system will be evaluated using measurable metrics.

Potential metrics:

- Precision
- Recall
- F1-score
- Accuracy, where applicable
- False positive rate
- False negative rate
- Response time, where relevant

A test set of predefined task scenarios will be created for the selected applications.

The final evaluation methodology will be determined after the validation mechanism and supported tasks are finalized.

---

## 17. Literature Review

Literature review areas:

1. AI desktop assistants
2. Intelligent personal assistants
3. Computer-use/GUI agents
4. Application and task recognition
5. Screen-based task understanding
6. Error/mistake detection
7. Application-specific validation
8. LLM-based task assistance
9. Human-computer interaction
10. AI system evaluation and benchmarking
11. Precision, recall and F1-score
12. Existing limitations and research gaps

---

## 18. Features to Consider Later

These are ideas, not confirmed requirements yet:

- More supported applications
- More avatar animations
- Additional avatar packs
- Voice interaction
- More advanced memory
- Calendar integration
- Additional productivity tools
- More assistant personalities

These should only be added if they do not interfere with the core FYP scope.

---

## 19. Important Decisions Still Pending

- [ ] Final supported applications
    
- [ ] Final supported tasks
    
- [ ] Screen capture method
    
- [ ] Application detection method
    
- [ ] Validation mechanism
    
- [ ] AI API/provider
    
- [ ] Database structure
    
- [ ] Evaluation dataset/test cases
    
- [ ] Benchmarking methodology
    
- [ ] Literature review
    
- [ ] Research gap
    
- [ ] Final project title
    
- [ ] Security method for API keys
    
- [ ] Final FYP scope