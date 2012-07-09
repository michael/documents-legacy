# Prose 0.3.0

Without further ado.. here's a list of features (roughly ordered by priority) that would make sense for the next Prose release.


## Improved frontmatter (1 - 4 days)

The way the frontmatter works is not ideal yet. We have to options here: 

- A rather quick one to get deeply nested YAML right (using block literals as Dave suggested ...) 
- Or just invest some more time to really improve UX (Alex created a ticket for that). I could think of displaying key/value pairs so we have a separate input field for each value. I think this would be less error prone than the plaintext YAML version, but indeed involve more time to be implemented, tested and deployed. Approximately 3-4 days.

## Commit Messages (~ 1 day)

Let's bring an optional commit message in. This is technically super easy, just a matter of a good UI/UX solution. We don't want to force people to add a custom commit message, but they should be able to do it. Should be done in ~ 1 day.

## Improved filebrowser (~ 1 week if we cover both)

which makes browsing and reading filenames easier..  also.. "as you type search.. for narrowing down the file listing" and quickly navigating to the post you're looking for..

- **Switch to a list view for files/folders**:
  This will make it easier to navigate and find the files you're looking for. We can also display more information (such as last-modified directly in the list view)
- **Search/Filter as you type**:
  I guess this could be really powerful. Imagine this: You go to a certain folder.. which contains many files. But now you can just start typing some letters and the list gets narrowed so you find the piece of information you're looking for. This would make obsolete structuring posts in subfolders as we did at the developmentseed blog. Instead you'd simply type "2012" and you'd see all posts of 2012.