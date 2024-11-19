pipeline 
{
    agent any
    
    stages{
        stage('Git Checkout'){
            steps {
             git 'https://github.com/pallavi-ichake/DeclaretivePipeline.git'
             echo 'This is exaple of Declarative jenkins file which is comman for project'
                 
            }
         }
            
         stage('Deploy') 
         {
            when {
              expression {
                currentBuild.result == null || currentBuild.result == 'SUCCESS' 
                echo 'Updated from eclipse'
                         }
                  }
            steps {
                sh 'make publish updtaed result'
               
                  }
           }
        }
    }
   
