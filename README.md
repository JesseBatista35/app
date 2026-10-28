npm test -- --watch=false --code-coverage --browsers=ChromeHeadlessCI ; ng build --configuration production --aot --output-path=dist

-Dproject.settings=NONE -Dsonar.branch.name=$(sonar_branch) -Dsonar.sources=src -Dsonar.tests=src -Dsonar.test.inclusions=**/*.spec.ts -Dsonar.exclusions=**/node_modules/**,**/*.spec.ts -Dsonar.javascript.lcov.reportPaths=`find . -path '*/coverage/*lcov.info' -not -path '*/node_modules/*' | tr '\n' ','`
