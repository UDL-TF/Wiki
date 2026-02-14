# Deployment Instructions

This document explains how to deploy the Markdown Guide to wiki.udl.tf.

## GitHub Pages Setup

After merging this PR to the `main` branch, you need to enable GitHub Pages in the repository settings:

1. Go to repository **Settings** → **Pages**
2. Under **Source**, select **GitHub Actions**
3. The workflow will automatically build and deploy the site

## Custom Domain Configuration

To make the site accessible at `wiki.udl.tf`:

1. In repository **Settings** → **Pages** → **Custom domain**, enter: `wiki.udl.tf`
2. Configure your DNS provider to point `wiki.udl.tf` to GitHub Pages:
   - Add a CNAME record: `wiki.udl.tf` → `udl-tf.github.io`
   - Or add A records pointing to GitHub's IPs:
     - 185.199.108.153
     - 185.199.109.153
     - 185.199.110.153
     - 185.199.111.153

3. Wait for DNS propagation (can take up to 48 hours, but usually much faster)
4. Check **Enforce HTTPS** in the Pages settings for secure access

## Automatic Deployment

The GitHub Actions workflow (`.github/workflows/deploy.yml`) will:

- Run automatically on every push to `main`
- Build the MkDocs site
- Deploy it to GitHub Pages
- Make it available at the configured domain

## Manual Deployment

If you need to manually trigger a deployment:

1. Go to **Actions** tab in the repository
2. Select the "Deploy MkDocs to GitHub Pages" workflow
3. Click **Run workflow** → **Run workflow**

## Verification

After deployment, verify the site is accessible at:
- https://wiki.udl.tf (custom domain)
- https://udl-tf.github.io/Wiki (GitHub Pages default URL)

## Troubleshooting

- **Site not updating**: Check the Actions tab for workflow errors
- **404 errors**: Ensure GitHub Pages is enabled and using GitHub Actions as source
- **Custom domain not working**: Verify DNS records are correctly configured
- **Build failures**: Check the workflow logs for Python or MkDocs errors
