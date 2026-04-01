# The Vault of Games

A clean and fast portal for unblocked web games.

## 🚀 How to Fix the "Built with AI Studio" Page

If you see a page that says "Built with AI Studio" instead of your app, it means GitHub is serving the wrong files. Follow these steps to fix it:

### 1. Enable GitHub Actions Deployment
1. Go to your repository **Settings** tab on GitHub.
2. Select **Pages** from the left sidebar.
3. Under **Build and deployment** > **Source**, click the dropdown and select **GitHub Actions**.
4. **Wait a few minutes** for the deployment to finish.

### 2. Why this happens
By default, GitHub Pages tries to serve the `index.html` file in your root folder. However, for this app, the real site needs to be **built** first. The GitHub Action I created automatically builds your site and tells GitHub to serve the finished version from the `dist` folder.

### 3. Trigger a fresh build
If you've already enabled GitHub Actions and it's still not working:
1. Go to the **Actions** tab in your repository.
2. Select the **Deploy static content to Pages** workflow on the left.
3. Click the **Run workflow** button.

Once the green checkmark appears, your site will be live at:
`https://<your-username>.github.io/<your-repo-name>/`

### 4. Setting up a Custom Domain (vaultofgames-v4.com)
If you want to use your own domain like `vaultofgames-v4.com`, you must link it to GitHub:
1. In your GitHub repository **Settings** > **Pages**, scroll down to **Custom domain**.
2. Type `vaultofgames-v4.com` and click **Save**.
3. **Crucial:** You must go to your domain provider (where you bought the domain) and add **DNS Records** (A records and CNAME) pointing to GitHub's servers. 
   - [Follow GitHub's official guide here](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site) to set up the IP addresses.

---

Built with React, Vite, and Tailwind CSS.
