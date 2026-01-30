# Thinking about collection management
ref: "Unbundling tools for thought", bkmr(cli), grit(cli), TagStudio

UTFT suggests that what we really need instead of knowledge-management is
collection-management. A collection manager is basically software that manages
collections of "things" (these things can either be links, text, code-snippets,
etc).


What I really liked with each software:
- TagStudio:
    - tagstudio has a really nice design/philosophy to organizing things
    - A problem that I immediately notice is the overload of tags. Anything can
      be tagged in a number of ways so we'll have the trim the fat and keep the
      important tags. but then the question becomes: How do you decide what tags
      are more useful?

- grit:
    - I really liked grit's underlying implementation, it uses multi-tree's to
      represent "nodes" so everything is a node even tags. I really liked that
      idea and would love to see more


- bkmr:
	- bkmr seems to best capture the spirit of what I want
	- It has good search function


- nushell:
    - another piece of software that has caught my attention would be nushell
    - in nu everything is a structured data 


# Colman
collection manager or colman (na(e)col(r) - nature collection)  is my idea for
the ideal collection management software. I'll combine what I like from:
- bkmr
- TagStudio
- grit

ideas for design:
- attribute value tags
- everything is a node and connected into a multi-tree
- database will be in sql(lite) and will support seperate database integration
- nodes can be files, http-links(bookmark), snippet code, shell script, any
  custom object (like a book, film, anime, light-novel, etc, etc)
- full blown tui for easy searching/organising
- it will also have capabilities to support custom "modules" through scripting
  (maybe in lua or a common config language)

I am not sure if I want to use Odin or Go to write this. Odin is the new hot
thing I am trying but it doesn't have a strong library for tui's or any other
cli. Go on the other hand has an entire ecosystem of cli frameworks (Viper,
Charm libraries: bubbletea, lipgloss)

@2026-01-31 -> I am writing this with go. I'll first prototype a bookmark
manager then work on this


Depending on the type of collectible it will activate different Modules:
- Book module
- Film module
- Literature -> Manga module, LN, novels, etc
- Knowledge module



# Knowledge module
The collectible will be api-ideas like the titles of evergreen notes. Basically
I was thinking of stripping evergreen notes content and just keep the api-ness
of the titles, that way I can use them for long form content. Sure you could've
done the same with evergreen notes by referencing them in non-atomic notes but
you probably wouldn't be to able to establish named links/backlinks between
ideas (wait maybe you can? fuck this)

ISSUES:
- How do I link ideas/collectibles from markdown (I think this is also going to
  be a general issue of all colman collectibles)
    - hey what if reference the id of the "idea" in the footnotes, so it'll go
      like this -- I'll search for an idea-api in colman it'll give me its
      id and then I'll just link that under references. I could have neovim
      integration later too, like there'll be a keybind in neovim to
      automatically create the reference under the cursor


