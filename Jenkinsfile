
pipeline {

    agent any
    tool {
        maven 'maven-3.9.1'

    stages {

        stage ("Cleanup Workspace") {
            steps {
                cleanWs()
            }   
        }

        stage ("Checkout From SCM") {
            steps {
               git branch: 'main', url: 'https://github.com/marviflame/DevOps_Java_Project.git'
            }   
        }

        stage ("Build Application") {
            steps {
                sh 'mvn clean install'
            }   
        }
        
       // stage ("Test Application") {
       //      steps {
       //          sh 'mvn test'
       //      }   
       //  }
    }    
        
}
