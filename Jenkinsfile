@Library('jenkins_library') _

pipeline{

    agent any

    parameters{

        choice(name: 'action', choices: 'create\ndelete', description: 'Choose create/Destroy')
    }

    stages{
         
        stage('Git Checkout'){
                    when { expression {  params.action == 'create' } }
            steps{
            gitCheckout(
                branch: "master",
                url: "https://github.com/Anshul1128/Java-Project1.git"
            )
            }
        }
        stage('Unit Test maven'){
         
                    when { expression {  params.action == 'create' } }
            steps{
               script{                   
                   mvnTest()
               }
            }
        }
    }
}    
