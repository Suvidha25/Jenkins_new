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


pipeline {
    agent any
    stages {

        stage(Checkout) {
            steps {
                echo "This is checkout stage"
            }
        }

        stage ('Build') {
            steps {
                sh 'pwd'
            }
        }

        stage ('Test') {
            steps {
                echo "This is test stage"
            }
        }
    }
}