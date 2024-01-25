pipeline { 

    agent any  

     

    environment { 

        def myString = 'https://github.com/EmeliePozzi/fooproject.git' 

    } 

  

    stages { 

        stage('Git') { 

            steps { 

                echo "myString : ${myString}" 

            } 

        } 

  

        stage('Build') { 

            steps { 

                bat "mvn compile" 

            } 

        }   

  

        stage('Test') { 

            steps { 

                bat "mvn test" 

            } 

            post { 

                always { 

                    junit '**/TEST*.xml' 

                } 

            } 

        } 

    } 

} 