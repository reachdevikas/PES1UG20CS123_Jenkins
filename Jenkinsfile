pipeline {
  agent any
  
  
  stages {
    stage('Build')
    {
      steps
      {
        sh 'g+ -o cs123 cs123_task5.cpp'
      }
    }
    stage('Test')
    {
      steps
      {
        sh './cs123'
      }
    }
    stage('Deploy')
    {
      steps
      {
        echo 'Successfully deployed ---PES1UG20CS123'
      }
    }
  }
  
  post
  {
    always
    {
      script
      {
        if (currentBuild.result == 'FAILURE')
        {
          echo 'Pipeline failed!!'
        }
      }
    }
  }
}
