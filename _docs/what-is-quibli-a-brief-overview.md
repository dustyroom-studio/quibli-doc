---
title: "What Is Quibli? A Brief Overview"
permalink: /
excerpt: "What is Quibli? How it differs from Flat Kit?"
toc: true
---



## Quibli and Flat Kit Comparison Chart

| Asset | **Quibli** | **Flat Kit**
| --- | --- | --- |
| In short | Everything you need to achieve a stylized look of traditional japanese animation | Everything you need to achieve any variation of minimal or toon shading |
| Shaders included | Stylized Lit, Cloud2D, Light Beam, Gradient Skybox, Stylized Grass | Stylized Surface, Stylized Surface with Outline, Terrain, Water, Light Beam, Gradient Skybox |
| Mobile friendliness | Yes | Yes |
| Outlines (shader-based) | No | Yes |
| Outlines (post effect) | No | Yes, [Outline Image Effect](https://flatkit.dustyroom.com/#42-outline-image-effect) |
| Fog (post effect) | No | Yes, [Fog Image Effect](https://flatkit.dustyroom.com/#41-fog-image-effect) |
| Stylized Detail (post effect) | Yes | No |
| Independent per-step color gradient | Yes | No |
| Number of possible independent shade colors per material | **8** (in any desirable degree of smoothness) | **3** (Using _Base color_ and 2 _additional cel layers_) |
| Real-time Gradient editor | Yes | No (‘Steps’ and ‘Curve’ modes require saving color info into offline internal textures) |
| Wind | Yes | No |
| Skybox shader | Yes, with **up to 8 color multi-stop gradient** color editor | Yes, with **2 colors** interpolation |
| Light Plane shader | Yes, called _Light Beam_, a more advanced version of a Light Plane shader | Yes |
| SRP batching | Yes | No |
| Pipelines support | URP | URP, Built-In RP LTS |
| Textures support (maps) | Albedo, Normal, Detail | Albedo, Normal, Emission |
| Additional tools | Wire Renderer, Foliage Generator | [UV Scroller](https://flatkit.dustyroom.com/#51-uv-scroller), CameraMouse Orbit, [Linear Motion](https://flatkit.dustyroom.com/#52-linear-motion), [Buoyancy](https://flatkit.dustyroom.com/#53-buoyancy) |




## What Is Included in Quibli?

{% include mermaid.html %}
<div class="mermaid">
graph TD
A[Quibli] --> B(Shaders)
A --> C(Post Effects)
A --> D(Additional Tools)
A --> E(Demo Scenes)
B --> G[Stylized Lit Shader]
G --> H[Cloud2D Shader]
H --> I[Light Beam Shader]
I --> J[Skybox Shader]
J --> K[Foliage Shader]
K --> L[Stylized Grass Shader]
C --> M[Stylized Detail Post Effect]
D --> N[Wire Renderer]
N --> O[Foliage Generator]
E -->|with all models + materials| P[Nature Scene]
P --> Q[City Scene]
Q --> R[Kitchenware Scene]
R --> S[Mugs Scene]
S --> T[Unity Default Sample Scene Quiblified Scene]
T --> U[Clouds Scene]


</div>


**TIP.** It is convenient to use presets with _Foliage Generator_: every time you export a nice model, save the parameters for later. After changing everything up on the _Foliage Generator_ interface you can always load a preset (preferably previously titled in a proper way) to fix that bush that bothers you. Because the preset, whose _Carrier Mesh_, _Particle Mesh_ and _Export Parameters_ are loaded but not altered, will not create a new separate mesh, but overwrite and update the model that was created earlier (if it was already created).  
{: .notice--info}

**NOTE.** If you turn off the ‘cast shadows’ option in the foliage model’s Mesh Renderer, the self-shadowing would be also turned off. It is the way the Universal RP works — in URP you cannot make the object cast a shadow onto other objects but not on itself. But there is a workaround (read the tip below).  
{: .notice--warning}




**If you enjoy this theme, please consider [sponsoring me](https://github.com/sponsors/mmistakes) to continue developing and maintaining it.**

[!["Buy Me A Coffee"](https://user-images.githubusercontent.com/1376749/120938564-50c59780-c6e1-11eb-814f-22a0399623c5.png)](https://www.buymeacoffee.com/mmistakes)

[![Support via PayPal](https://cdn.jsdelivr.net/gh/twolfson/paypal-github-button@1.0.0/dist/button.svg)](https://www.paypal.me/mmistakes)
{: style="margin-top: 0.5em;"}

## Installing the theme

If you're running Jekyll v3.7+ and self-hosting you can quickly install the theme as a Ruby gem.

[^structure]: See [**Structure** page]({{ "/docs/structure/" | relative_url }}) for a list of theme files and what they do.

**ProTip:** Be sure to remove `/docs` and `/test` if you forked Minimal Mistakes. These folders contain documentation and test pages for the theme and you probably don't want them littering up your repo.
{: .notice--info}

**Note:** The theme uses the [jekyll-include-cache](https://github.com/benbalter/jekyll-include-cache) plugin which will need to be installed in your `Gemfile` and added to the `plugins` array of `_config.yml`. Otherwise you'll throw `Unknown tag 'include_cached'` errors at build.
{: .notice--warning}

### Gem-based method

With Gem-based themes, directories such as the `assets`, `_layouts`, `_includes`, and `_sass` are stored in the theme’s gem, hidden from your immediate view. This allows for easier installation and updating as you don't have to manage any of the theme files. 

To install as a Gem-based theme:

1. Add the following to your `Gemfile`:

   ```ruby
   gem "minimal-mistakes-jekyll"
   ```

2. Fetch and update bundled gems by running the following [Bundler](https://bundler.io/) command:

   ```bash
   bundle
   ```

3. Set the `theme` in your project's Jekyll `_config.yml` file:

   ```yaml
   theme: minimal-mistakes-jekyll
   ```

To update the theme run `bundle update`.

### Remote theme method

Remote themes are similar to Gem-based themes, but do not require `Gemfile` changes or whitelisting making them ideal for sites hosted with GitHub Pages.

To install as a remote theme:

1. Create/replace the contents of your `Gemfile` with the following:

   ```ruby
   source "https://rubygems.org"

   gem "github-pages", group: :jekyll_plugins
   gem "jekyll-include-cache", group: :jekyll_plugins
   ```

2. Add `jekyll-include-cache` to the `plugins` array of your `_config.yml`.

3. Fetch and update bundled gems by running the following [Bundler](https://bundler.io/) command:

   ```bash
   bundle
   ```

4. Add `remote_theme: "mmistakes/minimal-mistakes@4.24.0"` to your `_config.yml` file. Remove any other `theme:` or `remote_theme:` entry.

You may also optionally specify a branch, [tag](https://github.com/mmistakes/minimal-mistakes/tags), or commit to use by appending an @ and the Git ref (e.g., `mmistakes/minimal-mistakes@4.9.0` or `mmistakes/minimal-mistakes@bbf3cbc5fd64a3e1885f3f99eb90ba92af84063d`). This is useful when rolling back to older versions of the theme. If you don't specify a Git ref, the latest on `master` will be used.

**Looking for an example?** Use the [Minimal Mistakes remote theme starter](https://github.com/mmistakes/mm-github-pages-starter/generate) for the quickest method of getting a GitHub Pages hosted site up and running. Generate a new repository from the starter, replace sample content with your own, and configure as needed.
{: .notice--info}

---

**Note:** Your Jekyll site should be viewable immediately at <http://USERNAME.github.io>. If it's not, you can force a rebuild by **Customizing Your Site** (see below for more details).
{: .notice--warning}

If you're hosting several Jekyll based sites under the same GitHub username you will have to use Project Pages instead of User Pages. Essentially you rename the repo to something other than **USERNAME.github.io** and create a `gh-pages` branch off of `master`. For more details on how to set things up check [GitHub's documentation](https://help.github.com/articles/user-organization-and-project-pages/).

<figure>
  <img src="{{ '/assets/images/mm-gh-pages.gif' | relative_url }}" alt="creating a new branch on GitHub">
</figure>

You can also install the theme by copying all of the theme files[^structure] into your project.

To do so fork the [Minimal Mistakes theme](https://github.com/mmistakes/minimal-mistakes/fork), then rename the repo to **USERNAME.github.io** --- replacing **USERNAME** with your GitHub username.

<figure>
  <img src="{{ '/assets/images/mm-theme-fork-repo.png' | relative_url }}" alt="fork Minimal Mistakes">
</figure>

**GitHub Pages Alternatives:** Looking to host your site for free and install/update the theme painlessly? [Netlify][netlify-jekyll], [GitLab Pages][gitlab-jekyll], and [Continuous Integration (CI) services][ci-jekyll] have you covered. In most cases all you need to do is connect your repository to them, create a simple configuration file, and install the theme following the [Ruby Gem Method](#ruby-gem-method) above.
{: .notice--info}

[netlify-jekyll]: https://www.netlify.com/blog/2015/10/28/a-step-by-step-guide-jekyll-3.0-on-netlify/
[gitlab-jekyll]: https://about.gitlab.com/2016/04/07/gitlab-pages-setup/
[ci-jekyll]: https://jekyllrb.com/docs/deployment/automated/#continuous-integration-service

### Remove the Unnecessary

If you forked or downloaded the `minimal-mistakes-jekyll` repo you can safely remove the following folders and files:

- `.editorconfig`
- `.gitattributes`
- `.github`
- `/docs`
- `/test`
- `CHANGELOG.md`
- `minimal-mistakes-jekyll.gemspec`
- `README.md`
- `screenshot-layouts.png`
- `screenshot.png`

**Note:** If forking the theme be sure to update `Gemfile` as well. The one found at the root of the project is for building the theme's Ruby gem and is missing dependencies. To properly setup a [`Gemfile`](https://github.com/mmistakes/minimal-mistakes/blob/master/docs/Gemfile) with the theme, consult the "[Install Dependencies](https://mmistakes.github.io/minimal-mistakes/docs/installation/#install-dependencies)" section.
{: .notice--warning}

## Setup Your Site

Depending on the path you took installing Minimal Mistakes you'll setup things a little differently.

**ProTip:** The source code and content files for this site can be found in the [`/docs` folder](https://github.com/mmistakes/minimal-mistakes/tree/master/docs) if you want to copy or learn from them.
{: .notice--info}

### Starting Fresh

Starting with an empty folder and `Gemfile` you'll need to copy or re-create this [default `_config.yml`](https://github.com/mmistakes/minimal-mistakes/blob/master/_config.yml) file. For a full explanation of every setting be sure to read the [**Configuration**]({{ "/docs/configuration/" | relative_url }}) section.

From `v4.5.0` onwards, Minimal Mistakes theme-gem comes bundled with the necessary data files for localization.
They will be picked up automatically if you have the [`jekyll-data`](https://github.com/ashmaroli/jekyll-data) plugin installed.
If you're hosting on GitHub Pages, you can copy the [`_data/ui-text.yml`][ui-text.yml] file into your repository for the localization feature to work.

You'll need to create and edit these data files to customize them:

- [`_data/ui-text.yml`][ui-text.yml] - UI text [documentation]({{ "/docs/ui-text/" | relative_url }})
- [`_data/navigation.yml`][navigation.yml] - navigation [documentation]({{ "/docs/navigation/" | relative_url }})

  [ui-text.yml]: https://github.com/mmistakes/minimal-mistakes/blob/master/_data/ui-text.yml
  [navigation.yml]: https://github.com/mmistakes/minimal-mistakes/blob/master/_data/navigation.yml

### Starting from `jekyll new`

Scaffolding out a site with the `jekyll new` command requires you to modify a few files that it creates.

Edit `_config.yml`. Then:

- Replace `<site root>/index.md` with a modified [Minimal Mistakes `index.html`](https://github.com/mmistakes/minimal-mistakes/blob/master/index.html). Be sure to enable pagination if using the [`home` layout]({{ "/docs/layouts/#home-page" | relative_url }}) by adding the necessary lines to **_config.yml**.
- Change `layout: post` in `_posts/0000-00-00-welcome-to-jekyll.markdown` to `layout: single`.
- Remove `about.md`, or at the very least change `layout: page` to `layout: single` and remove references to `icon-github.html` (or [copy to your `_includes`](https://github.com/jekyll/minima/tree/master/_includes) if using it).

### Migrating to Gem Version

If you're migrating a site already using Minimal Mistakes and haven't customized any of the theme files things upgrading will be easier for you.

Start by removing the following folders and any files within them: 

```terminal
├── _includes
├── _layouts
├── _sass
├── assets
|  ├── css
|  ├── fonts
|  └── js
```

You won't need these anymore as they're bundled with the theme gem --- unless you intend to [override them](https://jekyllrb.com/docs/themes/#overriding-theme-defaults).

**Note:** When clearing out the `assets` folder be sure to leave any files you've added and need. This includes images, CSS, or JavaScript that aren't already [bundled in the theme](https://github.com/mmistakes/minimal-mistakes/tree/master/assets). 
{: .notice--warning}

From `v4.5.0` onwards, the default language files are read-in automatically via the [`jekyll-data`](https://github.com/ashmaroli/jekyll-data) plugin if it's installed. For sites hosted with GitHub Pages, you still need to copy the [`_data/ui-text.yml`][ui-text.yml] file because the `jekyll-data` plugin [is unsupported on GitHub Pages](https://docs.github.com/en/github/working-with-github-pages/about-github-pages-and-jekyll#plugins).

If you customized any of these files leave them alone, and only remove the untouched ones. If done correctly your modified versions should [override](https://jekyllrb.com/docs/themes/#overriding-theme-defaults) the versions bundled with the theme and be used by Jekyll instead.

#### Update Gemfile

Replace `gem "github-pages` or `gem "jekyll"` with `gem "jekyll", "~> 3.5"`. You'll need the latest version of Jekyll[^update-jekyll] for Minimal Mistakes to work and load all of the theme's assets properly, this line forces Bundler to do that.

[^update-jekyll]: You could also run `bundle update jekyll` to update Jekyll.

Add the Minimal Mistakes theme gem: 

```ruby
gem "minimal-mistakes-jekyll"
```

When finished your `Gemfile` should look something like this:

```ruby
source "https://rubygems.org"

gem "jekyll", "~> 3.7"
gem "minimal-mistakes-jekyll"
```

Then run `bundle update` and add `theme: minimal-mistakes-jekyll` to your `_config.yml`.

**v4 Breaking Change:** Paths for image headers, overlays, teasers, [galleries]({{ "/docs/helpers/#gallery" | relative_url }}), and [feature rows]({{ "/docs/helpers/#feature-row" | relative_url }}) have changed and now require a full path. Instead of just `image: filename.jpg` you'll need to use the full path eg: `image: /assets/images/filename.jpg`. The preferred location is now `/assets/images/` but can be placed elsewhere or externally hosted. This applies to image references in `_config.yml` and `author.yml` as well.
{: .notice--danger}

---

That's it! If all goes well running `bundle exec jekyll serve` should spin-up your site.
