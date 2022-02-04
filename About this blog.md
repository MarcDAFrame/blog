# About this blog

This blog uses Github as the CMS, meaning github hosts the markdown and media files for the blog.

## Why?
This is nifty because 
1. you don't pay for a CMS / hosting
2. your blogs can be version tracked
3. you can write blogs with the same workflow as you write your code

## How?
The blog uses the `Github Rest API` to query all the files in a repo, it then iterates through all the markdown files, building a tree view which is viewed on the `/blogs` page.

When a user clicks on the a blog they are linked to `/blog?file=[SOME FILE IN THE REPO]` where a call is made to the `raw.githubusercontent.com` endpoint to fetch the content for that file.

The only complicated part of this is how images and links are handled. A custom `SvelteMarkdown` renderer was created for both the Image and the Link which translated the image `src` to be fetched from the `raw.githubusercontent.com`, and translated the Link `href` to be relative to the currently open file, linking to the relevant `/blog?file=[SOME FILE IN THE REPO]` (if it was a relative link).

### Images work
![svelte logo](./res/svelte.svg)
- this image is hosted on github

### Links Work
[link](<./Reflections/01-2022.md>)
- this link works in github, vs code, and this blog 

## Source Code
The following is a minimum repo of this blog built in Svelte

#### [repo](https://github.com/MarcDAFrame/SvelteGithubBlog)

## Caveats
An individual, unauthenticated user can only make 60 requests an hour, which means the user can only refresh the page 60 times and can only view 60 blogs. The rate limiting is separate between the two domains (raw and api) which means viewing a blog, and viewing all the blogs have different rate limits.

However, this isn't much of an issue as an individual user isn't going to be reading / refreshing your blog that much - and if they are then they probably deserve to be rate limited.