# Commerce for Agents

Static landing page for the Commerce for Agents hackathon and challenge series.

[Live website](https://commerce-for-agents-production.up.railway.app)

## Files

- `public/index.html` contains the page markup and styles.
- `public/logos/` contains the Topcoder, Wipro, and MIT SVG logos.
- `Caddyfile` configures the static web server.
- `Dockerfile` packages the page with Caddy.
- `railway.json` defines the Railway build and health check.

The page uses Neue Haas Grotesk loaded from the font CDN referenced in the HTML. There is no JavaScript framework, package installation, or frontend build step.

## Logo sources

- [Topcoder](https://uni-nav.topcoder.com/v1/assets/inverted-logo.svg), the inverse logo used on Topcoder's website.
- [Wipro](https://www.wipro.com/content/dam/wipro/social-icons/wipro_new_logo.svg), the logo used on Wipro's website.
- [MIT](https://brand.mit.edu/logos-marks/mit-logo), the Institute logo SVG from the official brand guide's stylesheet.

The original SVG geometry is preserved. CSS displays the Wipro and MIT marks in white against the dark background.

## Local preview

```sh
python3 -m http.server 4173 --directory public
```

Open <http://localhost:4173>.

## Deployment

Railway serves `public/` through Caddy on its assigned `PORT`, defaulting to 8080. The production service is `commerce-for-agents` in the NANDA Projects workspace.

Push changes to `main` to deploy automatically through the connected Railway service.
