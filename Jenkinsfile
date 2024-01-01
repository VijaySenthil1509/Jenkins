pipeline{
  agent any
  tools{
    jdk 'Java17'
    maven 'Maven3'
  }
  stages{
    stage("CleanWS"){
      steps{
        cleanWs()
      }
    }
    stage("Checkout frm SCM"){
      steps{
        git branch: 'Thalapathy', credentialsId: 'VijaySenthil1509', url: 'https://github.com/VijaySenthil1509/Jenkins'
      }
    }
    stage("Build app"){
      steps{
        sh "mvn clean package"
      }
    }
    stage("TEst app"){
      steps{
        sh "mvn test"
      }
    }
  }
}
