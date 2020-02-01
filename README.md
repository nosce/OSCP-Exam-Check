# OSCP-Exam-Check
A simple HTML-based checklist for the most important steps required during the OSCP exam

# What is it for?
When I prepared for my OSCP exam, I read the OSCP Certification Exam Guide a thousand times, marked the most important aspects, created a digital and analog checklist version etc. In short, I thought I was well prepared and knew what to do.

Then during the exam I got quite confused with my multiple checklists. Lack of sleep wasn't helpful either... In the end, I absolutly lost track and forgot some important steps.

So I decided to merge all my notes to just one clearly structured checklistwhich helps me keep track and shows me if I forgot something. Maybe the checklist will halp other OSCP candidates as well, so here you go :)

:warning:
**Please note that the checklist is based in the OSCP Certification Exam Guide as of January, 2020. I will not keep track of changes made to the Exam Guide later. Feel free to update the checklist yourself and customize it according to your needs.**

# How does it work?
I intentionally put all code in one file so that you do not have to take care that HTML, style and script information are stored properly.
Just open the HTML file in a browser of your choice (I have tested it with Chrome and Firefox).

You can prepare the checklist once you receive the exam reminder email (usually 3 days prior to your exam):
1. Enter your OSID
  - All commands including your OSID (e.g. for creating the report archive) will be updated.
2. Enter your login password under *Start*
3. Save your entries by clicking *Save Checklist*
  - Your input will be saved in the browsers local storage and will be restored the next time you open the file.
  
Follow the checklist when starting your exam. Mark all steps you have finished. The section title will be marked red if there are still some open checkitems. Once you have checked everything, the section title will be marked green.

You can store your current input at any time by clicking *Save Checklist*. To remove all input, click *Clear All*.

# How can I add entries?
To add your own checklist entries, just edit the HTML file. Checklist items have the following structure:

## Simple checklist item 
```html
<div class="checkitem">
  <input type="checkbox" id="id" name="id"/>
  <label for="id">
    Have your ID card ready
  </label>
</div>
```

## Checklist item with command
```html
<div class="checkitem">
  <input type="checkbox" id="extract" name="extract"/>
  <label for="extract">
    Extract the file
    <code>tar xvfj exam-connection.tar.bz2</code>
  </label>
</div>
```

## Checlist item with list
```html
<div class="checkitem">
  <input type="checkbox" id="apps" name="apps"/>
  <label for="apps">
    Start required applications
    <ul>
      <li>Kali Linux</li>
      <li>Separate browser window for proctoring</li>
    </ul>
  </label>
</div>
```
