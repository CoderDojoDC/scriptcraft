#CoderDojo ScriptCraft Activities

##Activity One: Get to Know the File System

Now that ScriptCraft is installed and we've practiced with some of the pre-installed example scripts, such as arrow.js, cottage.js, and skyscraper.js, it is time learn more about how to write ScriptCraft programs.

1. Using the file system, locate the scriptcraft plugins folder at

    <code>[Your Bukkit Server Folder]/plugins/scriptcraft/plugins/</code>

2. Within this directory you will find all the example scripts that you've been working with so far. When you start writing you own programs, you will need to save them in this folder in order for ScriptCraft to know where to look for them.

3. The files ending in .js are JavaScript files that you can open and edit with a text editor such as Notepad; you may want to install TextWrangler (Mac) or Komodo Edit (Mac/PC/Linux) which offer some nice features that make writing programs easier.

    * http://www.barebones.com/products/textwrangler/
    * http://www.activestate.com/komodo-edit/downloads

4. Explore the ScriptCraft folder, open some of the scripts, and see if you can find new commands to test on your ScriptCraft server.  When you open the files in this folder, at the top of the document, you may notice some blocks of text contained within tags like this: <pre>``/*``</pre> and <pre>``*/``</pre>.  These are comments, which means that when the computer runs the program, it knows to ignore these blocks of text.  Good programmers put comments in their code so that others who want to use of modify their programs later can more easily understand how it works.

5. As you explore the files in this folder, read the comments to see if you can figure out new commands to try on your ScriptCraft server; when you do find something that works, share it with the other kids, and show them how it works.

##Activity Two: Lava Arrows

1. One good way to learn about how programs work is to take an existing program, change it a little bit, and see what happens.  We're going to try that in this activity by adding lava arrows to the arrows.js script.

2. Make a copy of the arrows.js script and save it as arrows.js.bak.  It's a good idea to make a backup copy of any file you are modifying just in case things go wrong and you want to get back to the original script.

3. Open arrows.js in your text editor.

4. Notice the comments at the top that show you how to run the script.

5. The first block of code after the comments is a section where a lot of variables are being set.  Notice at the end of this block a list of arrow types is declared.  The first thing we need to do is add a new type to this list.  Look for this line: 
<code>_types = [ 'Normal', 'Explosive', 'Teleport', 'Flourish', 'Lightning', 'Firework' ];</code>
The list of things between the square brackets is called an array, and we're going to add an item to the array, like this:
     <code>_types = [ 'Normal', 'Explosive', 'Teleport', 'Flourish', 'Lightning', 'Firework', 'Lava' ];</code>
Notice that I've put a comma after 'Firework', and I've enclosed my new item in quotation marks.  These quotation marks tell the computer that this is a list of words or other text (= strings), not numbers or variables.

6. Now that we've added a new item to the list of possible arrows, we need to write instructions for the computer to know what to do when someone fires a lava arrow.

7. Look further down the arrows script until you find a line that says "switch" around line 100.  A switch is a block of code that tells the computer to do different things depending on the value of a variable.  In this case the computer will look at the variable "arrowType", which is enclosed in parentheses after the beginning of the switch.  Depending on what arrowType is set as, the computer will do different things.  You should see six different cases for the computer to follow.

8.  We're adding a new case, so what do you think we need to do?  Think back to how we added an item to the array above.  How many items are in the array we added to? Now look at how many "cases" are in this switch statement.  What number will our lava arrow be? The reason why the next item in the switch is 6, but there are 7 types in our array is because the first one is "normal" (just a normal arrow), and that would actually be case "0", but since a normal arrow doesn't need to do anything special, there is no case 0 in our switch statement.

9.  So we're going to add case 7 to the switch. Exactly how this code works is a topic for another day, but for now just add this to the end of the switch statement, placing it before the "}":

     <code>case 7:
        projectile.remove();
        d = new Drone(projectile.location)
        d.box(10)
        break;</code>

10. Save your text file.  Now, when you start up your Bukkit/ScriptCraft server and join your world, you should be able to type 

     <code>/js arrows.lava(self)`

And give yourself arrows that create a block of lava wherever they hit.

11. To practice this again, create another case for fire arrows.  Just add 'Fire' to the array of arrow types, and add an 8th case to the switch, changing the third line of the case to:
`d.box(10)` 
In fact, you can make arrows that create any placeable block by putting the number of the block in this statement.
