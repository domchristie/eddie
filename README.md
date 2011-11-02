# eddie

A basis for creating rich text editors on the web.

As many developers/designers have found, there isn't a single rich text editor that does exactly what they want, particularly from the UI perspective. This has consequently led to developers creating their own from scratch.

## Aims of this project:

*   to be UI free i.e. expose a set of methods that mark up the content, but leave the UI implementation open.
*   to normalize the output of contentEditable across browsers, creating nice, semantic markup (perhaps one for another library?)
*   to limit the permitted HTML elements to the Markdown subset (do you _really_ need more?)

## Proposed API

Something along these lines:
    
    var editable = document.getElementsById('editable'),
        editor = new Eddie(editable);
      
    onSomeEvent(editor.makeBold);