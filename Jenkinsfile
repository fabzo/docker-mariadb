node {
    milestone 100
    stage('Checkout and Build') {
        checkout scm
        sh "docker build -t eu.gcr.io/rewedigital-refill-int-v001/mariadb-delivery ."
    }
}

node {
    milestone 110
    stage('Push') {
        checkout scm
        sh "gcloud docker -- push eu.gcr.io/rewedigital-refill-int-v001/mariadb-delivery"
    }
}
