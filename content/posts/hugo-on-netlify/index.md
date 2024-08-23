---
title: Hugo on Netlify
date: 2024-08-23T09:35:00.000Z
image: img_0003.jpeg
---
Hugo is a fast and flexible open source static site generator written in Go.



\#Key features

These features provide important benefits for Hugo sites, including ones built and deployed with Netlify.



Build speed. Hugo boasts near-instant build times of less than one millisecond per page. For large sites with a lot of pages, this can translate into significant time savings during site development and Netlify build and deploy processes.

Choice of themes. The Hugo ecosystem includes a wide range of premade themes for styling static content.

Robust templating. Hugo uses Go templates with html/template and text/template libraries to control templating.

Instant previews. The LiveReload tool is integrated into Hugo for a hot reloading experience during development.

URL management. Hugo has built-in support for URL manipulations and redirects.

Functions and variables. When building out templates, you can use Go functions, built-in Hugo-specific functions, and a variety of variables.

\#Netlify integration

Hugo sites on Netlify can benefit from automatic framework detection and control over Hugo version selection. They also require theme setup considerations.



\#Automatic framework detection

When you link a repository for a project, Netlify tries to detect the framework your site is using. If your site is built with Hugo, Netlify provides a suggested build command and publish directory: hugo and public. If you’re using the CLI to run Netlify Dev for a local development environment, Netlify also suggests a dev command and port: hugo server -w and 1313. You can override suggested values or set them in a configuration file instead, but automatic framework detection may help simplify the process of setting up a site on Netlify.



For manual configuration, check out the typical build settings for Hugo.



\#Hugo version

By default we’ll use the Hugo version that is preinstalled in your site’s initial build image. Because the preinstalled version may not match your local version, we recommend setting a HUGO_VERSION environment variable. You can set the variable to the version string for any released version after 0.19, for example, 0.80.0.



First, confirm your local Hugo version with hugo version.



Then add an environment variable in the Netlify UI as you set up your site or in a Netlify configuration file stored in your repository.



Follow the steps to import from an existing repository and on the Configure site and deploy step, select Add environment variables. Select New variable and then enter the key and value.
