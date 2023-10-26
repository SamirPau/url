## 🔗 GitHub Pages URL Shortener

#### Demo

1. To add a new short link, add an issue with the title being the link you want
   to shorten (including the `http(s)://`) to
   [https://github.com/SamirPaulb/url/issues](https://github.com/SamirPaulb/url/issues).

2. The newly created short url can be accessed via `samirpaul.in/url/{issue_number}`


---


### How can you use this with your own domain?

1. Fork the repo before cloning your fork.
1. Set up GitHub pages for your forked repo.
   1. In your forked repo, **click the Settings tab** and scroll down to the
      GitHub Pages section.
   1. Then select the **main branch** source and click on the **Save** button.
   1. <img src="https://i.imgur.com/kjinFX9.png" alt="How to create GitHub page" height="176px">
1. If you are using your own domain:
   1. [Set your domain up for GitHub pages.](https://docs.github.com/en/free-pro-team@latest/github/working-with-github-pages/managing-a-custom-domain-for-your-github-pages-site#configuring-an-apex-domain)
   1. Change the URL in `CNAME` file to your domain.
1. If you are using GitHub page's default domain i.e. Something like
   `https://<username>.github.io/<repo-name>/`
   1. Delete the `CNAME` file.
   1. Change `var PATH_SEGMENTS_TO_SKIP = 0;` at the top of `404.html` to
      `var PATH_SEGMENTS_TO_SKIP = 1;`.
      1. This is as GitHub domains have an additional path segment (the repo
         name) after the host name.
1. Create a new repo as a database. (Or you could use your forked repo)
   1. Update `var GITHUB_ISSUES_LINK = "<your-github-issues-link>";` at the top
      of `404.html` accordingly afterwards.
      1. Format for `GITHUB_ISSUES_LINK`:
         `https://api.github.com/repos/{owner}/{repo}/issues/`
      1. Remember the trailing `/`!
1. Push your changes to your forked repo, and your low cost and cool as heck URL
   shortener will be ready for use!

