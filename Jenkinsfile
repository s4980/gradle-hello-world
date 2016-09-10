node('gradle-agent') {
  echo "Pulling from SCM"
  checkout scm
  input 'Ready to go?'
  echo "Building projec using Gradle"
  gradle helloWorld
  echo "Finished"
}
