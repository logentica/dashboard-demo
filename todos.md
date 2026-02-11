# Dashboard Demo - Implementation Tasks

## Deployment / Config
- [x] Confirm `values.yaml` matches tenant (`namespace`, ingress host, tls secret)
- [x] Confirm Plausible `data-domain` matches live domain

## Branding / Copy
- [x] Remove remaining template wording ("Simple Site", "template")
- [ ] Align dashboard page styling with site header/footer
- [ ] Replace sample blog post with dashboard-demo specific content (or remove blog)

## Health / Ops
- [x] Ensure `/health` returns 200 for ingress health checks

## Validation
- [ ] Local: `cd site && npm ci && npm run build`
- [ ] Local: run `npm run preview` and verify `/, /dashboard, /about, /blog, /health`
- [ ] Prod: verify `https://dashboard-demo.buildville.cloud` renders and analytics domain is correct
