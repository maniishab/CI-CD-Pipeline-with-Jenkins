pipeline {
    agent any

    stages {

        stage('Clone Repository') {
            steps {
                 git branch:'main', url:'https://github.com/maniishab/CI-CD-Pipeline-with-Jenkins.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'pip3 install -r requirements.txt'
            }
        }

        stage('Run Tests') {
            steps {
                sh 'pytest'
            }
        }

        stage('Deploy Application') {
            steps {
                sh 'python3 app.py &'
            }
        }

    }
}
