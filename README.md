# Login app to register a user.
### How to build this code
1. create a jenkins job
2. configure maven
3. use jenkins file mentioned below 
``` pipeline {  
    agent any  
    tools {  
        maven 'maven'  
    }  
    stages {  
        stage ("clone repo"){  
            steps {  
            git 'https://github.com/ravdsun/loginapp.git'  
        }  
        }  
        stage ("build code"){  
           steps {  
              dir('app'){  
              sh "mvn package"  
          }  
        }      
        }  
    }  
}  
```

4. Buld the job
