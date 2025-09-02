# Charlie Marshak's Website

Personal website built with Hugo and the hugo-coder theme.

## Local Development

First install `hugo` via `homebrew` (`brew install hugo`) or `mamba` (`mamba install hugo`).

To run the website locally and ensure it matches the live deployment:

1. **Initialize and update the theme submodule:**
   ```bash
   git submodule update --init --remote themes/hugo-coder
   ```

2. **Start the local development server:**
   ```bash
   hugo serve
   ```

3. **Access the website:**
   Open your browser to `http://localhost:1313`

## Important Notes

- The deployment workflow automatically updates the hugo-coder theme to the latest version using `--remote` flag
- If your local site looks different from the live site, run step 1 above to update your local theme to match the deployed version
- The site deploys automatically via GitHub Actions when changes are pushed to the main or dev branches

## Hugo Version Requirements

The latest hugo-coder theme requires Hugo v0.124.0 or higher. If you encounter template errors:

1. **Check your Hugo version:**
   ```bash
   hugo version
   ```

2. **Update Hugo if needed:**
   ```bash
   brew upgrade hugo
   ```

3. **Alternative - Use compatible theme version:**
   If you prefer to keep your current Hugo version, you can use an older theme commit:
   ```bash
   cd themes/hugo-coder
   git checkout 2fa8ce9  # Last commit compatible with Hugo v0.121.0
   ```

## Build for Production

To build the site for production:

```bash
hugo --minify
```

The generated files will be in the `public/` directory.