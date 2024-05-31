pipeline {
    agent any
    stages{
        stage("Build for Nextjs App") {
            steps{
                script{
                    docker build -t nextjs .
                }
            }
        }
        stage("Build for Django App") {
            steps{
                script{
                    docker build -t Django .
                }
            }
        }
stage("Login dockerhub") {
            steps{
                script{
                    docker login -u sravanaboyanagayathri -p  dckr_pat_iFPJdcF8WbgtAyFZ8Y4a43D33eY
                }
            }
        }
        stage("push image into dockerhub") {
            steps{
                script{
                    docker push sravanaboyanagayathri/nextjs:latest
                    docker push sravanaboyanagayathri/django:latest
                }
            }
        }
    }
}
