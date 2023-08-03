@Library('jenkins_library') _

pipeline{

    agent any

    parameters{

        choice(name: 'action', choices: 'create\ndelete', description: 'Choose create/Destroy')
    }

    stages{
         
        stage('Git Checkout '){
                    when { expression {  params.action == 'create' } }
            steps{
            gitCheckout(
                branch: "master",
                url: "https://github.com/Anshul1128/java-app-project.git"
            )
            }
        }
            
    }
}