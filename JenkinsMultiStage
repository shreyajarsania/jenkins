pipeline {
    agent none

    stages {
        stage("build and test the project") {
            agent {
                docker "our-build-tools-image"
            }
            stages {
               stage("build") {
                   steps {
                       sh "./build.sh"
                   }
               }
               stage("test") {
                   steps {
                       sh "./test.sh"
                   }
               }
            }
            post {
                success {
                    stash name: "artifacts", includes: "artifacts/**/*"
                }
            }
        }

        stage("deploy the artifacts if a user confirms") {
            input {
                message "Should we deploy the project?"
            }
            agent {
                docker "our-deploy-tools-image"
            }
            steps {
                sh "./deploy.sh"
            }
        }
    }
}
