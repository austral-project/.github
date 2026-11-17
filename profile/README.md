<p align="center">
  <a href="https://austral.dev"><strong>Austral</strong></a><br>
  Modular back office and CMS for Symfony
</p>

<p align="center">
  <a href="https://austral.dev">Website</a> ·
  <a href="https://github.com/austral-project/skeleton">Start a project</a> ·
  <a href="https://github.com/austral-project/.github/blob/master/CONTRIBUTING.md">Contribute</a>
</p>

---

Austral is a set of **open source (MIT)** Symfony bundles to build a back office, a multilingual and multi-domain website, and pages made of content blocks. Each bundle has its own repository and can be installed on its own; they are released together, with the same version number.

## Getting started

```bash
composer create-project austral/skeleton my-project "^4.0"
```

## Maintained versions

| Version | Symfony | PHP | Branch | Status |
|---------|---------|-----|--------|--------|
| **4.x** | 7.4 LTS | ≥ 8.2 | `4.x` | Active development |
| 3.1 | 5.4 / 6.4 | ≥ 8.0 | `3.1` | Security fixes only |
| 3.0 | 5.4 | ≥ 8.0 | `3.0` | No longer maintained |

## The bundles

| Layer | Bundles |
|-------|---------|
| Contracts | [contracts](https://github.com/austral-project/contracts) |
| Core | [tools-bundle](https://github.com/austral-project/tools-bundle) · [entity-bundle](https://github.com/austral-project/entity-bundle) |
| Entity capabilities | [entity-file-bundle](https://github.com/austral-project/entity-file-bundle) · [entity-translate-bundle](https://github.com/austral-project/entity-translate-bundle) · [http-bundle](https://github.com/austral-project/http-bundle) · [elastic-search-bundle](https://github.com/austral-project/elastic-search-bundle) · [cache-bundle](https://github.com/austral-project/cache-bundle) |
| Back office | [form-bundle](https://github.com/austral-project/form-bundle) · [list-bundle](https://github.com/austral-project/list-bundle) · [filter-bundle](https://github.com/austral-project/filter-bundle) · [design-bundle](https://github.com/austral-project/design-bundle) · [security-bundle](https://github.com/austral-project/security-bundle) · [admin-bundle](https://github.com/austral-project/admin-bundle) |
| Features | [seo-bundle](https://github.com/austral-project/seo-bundle) · [content-block-bundle](https://github.com/austral-project/content-block-bundle) · [graphic-items-bundle](https://github.com/austral-project/graphic-items-bundle) · [social-network-bundle](https://github.com/austral-project/social-network-bundle) · [email-bundle](https://github.com/austral-project/email-bundle) · [notify-bundle](https://github.com/austral-project/notify-bundle) |
| Website | [website-bundle](https://github.com/austral-project/website-bundle) |
| Tools | [skeleton](https://github.com/austral-project/skeleton) · [maker-bundle](https://github.com/austral-project/maker-bundle) |

## Docker images

Ready-to-use images for Austral projects, published on Docker Hub under [`australproject`](https://hub.docker.com/u/australproject). One Git branch = one image tag.

| Image | Purpose | Tags |
|-------|---------|------|
| [docker-php](https://github.com/austral-project/docker-php) | PHP-FPM, configured with environment variables, root or any UID/GID | `8.4` (default), `8.2`, `8.1`… |
| [docker-nginx](https://github.com/austral-project/docker-nginx) | Nginx for PHP-FPM or static/SPA sites, Brotli, error pages | `1.28` (default), `1.26`… |
| [docker-image-optimizer](https://github.com/austral-project/docker-image-optimizer) | HTTP service converting images to WebP, AVIF, MozJPEG, OxiPNG | `sharp` (default), `squoosh` |
| [docker-alpine](https://github.com/austral-project/docker-alpine) | Alpine base image used by the images above | `3.23` (default)… |

## Security

Found a vulnerability? Do not open a public issue: use the **"Report a vulnerability"** button in the *Security* tab of the repository concerned (see the [security policy](https://github.com/austral-project/.github/blob/master/SECURITY.md)).
