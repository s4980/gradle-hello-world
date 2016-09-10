node('gradle-agent') {
  echo pwd()
  echo "Pulling from SCM"
  checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: '3ef76e85-9aad-4448-9c46-36ceda327dae', url: 'git@github.com:s4980/gradle-hello-world.git']]])
  echo fileExists './build.gradle'
  input message: 'Do you accept', ok: 'Yes'
  echo "Building projec using Gradle"
  gradle helloWorld
  echo "Finished"
}
