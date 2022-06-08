pipeline{
    agent any
    stages {
        stage('Build Docker Image') {
            steps {
                   sh "git config user.email viraj02p@gmail.com"
                    sh "git config user.name Patel-Viraj"
                    sh "cat deployment.yaml"
                    sh "git add ."
                    sh "git commit -m 'Done by Jenkins Job changemanifest'"
                    sh "git push https://${GIT_USERNAME}:${GIT_PASSWORD}@github.com/${GIT_USERNAME}/kubernetesmanifest.git HEAD:main"
            }
        }
        stage('Deploy Docker Image') {
            steps {
                sh "echo staring deploy the image"

            }
        }
    }
}