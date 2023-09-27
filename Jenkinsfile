
pipeline {

    agent any

    stages {

        stage ("Cleanup Workspace") {
            steps {
                cleanWs()
            }   
        }

        stage ("Checkout From SCM") {
            steps {
               git branch: 'main', url: 'https://github.com/marviflame/OctoberProject.git'
            }   
        }

        stage ("Build Application") {
            steps {
                sh 'mvn clean install'
            }   
        }
        
       stage ("Test Application") {
            steps {
                sh 'mvn test'
            }   
        }
    }    
        
}
