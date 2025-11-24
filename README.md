# Hydrogen Energy Presentation

To start the slide show:

- `pnpm install`
- `pnpm dev`
- visit <http://localhost:3030>

Edit the [slides.md](./slides.md) to see the changes.

Learn more about Slidev at the [documentation](https://sli.dev/).

## Deploy

### Netlify

1. Install Netlify CLI:
   ```bash
   npm install -g netlify-cli
   ```

2. Build and deploy:
   ```bash
   npm run deploy:netlify
   ```

   Or step by step:
   ```bash
   npm run build
   netlify deploy
   ```

### Vercel

1. Install Vercel CLI:
   ```bash
   npm install -g vercel
   ```

2. Build and deploy:
   ```bash
   npm run deploy:vercel
   ```

   Or step by step:
   ```bash
   npm run build
   vercel deploy
   ```

### Cloudflare Pages

#### Method 1: Using Wrangler CLI

1. Install Wrangler globally:
   ```bash
   npm install -g wrangler
   ```

2. Build and deploy:
   ```bash
   npm run deploy:cf
   ```
   
   Or step by step:
   ```bash
   npm run build
   wrangler pages deploy
   ```

#### Method 2: Git Deployment

If you want to deploy to Cloudflare Pages with a Git workflow:

1. Push your project to a GitHub/GitLab repository
2. Go to the Cloudflare Dashboard > Workers & Pages > Create Application > Pages > Connect to Git
3. Select your repository
4. Configure the build settings:
   - Framework preset: None
   - Build command: `npm run build`
   - Build output directory: `dist`
5. Click "Save and Deploy"

> Note: You may need to add environment variables in Cloudflare Pages settings:
> - NODE_VERSION: 20
