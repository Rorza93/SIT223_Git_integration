pipeline{
    agent any
    stages{
        stage("1: Build"){
            steps{
                echo "This stage is to Compile and Package the code"
                echo "Some tool we can use for this are Maven, Gradle or Ant"
            }            
        }
        stage("2: Unit and Integration Tests"){
            steps{
                echo "This stage is to Run unit tests to check code functionality and integration tests to ensure that different components of the application work together."
                echo "Some tools that we could use for this include JUnit for unit testing, Mickito for mocking and Selenium or JMeter for integration."
            }                
        }
        stage("3: Code Analysis"){
            steps{
                echo "This stage is to analyze the code to ensure that it meets industry standards."
                echo "Some tools that we can use for this include ESLint for javascript or Pylint for Python."
            }
        }
        stage("4: Security Scan"){
            steps{
                echo "This stage is to perform a security scan to identify any code vulnerabilities."
                echo "Tools that we can use for this include OWASP Dependency-Check, Fortify, Veracode"
            }
        }
        stage("5: Deploy to Staging"){
            steps{
                echo "This stage is to deploy the application to a staging server like an AWS EC2 instance."
                echo "Tools that we can use for this include AWS CLI, Docker, Kubernetes, or other orchestration tools."
            }
        }
        stage("6: Integration Tests on Staging"){
            steps{
                echo "This stage is to run integration tests on the staging environment to ensure the application functions in a production-like environment."
                echo "Tools that we could use for this include Selenium for web interface testing, Postman for API testing, or similar tools tailored to your specific application."
            }
        }
        stage("7: Deploy to Production"){
            steps{
                echo "This stage is to deploy the application to a production server like an AWS EC2 instance."
                echo "Tools that we can use for this include AWS CLI, Docker, Kubernetes, Terraform, or other Infrastructure as Code (IaC) and orchestration tools."
            }
        }        
    }
    post{
        always{
            mail to: "r.hambrook93@gmail.com",
                    subject: "Unit and Integration Tests: ${currentBuild.result}",
                    body: 'Check the logs for details.'
                    ${BUILD_LOG, maxLines, escapeHtml}
                    
        }
        success{
            echo "========pipeline executed successfully ========"
        }
        failure{
            echo "========pipeline execution failed========"
        }
    }
}
