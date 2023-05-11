pipeline {
  agent {
    label "test"
  }
  tools{
    jdk 'jdk'
  }
  stages {
    stage('Cloning Git') {
      steps {
        git([url: 'https://github.com/santhosh-git-23/helloworld-java.git', branch: 'main'])
       }
    }
    stage ('jar execution') {
      steps{
        echo "Compiling ... "
        sh 'javac HelloWorld.java'
        echo "Execution ..."
        //sh 'java HelloWorld'
        sh 'jar cvfe HelloWorld.jar HelloWorld *.class'
        echo "============================"
        sh 'java -jar HelloWorld.jar'
        echo "============================"
      }
    }
  }
}
