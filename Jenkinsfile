pipeline{
    agent any
    tools{
        jdk 'jdk'
        terraform 'terraform'
    }
    stages{
        stage('clean Workspace'){
            steps{
                cleanWs()
            }
        }
        stage('checkout from Git'){
            steps{
                git branch: 'main', url: 'https://github.com/rameshm0490/Terraform-Jenkins.git'
            }
        }
        stage('Terraform version'){
             steps{
                 sh 'terraform --version'
                }
        }
        stage('Terraform init'){
            steps{
                sh 'terraform init'
            }
        }
        stage('Terraform plan'){
            steps{
                sh 'terraform plan'
            }
        }
        stage('Terraform apply'){
            steps{
                sh 'terraform ${action} --auto approve'
            }
        }
    }
}
