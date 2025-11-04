pipeline {
    agent any

    environment {
        AUTHOR = "Anannya"
        PROJECT = "DevOps CI Pipeline"
    }

    stages {
        stage('Declarative: Checkout SCM') {
            steps {
                echo "🔹 Checking out repository for ${PROJECT} by ${AUTHOR}..."
                sh 'ls -l'
                echo "✅ Repository checkout complete!"
            }
        }

        stage('Initialize Environment') {
            steps {
                echo "⚙️ Setting up build environment..."
                sh 'echo Preparing workspace...'
            }
        }

        stage('Build Simulation') {
            parallel {
                stage('Compile Module A') {
                    steps {
                        echo "🧩 Compiling Module A..."
                        sh 'sleep 2'
                        echo "✅ Module A compiled!"
                    }
                }
                stage('Compile Module B') {
                    steps {
                        echo "🧩 Compiling Module B..."
                        sh 'sleep 2'
                        echo "✅ Module B compiled!"
                    }
                }
            }
        }

        stage('Testing Phase') {
            steps {
                echo "🧪 Running simulated tests..."
                sh 'sleep 2'
                echo "✅ All tests passed successfully!"
            }
        }

        stage('Post-Build Analysis') {
            steps {
                echo "📊 Running post-build checks..."
                sh 'echo Checking build artifacts...'
                echo "✅ Analysis complete!"
            }
        }

        stage('Deploy Simulation') {
            steps {
                echo "🚀 Simulating deployment..."
                sh 'sleep 2'
                echo "✅ Deployment simulated successfully!"
            }
        }
    }

    post {
        always {
            echo "📜 Build completed by ${AUTHOR}."
        }
        success {
            echo "🎉 Pipeline executed successfully!"
        }
        failure {
            echo "❌ Pipeline failed — check console logs."
        }
    }
}
