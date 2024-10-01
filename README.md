# django-tutorial.dev

# Contributing to Django Tutorials

Thank you for considering contributing to this repository! 🎉 This repository contains documentation and tutorials related to Django, and all contributions will be added to the [django-tutorial.dev](https://django-tutorial.dev) website, which aims to teach Django in simple language and conceptual terms to new developers.

## Hacktoberfest Participation 🎃
We are proudly participating in Hacktoberfest! If you are new to open source or want to contribute, you are more than welcome to join us. Follow the steps below to start contributing.

## DO NOT REMOVE THE GITIGNORE,CONTRIBUTING,README & OTHER'S CONTENTS
### Contribution Guidelines

1. **Create a Folder for Each Tutorial/Documentation**  
   - For each new topic or Django-specific concept, create a new folder named after the tutorial or topic.
   - Within this folder, create a `main.html` file where you will place the content for the main topic.
   
   **Example:**
```
tutorials/
└── views/
    ├── main.html  # Main topic (Views in Django)
    ├── function-based.html  # Subtopic: Function-based Views
    └── class-based.html  # Subtopic: Class-based Views
```

3. **Organizing Subtopics**  
- If your tutorial or documentation has subtopics, create multiple `.html` files for each subtopic inside the same folder.
- Ensure that each subtopic file is descriptive and follows the naming format: `<name-of-subtopic>.html`.
- Link the subtopic `.html` files from the `main.html` file for easy navigation.

3. **Markdown for Readability**  
- If you'd like to include Markdown for ease of readability and formatting before converting to HTML, ensure that you use it properly. Tools such as Markdown to HTML converters can help with this process.

### Code Style and Content Requirements

- Use **simple language** and **clear explanations** to help new developers understand complex concepts.
- Where possible, link to relevant official Django documentation to support your explanations.
- Include **code snippets** inside `<code>` tags, ensuring they are properly indented and easy to follow.
- Avoid advanced jargon unless it's essential to the topic, and provide explanations for any technical terms.

### Submitting Your Contribution

1. **Fork the Repository**  
Create a fork of this repository by clicking the "Fork" button in the upper right corner. This creates a copy of the repository under your GitHub account.

2. **Clone Your Fork**  
Clone your fork to your local machine:
```git clone https://github.com/your-username/django-tutorials.git```

3. **Create a New Branch**  
Before you start working on your changes, create a new branch for your feature or fix:
```git checkout -b your-branch-name```

4. **Make Your Changes**  
Add your folder, content, and HTML files. Make sure to follow the guidelines mentioned above.

5. **Commit Your Changes**  
After making your changes, stage them and commit:
```
git add .
git commit -m "Add tutorial for <topic>"
```

6. **Push to GitHub**  
Push your changes to your GitHub repository:
``` git push origin your-branch-name ```


7. **Create a Pull Request**  
Go to your fork on GitHub, and click the "New Pull Request" button. Provide a meaningful title and description of your changes.

### Hacktoberfest Tips
- Ensure your pull request adheres to Hacktoberfest's quality standards.
- If your pull request is valid and helpful, it will be labeled with `hacktoberfest-accepted`.

### Reviewing Process

- Your pull request will be reviewed for content quality, accuracy, and adherence to the guidelines.
- Feedback will be provided for any necessary changes.
- Once approved, your contribution will be merged into the repository.

### Getting Help

If you need any help while contributing, feel free to open an issue or reach out by creating a discussion thread. We are here to support new contributors!

---

Thank you for contributing and making Django learning easier for everyone! 🙌
