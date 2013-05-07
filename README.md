shelltrainer
============

Repetition trainer. Some things need to be rote-learned and doing so is
easiest by repetition. This tool simply prints an item from a source file on
the shell. Hook this up to frequently used commands and you're constantly
exposed to the what you want to rote-learn.

For example, I use it to teach myself vocabulary in various languages

Invocation
----------

     $> shelltrainer --add-to spanish azul blue

     $> shelltrainer [category]
     [spanish] azul: blue

The category matches the name of a .json file in $HOME/.shelltrainer. If
none is given, a random one is picked. The category is only displayed if
none is given.

Example hook
------------

    alias mutt="mutt; shelltrainer"

i.e. whenever I quit mutt, I see one word displayed

Config file format:
<pre>
 {
 "words" : [
     { 
        "definition" : "zapato",
        "description" : "shoe"
    },
    { 
        "definition" : "azul",
        "description" : "blue"
    }
]
}
</pre>
