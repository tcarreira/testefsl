# 2025
Festa do Sofware Livre 2025 Website
Built with [Hugo](https://gohugo.io) and [Vanilla framework](https://vanillaframework.io/)

# Adding contents
You will need to install [Hugo CLI](https://gohugo.io/getting-started/installing/) to easily add contents.

To create new content, run the following command
```bash
# Create session content
hugo new --kind sessions sessions/<session-name>/index.md
# Example: Create session content with title "Keynote session"
hugo new --kind sessions sessions/keynote-session/index.md

# Create host community content
hugo new --kind hosts hosts/<community-name>/index.md
# Example: Create host community content for "Ubuntu Korea Community"
hugo new --kind hosts hosts/ubuntu-kr/index.md

# Create sponsor content
hugo new --kind sponsors sponsors/<sponsor-name>/index.md
# Example: Create sponsor content with title "Canonical Ltd"
hugo new --kind sponsors sponsors/canonical-ltd/index.md

# Create news content
hugo new --kind news news/YYYY-MM-DD-post-title/index.md
# Example: Create news content with title "Welcome to FSL2025" and date "2024-12-15"
hugo new --kind news news/2024-12-15-welcome-to-fsl2025/index.md
```

After that, You will find generated markdown file under `content` directory. Edit the markdown file to add details.
To add photo files, put files on content item directory.(The same path where content item's `index.md` exists.)

# How to localize

1. Add language info in `config.yml` under `languages:` section. And fill out translation for site title, description and navigation menu. 
After adding language in `config.yml` you will be able to see your new language in language chooser menu.

```yml
languages:
  pt: # Language code
    languageName: Português # Language name
    title: Festa do Software Livre 2025 # Site title
    weight: 2
    params:
      description: >-
       some description
      period: October 3rd ~ 5th, 2025 | Somewhere in Portugal # description for event period
    menu:
      main: # site navigation fields
        - identifier: about
          name: Sobre # Make sure to translate only "name" field
          url: about
          weight: 1
        - identifier: sessions
          name: Sessões
          url: sessions
          weight: 2
```

2. UI localization  
You can see UI locale files in `i18n` directory. make a copy of `en.toml` And translate strings wrapped with quotation marks. Below is an example.

```toml
[learn_more]
other = "Learn more"
```

3. Markdown content localization

Most markdown files are name `index.md` or `_index.md`. To translate, Make a copy of markdown file on same path. with the filename `index.<lang-code>.md` or `_index.<lang-code>.md` (e.g. `index.en.md`). Then, translate the copied file.

This website uses hugo's i18n feature to support localization. To learn more, please refer to ["Multilingual Mode"](https://gohugo.io/content-management/multilingual/)

# License
Code: MIT, Contents: CC BY 4.0

Adapted with love from our friends: https://github.com/ubucon-asia/2022
