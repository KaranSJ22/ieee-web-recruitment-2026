# ieee-web-recruitment-2026

Welcome to the technical assessment for the IEEE Web Resources chapter. This repository serves as the base for your recruitment tasks. Please follow the instructions carefully.

## 📌 Submission Guidelines
- **Deadline:** 27-02-2026 6:00 pm
- **Deliverables:**
    1. A link to your own GitHub repository containing the code for Tasks 1, 2, and 3.

---

##  Task 1: Frontend : "IEEE Chapter Team Card"
**Goal:** Go to our current ieee.ritb.in website, check for chapters page and come up with a clean , responsive "Team section" it must consists of cards.

- **Requirements:**
    - Create a card containing a placeholder image, title, chapter, and position.
    - **Functionality:** The layout must be perfectly responsive on mobile devices using Flexbox or CSS Grid.
    - **Enhancement:** Add a hover effect that reveals a short event description. Use React and Tailwind CSS maintain the same theme as current website.

---

##  Task 2: Backend Logic : "Membership API"
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
**Goal:** Complete all the tasks mentioned above create a repo in your account and push all your solutions. 
    1. add screenshot of the UI in readme.md and send us link for your solution repository. 
