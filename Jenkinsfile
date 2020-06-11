pipeline {
    agent any

//    environment{
//        //my_tag = "c:\\temp"
//        //my_tag = my_tag
//    }

    stages{
        stage('Build'){
            steps{
                sh 'mvn clean package'
                //sh "docker build . -t tomcatwebapp:${env.BUILD_ID}"
                //sh "echo ${my_tag}"
            }

        }
    }
}
