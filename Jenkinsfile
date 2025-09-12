pipeline {
    agent any

    stages {
        stage("Prepare environment") {
            steps {
                dir("server") {
                    sh """
                    npm install
                    """
                }
            }
        }
        stage("Lint checks") {
            steps {
                dir("server") {
                    sh """
                    npm run lint
                    """
                }
            }
        }
        stage("Build") {
            steps {
                dir("server") {
                    echo "Pretending to run npm run build"
                }
            }
        }
        stage("Publish artifact") {
            steps {
                dir("server") {
                    echo "Copying artifact to our Registry"
                }
            }
        }
    }
}