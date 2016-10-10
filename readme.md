##Running the Web Server

I had a lot of trouble setting up a grunt web server with phaser on Windows 10 using the new bash shell for Ubuntu on Windows. This is the result of my efforts, and hopefully by sharing this template others can benefit and get to programming faster.

To run the server, clone this repo:

```
https://github.com/brandonraphael/phaser-grunt-bash-ubuntu-windows-boilerplate.git
```

Install all dependencies:

```
npm install
```

And run the grunt web server:

```
grunt
```

##Useful bits of Information and Suggestions
I would highly recommend double checking that the repo phaser.min.js file version is current (located in src/lib/phaser.min.js) here: <a target="_blank" href="http://phaser.io/download/stabler">Phaser</a>.

The original project structure can be found on <a target="_blank" href="https://github.com/gamecook/phaser-project-template">Gamecook's repo</a>.

Should you attempt to use this boilerplate on a linux-based system other than Ubuntu, remove the list of dependencies in the package.json file, and re-download them using:

```
npm install --save grunt-open grunt grunt-contrib-concat grunt-contrib-connect grunt-contrib-watch
```

Then re-run

```
grunt
```

##Issues with using Grunt and Phaser on bash on Ubuntu on Windows
For anyone interested, the original issue I had trying to run grunt was very similar to the one found <a target="_blank" href="https://github.com/feathersjs/generator-feathers-plugin/issues/8">here</a>. And its <a target="_blank" href="https://github.com/Glavin001/generator-feathers-plugin/commit/39f1a18922abb99ef47d52a7ee18955a53a2c7ef">solution</a> was a single line change located in the Gruntfile.js file.

Additionally, I had some trouble locating the corresponding Ubuntu files in my Windows file browser. These files can be found in:

```
%LocalAppData%\lxss
```

Although they are not editable in the windows system, the best way I have found to transfer files is a simple alias moving files from my desktop (located under /mnt/c/Users/USERNAME/Desktop) to my Ubuntu workspace in the bash console.
