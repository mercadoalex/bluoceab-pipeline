pipeline {
  agent any
  stages {
    stage('buid') {
      steps {
        echo 'Etapa de construccion'
        sh '''sleep 5
echo Exito!'''
      }
    }

    stage('test') {
      steps {
        echo 'Etapa de prueba'
        sh "chmod +x -R ${env.WORKSPACE}"
        sh './while_example.sh'
      }
    }

    stage('staging') {
      steps {
        echo 'Etapa de  consolidacion'
      }
    }

    stage('deploy') {
      steps {
        echo 'Etapa de entrega'
      }
    }

  }
}