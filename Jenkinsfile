pipeline {
  agent any

  environment{
    JAVA_HOME= "/usr/lib/jvm/java-1.8.0-openjdk-1.8.0.252.b09-2.el7_8.x86_64"
    M2_HOME = "/opt/maven/apache-maven-3.6.1"
    M2 = "$M2_HOME/bin"
    PATH = "$JAVA_HOME/bin:$M2_HOME:$M2:$PATH"
  }

  stages{
    stage('Build'){
      steps{
        sh 'mvn clean package'
        sh "docker build . -t tomcatwebapp:${env.BUILD_ID}"
        //sh "echo ${my_tag}"
      }

    }
  }
}
