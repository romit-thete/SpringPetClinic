pipeline{
    agent{label 'master'}
    tools{maven 'M3'}
    stages{
        stage('Git Checkout'){
            steps{
                git branch: 'main', url: 'https://github.com/romit-thete/SpringPetClinic.git'
            }
        }
        stage('Build Spring Pet Clinic'){
            steps{
                sh 'mvn compile'
            }
        }
        stage('Test Spring Pet Clinic'){
            steps{
                sh 'mvn test'
            }
        }
        stage('Package Spring Pet Clinic'){
            steps{
                sh 'mvn package'
            }
        }
        stage('Deploy Spring Pet Clinic'){
            steps{
                sh 'java -jar /var/lib/jenkins/workspace/PetClinicDeclarativePipeline/target/*.jar'
            }
        }
    }
}
