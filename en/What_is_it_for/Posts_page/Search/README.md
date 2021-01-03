# String search syntax

(word)-Search for post author name
{word}-Search post title
[word]-Search posts related to this tag
<word1,word2>-Search word1 or word2
word1,word2--Search word1 and word2
word-Search by name in default_name
number-Search by id
"space"-Add to array
enter-Send search request
-word-Search everything except this word
default_name-type default name creates a type that has been assigned as the default type example:author, title, tag.

Example
{red,blue},[-yellow,green],(gray,<-pink,black>),white,brown,purple

Return
{
	"red":{"type":"tag_title","not":false,"byid":false,"tag_and":["blue"]},
	"blue":{"type":"tag_title","not":false,"byid":false,"tag_and":[]},

	"yellow":{"type":"tag_tag","not":true,"byid":false,"tag_and":["green"]},
	"green":{"type":"tag_tag","not":false,"byid":false,"tag_and":[]},

	"gray":{"type":"tag_author","not":false,"byid":false,"tag_and":["pink",black]},
	"pink":{"type":"tag_author","not":true,"byid":false,"tag_or":[black]},
	"black":{"type":"tag_author","not":false,"byid":false,"tag_or":[]},

	"white":{"type":"default_name","not":false,"byid":false,"tag_and":["brown",purple]},
	"brown":{"type":"default_name","not":false,"byid":false,"tag_and":[]},
	"purple":{"type":"default_name","not":false,"byid":false,"tag_and":[]},
}

