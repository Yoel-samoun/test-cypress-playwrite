pipeline {
    agent any
    stages {
        
        stage('Stage 1') {
                  steps {
                      echo 'Enter Hello world!' 
                  }
              }
        stage('git repo & clean') {
            steps {
               //sh "rmdir  /s /q Testcypressinjenkins"
                sh "git clone https://github.com/Yoel-samoun/test-cypress-playwrite.git"
               // sh "mvn clean -f Testcypressinjenkins"
            }
        }
        
        
        stage('install') {
            steps {
               // sh "mvn install -f Testcypressinjenkins"
                 echo 'Install Hello world!' 
            }
        }
         
        stage('test') {
            steps {
                npx cypress run --spec "cypress/integration/pulse/*-spec.js"
                //sh "mvn test -f Testcypressinjenkins"
            }
        }
        stage('package') {
            steps {
               // sh "mvn package -f Testcypressinjenkins"
                echo 'package Hello world!' 
            }
        }
    }
}
