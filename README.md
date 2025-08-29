<h1 align='center'>cfuen's gitmoji syntax + builder

<br>
<a href="https://gitmoji.dev">
  <img
    src="https://img.shields.io/badge/gitmoji-%20😜%20😍-FFDD67.svg?style=flat-square"
    alt="Gitmoji"
  />
</a>
<a>
  <img
    src="https://img.shields.io/badge/version-1.0-blue.svg?style=flat-square"
    alt="Gitmoji"
  />
</a>
</h1>

Just a simple commit message format/syntax based on the [gitmoji](https://github.com/carloscuesta/gitmoji?tab=readme-ov-file#about) standard + [small builder webapp](https://cfuendev.github.io/gitmoji-syntax/) to quickly build commit messages based on it

## what?

So, people like to use emojis in their commit messages, right? Looks pretty

And there's this cool website called [Gitmoji](https://gitmoji.dev/) which acts as both a standard and dictionary for commit message emojis, searchbar and all.

However, I wanted to stadardize the emojis I use in my git commits so that they require less search time and are easy to index and search through.

For this, I created
- a little format to prefix your commit messages text using gitmojis
- a [small web app](https://cfuendev.github.io/gitmoji-syntax/) that lets you construct simple commit messages prefixed by emojis from the gitmoji website.

## how?

As of v.1.0 (First version) there's 4 categories:
- Project Stage: Reflects the stage of the project that this commit marks. They're few and optional.
- Commit Type: Explains the type of code/changes that make up the commit. Mandatory.
- Commit Area: Explains the specific part of the codebase that is being worked on. Mandatory. Up to 2.
- Misc: Not the most explanatory but fun to use. Optional.

The syntax is as follows:

```
[Project Stage] <Commit Type> <Commit Area> [Commit Area 2] [Misc.]
```

The format and categories would not only make it so that a small subset of these emojis (The most common/general ones, making them easier to remember and taking less space in your memory unless you REALLY needed a specific type of emoji), It'd also make the emojis in your commit messages a bit more expressive, acting as *tags* that identify the type of commit/feature or the part of your code being worked on without having to explicitly state it.

<details>
<summary>
<h3>List of Emojis (Click to open)</h3>
</summary>

### Project Stage (Max. 1)
- BEGIN PROJECT - :tada:
- UNFINISHED (WIP) - :construction:
- DEPLOYMENT - :rocket:
- RELEASE - :bookmark:

### Commit Type (Max. 1)
- NEW FEATRUE - :sparkles:
- BIG ISSUE/FIX - :bug:
- MINOR ISSUE/FIX - :adhesive_bandage:
- OPTIMIZATION - :zap:
- REFACTORING - :recycle:

### Commit Areas (Max. 2)

**Front-end**
- UI STUFF - :lipstick:
- RESPONSIVITY - :iphone:
- SEO - :mag:

**Back-end**
- AUTH - :passport_control:

**DevOps and QA**
- CI PIPELINE - :construction_worker:
- TESTING - :test_tube:
- COMPILED FILES / PACKAGES - :package:

**General**
- TYPES - :label:
- I18N - :globe_with_meridians:
- A11Y - :wheelchair:
- DEV TOOLING - :hammer:
- DATASOURCES - :card_file_box:
- ASSETS / CONTENT - :bento:
- CONFIGURATION - :wrench:
- FORMATTING / READABILITY - :art:
- COMMENTS - :bulb:
- DOCS - :memo:

### Misc.
- DRUNKEN / HIGH - :beers:
- BAD CODE - :poop:
- TYPO - :pencil2:
</details>

### why? (philosophy)

**Gitmoji doesn't need a custom syntax or categorization**

You could argue that this is complicating things, since gitmoji [suggests](https://github.com/carloscuesta/gitmoji?tab=readme-ov-file#example-of-usage) the use of a single emoji in every commit message, :

```
<intention> [scope?][:?] <message>
```

I understand this is simple and more than enough for most people who just want to write code and commit whatever in order to make it look pretty, however it is just a proposal of the ways emojis can be used and I think it's cool to use at least two emojis in every commit, since that way you can more clearly understand the scope of the code being pushed to the repo. Plus categorizing things takes out the need to search their website, specially if you can have a quick tool like the one I made.

**Gitmoji has a CLI tool**

I haven't checked it out, and it seems like it simplifies the process. However I want to have a middle point between the website (Which is a nice quick tool to grab emojis to use) and the CLI, which "hijacks" your committing flow by asking you to use it's interactive commands that wrap around git, or integrating the pre-commit hook.

Besides -despite following gitmoji's own standard for what emojis correspond to what types of commits/commit scopes- my categorization and syntax are a little opinionated, and the webapp directly assists in said opinionated use of the emojis.