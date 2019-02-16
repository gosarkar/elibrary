pipeline{
    //agent{
        //label "node"
    //}
    agent any
    
    environment{
        groovyHome = tool name: 'Groovy', type: 'hudson.plugins.groovy.GroovyInstallation'
    }

    stages{
        stage("A"){
            steps{
                echo "========executing A========"
                bat groovyHome+'/bin/groovy C:/GS/Practise/Jenkins/script1'
                
            }
            post{
                always{
                    echo "========always========"
                }
                success{
                    echo "========A executed successfully========"
                }
                failure{
                    echo "========A execution failed========"
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