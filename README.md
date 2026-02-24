# ieee-web-recruitment-2026

Welcome to the technical assessment for the IEEE Web Resources chapter. This repository serves as the base for your recruitment tasks. Please follow the instructions carefully.

## 📌 Submission Guidelines
- **Deadline:** 26-02-2026
- **Deliverables:**
    1. A link to your own GitHub repository containing the code for Tasks 1, 2, and 3.
    2. A link to your successfully opened Pull Request for Task 4 in this repository.

---

##  Task 1: Frontend & UI Challenge (The "IEEE Event Card")
**Goal:** Build a clean, responsive "Upcoming Event" card.

- **Requirements:**
    - Create a card containing a placeholder image, title, date, and a "Register Now" button.
    - **Functionality:** The layout must be perfectly responsive on mobile devices using Flexbox or CSS Grid.
    - **Enhancement:** Add a hover effect that reveals a short event description. Use React and Tailwind CSS, make the button trigger a simple personalized alert.

---

##  Task 2: Backend Logic (The "Membership API")
**Goal:** Develop a simple REST API to manage a list of club members.

- **Requirements:**
    - **Framework:** Node.js and Express.
    - **Functionality:**
        - `GET /members`: Returns a JSON list of existing members (Name, USN, Domain).
        - `POST /members`: Adds a new member to the list with validation (USN must be exactly 10 characters).
        - `DELETE /members/:usn`: Removes a member based on their USN.
    - ** ADD-ON:** Think of all possible attributes to manage a members' detail and their hierarchy in club

---

##  Task 3: Debugging Challenge
**Goal:** Identify and fix errors in the following snippets. Provide the corrected code and a brief explanation of the bugs found in your repository's README.

### Part A: JavaScript
```javascript
function Counter() {
  let count = 0;

  const handleIncrement = () => {
    count = count + 1; 
    console.log("Count is now: " + count);
    document.getElementById('display').innerText = count;
  };

  for (var i = 0; i < 3; i++) {
    setTimeout(() => {
      console.log("Iteration: " + i); 
    }, 1000);
  }
}
```
### Part B: Express.js API
``` javascript
const express = require('express');
const app = express();

app.get('/user/:id', (req, res) => {
  try {
    const userData = fetchUserFromDB(req.params.id); 
    
    if (!userData) {
      res.status(404).send("User not found");
    }

    res.json({
      status: "success",
      data: userDate 
    });
  } catch (error) {
    res.status(500).send("Server Error: " + error.message); 
  }
});

async function fetchUserFromDB(id) {
  return { id, name: "IEEE Member" };
}
```

##  Task 4: Collaboration & Git Workflow (Mandatory)
**Goal:** Demonstrate mastery of the professional "Pull Request" workflow and team collaboration standards.

1. **Fork & Clone:** - Click the **Fork** button at the top of this repository.
   - Clone your fork locally: `git clone https://github.com/KaranSJ22/ieee-web-recruitment-2026.git`.

2. **Branching:** - Create a new branch: `git checkout -b feature/add-[YourName]`.

3. **Organization:**
   - Create a folder in the root directory named after yourself (e.g., `KaranSJ/`).
   - Inside this folder, place your solution files for **Task 1, Task 2, and Task 3**.

4. **The Change:** - Open the `members.md` file in the root directory.
   - Add your details to the table: **Name**, **Bio**, and **Technical Goal**.

5. **Commit & Push:** - Stage all changes (including your new folder): `git add .`.
   - Commit: `git commit -m "feat: add [YourName]"`.
   - Push: `git push origin feature/add-[YourName]`.

6. **Pull Request:** - Open a Pull Request back to the original repository (**KaranSJ22/ieee-web-recruitment-2026**).
   - In the description, provide a one-sentence justification for your chosen technical goal.
