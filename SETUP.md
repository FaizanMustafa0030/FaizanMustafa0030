# Publish your GitHub profile README

## 1. Open your profile repository

1. On GitHub, select your avatar and choose **Your profile**. The last part of that page’s address is your username.
2. Open the repository with the exact same name as your username. If it does not exist, choose **+ → New repository**, enter your username as the repository name, select **Public**, turn on **Add README**, and create the repository.
3. Check that the repository is public. GitHub displays the profile README when a nonempty `README.md` is in the root of that repository. [GitHub profile README requirements](https://docs.github.com/en/account-and-profile/how-tos/profile-customization/managing-your-profile-readme)

## 2. Add the files

### Using the GitHub website

1. Open the profile repository. Choose **Add file → Upload files**, then drag the local `assets` folder onto the upload area. Check that the uploaded paths start with `assets/` and include both banners and the `assets/icons/` folder. Commit the upload. [GitHub file upload instructions](https://docs.github.com/en/repositories/working-with-files/managing-files/adding-a-file-to-a-repository)
2. Open the top-level `README.md` and click the pencil icon. Replace its contents with the contents of the local `README.md`. If the file is missing, choose **Add file → Create new file** and name it `README.md`.
3. Select **Preview**, then commit the README to the default branch. Return to **Your profile** to check the banner, icons, and project tables.

### Using Git

Install Git if needed. On the profile repository page, choose **Code → HTTPS** and copy the clone URL. In your terminal, run these commands, replacing the example username `octocat` with your own.

```shell
git clone https://github.com/octocat/octocat.git
cd octocat
```

Copy the local `README.md` and the entire `assets` folder into that cloned folder. Then run these commands from inside the clone.

```shell
git status --short
git add README.md assets/
git diff --cached --stat
git commit -m "Redesign GitHub profile README"
git push
```

Open your GitHub profile after the push and check the rendered result. Try a narrow window and both GitHub themes. `SETUP.md` is a local guide. Publish `README.md` and `assets/` for the profile itself.

## 3. Add contact badges when your links are ready

The following destinations are still needed. Copy the public addresses from your own profiles and check that they open the intended pages. For email, choose an address you want to share publicly.

| Badge | Destination to supply | Local badge |
| --- | --- | --- |
| LinkedIn | Public LinkedIn profile URL | `assets/icons/contact-linkedin.svg` |
| Upwork | Public Upwork freelancer profile URL | `assets/icons/contact-upwork.svg` |
| Personal Portfolio | Public portfolio homepage URL | `assets/icons/contact-portfolio.svg` |
| Email | Public contact email in the form `mailto:you@your-domain` | `assets/icons/contact-email.svg` |

Once you have at least one destination, add a `## Connect With Me` heading at the end of `README.md`. Copy the relevant lines below and replace the uppercase destination with the full URL or `mailto:` link. Add each badge only after its destination is ready.

```markdown
[![LinkedIn](assets/icons/contact-linkedin.svg)](YOUR_LINKEDIN_URL)
[![Upwork](assets/icons/contact-upwork.svg)](YOUR_UPWORK_URL)
[![Personal Portfolio](assets/icons/contact-portfolio.svg)](YOUR_PORTFOLIO_URL)
[![Email](assets/icons/contact-email.svg)](YOUR_MAILTO_LINK)
```

Preview the new section and click through each badge after committing the change.

## Asset sources

The banners and contact badges were created for the profile. Technology artwork includes locally stored [Devicon v2.17.0](https://github.com/devicons/devicon/releases/tag/v2.17.0) logos and custom icons for data and testing tools. The Devicon notice is included in `assets/icons/DEVICON-LICENSE.txt`.
