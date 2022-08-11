# Green Web Template

This Jekyll template is a way to organize and publish your thoughts from [Obsidian](https://obsidian.md/) to the web, complete with backlinks, notes graph, and wikilink support. This template was modified by [Megumi Tanaka](https://megumi.co) in 2021, and [Defyd](https://github.com/defyd) in 2022. Here's <a href="https://garden.megu.space/your-first-note.html#installation" class="internal-link">how to install this template</a>. View this template on [Github](https://github.com/defyd/green-web-template).

Based on the [Jekyll digital garden template](https://github.com/maximevaillancourt/digital-garden-jekyll-template) by Maxime Vaillancourt, and [This modified version of it](https://github.com/meewgumi/green-web-template/)

## How is this different?

### New Features

-   **Obsidian embeds!** Yes, images formatted `![[like this]]` will render automatically with the correct asset path!
-   **Categories!** (not clickable yet)
-   **Emoji favicons!** Configure at site level or page level with `favicon:` variable
-   **Archive Page!** An index of all notes, date updated, category, and excerpt.
-   **Tables!** Table syntax matches Obsidian and Github with [Commonmark Github Flavored Markdown](https://github.com/github/jekyll-commonmark-ghpages) integration
-   **Obsidian Templates!** Easily create a new note or page with the proper front matter variables.
-   **A dark blue theme!** That can easily be edited in the style.css file

### Netlify

This whole project is set up to wrok with Netlify.

### More great nerdy changes

-   New Obsidian Embed plugin also handles standard MD Images and adds path to Jekyll assets folder, including `title` and `alt`.  New plugin is called `obsidian_images_generator.rb`
-   Brackets inside code blocks are now `[[ignored]]` by the bidirectional link generator! Check my updates to `bidirectional_links_generator.rb` regex
-   Automatic Title Generation from `title:` variable! Renders as `<h1>` heading at the top of the page, so you don't need to type it manually for `_pages` anymore.
-   Permalink `/:slug` by default for all notes and pages, so you don't need to specify `permalink:` anymore! By default, all pages will be built in the root directory.
-   Responsive code blocks! Enabled horizontal scroll for codeblocks on narrow browsers.
-   Updated metadata in `head.html` with way more conditional logic based on site configuration, stripped extra whitespace from descriptions, and made sure absolute URLs for OpenGraph are rendering properly
-   Notes graph uses primary theme color variable from `style.css`
-   Privacy focused. No external calls to scripts, instead they're all saved in `assets/js`

## Why not Wordpress?

You might be wondering why I don't just use PHP based software on a PHP server. Well, Wordpress is a database system, so each post gets saved to a MySQL database and requires more computing power than a flat file system like Jekyll.

Wordpress also hinders my ability to write—not only because the editor is slow, but also the emotion I get when I open up a draft. Something about the process actually dampens my motivation to write down an idea.

I'm teaching myself Jekyll, Ruby, and Liquid to modify this digital garden template because I believe it's the best organization system for the way my mind works. And it makes me excited to open Obsidian and write things!

Read more about digital gardening on [Maggie Appleton's repo](https://github.com/MaggieAppleton/digital-gardeners).

# Template Quirks

Interesting errors I've encountered:

-   Your file path must not have any spaces in it or your `bundle` command will fail!
-   Plugins are not compatible with Github Pages instance of Jekyll, so you have to build your site locally and reconfigure output to `docs` folder. I have a similar setup in [this github pages repository](https://github.com/meewgumi/digital-garden-ghpages-template)
-   This template only works for apex and subdomains. If you build your site in a `/directory`, you may have to reconfigure the relative links throughout the template.
-   ~~Bidirectional link generator converts double bracket links inside codeblocks too~~ **Fixed!**
-   Does not yet support Obsidian Heading Links in this format `[[page#Heading]]`, although each heading automatically generates an `id=` so you can create anchor links manually with HTML
-   Emoji is not unicode, so they might not display properly in all browsers and operating systems
-   ~~Footnotes automatically open in new tab, even if they're internal links~~ **Fixed!**
-   ~~D3.js graph zooms when you scroll, so I disabled the graph by default~~ **Fixed!**
-   Excerpts on archive page truncate weirdly. I wish there was a way to exclude headings. There probably is if I get deeper into Nokogiri documentation.

# License
This blue theme version is available on github [here](https://github.com/defyd/green-web-template)

The base, "Green" version, by Megumi Tanaka is [publicly available on Github](https://github.com/meewgumi/green-web-template) and you are free to edit as you wish! [Buy Megumi a tea](https://www.buymeacoffee.com/megumi)! 🍵
