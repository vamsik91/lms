//Jenkins file 
pipeline {
    agent{
       label 'Slave'
    }

    //environment {

    //DOCKERHUB_CREDENTIALS = credentials('dockeruservamsik91')
     //registry = "vamsik91/backend-lms"
        //registryCredential = 'dockeruservamsik91'
        //dockerImage = ''
    }

    stages {
        
        stage('login into docker'){
            steps{
                script
                {
                    sh withCredentials([string(credentialsId: 'docker', variable: 'docker')])
                }
            }
        }
       
      
        
// stage('Building the docker image') {
//            steps {
//                sh 'cd api && docker build -t vamsik91/backend-lms .'
//             }
//         }
//         stage('Logging into dockerhub account') {
//             steps {
//                 sh 'echo $DOCKERHUB_CREDENTIALS_PSW | docker login -u $DOCKERHUB_CREDENTIALS_USR --password-stdin'
//             }
//         }
//         stage('pushing the docker image into dockerhub') {
//             steps {
//                   sh 'docker push vamsik91/backend-lms'
//             }
//         }
//         stage('Remove old docker images') {
//              steps {
//                  sh 'docker rmi -f vamsik91/backend-lms'
//             }
//         }
//          stage('creating database container') {
//              steps {
//                  sh 'docker container rm --force lmsdb'
//                  sh 'docker run -d -p 5432:5432 --network lmsnetwork -e  POSTGRES_PASSWORD=password --name lmsdb postgres'
//             }
//         }
//          stage('Running the docker container') {
//             steps {
//                   sh 'docker container rm --force backend'
//                   sh 'docker run -d -p 8080:8080 --network lmsnetwork -e DATABASE_URL=postgresql://postgres:password@lmsdb:5432/postgres --name backend -e PORT=8080 -e MODE=local  mubeen507/backend-lms'
//             }
//         }
//     }
// }
