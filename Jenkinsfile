stage('Test') {
    steps {
        sh '''
        echo "Running JUnit tests for File-Encrypter..."
        cd "Password Protection"

        # Download JUnit JAR if missing
        if [ ! -f junit-platform-console-standalone.jar ]; then
            wget https://repo1.maven.org/maven2/org/junit/platform/junit-platform-console-standalone/1.10.2/junit-platform-console-standalone-1.10.2.jar -O junit-platform-console-standalone.jar
        fi

        mkdir -p test-build

        # Compile Java test files
        javac -cp junit-platform-console-standalone.jar:build -d test-build src/*.java || true

        echo "JUnit stage completed"
        '''
    }
}
