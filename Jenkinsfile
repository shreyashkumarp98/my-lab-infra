pipeline {
    agent any

    stages {
        stage('Clone the Repo') {
            steps {
                echo 'Cloning the Code from Git'
                git branch:'main', url: 'https://github.com/nishanthkumarpathi/my-lab-infra.git'
            }
        }
        stage('Provision the Terraform Infra') {
            steps {
                echo 'Init the Terraform to Download and Apply Terraform with -auto-approve option'
                sh '''
                cd terraforminfra
                terraform init
                terraform validate
                terraform fmt
                echo "its time to apply the code"
                terraform apply -auto-approve
                '''
            }
        }
        stage('Dummy1') {
            steps {
                echo 'Hello World'
            }
        }
        stage('Dummy2') {
            steps {
                echo 'Hello World'
            }
        }
    }
}
