pipeline{
    agent { label 'terra' }
    stages {
        stage('vcs') {
            git branch : 'main',
                url : 'https://github.com/GOWTHI143/terraform.git'
        }
        stage ('build') {
            sh """ terraform init
                   terraform validate
                   terraform apply -yes """
        }
    }
}