pipeline {

    agent any



    stages {

        stage('Clone repo') {

            steps {

                git branch: 'main',

                    credentialsId: 'github-ssh-key',

                    url: 'git@github.com:ziedbouafif/node_test.git'

            }

        }



        stage('Run Ansible Role') {

            steps {

                sh '''

                    cd ansible_node_exporter_role/ansible

                    ansible-playbook playbook.yml -i inventory.ini

                '''

            }

        }

    }

}


