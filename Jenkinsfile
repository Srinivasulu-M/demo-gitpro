def git_branch = "${env.GIT_BRANCH}"
def git_commit = "${env.GIT_COMMIT}"
def job_url = "${env.JOB_URL}"
pipeline {
         agent any
         stages {
                 stage('generating env variables') {
                 steps {
                          echo "this is build number ${env.BUILD_NUMBER}"
                          echo "this is build url ${env.BUILD_URL}"
                          echo "this is build id ${env.BUILD_ID}"
                          echo "this is git url ${env.GIT_URL}"
                          echo "branch name is ${env.GIT_COMMIT}"
                          echo "branch name is ${env.GIT_BRANCH}"
                 }
                 }
                  stage('Two') {
                 steps {
                          echo "git branch is: $git_branch"
                          echo "git_commit is: $git_commit"
                          echo "job url is : $job_url"
                    input('Do you want to proceed?')
                 }
                 }
                 stage('Three') {
                 when {
                       not {
                            branch "master"
                       }
                 }
                 steps {
                       echo "Hello"
                 }
                 }
                 }
          }
