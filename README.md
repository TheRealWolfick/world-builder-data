# World Builder starter data

A dataset for [World Builder](https://github.com/TheRealWolfick/world-builder): the structure a new vault needs.

- `90. Templater/Data Store Schema.md`: the fields of every data store collection and of character sheets
- `90. Templater/Ledger Types.md`: ledger types (Inventory, Journal, Stats, Relationships) and their callout templates
- `80. Global Data Store/Taxonomy/…`: values for every facet the schema links to: Rarity, Item Condition, Rating, Location Scales and Attack Power (ranked), Units, Genres, Elements, Energy Sources, Traditions, Material, Creature, Ability and Recipe Categories, Faction Types, Location Types, Item Categories, Engineering Disciplines, Upgrade Slots and Topics. **Novels** is left empty on purpose: a novel's note is made when you add the novel (`npm run scaffold` or Templater's createNovel).

## Importing

In World Builder open **Tools → Import data** and paste this repository's URL. Files you already have with the same content are skipped; for files that differ you choose to overwrite or skip them (one by one or all at once).

## Making your own dataset

A dataset is any GitHub repository laid out like this one:

```
world-builder.json     optional: {"name", "description", "root"}
vault/                 files exactly where they go in the vault (the "root" folder; default "vault" when it exists,
                       else the repository itself without README, LICENSE and dot files)
```

Copy notes from your own vault into `vault/` at the same paths (for example `80. Global Data Store/Items/Steel Sword.md`), commit and share the URL. A URL can also point at a branch or sub folder: `https://github.com/<owner>/<repo>/tree/<branch>/<folder>`.

Note names must stay unique across a vault (Obsidian links by name), so the importer warns about files whose name is already used elsewhere.
