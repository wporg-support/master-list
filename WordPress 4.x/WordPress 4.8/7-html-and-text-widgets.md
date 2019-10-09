# HTML and text widgets in WordPress 4.8.1

A new **Custom HTML** widget was introduced in WordPress 4.8.1 to give a proper home for little markup snippets that the existing text widget was commonly used for in the past.

You may see some notices when using the **Text Widget**, these leave no cause for alarm, and are only there to help you use the right tools for the job.

—

**Existing text widgets**

When an existing text widget has any markup in it, it will detect this. If this happens the widget will go into legacy mode, and show the warning
```
This widget may contain code that may work better in the new "Custom HTML" widget. How about trying that widget instead?.
```

Legacy mode means that the text widget will look and behave like before the 4.8.0 update, but it is not an ideal approach, which is why we show the notice and recommend moving it over to the new Custom HTML widget.

**Adding markup to the text widget visual tab**

If you attempt to paste a snippet of markup into the text editor, you will be presented wit ha notice stating
```
Hey there, looks like you just pasted HTML into the "Visual" tab of the Text widget. You may want to paste your code into the "Text" tab instead. Alternately, try out the new "Custom HTML" widget!.
```

This is presented because markup in the visual tab is stripped down and sanitized, and you will end up seeing HTML code on your front end.

**Adding markup to the text widget text tab**

When opening the text tab of the widget you may be presented with the notice
```
Hey, did you hear we have a "Custom HTML" widget now? You can find it by scanning the list of available widgets on this screen. Check it out to add some custom code to your site!.
```

The notice is there to guide users who to use the appropriate widget, as many tutorials online will say to use the text widget. It is still possibly to put markup in the text tab, but we highly recommend using the Custom HTML widget instead.