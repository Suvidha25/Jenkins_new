//agent any is used to execute the code on any available agents
// pipeline {
//     agent any
//     stages {
//         stage ("Checkout SCM") {
//             steps {
//                 echo "This is first stage"
//             }
//         }
//        stage ("Build") {
//             steps {
//                 echo "This is second stage"
//             }
//        }
//     }
// }

//we cannot have wrong label name
// pipeline {
//     agent {
//        label 'slavaf'
//     }

//     stages {
//         stage ("Checkout") {
//             steps {
//                 echo "This is first stage"
//             }
//         }
//     }
    
// }

// pipeline {
//     agent none
//     stages {

//         stage ("Checkout") {
//             agent {
//                 label 'slave1'
//             }

//             steps {
//                 echo "This is first stage"
//             }
//         }

//         stage ("Build") {
//             agent {
//                label 'slave1'
//             }

//             steps {
//                echo "This is second stage"
//             }
//        }
//    }
// }


// pipeline {
//     agent none
//     stages {

//         stage ("checkout") {
            
//             agent {
//                 label 'slave1'
//             }

//          steps {
//             echo "This is first stage"
//          }   
//         }
        
//         stage ("build") {

//             agent {
//                 label 'slave1'
//             }

//             steps {
//                 echo "This is second stage"
//             }
//         }

//         stage ("Test1") {

//             agent {
//                 label 'slave1'
//             }

//             steps {
//                 echo "This is third stage"
//             }
//         }   
//     }
// }


// to run jobs parallely
// pipeline {
//     agent any
//     stages {

//         stage ("Checkout") {
//             steps {
//                 echo "This is first stage"
//             }
//         }

//         stage ('Parallel Building') {
//             parallel {
//                 stage ('Build1') {
//                     steps {
//                         echo "This is Build1 stage"
//                     }
//                 }

//                 stage ('Build2') {
//                     steps {
//                         echo "This is Build2 stage"
//                     }
//                 }
                
//             }
//         }    
//    }
// }


// using parallel jobs for multiple stages
// pipeline {
//     agent any
//     stages {

//         stage ('Parallel checkout') {
//             parallel {
//                 stage('checkout1') {
//                     steps {
//                         echo "This is checkout1 stage"
//                     }
//                 }

//                 stage ('checkout2') {
//                     steps {
//                         echo "This is checkout2 stage"
//                     }
//                 }
//             }
//         }

//         stage ('Parallel Build') {
//             parallel {
//                 stage ('Build1') {
//                     steps {
//                         echo "This is Build1 stage"
//                     }
//                 }

//                 stage ('Build2') {
//                     steps {
//                         echo "This is Build2 stage"
//                     }
//                 }
//             }
//         }
//     }
// }

//How to use shell scripting in jenkins
// pipeline {
//     agent any
//     stages {

//         stage(Checkout) {
//             steps {
//                 echo "This is checkout stage"
//             }
//         }

//         stage ('Build') {
//             steps {
//                 sh 'pwd'
//             }
//         }

//         stage ('Test') {
//             steps {
//                 sh '''pwd
//                 ls -lrt
//                 '''
//             }
//         }
//     }
// }


// pipeline {
//     agent any

//     triggers { 
//         pollSCM('H/2 * * * *') 
//     }

//     stages {

//         stage('Checkout') {
//             steps {
//                echo ""
//             }
//         }

//         stage ('Build') {
//             steps {
//                 sh 'ls -lrt'
//             }
//         }
//     }
// }



// pipeline {
//     agent any

//     environment {
//         APP = 'frontend'
//         ENV = 'prod'
//     }

//     stages {
//         stage('checkout') {
//             steps {
//                 echo "This is checkout stage"
//                 sh '''
//                   echo "APP_TYPE: $APP TARGET_ENV : $ENV"
//                 '''  
//                 sh 'ls -lrt'
//             }
//         }

//         stage ('Build') {
//             steps {
//                 sh '''
//                   echo "APP_TYPE: $APP TARGET_ENV : $ENV"
//                 '''
//                 sh 'pwd'
//             }
//         }
//     }
// }


// pipeline {
//     agent any
//     stages {

//         stage('Checkout') {
//             steps {
//                 catchError(stageResult: 'Failure')
//                 sh 'exit 1'
//             }
//         }

//         stage ('Build') {
//             steps {
//                 echo "This is Build stage"
//             }
//         }    
//     }
// }


// pipeline {
//     agent any

//     environment {
//          FN = 'suvidha'
//          LN = 'hezib'
//     }
//     stages {

//         stage ("SCM Checkout") {
//             steps {
//                 echo "This is checkout stage"
//                 sh '''
//                 echo "First_name: $FN Last_name: $LN"
//                 '''
//             }
//         }  
        
//         stage ("Build") {
//             steps {
//                 echo "This is Build stage"
//                 sh '''
//                 echo "last_name: $LN First_name:$FN"
//                 '''
//             }
//         }
//     }
// }



// pipeline {
//     agent any


//     stages {

//         stage ("SCM Checkout") {
//            environment {
//                FN = 'suvidha'
//                LN = 'hezib'
//             }
//             steps {
//                 echo "This is checkout stage"
//                 sh '''
//                 echo "First_name: $FN Last_name: $LN"
//                 '''
//             }
//         }  
        
//         stage ("Build") {
//             steps {
//                 echo "This is Build stage"
//             }
//         }
//     }
// }


// pipeline {
//     agent any

//     environment {
//          APP = 'frontend'
//          ENV = 'prod'
//     }
//     stages {

//         stage ("SCM Checkout") {
//             steps {
//                 echo "This is checkout stage"
//                 sh '''
//                 echo "APP_TYPE: $APP ENV_Type: $ENV"
//                 '''
//             }
//         }  
        
//         stage ("Build") {
//             steps {
//                 echo "GROOVY ---> APP_TYPE: ${env.APP} ENV_TYPE: ${env.ENV}"

//                 script {
//                     echo "GROOVY ---> APP_TYPE : $APP ENV_TYPE: $ENV"
//                 }                
//             }
//         }
//         stage("Test") {
//             steps {
//                 script {
//                     echo "GROOVY ---> APP_TYPE : ${env.APP} ENV_TYPE: ${env.ENV}"
//                 }
//             }
//         }
//     }
// }




// pipeline {
//     agent any

//     parameters {
//         booleanParam(name : 'Build', defaultValue : 'true', description : 'Do you want to Build?')
//         string(name : 'Branch_Name', defaultValue : 'main', description : 'Enter the branch name to deploy?')
//         choice(name : 'Env_Deploy', choices : ['test', 'QA', 'Stagging', 'Prod'], description : 'Choose the Environment to deploy')
//     }
//     stages {

//         stage("Checkout") {
// //             steps {
//                 echo "Groovy ---> BranchName: ${params.Branch_Name}"

//                 script {
//                     echo "Groovy ---> BranchName: ${params.Branch_Name}"
//                 }

//                 sh '''
//                 echo "Shell ---> BranchName: ${Branch_Name}"
//                 '''
//             }
//         }

//         stage("Build") {
//             steps {
//                 echo "Groovy ---> Build_Type: ${params.Build}"

//                 script {
//                     echo "Groovy ---> Build_Type: ${params.Build}"
//                 }

//                 sh '''
//                 echo "Shell ---> Build_Type: ${Build}"
//                 '''
//             }
//         }


//         stage("Deploy") {
//             steps {
//                 echo "Groovy ---> Deploy_Type: ${params.Env_Deploy}"

//                 script {
//                     echo "Groovy ---> Deploy_Type: ${params.Env_Deploy}"
//                 }

//                 sh '''
//                 echo "Groovy ---> Deploy_Type: ${Env_Deploy}"
//                 '''
//             }
//         }
//     }
// }


// boolean runStage1 = False

// pipeline {
//     agent any

//     stages {
//         stage (stage1) {
//             when expression(runStage1 == True)

//            steps {

//            }   
//         }
//     }
// }


pipeline {
   agent any
   parameters {
           booleanParam(name : 'Build', defaultValue : 'true', description : 'Do you want to Build?')
           choice(name : 'Env_Deploy', choices : ['test', 'QA', 'Prod'], description : 'Choose the Environment to deploy')
     }
     stages {

         stage("Checkout") {
              when {
                  branch 'main'
              }  
             steps {
                checkout scmGit
                (branches: [[name: '*/main']], 
                extensions: [], 
                userRemoteConfigs: [[credentialsId: 'aws_pem', 
                url: 'https://github.com/Suvidha25/Jenkins_new.git']])
                branch : 'main'    
                }
            }
        

        stage("Build") {
            steps {
                echo "Groovy ---> Build_Type: ${params.Build}"

                script {
                    echo "Groovy ---> Build_Type: ${params.Build}"
                }

                sh '''
                echo "Shell ---> Build_Type: ${Build}"
                '''
            }
        }


        stage("Deploy") {
            steps {
                echo "Groovy ---> Deploy_Type: ${params.Env_Deploy}"

                script {
                    echo "Groovy ---> Deploy_Type: ${params.Env_Deploy}"
                }

                sh '''
                echo "Groovy ---> Deploy_Type: ${Env_Deploy}"
                '''
            }
        }
    } 
}