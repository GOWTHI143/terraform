pipeline{
    agent { label 'terra' }
    stages {
        stage('vcs') {
            steps {
                git branch : 'main',
                url : 'https://github.com/GOWTHI143/terraform.git'
            }
            
        }
        stage ('build') {
            steps {
                sh """ terraform init
                   terraform validate
                   terraform apply -yes """
            }
            
        }
    }
}