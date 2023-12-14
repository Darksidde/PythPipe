pipeline {
    agent {
        docker {
            image 'alpine' // veya uygun Docker imajı
        }
    }
    stages {
        stage('Setup') {
            steps {
                script {
                    sh 'python --version' // Python sürümünü kontrol etme
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    sh 'pip show pytest || pip install pytest' // Pytest'in yüklü olup olmadığını kontrol etme
                    sh 'python -m pytest calculator.py' // Test senaryolarını çalıştırma
                }
            }
        }
        stage('Deploy') {
            steps {
                // Uygulamanın dağıtımı için gereken adımlar (isteğe bağlı)
            }
        }
    }
}
