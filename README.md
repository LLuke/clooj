# clooj

### the application
clooj is a small, simple IDE (integrated development environment) for the clojure programming language. clooj is written entirely in clojure and uses a swing-based GUI. It is intended to be cross-platform (assuming Java 1.6 has been installed on your operating system), and run as a standalone application or as a clojure editor embedded in another java or clojure application. The standalone version is simple a single jar file, containing a copy of the clojure core, that can typically be launched by double-clicking its file icon or running
java -jar clooj-XXX-STANDALONE.jar from the command line. To embed in java, simply call clooj.core.show().

### the layout
clooj has a very simple layout of three columns that should be mostly self-explanatory. The left-most column is a tree showing clojure projects and the source files they contain. The middle column is the source file editor. The right column displays inputs and outputs of clojure REPLs (read-evaluate-print loops).

### the source editor
The source code editor offers a few simple things to make writing clojure code easier. A non-traditional bracket-matching feature highlights in gray those brackets that contain the innermost form you are currently editing. In addition, mismatched or unmatched brackets are highlighted in pink. When newlines are entered, the next line is automatically indented. You can press ctrl-ENTER to send either the nearest root form or the selected text to the REPL. Source files are continuously saved in the background to prevent accidental loss of your work in the event of a crash.

### clojure projects
Each clojure project corresponds to a project directory somewhere in the hard drive, containing a src directory. Inside the src directory is the source code hierarchy, composed of directories and .clj files. Note this directory structure is completely compatible with the lein and cake clojure build programs and you are encouraged to use one of these from the command line in conjunction with the clooj editor. Clicking different source files in the projects tree will automatically change the source file currently being edited, as well as switch the REPL to the corresponding current namespace.

### read-evaluate-print loops
The upper part of clooj's REPL display column shows the REPL history (inputs and outputs) and the lower part is a text area for inputting forms into REPL. Each project gets its own REPL environment: when a project is first selected, a new clojure REPL is created behind the scenes and becomes the REPL in use. By choosing "Restart REPL" you cause a new REPL to be created for the currently selected project and the old one discarded, if possible. If the project directory contains directories named "lib" and/or "jars" and there are any jar files inside, these jars will be added to the project REPL's classpath whenever it is launched or restarted. If you want to add new jars to the REPL's classpath, simply add jar files to the project's "lib" and/or "jars" directories and restart the REPL.

### more work needed
clooj is a work in progress. Your suggestions, criticisms and code contributions are appreciated.

### known issues
The "New" and "Open" menus don't work at present. Creating a new clojure project or an additional source file needs to be done from the command line.

-- Arthur Edelstein

