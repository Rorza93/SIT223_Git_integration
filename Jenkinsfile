pipeline{
    agent any
    stages{
        stage("Build"){
            steps{
                echo "========executing Build========"
            }
            post{
                always{
                    mail to: "r.hambrook93@gmail.com",
                    subject: "Build status Email",
                    body: "Build was successful"
                }
            }
        }
        stage("Test"){
            steps{
                echo "========executing Test========"
            }
            
        }
        stage("Deploy"){
            steps{
                echo "========executing Deploy========"
            }
        }
        stage("Complete"){
            steps{
                echo "========executing Complete========"
            }
        }
    }
    post{
        always{
            echo "========always========"
        }
        success{
            echo "========pipeline executed successfully ========"
        }
        failure{
            echo "========pipeline execution failed========"
        }
    }
}
