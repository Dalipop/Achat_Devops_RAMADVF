pipeline {
    
    agent any


    stages {
        stage('Get prject from GIT') {
            steps {
                // Get some code from a GitHub repository
                git branch: 'Amir-Ayed', credentialsId: 'd9c3df91-0beb-4636-ae2a-8d1724af1e38', url: 'https://github.com/molka777/Achat_Devops_RAMAD.git'
            }

            post {
                success {
                    echo 'Récupération done'
                }
            }
        }
        
        stage('Maven Clean') {
            steps {
                sh 'mvn clean'
            }
        }

        stage('Maven Compile'){
            steps {
                sh 'mvn compile -DskipTests'
            }
        }
        
        stage('Les tests unitaires') {
            steps {
                sh 'mvn test'
            }
        }
        
        stage('SonarQube Tests') {
            steps {
                sh "sonar:sonar"
            }
        }
        
        stage('Déposer le livrable sur Nexus') {
            steps {
                echo "stage 3"
            }
        }
        
        stage('Build de l’image (partie spring)') {
            steps {
                echo "stage 4"
            }
        }
        
        stage('Création du livrable Spring à partir du fichier DockerFile') {
            steps {
                echo "stage 5"
            }
        }
        
        stage('Déposer l\'image créée sur DockerHub') {
            steps {
                echo "stage 6"
            }
        }
        
        stage('Lancer simultanément les images avec docker-compose') {
            steps {
                echo "stage 7"
            }
        }
        
        stage('Tester les services avec Postman ou Swagger') {
            steps {
                echo "stage 8"
            }
        }
        
        stage('Superviser les outils avec Prometheus et Grafana') {
            steps {
                echo "stage 9"
            }
        }
    }
}
