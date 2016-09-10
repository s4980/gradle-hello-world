node('gradle-agent') {
  stage ('Validation') {
  }
  stage ('SCM checkout') {
  echo "Pulling from SCM"
  // checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: '3ef76e85-9aad-4448-9c46-36ceda327dae', url: 'git@github.com:s4980/gradle-hello-world.git']]]) 
  checkout scm
  }
  stage ('Workspace validation') {
  input message: 'Do you accept', ok: 'Yes'
  }
  stage ('Build') {
  echo "Building projec using Gradle"
  gradle "-q helloWorld"
  echo "Finished"
  }
}

def gradle(args) {
    sh "gradle ${args}"
}
