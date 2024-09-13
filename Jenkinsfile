pipeline {
    agent any
    stages {

        stage('pull') {
            steps {
                git branch: 'master', url: 'https://github.com/manjunath14321/sBoot.git'
            }
        }
        stage('compile') {
            steps {
                sh 'mvn compile'
            }
        }

        stage('build') {
            steps {
                 sh 'mvn clean install'
            }
        }

        
    }

  post{

  success{
     echo 'Build success'
  }
    
  failure{
       echo 'Failure in the build'
   }

  }


}
