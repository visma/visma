##Installation##

- clone visma repository (parent of all maven visma repositories)
- download all sub repositories with clone_cmd.txt
- install all with mvn install -Dmaven.test.skip.exec=true -P codjo on visma repository

##Optionnal (for UI tests)##

**Prerequisites**  
  
UI tests requires [codjo framework](https://github.com/codjo "codjo")  
To use codjo test-release feature, follow the  [codjo installation procedure](https://github.com/gonnot/codjo-install-workstation "install codjo")  
visma projects require only 2 codjo modules (using codjo.sh) : "pom" and "release-test"  

**UI test command sample** : visma/isma-project-dirmanager/isma-dirmanager-release-test$ mvn -P codjo test-release:run  

#Description of all programs#

##DirManager##
[DirManager](https://github.com/visma/isma-project-dirmanager "dirmanager") allows files synchronisation between 2 directories

**Features**  
_Classic_ : Preview and synchro of differences on same structure  
_Advanded_ : Preview and synchro of differences on differents structures (paths and filenames)  
_Clone eradication_ : Preview and allows deletion of clones files  
_MainClass_ : `DirManagerLauncher`  
     
**UI Test**  
visma/isma-project-dirmanager/isma-dirmanager-release-test$ mvn -P codjo test-release:run 

##Memos##
[Memos](https://github.com/visma/isma-project-memos "memos") is a knowledge base tool.  
It provides a way to save small notes with tags and attachments and a search feature to find an old note.  

**Features**  
_Tags_ : hierarchicals tags.  
_Attachments_ : multiples attachments possible.  
_MainClass_ : `MemosLauncher`  

**UI Test**  
disabled at this time due to unsupported database (hsqldb) on codjo-release-test  

##VersusFighting (webapp)##
[VersusFighting](https://github.com/visma/isma-project-versusfighting "vs") is a versusfighting game tournament manager.  
Only 1on1 vf games are supported (aka street fighters, blaze blue...), 3on3 are not (aka kof).  
It's just avoid to use pen and paper.  

**Features**  
_Partipants_ : simple participants subscription by nickname.  
_Game Selection_ : only ssf4 ae edition is actually supported.  
_Fighter Selection_ : each participant choose X fighters.  
_Iteration_ : app determinate random opponents order and iterate until only one participant has fighter(s) remaining.

**UI Test**  
no UI tests  
