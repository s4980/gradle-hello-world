node('gradle-agent') {
  echo "Pulling from SCM"
  checkout scm
  input 'Ready to go?'
      new File("test").eachFile() { file->  
        println file.getName()  
    }  
  echo "Building projec using Gradle"
  gradle helloWorld
  echo "Finished"
}
