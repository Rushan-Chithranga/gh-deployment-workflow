# GitHub Actions Deployment to GitHub Pages

This project demonstrates the usage of GitHub Actions to automatically deploy a static website to GitHub Pages. The website consists of a simple `index.html` file with a gradient text effect, and a linked `styles.css` file for styling.

## How It Works

1. **GitHub Actions Workflow**:
   - A GitHub Actions workflow is set up to trigger whenever there are changes to the `index.html` or `styles.css` files.
   - The workflow builds the site by copying these files into the `public/` directory and deploys them to GitHub Pages.
   - The website is available at `https://<username>.github.io/gh-deployment-workflow/`.

2. **Automatic Deployment**:
   - The workflow deploys the website to GitHub Pages whenever there are changes to the `index.html` or `styles.css` files in the `main` branch.

## Files in the Repository

- **`index.html`**: The main HTML file that displays the "Hello, GitHub Actions!" text with a gradient animation.
- **`styles.css`**: The CSS file that contains styling for the `index.html` file, including the gradient text animation.
- **`.github/workflows/deploy.yml`**: The GitHub Actions workflow file that deploys the site to GitHub Pages whenever the `index.html` or `styles.css` files are changed.

## Workflow Explanation

The `deploy.yml` GitHub Actions workflow consists of the following steps:

1. **Trigger**: The workflow is triggered by changes to `index.html` and `styles.css`.
2. **Checkout code**: It checks out the repository's code.
3. **Set up GitHub Pages**: Uses the `actions/setup-pages` action to prepare the deployment to GitHub Pages.
4. **Deploy**: Copies the `index.html` and `styles.css` files to the `public/` directory and creates a `.nojekyll` file to prevent Jekyll from processing the files.
5. **Deploy to GitHub Pages**: Deploys the files to GitHub Pages, making the website live.

## How to Set Up and Use

1. **Create a new repository**:
   - Create a new GitHub repository named `gh-deployment-workflow` (or use your own name).

2. **Add files**:
   - Upload the `index.html` and `styles.css` files.
   - Create the `.github/workflows/` directory and add the `deploy.yml` GitHub Actions workflow file.

3. **Enable GitHub Pages**:
   - Go to the **Settings** of your repository.
   - Under the **Pages** section, set the source branch to `gh-pages` and save.

4. **Commit Changes**:
   - Commit and push your changes to the `main` branch.

5. **Visit Your Website**:
   - Once the workflow completes, your website will be accessible at:
   ```text
   https://<username>.github.io/gh-deployment-workflow/
   ```

### Key Sections in the README:

1. **Introduction**: Describes what the project is and how GitHub Actions is used for deployment.
2. **How It Works**: Explains the GitHub Actions workflow and how it triggers on file changes to deploy the website.
3. **Files in the Repository**: Lists and explains the key files in the repository.
4. **Workflow Explanation**: Gives a breakdown of what happens in the GitHub Actions workflow.
5. **How to Set Up and Use**: Step-by-step instructions to set up the repository, commit changes, and enable GitHub Pages.
6. **License**: Mentions licensing (if applicable).

Let me know if you'd like to add or modify any sections!
