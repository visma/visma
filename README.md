##Installation##

- clone visma repository (parent of all maven visma repositories)
- download all sub repositories with clone_cmd.txt
- install all with `mvn install -Dmaven.test.skip.exec=true -P codjo` on visma repository

*if you don't need UI tests command, remove codjo parent in the maven pom file*  

##Optionnal (for UI tests)##

**Prerequisites**  
  
UI tests requires [codjo framework](https://github.com/codjo "codjo")  
To use codjo test-release feature, follow the  [codjo installation procedure](https://github.com/gonnot/codjo-install-workstation "install codjo")  
visma projects require only 2 codjo modules (using codjo.sh) : "pom" and "release-test"  

**UI test command sample** : `visma/isma-project-dirmanager/isma-dirmanager-release-test$ mvn -P codjo test-release:run`  

#Description of all programs#

##DirManager##
[DirManager](https://github.com/visma/isma-project-dirmanager "dirmanager") allows files synchronisation between 2 directories

**Features**  
_Classic_ : Preview and synchro of differences on same structure  
_Advanded_ : Preview and synchro of differences on different structures (paths and filenames)  
_Clone eradication_ : Preview and eradication of clone files  
_MainClass_ : `DirManagerLauncher`  
     
**UI Test**  
`visma/isma-project-dirmanager/isma-dirmanager-release-test$ mvn -P codjo test-release:run`  

##Memos##
[Memos](https://github.com/visma/isma-project-memos "memos") is a knowledge base tool.  
It provides a way to save small notes with tags and attachments and search features.  

**Features**  
_Tags_ : hierarchical tags.  
_Attachments_ : multiple possible attachments.  
_MainClass_ : `MemosLauncher`  

**UI Test**  
disabled at this time due to unsupported database (hsqldb) on codjo-release-test  

##VersusFighting (webapp)##
[VersusFighting](https://github.com/visma/isma-project-versusfighting "vs") is a versusfighting game tournament manager.  
Only 1on1 vf games are supported (aka street fighters, blaze blue...), 3on3 are not (aka kof).  
It just avoids to use pen and paper.  

**Features**  
_Partipants_ : simple participants subscription by nickname.  
_Game Selection_ : only ssf4 ae edition is actually supported.  
_Fighter Selection_ : each participant chooses X fighters.  
_Iteration_ : app determinates random opponents order and iterates until only one participant has fighter(s) remaining.

**UI Test**  
no UI tests  

##CV Generator##
[CV Generator](https://github.com/visma/isma-tools "tools") can generate Html resumes.  
User provides an xml resume and chooses the template, the application generates the Html resume.  

**Features**  
_Templates_ : support different jsp templates (only one available at this time).  
_Input_ : input file to provide is xml file, a xsd exists on repository for validation.  
_MainClass_ : `CvMain`  

##Subtitles synchronizer##
[Subtitles synchronizer](https://github.com/visma/isma-tools "tools") corrects .avi subtitles files.  

This tool corrects time offsets on subtitles files.  

_Input_ : unsynchronized file  
_Output_ : synchronized file  

_Format_ : .srt supported  

_MainClass_ : `SubtitlesSynchronizerTool`  

##Pacman##

[Pacman](https://github.com/visma/isma-pacman)  


