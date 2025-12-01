# ☁️ AWS CLF-C02 Reviewer

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Status](https://img.shields.io/badge/status-stable-green.svg)
![Tech](https://img.shields.io/badge/built%20with-React%20%2B%20Tailwind-3b82f6)

A modern, high-performance web application designed to help you master the **AWS Certified Cloud Practitioner (CLF-C02)** exam. Built with a focus on **Minimalism, Speed, and User Experience**.

## ✨ Features

* **📚 Dual Study Modes:**
    * **Standard Study:** Instant feedback on every question. Perfect for learning concepts.
    * **Exam Simulation:** Timed session (90s per question) with no immediate answers. Simulates the real testing environment.
* **📊 Advanced Analytics:** Visual breakdown of your performance by exam domain (Cloud Concepts, Security, Technology, Billing) with pass/fail prediction.
* **🎨 Modern Glassmorphism UI:** A sleek, dark-mode interface using Tailwind CSS and glass-panel aesthetics that looks great on **Desktop** and **Mobile**.
* **⚡ Dynamic Question Bank:** Questions are loaded dynamically from `questions.json`. The app automatically detects the total number of questions available.
* **⌨️ Power User Shortcuts:** Navigate the entire quiz using your keyboard (Numbers `1-9` to select, `Enter` to confirm, `Backspace` to go back).
* **💾 No Backend Required:** Runs entirely in the browser using React (CDN) and Babel. Deployable anywhere static files are hosted.

## 🚀 Getting Started

Because this project uses `fetch()` to load the question database, it works best when served via a web server (like GitHub Pages or a local server) rather than opening the file directly.

### Option 1: Run Locally (Recommended)

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/mnco25/aws-reviewer.git](https://github.com/mnco25/aws-reviewer.git)
    cd aws-reviewer
    ```

2.  **Start a local server:**
    * If you have **Python** installed:
        ```bash
        python3 -m http.server
        ```
    * If you use **VS Code**:
        * Install the "Live Server" extension.
        * Right-click `index.html` and choose "Open with Live Server".

3.  Open `http://localhost:8000` (or the port shown) in your browser.

### Option 2: Deploy to GitHub Pages

1.  Go to your repository settings on GitHub.
2.  Navigate to the **Pages** section.
3.  Select `main` branch as the source.
4.  Your site will be live at `https://<your-username>.github.io/aws-reviewer/`.

## 🛠️ Customization

You can easily expand the question bank without touching the application code.

1.  Open the `questions.json` file.
2.  Add a new question object to the array following this format:

```json
{
    "id": 176,
    "c": 3,
    "q": "Which AWS service is used for...",
    "a": "Correct Answer String",
    "d": ["Wrong Answer 1", "Wrong Answer 2", "Wrong Answer 3"],
    "e": "Explanation of why the correct answer is correct."
}
````

**Key:**

  * `id`: Unique identifier (increment this number).
  * `c`: Category ID (`1`=Cloud Concepts, `2`=Security, `3`=Technology, `4`=Billing).
  * `q`: The Question text.
  * `a`: The Correct Answer (must match one of the choices exactly).
  * `d`: Distractors (incorrect answers).
  * `e`: Explanation shown after answering.

The application will **automatically** count the new questions and update the total bank size on the home screen.

## ⌨️ Keyboard Shortcuts

| Key | Action |
| :--- | :--- |
| **1 - 9** | Select Option |
| **Enter** | Submit Answer / Next Question |
| **Backspace** | Previous Question |

## 🏗️ Tech Stack

  * **Frontend Library:** [React 18](https://reactjs.org/) (via CDN)
  * **Styling:** [Tailwind CSS](https://tailwindcss.com/) (via CDN)
  * **Compiler:** [Babel](https://babeljs.io/) (Standalone)
  * **Icons:** Inline SVG icons

## 🤝 Contributing

Contributions are welcome\! If you find an error in a question or want to improve the code:

1.  Fork the Project.
2.  Create your Feature Branch (`git checkout -b feature/AmazingFeature`).
3.  Commit your Changes (`git commit -m 'Add some AmazingFeature'`).
4.  Push to the Branch (`git push origin feature/AmazingFeature`).
5.  Open a Pull Request.

## 📝 License

Distributed under the MIT License. See `LICENSE` for more information.

**Created by Marc**
