# Admin panel setup (one time, about 20 minutes)

Your site has an admin panel at **www.noxussystems.in/admin**. You sign in, edit text and
photos in a simple form, press Save, and the website updates by itself in about a minute.

It works through a free GitHub account that stores your site files. Netlify rebuilds the site
whenever you save.

## 1. Make a GitHub account and repository
1. Go to github.com and create a free account. Turn on two-step login.
2. Click **New repository**. Name it `noxus-site`. Choose **Private**. Create it.
3. On the new repository page click **uploading an existing file**.
4. Open this folder on your computer, select everything inside it (files and folders) and drag
   it into the page. Click **Commit changes**.

## 2. Tell the admin panel your GitHub name
1. In the repository open `admin` then `config.yml` and click the pencil (edit) icon.
2. Change `YOUR-GITHUB-USERNAME/noxus-site` to your real username, for example `noxus-systems/noxus-site`.
3. Click **Commit changes**.

## 3. Connect Netlify to GitHub
1. In Netlify choose **Add new site, Import an existing project, GitHub**, and pick `noxus-site`.
2. Leave the build command empty. Set the publish directory to `.` (a single dot). Deploy.
3. Move your domain to this new site (Domain management, Add a domain). The GoDaddy DNS
   records stay the same. Remove the domain from the old manual site first.
4. Set up the enquiry email again: Forms, Form notifications, Email notification.

## 4. Make your sign-in token
1. On GitHub open Settings, Developer settings, Personal access tokens, **Fine-grained tokens**, **Generate new token**.
2. Name it "NOXUS admin". Set the expiry (up to one year).
3. Repository access: **Only select repositories**, then `noxus-site`.
4. Permissions, Repository permissions: **Contents: Read and write**. Nothing else.
5. Generate, and copy the token. You only see it once.

## 5. Use the admin panel
1. Open www.noxussystems.in/admin and click **Sign In Using Access Token**. Paste the token.
2. Choose what to edit: Site text and contact, Services, Project photos, Questions and answers, Service areas.
3. Change things and press **Save**. Wait about a minute, then refresh the website.

## Safety
- The token is your password. Do not share it or post it. If it is lost, delete it on GitHub and make a new one.
- Anyone who needs to edit needs their own GitHub account, added as a collaborator on the repository, and their own token.
- Resize photos to about 1600 pixels wide before uploading so the site stays fast.

## What the admin panel can and cannot change
It can change: the hero text, phone, WhatsApp number, email, address, Google Maps link,
all services, project photos, FAQ answers and service areas.
It cannot change: the Terms & Conditions text, the section headings, the "support" panels and the
four "how we work" steps. Ask for those changes, or edit `index.html` and `terms.html` in GitHub.
Note: the "Find your setup" guide uses service names to pick suggestions. If you rename a service,
that suggestion may no longer match it.
