pipeline{
    agent none
    stages{
        stage('Build jobs'){
            parallel{
                stage('server-0'){
                    agent{label 'ubuntu-slave-0'}
                    steps{
                        build job: "server-slave-0", wait: true
                    }
                }
                stage('server-1'){
                    agent{label 'ubuntu-slave-1'}
                    steps{
                        build job: "server-slave-1", wait: true
                    }
                }
                stage('server-2'){
                    agent{label 'ubuntu-slave-2'}
                    steps{
                        build job: "server-slave-2", wait: true
                    }
                }
                stage('server-3'){
                    agent{label 'ubuntu-slave-3'}
                    steps{
                        build job: "server-slave-3", wait: true
                    }
                }
                stage('server-4'){
                    agent{label 'ubuntu-slave-4'}
                    steps{
                        build job: "server-slave-4", wait: true
                    }
                }
                stage('server-5'){
                    agent{label 'ubuntu-slave-5'}
                    steps{
                        build job: "server-slave-5", wait: true
                    }
                }
            }
        }
    }
}