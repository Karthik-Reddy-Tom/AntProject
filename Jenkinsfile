pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(Ant : 'Ant 1_10_5') {
                    sh 'Ant compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(Ant : 'Ant 1_10_5') {
                    sh 'Ant dist'
                }
            }
        }


        stage ('Deployment Stage') {
            steps {
                withMaven(Ant : 'Ant 1_10_5') {
                    sh 'Ant deploy'
                }
            }
        }
    }
}