pipeline {
    agent any

    stages {
        stage('Build') {
            agent {
                docker {
                    image 'node: 18-alpine'
                    reuse true
                }
            }
            steps {
                sh '''
                    ls -la
                    node --vertion
                    npm --vertion
                    npm ci
                    npm run build
                    ls -la
                '''
            }
        }
    }
}
