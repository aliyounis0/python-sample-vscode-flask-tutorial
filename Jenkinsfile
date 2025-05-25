// pipeline{
//     agent{
//         label "java"    }
//     environment{
//         XYZ='ITI ITI ITI'
//     }
//     stages{
//         stage("build Docker image"){
//             steps{
//                 sh "docker build -t itiv4/data-iti:v${BUILD_NUMBER} ."
//             }
//         }
//         stage("Push Docker image"){
//             steps{
//                 sh "docker tag itiv4/data-iti:v${BUILD_NUMBER} aliyounis22/data-iti:v${BUILD_NUMBER}"
//                 sh "docker push aliyounis22/data-iti:v${BUILD_NUMBER}"
//             }
//         }
//     }
// }

node('java') {
    env.XYZ = 'ITI ITI ITI'
    
    stage("Build Docker Image") {
        sh "docker build -t itiv4/data-iti:v${BUILD_NUMBER} ."
    }
    
    stage("Push Docker Image") {
        sh "docker tag itiv4/data-iti:v${BUILD_NUMBER} aliyounis22/data-iti-way2:v${BUILD_NUMBER}"
        sh "docker push aliyounis22/data-iti-way2:v${BUILD_NUMBER}"
        }
}