pipeline 
{
    agent any
     parameters {
    string(name: 'STATEMENT', defaultValue: 'hello; ls /', description: 'What should I say?')
  }
    stages{
        stage('Git Checkout'){
            steps {
             git 'https://github.com/pallavi-ichake/DeclaretivePipeline.git'
             echo 'This is exaple of Declarative jenkins file which is comman for project'
                  sh("echo ${STATEMENT}")
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
   
