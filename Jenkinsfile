pipeline{
    agent{
        label "agent_0"
    }
    environment{
        XYZ='ITI ITI ITI'
    }
    stages{
        stage("build Docker image"){
            steps{
                sh "docker build -t itiv4/data-iti:v${BUILD_NUMBER} ."
            }
        }
        stage("Push Docker image"){
            steps{
                sh "docker tag itiv4/data-iti:v${BUILD_NUMBER} aliyounis22/data-iti:v${BUILD_NUMBER}"
                sh "docker push aliyounis22/data-iti:v${BUILD_NUMBER}"
            }
        }
    }
}