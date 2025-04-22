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



pipeline {
    agent any
    stages {

        stage ("Checkout") {
            steps {
                echo "This is first stage"
            }
        }

        stage ('Build') {
            steps {
                echo "This is second stage"
            }
        } 

        stage ('Parallel Testing') {
            parallel {
                stage ('Test1') {
                    steps {
                        echo "This is Test1 stage"
                    }
                }

                stage ('Test2') {
                    steps {
                        echo "This is Test2 stage"
                    }
                }
                
            }
        }    
   }
}