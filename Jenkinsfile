#agent any is used to execute the code on any available agents
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

#we cannot have wrong label name
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


pipeline {
    agent any
    stages {

        stage ("checkout") {
            
            agent {
                label 'slave1'
            }

         steps {
            echo "This is first stage"
         }   
        }
        
        stage ("build") {

            agent {
                label 'slave1'
            }

            steps {
                echo "This is second stage"
            }

        stage ("Test1") {

            agent {
                label 'slave1'
            }

            steps {
                echo "This is third stage"
            }
        }   
        }
    }
}