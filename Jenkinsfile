node{
    git:branch: 'main', url: 'https://github.com/Diaadam/simple-java-app.git'
    stage('build'){
        
        try {
        sh 'echo "Building the application..."'
        } catch (Exception e) {
            sh'echo "Error during build stage"'
            throw e
        }
    }
    stage('test'){
        if(env.BRANCH_NAME == 'feature'){
            
            sh 'echo "Running tests..."'
           
        } else {
            sh 'echo "Skipping tests for non-feature branch"'
        }
}

















// pipeline{
//     agent{
//         label 'aws-agent'
//     }
//     stages{
//         stage('build'){
//             steps{
//                 script{
//                     sh 'docker build -t java-app .'
//                 }
//             }
//         }

//         stage('push'){
//             steps{
//                 script{
//                     withCredentials([usernamePassword(credentialsId: 'docker-hub', passwordVariable: 'Password', usernameVariable: 'Username')]) {
//                     sh 'docker login --username $Username --password $Password'
//                     sh 'docker tag java-app $Username/java-app'
//                     sh 'docker push $Username/java-app'
//                     }
//                 }
//             }
//         }

//         stage('deploy'){
//             steps{
//                 script{
//                     withAWS(credentials: 'aws-cli', region: 'us-east-2') {
//                     sh 'aws eks update-kubeconfig --region us-east-2 --name eks'
//                     sh 'kubectl apply -f ./k8s/deployment.yaml'
//                     }
//                 }
//             }
//         }
//     }
// }
