We've got pretty far with Prose, and the next release 0.4.0 will probably be ready tomorrow, adding support for sending patches, which essentially allows Prose users to contribute to repositories they don't have access to. When sending a patch to a particular file a pull request gets created behind the curtain.

Well, I consider Prose more or less feature-complete, but we should invest some more time in tightening up the user interface. New features such as search, commit messages and patches could have an even better impact if we tweak the UI, wording etc.


Here's a couple of things we should consider. I'll move the details of the backlog to tickets on GitHub and assign them to the ambitious "1.0" milestone. We can decide later if we want to tag the next release 1.0 or rather keep the beta communication and get it out as 0.5.0.

### Improving the filebrowser

- List view
- Keyboard navigation
- Invididual colors / icons for different file types (emphasize Jekyll posts)

### Changeset View

- visually improve the changeset viewer
- we could come up with a much better way of showing the changes since the last save.


### Improving the repository selection page

- bringing in search as well (UX for selecting a repo is not really good yet)
- consider switching to a list view too
- show more context information (private vs. public repo / last modified, watchers + forks)

### Preview

### Improving and better communicating the send-patch workflow

This is probably one of the most interesting features we can offer to the GitHub community. We should not fail in communicating it within the app and documentation.


# Timing (2-3 week scope)

*Michael* (2-3 more weeks, until we hit that stable-point)

- code refactoring and removing redundant pieces now that all features are in place

*Saman* (one, ideally two weeks for a UI sprint)

- Sketching the UI and helping me polishing the CSS I setup

*Tristen*  (we could move faster if we push as a gang of three) depending on other priorities it would be great to work togehter with Tristen on this. :)

