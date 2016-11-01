1. Determine the URL of the latest Scratch tips window

* Make sure Scratch is running in the desired language

* Open the Tips Window and enter any of the tutorials

* Go to the last step of that tutorial

* Copy the URL of the "All Tips" link that is at the bottom of the page. That URL usually looks like

   https://cdn.scratch.mit.edu/scratchr2/static/__787158ad1362201586979068ba002765__/help/pt-br/home.html


2. Download the Tips Window's files to your server

wget \
     --recursive \
     --no-host-directories \
     --page-requisites \
     --html-extension \
     --convert-links \
     --restrict-file-names=windows \
     --domains cdn.scratch.mit.edu \
     --no-parent -erobots=off -P ./tips_window <Your URL>

3. Move the files to the proper folder

   mv tips_window/scratchr2/static/<Your URL>/* tips_window

   the URL for the files should be tips_window/help/pt-br/home.html

4. Make it available on Github

