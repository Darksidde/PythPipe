pipeline {
    agent any
    stages {
        stage('Setup') {
            steps {
                // Sanal ortam oluşturma veya Python sürümünü belirleme (varsayılan olarak Jenkins sunucusunda yüklü ise)
                script {
                    sh 'python --version' // Python sürümünü kontrol etme
                }
            }
        }
        stage('Test') {
            steps {
                // Pytest'in yüklü olup olmadığını kontrol etme ve test senaryolarını çalıştırma
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
