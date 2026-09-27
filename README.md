# CRAFTD website

This is a Vercel-ready poster shop. `index.html` contains the public website, while `api/` provides the password-protected owner catalog and image-upload backend.

## Deploy with GitHub and Vercel

1. Create a new GitHub repository, for example `craftd-studio`.
2. Upload the complete contents of this folder — including `api/`, `package.json`, and `index.html` — to the repository root.
3. Import the GitHub repository in Vercel. Vercel deploys the site and API routes on every push to `main`.
4. In Vercel’s Storage tab, create a **Vercel Blob** store for this project. It automatically adds `BLOB_READ_WRITE_TOKEN`.
5. In **Vercel → Project Settings → Environment Variables**, add `ADMIN_PASSWORD` with a strong private password. Do not put it in GitHub.
6. Redeploy once after adding the environment variables.

## Before launch

- The custom poster form sends reference images and requests to `craftdstudio26@gmail.com` through FormSubmit. Confirm FormSubmit's first activation email once before launch. The service supports native file uploads up to 10 MB per submission.
- On the deployed website, click **Owner: add a drop**. Enter the owner password, fill in the poster details, and choose an image. Vercel Blob stores the image and the backend stores the live catalogue, so updates persist for all visitors across deployments.
- Click **Owner login** to turn editing on. You can then use **Add poster** for the ready-made shop and **Add showcase image** in “Made to get noticed.” Every poster and showcase tile gains a **Delete** button while owner editing is on; deletion removes it from the live catalogue (the unused image stays in Blob storage until you remove it from Vercel Storage).
- GitHub stores your code; Vercel Blob stores poster art and catalogue data. This is why your owner edits survive a new Vercel deployment.
- Replace the demo portfolio names and placeholder copy with real campus projects.
- `craftdstudio26@gmail.com` receives custom-poster briefs and reference images through FormSubmit. Confirm its first activation email once before launch.
- `qr-payment.png` is already included and cropped to the scannable QR only. Keep this filename and file at the repository root when uploading to GitHub. Customers must upload a payment screenshot plus their delivery address before the order request reaches your email.
