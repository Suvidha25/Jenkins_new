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


pipeline {
    agent {
        label 'slave1'
    }

    stages {
        stage ("Checkout") {
            steps {
                echo "This is first stage"
            }
        }
    }
    
}


