# PaperBright Text Editor

PaperBright is a focused Astro text editor with local live-save, custom font upload, export/import, and optional Google Drive live-save.

## Local Development

```sh
npm install
npm run dev
```

## Build

```sh
npm run build
npm run preview
```

## Google Drive Login

PaperBright uses Google Identity Services in the browser and Drive API `drive.file` scope. To enable the public **Sign in with Google** button:

1. In Google Cloud Console, create an OAuth 2.0 Client ID.
2. Choose **Web application**.
3. Add this authorized JavaScript origin:

```text
https://paperbright.vercel.app
```

4. Add this authorized redirect URI:

```text
https://paperbright.vercel.app/
```

5. For local testing, also add these JavaScript origins:

```text
http://localhost:4321
http://127.0.0.1:4322
```

6. For local redirect testing, also add these redirect URIs:

```text
http://localhost:4321/
http://127.0.0.1:4322/
```

7. Enable the Google Drive API for the same Google Cloud project.
8. In Vercel, add this environment variable for Production:

```text
PUBLIC_GOOGLE_CLIENT_ID=your-oauth-client-id.apps.googleusercontent.com
```

9. Redeploy the Vercel project.

The OAuth Client ID is public browser configuration, not a client secret. Do not add a Google OAuth client secret to this app.

## Vercel

The app is static and deploys normally on Vercel. If the production site shows `Setup required` beside Google Drive, the `PUBLIC_GOOGLE_CLIENT_ID` environment variable is missing from the deployed build.
