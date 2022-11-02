pipeline{
    agent { label 'STANDARD'}
    stages{
        stage('clonning git url of jenkins'){
            steps{
                git url:'https://github.com/kishorebittu3003/for-trfm.git',
                branch: 'trfm' 
            }
        }
        stage ('build with terraform'){
            steps{
                sh 'terraform init'
                //sh 'terraform apply -var-file "dev.tfvars" -auto-approve'
                sh 'terraform destroy -var-file "dev.tfvars" -auto-approve'
            }
        }

    }
}
