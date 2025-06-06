pipeline{
  agent any
  tools{
    jdk 'jdk'
    maven 'maven'
  }
  stages{
    stage('checkout'){
      git branch: 'master', url: 'https://github.com/Megharaj2004/AnsibleApp.git'
    }
    stage('build'){
      sh 'mvn clean package'
    }
    stage('deploy'){
      sh 'sudo ansible-playbook Ansible/playbook.yml -i Ansible/hosts.ini'
    }
  }
}
