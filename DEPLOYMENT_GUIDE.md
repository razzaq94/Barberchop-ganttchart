# GitHub Pages Deployment Troubleshooting Guide

## Step-by-Step Fix for 404 Error

### Step 1: Check GitHub Actions Workflow Status

1. Go to your repository: https://github.com/razzaq94/Barberchop-ganttchart
2. Click on the **Actions** tab (top menu)
3. Check if there are any workflow runs:
   - If you see workflow runs, check if they completed successfully (green checkmark) or failed (red X)
   - If there are no workflow runs, the workflow hasn't been triggered yet

### Step 2: Manually Trigger the Workflow (If Needed)

1. Go to **Actions** tab
2. Click on **Deploy to GitHub Pages** workflow on the left
3. Click **Run workflow** button (top right)
4. Select your branch (usually `main` or `master`)
5. Click the green **Run workflow** button
6. Wait for it to complete (watch the progress)

### Step 3: Configure GitHub Pages Settings

**IMPORTANT: Do this AFTER the workflow has created the gh-pages branch**

1. Go to **Settings** → **Pages** in your repository
2. Under **Source**, select **Deploy from a branch**
3. Select branch: **gh-pages**
4. Select folder: **/ (root)**
5. Click **Save**

### Step 4: Verify the gh-pages Branch Exists

1. Go to your repository main page
2. Click on the branch dropdown (usually shows "main" or "master")
3. Look for a branch called **gh-pages**
4. If it doesn't exist, the workflow hasn't run successfully yet

### Step 5: Check Workflow Logs for Errors

1. Go to **Actions** tab
2. Click on the latest workflow run
3. Click on the **deploy** job
4. Expand each step to see if there are any errors
5. Common issues:
   - Permission errors
   - Branch name mismatch
   - Missing files

## Quick Fix: Alternative Simple Deployment

If the workflow continues to fail, you can manually create the gh-pages branch:

1. Make sure your code is pushed to main/master branch
2. The workflow should automatically create gh-pages branch
3. If not, check the Actions tab for error messages

## Still Not Working?

1. **Check branch name**: Make sure your default branch is `main` or `master` (the workflow listens to both)
2. **Check file location**: Ensure `index.html` is in the root directory
3. **Wait a few minutes**: GitHub Pages can take 1-5 minutes to update after deployment
4. **Clear browser cache**: Try accessing the site in incognito mode
5. **Check URL**: Make sure you're using: `https://razzaq94.github.io/Barberchop-ganttchart` (case-sensitive!)
