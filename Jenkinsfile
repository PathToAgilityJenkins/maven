pipeline 
{
  agent any
  
  stages 
  {
    stage('Build') 
    {
      steps 
      {
        dir(path: 'maven') 
        {
          withMaven(maven: 'Maven 3.5.0') 
          {
            sh 'mvn package'
          }
        }
      }
    }
    
    stage('Document') 
    {
      steps 
      {
        dir(path: 'maven') 
        {
          withMaven(maven: 'Maven 3.5.0') 
          {
            sh 'mvn site:site'
          }
        }
      }
    }
    
    stage('Analyze') 
    {
      steps 
      {
        echo 'Perform code analysis here.'
      }
    }
    
    stage('Deploy') 
    {
      steps 
      {
        echo 'Perform automated deployment here.'
      }
    }
    
    stage('Test') 
    {
      steps 
      {
        echo 'Perform automated functional tests here.'
      }
    }
  }
  
  post
  {
  	unstable
  	{
  		echo 'Unit tests failed.'
  	}
  }
}