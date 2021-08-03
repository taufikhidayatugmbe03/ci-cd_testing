//Testing to know changes on jenkins
pipeline {
    agent any
    stages {
       stage('BUILD') {
          steps {
             echo 'Notify GitHUb'
             updateGitlabCommitStatus name: 'build', state: 'pending'
             echo 'build step goes here'
             updateGitlabCommitStatus name: 'build', state: 'success'
          }
       }
       stage('TEST') {
           steps {
               echo 'Notify GitHub'
               updateGitlabCommitStatus name: 'test', state: 'pending'
               echo 'test step goes here'
               updateGitlabCommitStatus name: 'test', state: 'success'

           }
       }
    }
 }
