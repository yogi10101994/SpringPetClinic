pipeline{
    agent{label 'master'}
    tools{maven "M3"}
    stages{
        stage('Checkout'){
            steps{
                git branch: 'msin', url: 'https://github.com/yogi10101994/SpringPetClinic.git'
            }
        }
        stage('Build'){
            steps{
                sh 'mvn compile'
            }
        }  
        stage('Test'){
            steps{
                sh 'mvn test'
            }
        }
          stage('Package'){
            steps{
                sh 'mvn package'
            }
        }
          stage('Deploy'){
            steps{
                sh 'java -jar /var?lib?jemkins/workspace/PetClinicDeclarativePipeline/target/*.jar'
            }
        }
    }
}
