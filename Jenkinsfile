pipeline {
    agent any
    stages {
        stage("Clean Up") {
            steps {
                deleteDir()
            }
        }
        stage("Clone repo") {
            steps {
                sh "git clone https://github.com/vinur85/clone-test.git"
            }
        }
        stage("Build") {
            steps {
                echo "Building app - jenkins automatic"
            }
        }
        stage("Test") {
            steps {
                echo "Testing app - jenkins automatic"
            }
        }
    }
}
