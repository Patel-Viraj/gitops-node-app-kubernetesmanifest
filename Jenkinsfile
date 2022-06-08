pipeline{
    agent any
    stages {
        stage('Build Docker Image') {
            steps {
                   sh "git config user.email viraj02p@gmail.com"
                    sh "git config user.name Patel-Viraj"
                    sh "cat deployment.yaml"
                    sh "sed -i 's+viraj5132/gitops.*+viraj5132/gitops:${DOCKERTAG}+g' deployment.yaml"
                    sh "cat deployment.yaml"
                    sh "git add ."
                    sh "git commit -m 'Done by Jenkins Job changemanifest'"
                    sh "git push https://${GIT_USERNAME}:${GIT_PASSWORD}@github.com/${GIT_USERNAME}/gitops-node-app-kubernetesmanifest.git HEAD:master"
            }
        }

    }
}
