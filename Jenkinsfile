
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
               git branch: 'main', url: 'https://github.com/marviflame/DevOps_Java_Project.git'
            }   
        }

    }    
        
}
