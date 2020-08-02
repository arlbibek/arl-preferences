# Open Command Line Prompt(CMD) from Sublime Editor in Windows

**Add 'CMD' in Sublime Text Contex Menu**

1. Open Sublime editor.
2. Click on the Preferences and then select Browser Packages… (It will open a new window.)
3. Create new folder CMD (all uppercase letters).
4. Create a file `cmd.py` and write the following code and save the file. (Inside CMD folder)
```python
import os, sublime_plugin
class CmdCommand(sublime_plugin.TextCommand):
	def run(self, edit):
		file_name=self.view.file_name()
		path=file_name.split("\\")
		current_driver=path[0]
		path.pop()
		current_directory="\\".join(path)
		command= "cd "+current_directory+" & "+current_driver+" & start cmd"
		os.system(command)
```
5. Create another file with a name `Context.sublime-menu`. Copy and paste lines given below into the file and save it.

```
[
	 { "command": "cmd" }
]
```
## That is all.

6. Verify:

- Open any program file in the sublime editor and Right-click (context menu).
- You should see the Cmd menu in Context menu options.
- Click on it.
- The command prompt will be opened through which you can compile and run your program.

Reference: https://www.csestack.org/open-command-line-prompt-from-sublime-windows/

\# The End.
