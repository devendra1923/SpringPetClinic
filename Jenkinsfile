pipeline{
    agent any
    
    tools {maven "M3"}
    
    stages{
        
        stage("checkout"){
            steps{
                git url: "https://github.com/devendra1923/SpringPetClinic.git" , branch: "main"
            }
        }
        
        stage("build"){
            steps{
                sh "mvn compile"
            }
        }
        
        stage("test"){
            steps{
                sh "mvn test"
            }
        }
        
        stage("package"){
            steps{
                sh "mvn package"
            }
        }
        
        stage("deploy"){
            steps{
                sh "java -jar /home/coder/.jenkins/workspace/petclinincDeclarativePipeline/target/*.jar"
            }
        }
    }
}
