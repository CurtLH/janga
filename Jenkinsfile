pipeline {
    agent condaforge/linux-anvil-comp7
    stages {
        stage('create-env') {
            steps {
                sh """#!/bin/bash -il
                   conda env update -f environment.yml
                   conda activate janga-env 
                   """
            }
        }
        stage('build-docs') {
            steps {
                sh """#!/bin/bash -il
                   make html
                   """
            }
        }
    }
}