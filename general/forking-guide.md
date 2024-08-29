### Guide to Forking a Repository on GitHub

#### What is a Fork?

A **fork** is essentially a copy of a repository that you manage. Forking a repository allows you to make changes to a project without affecting the original codebase. It’s like making a photocopy of a document so you can write on it and make edits without changing the original.

When you fork a repository, you create a personal copy of it in your GitHub account. You can experiment with the code, make changes, and even propose those changes to the original project through a **pull request**.

#### Why Fork a Repository?

In a classroom or collaborative environment, forking allows each student or contributor to:
- **Experiment** with the code without affecting the original project.
- **Practice** their coding skills in a safe, personal space.
- **Contribute** back to the original project by suggesting changes.

#### How to Fork the `solid-garbanzo` Repository

Here’s a step-by-step guide on how to fork a repository:

##### 1. **Sign in to GitHub**
   - Go to [GitHub](https://github.com) and sign in with your account. If you don’t have an account, you’ll need to create one.

##### 2. **Find the `solid-garbanzo` Repository**
   - Use the GitHub search bar or follow the link provided by your instructor to find the `solid-garbanzo` repository.

##### 3. **Fork the Repository**
   - Once you’re on the `solid-garbanzo` repository page, look in the upper-right corner of the page. You’ll see a **Fork** button. 
   - Click the **Fork** button. This will create a copy of the repository in your own GitHub account.

##### 4. **Clone Your Fork**
   - After forking the repository, you’ll be redirected to your new forked repository. 
   - To work with the code on your own computer, you’ll need to **clone** the repository.
   - On your fork’s page, click the **Code** button (usually green) and copy the repository URL.
   - Open your terminal (Command Prompt, Git Bash, etc.) and run the following command:
     ```bash
     git clone <your-copied-url>
     ```
     Replace `<your-copied-url>` with the URL you copied from GitHub.

##### 5. **Make Changes in Your Fork**
   - Navigate to the cloned repository folder on your computer:
     ```bash
     cd solid-garbanzo
     ```
   - You can now edit the files in this directory using your preferred code editor.
   - After making changes, you can add and commit them:
     ```bash
     git add .
     git commit -m "Describe your changes here"
     ```
   - Push your changes back to your forked repository on GitHub:
     ```bash
     git push 
     ```

##### 6. **Creating a Pull Request**
   - If you want to suggest your changes to the original `solid-garbanzo` repository, you can create a **pull request**.
   - Go back to the original `solid-garbanzo` repository on GitHub.
   - Click the **Pull Requests** tab, then click the **New Pull Request** button.
   - Follow the instructions to compare changes from your fork with the original repository. Once ready, submit the pull request.

#### Summary

- **Forking** creates a personal copy of a repository in your GitHub account.
- **Cloning** allows you to work on the code locally on your computer.
- **Pull requests** enable you to suggest changes to the original project.


Feel free to reach out if you need any help or have questions!