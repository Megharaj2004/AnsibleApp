pipeline{
  agent any
  tools{
    jdk 'jdk'
    maven 'maven'
  }
  stages{
    stage('checkout'){
      steps{
      git branch: 'master', url: 'https://github.com/Megharaj2004/AnsibleApp.git'
    }
    }
    stage('build'){
      steps{
      sh 'mvn clean package'
    }
    }
    stage('deploy'){
      steps{
      sh 'sudo ansible-playbook Ansible/playbook.yml -i Ansible/hosts.ini'
    }
    }
  }
}
