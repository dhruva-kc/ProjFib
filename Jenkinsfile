#!/usr/bin/env groovy

pipeline{
    agent{
        label "devops1"
    }
    stages{
        stage("STAGE-1"){
            steps{
                echo "Hello World!"
            }
            post{
                success{
                    echo "========STAGE-1 executed successfully========"
                }
                failure{
                    echo "========STAGE-1 execution failed========"
                }
            }
        }
        stage("STAGE-2"){
            steps{
                echo "Hi There!"
            }
            post{
                success{
                    echo "========STAGE-2 executed successfully========"
                }
                failure{
                    echo "========STAGE-2 execution failed========"
                }
            }
        }
    }
    post{
        always{
            echo "========always========"
        }
        success{
            echo "========pipeline executed successfully ========"
        }
        failure{
            echo "========pipeline execution failed========"
        }
    }
}