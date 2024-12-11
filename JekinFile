pipeline{
    agent any
    stages{
        stage(git){
            steps {
            git branch: 'main', url: 'https://github.com/srilekha2831/jen.git'
        }
        }
        stage(compile){
            steps{
                sh 'mvn compile'
            }
            }
            stage(test){
                steps{
                    sh 'mvn test'
                }
            }
            stage(validate){
                steps{
                    sh 'mvn validate'
                }
            }
            stage(qa){
                steps{
                    sh 'mvn pmd:pmd'
                }
            }
            stage(pack){
                steps{
                    sh 'mvn package'
                }
            }
}
}
