pipleline{
  agent {label 'MyNode'}
  tools{
    jdk 'Java17'
    maven 'Maven3'
  }
  stages{
    stage("Cleanup Worksapce"){
            steps {
              CleanWs()
          }
       }
    
    stage("Checkout from SCM"){
            steps {
              git branch: 'main', credentialsId: 'github', url: 'https://github.com/ibanoba/register-app.git'
          }
       }
    
    stage("Build application"){
            steps {
              sh "mvn clean package"
          }
       }
    stage("Test applicaion"){
            steps {
              sh "mvn test"
          }
       }
    }
}
