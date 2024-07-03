###	how to get cards in a deck pyanki

there are two functions `collection::find_cards()` and `collection::find_notes()`, each takes a search string. 

the search string is kind of like scryfall syntax.

https://docs.ankiweb.net/searching.html


###	how to search for a sub-deck

path to the sub-deck from the parent decks, delimited by `::`; note: regex is permitted.

`deck:parent_deck::sub_deck`

`deck:*::sub_deck`


###	how to search for a deck with spaces in the name

enclose the entire query in double quotes (not just the stuff after the colon)

`"deck:deckname with spaces"`

`"deck:parent_deck::subdeck with spaces"`


### how to delete notes

the `collection::remove_notes()` function takes a list of note ids to be deleted.

```py
notes = col.find_notes("")
col.remove_notes(notes)
```




