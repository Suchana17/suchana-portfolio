# Suchana Shrestha — Portfolio

A single-page, responsive portfolio for GitHub Pages.

## Publish on `suchanashrestha.com.np`

This portfolio is a static site, so GitHub Pages can host it for free. Keep this `index.html` and `CNAME` at the top level of the portfolio repository.

### 1. Create a portfolio repository

On GitHub, create a new **public** repository, for example `suchana-portfolio`. Do not initialize it with a README if you plan to push this folder as-is. The existing project repositories stay separate.

From this folder, run:

```sh
git init
git add index.html CNAME README.md
git commit -m "Create personal portfolio"
git branch -M main
git remote add origin https://github.com/Suchana17/suchana-portfolio.git
git push -u origin main
```

If you already made a repository with a different name, replace `suchana-portfolio` in the remote URL. If this folder is already a Git repository, skip `git init` and add the new GitHub remote if needed.

### 2. Turn on GitHub Pages

1. Open the new repository on GitHub and choose **Settings → Pages**.
2. Under **Build and deployment**, choose **Deploy from a branch**.
3. Select the `main` branch and `/(root)`, then save.
4. In the **Custom domain** field, enter `suchanashrestha.com.np` and save. The `CNAME` file in this folder contains the same name.

### 3. Point the domain to GitHub Pages

Sign in to the company where you registered `suchanashrestha.com.np`, open its DNS management page, and add these records. If it has default parking records for `@`, remove conflicting ones. Leave unrelated email records (MX/TXT) alone.

| Type | Host / Name | Value |
| --- | --- | --- |
| A | `@` | `185.199.108.153` |
| A | `@` | `185.199.109.153` |
| A | `@` | `185.199.110.153` |
| A | `@` | `185.199.111.153` |
| CNAME | `www` | `Suchana17.github.io` |

DNS providers may label the host field differently; `@` means the root domain. If the provider offers `ALIAS`/`ANAME`, GitHub supports those as an alternative for the root domain, but the four A records above are the common setup. Do not add a wildcard record. DNS changes can take up to 24 hours to spread.

### 4. Enable HTTPS and check the site

Return to **Settings → Pages**. After GitHub verifies the DNS records, turn on **Enforce HTTPS**. Check both `https://suchanashrestha.com.np` and `https://www.suchanashrestha.com.np` after the deployment finishes. GitHub Pages may take several minutes to publish the first time.

If HTTPS is unavailable, give DNS more time, check that no conflicting `A`, `AAAA`, or `CNAME` records remain for `@` or `www`, then revisit the Pages settings.

## Personalize before launch

- Replace the LinkedIn feed link with your public profile URL if you want visitors to land directly on your profile.
- Review the About copy and skill tags so they match how you want to introduce yourself.
- Replace the CSS project illustrations with real screenshots later if you’d like.

The domain DNS values and publishing steps follow GitHub’s [custom domain documentation](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site) and [publishing source guide](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site).
