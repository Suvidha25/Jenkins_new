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


// pipeline {
//     agent {
//         label 'slavaf'
//     }

//     stages {
//         stage ("Checkout") {
//             steps {
//                 echo "This is first stage"
//             }
//         }
//     }
    
// }

pipeline {
    agent none
    stages {

        stage ("Checkout") {
            agent {
                label 'slave1'
            }

            steps {
                echo "This is first stage"
            }
        }

        stage ("Build") {
            agent {
               label 'slave1'
            }

            steps {
               echo "This is second stage"
            }
       }
   }
}