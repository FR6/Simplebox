# Simplebox #

Simple box is a lightweight lightbox-like jQuery plugin.

# Usage #

Open dialog: 

    $.simplebox.show(content, {
        //settings
        'title'     : false,
        'closeOnEsc': true,
        'theme'     : 'default',
        'height'    : 'auto',
        'width'     : 'auto',
        'speed'     : 500,
        'easing'    : 'swing',
        'buttons'   : false,

        //events
        'beforeShow'  : function(){},
        'beforeClose' : function(){},
        'onClose'     : function(){}
    });

where content could be a string, dom element or jQuery element.

Close dialog: 

    $.simplebox.close();

*Shortcuts*

- Alert

    $.simplebox.alert("...")

    
- Confirm

    $.simplebox.confirm("...", function(){ 
        //your callback code
    });

# Change log #

2012/05/31: 
  fixed: When the content is a hidden div, when the dialog is closed it leaves the content visible.
  added: Allow to open multiple dialogs (open a dialog from another dialog; when we close the second dialog, we reopen the first one).
