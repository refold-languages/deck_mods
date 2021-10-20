# Tap on Mobile

This mod allows you to tap anywhere on screen to reveal the reading and replay the audio afterwards.
Just follow the instructions carefully!

## Instructions

If you need help reading these instructions, check out *[Jade's guide to modding anki](https://github.com/Fumon/Refold-Deck-Mods/blob/main/How-To-Mod.md)*.

To reveal the reading and replay the audio on tap, look into *[front_template.html](front_template.html)* and copy the marked funtions into the "Front Template" tab of the Anki card editor. The general template structure is included, so you can easily find the right location to paste them. Make sure to just copy the marked funktions, which look like this:

```
//----------------------------------------------------------
// function description
document.addEventListener('touchstart', function(event) {
    // instruction
});
//----------------------------------------------------------
```

If you want to be able to replay the sentence audio on tap, do the same with *[back_template.html](back_template.html)* in the "Back Template" tab.

After saving everything it should work!

## How it works

The added function is just an event listener, that will execute the code inside.
With the event type ``'touchstart'`` the listener is invoked every time you tap on your screen.
That means you can put any arbitrary functionality inside this listener.