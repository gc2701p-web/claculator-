pipeline{
  agent any
  stages{
    stage('clone'){
      steps{
        git branch:'https://github.com/gc2701p-web/claculator-.git';
      }
    }
    stage('compile'){
      steps{
        sh'javac Calculator.java'
      }
    }
    stage('build'){
      steps{
        sh'java Calculator 25 5'
      }
    }
    stage('test'){
      steps{
        sh'java Calculator 30 5'
      }
    }
  }
}
