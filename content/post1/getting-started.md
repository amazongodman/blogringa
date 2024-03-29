---
date: "2018-05-28T13:22:14+07:00"
draft: false
tags:
- hugo
- theme
title: Getting Started With Hugo
type: post
---

## Step 1: Install Hugo

```bash
brew install hugo
```

To verify your new install:

```bash
hugo version
```


## Step 2: Create a New Site

```bash
hugo new site quickstart
```

The above will create a new Hugo site in a folder named `quickstart`.


## Step 3: Add a Theme

See [themes.gohugo.io](https://themes.gohugo.io/) for a list of themes to consider. This quickstart uses the beautiful [Ananke theme](https://themes.gohugo.io/gohugo-theme-ananke/).

```bash
cd quickstart;\
git init;\
git submodule add https://github.com/budparr/gohugo-theme-ananke.git themes/ananke;\

# Edit your config.toml configuration file
# and add the Ananke theme.
echo 'theme = "ananke"' >> config.toml
```


## Step 4: Add Some Content

```
hugo new posts/my-first-post.md
```


Edit the newly created content file if you want. Now, start the Hugo server with [drafts](/getting-started/usage/#draft-future-and-expired-content) enabled:

```
▶ hugo server -D

Started building sites ...
Built site for language en:
1 of 1 draft rendered
0 future content
0 expired content
1 regular pages created
8 other pages created
0 non-page files copied
1 paginator pages created
0 categories created
0 tags created
total in 18 ms
Watching for changes in /Users/bep/sites/quickstart/{data,content,layouts,static,themes}
Serving pages from memory
Web Server is available at http://localhost:1313/ (bind address 127.0.0.1)
Press Ctrl+C to stop
```


**Navigate to your new site at [http://localhost:1313/](http://localhost:1313/).**



## Step 5: Customize the Theme

Your new site already looks great, but you will want to tweak it a little before you release it to the public.

### Site Configuration

Open up `config.toml` in a text editor:

```
baseURL = "https://example.org/"
languageCode = "en-us"
title = "My New Hugo Site"
theme = "ananke"
```

Replace the `title` above with something more personal. Also, if you already have a domain ready, set the `baseURL`. Note that this value is not needed when running the local development server. 

**Tip:** Make the changes to the site configuration or any other file in your site while the Hugo server is running, and you will see the changes in the browser right away.


For theme specific configuration options, see the [theme site](https://github.com/budparr/gohugo-theme-ananke).

**For further theme customization, see [Customize a Theme](/themes/customizing/).**
