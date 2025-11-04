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
                bat 'dir'
                echo "✅ Repository checkout complete!"
            }
        }

        stage('Initialize Environment') {
            steps {
                echo "⚙️ Setting up build environment..."
                bat 'echo Preparing workspace...'
            }
        }

        stage('Build Simulation') {
            parallel {
                stage('Compile Module A') {
                    steps {
                        echo "🧩 Compiling Module A..."
                        bat 'ping -n 3 127.0.0.1 >nul'
                        echo "✅ Module A compiled!"
                    }
                }
                stage('Compile Module B') {
                    steps {
                        echo "🧩 Compiling Module B..."
                        bat 'ping -n 3 127.0.0.1 >nul'
                        echo "✅ Module B compiled!"
                    }
                }
            }
        }

        stage('Testing Phase') {
            steps {
                echo "🧪 Running simulated tests..."
                bat 'ping -n 3 127.0.0.1 >nul'
                echo "✅ All tests passed successfully!"
            }
        }

        stage('Post-Build Analysis') {
            steps {
                echo "📊 Running post-build checks..."
                bat 'echo Checking build artifacts...'
                echo "✅ Analysis complete!"
            }
        }

        stage('Deploy Simulation') {
            steps {
                echo "🚀 Simulating deployment..."
                bat 'ping -n 3 127.0.0.1 >nul'
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
