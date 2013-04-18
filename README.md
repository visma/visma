##Installation##

- clone visma repository (parent of all maven visma repositories)
- download all sub repositories with clone_cmd.txt
- install all with mvn install -Dmaven.test.skip.exec=true on visma repository

##Optionnal (for UI tests)##

**Prerequisites** : [codjo framework](https://github.com/codjo "codjo")  
**UI test command sample** : visma/isma-project-dirmanager/isma-dirmanager-release-test$ mvn -P codjo test-release:run  

#Description of all programs#

##DirManager##
Allows synchronisation between 2 directories

**Features**  
_Classic_ : Preview and synchro of differences on same structure  
_Advanded_ : Preview and synchro of differences on differents structures (paths and filenames)  
_Clone eradication_ : Preview and allows deletion of clones files  
_MainClass_ : `DirManagerLauncher`  
     
**UI Test**  
visma/isma-project-dirmanager/isma-dirmanager-release-test$ mvn -P codjo test-release:run 
