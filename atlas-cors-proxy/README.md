# Atlas CORS Proxy

A simple Vercel serverless function to bypass CORS issues when accessing https://www.atlasdb.dev/api/chat from static websites.

## Usage

Deploy this to Vercel and make POST requests to:

```
https://<your-vercel-project>.vercel.app/api/chat
```

## Deployment

1. Go to https://vercel.com/import/git
2. Import this project from GitHub or upload manually
3. Done!

## Example Request

```js
fetch('https://<your-vercel-project>.vercel.app/api/chat', {
  method: 'POST',
  headers: {
    'Content-Type': 'application/json',
  },
  body: JSON.stringify({ message: 'Hello from atlasai.site' })
})
.then(res => res.json())
.then(data => console.log(data));
```