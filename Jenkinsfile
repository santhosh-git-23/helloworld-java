pipeline {
  agent {
    label "test"
  }
  stages {
    stage('Cloning Git') {
      steps {
        git([url: 'https://github.com/santhosh-git-23/helloworld-java.git', branch: 'master'])
       }
    }
    stage ('jar executinon') {
      steps{
        echo "Compiling ... "
        sh 'javac HelloWorld.java'
        echo "Execution ..."
        sh 'java HelloWorld'
        sh 'jar cvfe HelloWorld.jar HelloWorld *.class'
        echo "============================"
        sh 'java -jar HelloWorld.jar'
        echo "============================"
      }
    }
  }
}
