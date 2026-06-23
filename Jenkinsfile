cat > Jenkinsfile <<'EOF'
@Library('gradle-lib') _

pipeline {
agent any

```
stages {
    stage('Checkout') {
        steps {
            checkout scm
        }
    }

    stage('Prepare') {
        steps {
            sh 'chmod +x gradlew'
        }
    }

    stage('Build') {
        steps {
            gradleBuild()
        }
    }

    stage('Unit Test') {
        steps {
            gradleTest()
        }
    }
}
```

}
EOF
