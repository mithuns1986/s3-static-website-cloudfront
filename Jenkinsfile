pipeline {
    agent any
        tools {
  terraform 'terraform' 
}
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', credentialsId: 'github', url: 'https://github.com/mithuns1986/s3-static-website-cloudfront.git'
            }
        }
        stage('Terraform init') {
            steps {
                sh 'terraform init'
            }
        }
      stage('Terraform PLan') {
steps{

  sh 'terraform plan'
}
        
      }
        stage('Terraform apply') {
            steps {
                sh 'terraform apply --auto-approve'
            }
        }
        
    }
}
