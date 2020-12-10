pipeline {
agent any
environment {
dotnet = 'path\\to\\dotnet.exe'
}
stages {
stage ('Checkout') {
            steps {
                 git url: 'https://github.com/arjunachari12/pipelines-dotnet-core',branch: 'master'
            }
}
stage ('Restore PACKAGES') {     
         steps {
             bat "dotnet restore"
          }
        }

stage('Build') {
     steps {
            bat 'dotnet build'
      }
   }
   stage('Publish') {
     steps {
           bat 'dotnet publish'
      }
   }

 }
}
