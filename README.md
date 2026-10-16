# Shorts Publisher information website

A minimal English static website for the Shorts Publisher Google OAuth branding
configuration. No build step, dependencies, JavaScript or custom domain is needed.
The public contact address matches the application's configured support email.

## Publish with GitHub Pages

1. Copy **all files in this folder**, including `.nojekyll`, into the root of a
   separate repository. Do not copy the parent video-generator project.
2. Create a public GitHub repository, for example `shorts-publisher-site`, and
   push these files to its `main` branch. Public repositories support Pages on
   GitHub Free. The repository contains only this website, not the desktop app.
3. Open the repository's **Settings > Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**, select
   **main** and **/ (root)**, then **Save**.
5. Wait for deployment. Use the actual HTTPS site URL shown on that page.
   No custom domain or CNAME file is needed. Enable **Enforce HTTPS** if offered.
6. Open Home, Privacy and Terms at the published address and check that all load.

## Google Auth Platform > Branding

Keep the app name **Shorts Publisher** and the support email
**minifablo.team@gmail.com**. A logo is not included or required by this site.

If GitHub gives you `https://USERNAME.github.io/shorts-publisher-site/`, enter:

| Branding field | Value |
| --- | --- |
| Application home page | `https://USERNAME.github.io/shorts-publisher-site/` |
| Application privacy policy link | `https://USERNAME.github.io/shorts-publisher-site/privacy.html` |
| Application terms of service link | `https://USERNAME.github.io/shorts-publisher-site/terms.html` |
| Authorized domains | `USERNAME.github.io` (no scheme or path) |

Replace USERNAME with your actual GitHub username. If your repository name differs,
use the deployed path instead. All website links are relative, so the HTML files
do not need editing for your username or repository name.

Save the branding configuration, then return to **Audience** and check whether
**Publish app** is available. A website does not guarantee Google approval or
remove separate OAuth verification or YouTube API audit requirements.

## If Google asks for site ownership verification

Use Google Search Console with the Google account that manages the Cloud project.
Add a **URL-prefix** property using your actual deployed site URL. Use the HTML
tag verification option and add Google's exact verification meta tag inside the
`<head>` of `index.html`. Commit and publish it, then select Verify. Keep the tag
in the page afterwards. Do not invent a verification value or enter `github.io`
as a domain you own. If Google asks to verify a broader URL prefix, host the
verification at that exact prefix; a tag on a project subpath cannot prove control
of a different parent URL.

## Files and maintenance

- `index.html`: public application homepage.
- `privacy.html`: data access, use, storage, sharing, retention and deletion.
- `terms.html`: personal-use conditions and platform links.
- `style.css`: shared responsive styles using system fonts.
- `.nojekyll`: serves these static files without Jekyll processing.

Review the disclosures before publication and update them if the app's actual
behavior changes. This site describes the current private YouTube upload behavior,
Windows DPAPI credential storage, local logs, and optional Meta/Buffer/Cloudinary
publishing. It does not claim Google verification or permanent token validity.
No credentials, OAuth client JSON, account configuration, logs, or videos belong
in this public repository.

Official references:
- https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site
- https://support.google.com/cloud/answer/15549049?hl=en
- https://support.google.com/webmasters/answer/9008080?hl=en
- https://developers.google.com/terms/api-services-user-data-policy
