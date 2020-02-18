# Basic Debugging and Reporting

Basic debugging skills are required for the support engineer to solve basic queries and reduce time for bug fixing cycle.

Here, we have created three tasks related to CSS, JavaScript and PHP. Each task is of intermediate difficulty. Your task it to:

1. Identify the issue
2. Share the steps for fixing the issue with us
3. Share your thought process for debugging

### CSS

The following page consists of a Timeline in which Title Color is not appearing when set for individual timeline item. Identify the reason behind the issue and provide a fix for it.

**Link:** https://test.ideabox.dev/css-error/

**Reason:** Wrong Color Code 

**Fix:**  Follow the steps:
1. Open the following file - https://test.ideabox.dev/wp-content/uploads/elementor/css/post-151.css?ver=1580668369
2. Search for - .pp-timeline-card-title .
3. Change the Color code from #13A769 to #ff0000 .
4. Now, Save the file.

OR

Just add the color-attribute under -
.pp-timeline-card-title {
color: #ff0000;
}

**Thought Process:**  Inspect the particular section and then will try to find the error occuring.

### **JavaScript**

The following page consists of an Instagram Feed which is throwing JS error in the web console. Identify the reason behind the issue and provide a fix for it.

**Link:** https://test.ideabox.dev/js-error/

**Reason:**  Invalid Syntax & Reference error.

**Fix:** Open The Following File - https://test.ideabox.dev/wp-content/plugins/powerpack-elements/assets/js/pp-instagram.js?ver=1.4.12.3
  at InstaFeedPopupHandler (frontend.js?ver=1.4.12.3:267)
  at _runHook (frontend.min.js?ver=2.8.5:2)
  at Object.doAction (frontend.min.js?ver=2.8.5:2)
  at e.exports.runReadyTrigger (frontend.min.js?ver=2.8.5:2)
  at HTMLDivElement.<anonymous> (frontend.min.js?ver=2.8.5:2)
  at Function.each (jquery.js?ver=1.12.4-wp:2)
  at a.fn.init.each (jquery.js?ver=1.12.4-wp:2)
  at _default.runElementsHandlers (frontend.min.js?ver=2.8.5:2)
  at _default.onInit (frontend.min.js?ver=2.8.5:2)
  at _default.Module.trigger (frontend-modules.min.js?ver=2.8.5:2)

After defining the PPInstragramFeed we will save the file.

**Thought Process:** Inspect the particular page and use *DEVTOOLS for identifing the issue and solve it.

### **PHP**

The following page is throwing a PHP error and is not loading. Identify the reason behind the issue by using the Stack Trace of the issue appearing on the page and provide/suggest a fix for it.

**Link:** https://test.ideabox.dev/php-error/

**Reason:** Undefined or wrong defined variable

**Fix:** Follow the path in *Back-Panel of the current file like in this case - /home/vinavb/public_html/test/wp-content/plugins/powerpack-elements/modules/advanced-tabs/widgets/advanced-tabs.php
on line
1160
Then judge the problem by just define the variable or place an empty function around the current error.
Save The File, check again.


**Thought Process:** Before applying any changes we will take the backup of the current file and it will be best to create an wp_debug_log file and turn true, create the wp_debug_display file and turn it false so that we can make our changes witthout showing our error on our website.


