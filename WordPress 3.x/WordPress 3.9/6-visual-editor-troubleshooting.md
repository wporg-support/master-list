From https://wordpress.org/support/topic/how-to-troubleshoot-visual-editor-issues?replies=3&view=all

**HOW TO TROUBLESHOOT VISUAL EDITOR ISSUES**

> Okay.. I have seen a lot of people reporting various issues with the WordPress editor after updating to version 3.9.
> 
> Remember… remain calm!! WordPress would not have released this update if there were problems with the core software. The update definitely works. BUT.. many themes and plugins have been affected by the update.
> 
> **Main Reason**
>
> TinyMCE version 4. This is the software used to run the WordPress content editor. The framework has completely changed.. and most all plugins and themes which modified aspects of the tinymce editor will have to be updated. Plupload has also been updated.
> 
> There have also been changes with how WP Galleries are handled, displayed, and processed.
> 
> FIRST, empty your browser cache manually, and make sure to clear any caching plugin you are using in your WP admin panel. The content editor is notorious for serving cached files. Manually emptying and refreshing your browser cache may be the answer.
> 
> **Troubleshoot**
>
> So, what do you do if your editor is not loading properly??
> 
> 1. Deactivate all plugins.. yes, ALL plugins.
> 2. Switch to the defualt 2014 theme… because we know it works.
> 3. Manually empty and refresh your browser cache.
> 
> These steps are VERY important.. and should be followed concisely!
> 
> Now.. with NO plugins.. the default 2014 theme.. and a clean browser cache… go back and see if the editor loads properly.
> 
> **If Editor Loads Properly**
>
> Now.. the editor should load properly. If it does not, skip to the next section.
> 
> We have a working editor again; YAY! Now, we have to get our theme and plugins back.
> 
> **Testing Theme**
>
> Start with your theme. Go back and switch to the theme you were using. Then, go back to the editor page. Test to see if the editor is still working properly.
> 
> If it does not… you know the issue is with your theme.
> 
> If it does… continue….
> 
> **Testing Plugins**
>
> Now… let’s begin re-activating our plugins ONE AT A TIME. Each time we activate a plugin.. we are going to go back and see if the editor loads properly.
> 
> If a plugin was at fault.. you will eventually find a plugin that causes the editor to load improperly. That is your faulty plugin. You will need to contact the plugin author and see if they are aware of the issue.
> 
> **Digging Further**
>
> If you are feeling super savvy… you can dig into this further by exploring the browser console.
> 
> 99 out of 100 times the editor does not load properly.. it is a javascript issue of some sort. By using our browser inspection tools; we can usually see the issue in real time.. exactly as it is occurring.. and extract useful information for troubleshooting.
> 
> This [Codex Page](https://codex.wordpress.org/Using_Your_Browser_to_Diagnose_JavaScript_Errors) has more information for how to troubleshoot these errors.
> 
> **If Editor Still Loads Improperly**
>
> If, after all of these troubleshooting steps, the editor is still loading improperly… and there are no error or warning messages in the browser console… then something MUCH deeper is going on.
> 
> You may need to manually re-update your WP installation… or work out another solution. In this case, I would suggest starting a new forum topic, explain everything you tried above.. and explaining any other important facts you can determine.
> 
> **Closing**
>
> I work in the editor extensively. I can assure everyone it works properly in WP 3.9. I see these issues all the time.. and 99% of the time, it is an incompatible plugin or theme.