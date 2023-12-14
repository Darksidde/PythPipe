pipeline {
    agent any
    stages {
        stage('Setup') {
            steps {
                script {
                    sh 'python --version' // Python sürümünü kontrol etme
                    sh 'pip install -r requirements.txt' // requirements.txt'deki bağımlılıkların yüklenmesi
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
                // Örneğin, bu aşamada bir sunucuya kopyalama veya Docker imajının oluşturulması gibi işlemler olabilir
            }
        }
    }
}
