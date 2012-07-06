# Prose 0.2.0

It's been two weeks since we launched [Prose](http://developmentseed.org/blog/2012/june/25/prose-a-content-editor-for-github/), a content editor for GitHub. The feedback for the initial version was incredible and so we started implementing some features that were highly requested. This release of Prose adds support for organizations, user profiles and syntax highlighting, and also fixes a number of issues that have been identified.

# Support for Organizations

Organizations are now accessible from the startpage. 

![](http://f.cl.ly/items/1M1B0r100k2l1u25163i/organizations.png)

Selecting one of them takes the user to the organization profile, where the repositories can be accessed.

![](http://f.cl.ly/items/1j0i1Q3V1E1b3T3G1E0Q/organization-profile.png)

We've added routes to access user profiles as well. 

![](http://f.cl.ly/items/0M1P2z280X0X01023W32/user-profile.png)

Organizations and users can easily be accessed by using an URL.

- `http://prose.io/#developmentseed`
- `http://prose.io/#michael`


# Syntax Highlighting

Although Prose is primarily an editor for Markdown files, many users found it to be useful for editing source code files as well. We've added syntax highling for a range of programming languages to make this task even easier.

![](http://f.cl.ly/items/3l1h3R0E2R311L3a3341/syntax-highlighting.png)

# Bugfixes and smaller improvements

Here's a complete list of bugfixes and smaller improvements we've made.

- We now use the same URL schemes as Github, to have explit routes for editing and previewing files
- Upgraded CodeMirror to Version 2.3
- Loading indicator for posts
- Fixed a problem with UTF-8 characters
- Handle binary files (e.g. images are previewed by default and not longer loaded into the editing interface)