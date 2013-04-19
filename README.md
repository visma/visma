##Installation##

- clone visma repository (parent of all maven visma repositories)
- download all sub repositories with clone_cmd.txt
- install all with mvn install -Dmaven.test.skip.exec=true [-P codjo] on visma repository

##Optionnal (for UI tests)##

**Prerequisites**  
  
UI tests requires [codjo framework](https://github.com/codjo "codjo")  
To use codjo test-release feature, follow the  [codjo installation procedure](https://github.com/gonnot/codjo-install-workstation "install codjo")  
visma projects require only 2 codjo modules (using codjo.sh) : "pom" and "release-test"  

**UI test command sample** : visma/isma-project-dirmanager/isma-dirmanager-release-test$ mvn -P codjo test-release:run  

#Description of all programs#

##DirManager##
Allows files synchronisation between 2 directories

**Features**  
_Classic_ : Preview and synchro of differences on same structure  
_Advanded_ : Preview and synchro of differences on differents structures (paths and filenames)  
_Clone eradication_ : Preview and allows deletion of clones files  
_MainClass_ : `DirManagerLauncher`  
     
**UI Test**  
visma/isma-project-dirmanager/isma-dirmanager-release-test$ mvn -P codjo test-release:run 
