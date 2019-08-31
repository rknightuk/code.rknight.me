---
title: almanac
forkme: https://github.com/rknightuk/almanac
screenshot: /almanac/screenshot.png
---

A media microblog.

WORK IN PROGRESS

[View a live demo](https://almanac.rbbl.ws)

## Features

### Post types

Almanac has eight post types:

- Movies
- TV
- Games
- Music
- Books
- Podcasts
- Videos
- Quotes

Most of these types display the same with the exception of quotes; the content of the post is the quote and the title is the "author".

SCREENSHOT OF QUOTE POST

### Automatic Media Embeds

The post editor supports HTML so any media can be embedded in a post. This section refers only to automatically embedding specific services.

Although automatic media embeds are designed for video and music posts, any post type can automatically embed media by adding a link to a post. The following services are supported:

- YouTube videos
- Vimeo videos
- Spotify tracks, albums and playlists

SCREENSHOT OF YOUTUBE POST
SCREENSHOT OF SPOTIFY POST

### Spoilers

If a post contains spoilers there are two options to obscure the post:

- Turning "Spoilers?" on in the post editor. This will obscure all the content of the post.
- Wrapping specific section in `[spoiler]Your Spoiler Here[/spoiler]` will obscure just that section, while leaving the rest of the content available.

Visitors can then click on the spoiler to reveal the contents.

SCREENSHOT OF FULL SPOILER POST
SCREENSHOT OF PARTIAL SPOILER POST

### Tags

Tags can be added in the post editor and all posts for a specific tag can be viewed at `yourdomain.com/?tags[]=TAGNAME`

### Rewatches

Almanac will match up previous posts where the same thing has been watched and display this on the site. When visiting a permalink for a post, any other posts related to the same thing will be shown. Posts have a "repost" button  so you can easily repost the same thing, with new content, again.

SCREENSHOT OF MULTIPLE WATCH POST
SCREENSHOT OF REPOST POST

## Installation

### Requirements

- See the [Laravel requirements](https://laravel.com/docs/5.6#server-requirements)

### Initial Setup

- Clone the repository `git clone https://github.com/rknightuk/almanac.git almanac`
- Navigate to the root `cd almanac`. 
- Run `composer install`
- Create a copy of the example env file `cp .env.example .env`. 
- Open `.env`, fill in your details. 
- Run `php artisan key:generate`
- Run `php artisan migrate` to create the database tables
- Run `npm install` to install the javascript dependencies
- Run `npm run watch` for development or `npm run production` for a production build
- Run `php artisan almanac:setup`; this will prompt for an email and password. This user account is used to login to Alamanc to create new posts.
- Run `php artisan serve` and open [http://127.0.0.1:8000](http://127.0.0.1:8000) to view the site

## Contributing

If you have an idea for a new feature, open an issue describing the feature so we can discuss if it before you put significant work into it.

## License

[https://rknightuk.mit-license.org/](https://rknightuk.mit-license.org/)


