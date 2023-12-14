pipeline {
    agent any
    stages {
        stage("Setup") {
            steps {
                // Eğer gerekli ise: Virtual environment oluşturulması veya Python sürümü belirleme
                sh 'python --version' // Python sürümünü kontrol etme
            }
        }
        stage("Test") {
            steps {
                sh 'python -m pytest calculator.py' // Test senaryolarının çalıştırılması
            }
        }
        stage("Deploy") {
            steps {
                // Uygulamanın dağıtımı için gereken adımlar (isteğe bağlı)
            }
        }
    }
}
