!\[CI/CD Pipeline](https://github.com/Alexandra5150/qa-final-project-java/actions/workflows/ci.yml/badge.svg)





Acesta este un proiect de QA Automation realizat folosind Java, Maven, Docker si GitHub Actions.



Proiectul contine un test API definit in pseudocod, un Dockerfile pentru rularea proiectului cu Maven si un pipeline CI/CD care ruleaza testele si publica imaginea Docker pe Docker Hub.





Testul API este definit in:

src/test/java/com/alexandrabadarau/tests/ApiTest.txt



si verifica endpoint-ul:

GET https://jsonplaceholder.typicode.com/todos/1



Logica testului este organizata folosind principiul Arrange-Act-Assert si verifica:

status code 200

existenta campului title in raspuns



Pentru rularea testelor local, se executa:

mvn test





Docker

Pentru construirea imaginii Docker:

docker build -t qa-final-project-java .



Pentru rularea containerului:

docker run --rm qa-final-project-java



Containerul executa testele Maven folosind:

mvn test

