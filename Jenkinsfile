pipeline {
    agent any

    stages {
         
        stage ("terraform init") {
            steps {
                sh ("terraform init ") 
            }
        }
        
        stage ("plan") {
            steps {
                sh ('terraform plan') 
            }
        }

        stage (" Action") {
            steps {
                echo "Terraform action is --> ${action}"
                sh ('terraform ${action} --auto-approve') 
           }
        }
        stage (" Final Stage") {
            steps {
                echo "Successfully deployes EC2 on eu-west-2"
                
           }
        }
    }
}
