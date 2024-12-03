pipeline {
    agent any
 
    stages {
      stage('Add Tag'){
            steps{
                script{
                    // Create a tag with current data and time
                    def tagName = "update-${new Date().format('yyyyMMdd-HHmmss')}"
                    currentBuild.description = "Tagged with ${tagName}"
                    currentBuild.displayName = "#${currentBuild.number} - ${tagName}"
                }
            }
         }
        stage("build"){ 
            steps{
                echo 'building the application...'
            }
        }

        stage("test"){
            steps{
                echo 'testing the application...'
            }
        }

        stage("deploy"){
            steps{
                echo 'deploying the application'
            }
        }
    }
}
