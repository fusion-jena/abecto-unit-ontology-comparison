# Comparison and Evaluation of Unit Ontologies with ABECTO

This is a project to compare and evaluate unit ontologies using [ABECTO](https://github.com/fusion-jena/abecto).

## Execution

To locally running the project, you first need to checkout ABECTO and this project and to build ABECTO:
```
git clone git@github.com:fusion-jena/abecto.git
mvn -f abecto -B -Dmaven.test.skip=true package
git clone https://github.com/fusion-jena/abecto-unit-ontology-comparison.git
java -jar abecto/target/abecto.jar --trig abecto-unit-ontology-comparison/unit-ontology-comparison-result.trig abecto-unit-ontology-comparison/unit-ontology-comparison.trig
```

## Licenses

* This comparison project is licensed under a [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0)
* [ABECTO](https://github.com/fusion-jena/abecto) is licensed under a [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0)
* The generated result data are derived from the compared ontologies, which are licensed as follows:
	* [OM 2](https://github.com/HajoRijgersberg/OM) by Hajo Rijgersberg, Don Willems, Jan Top ([CC BY 4.0](https://creativecommons.org/licenses/by/4.0/))
	* [QUDT 2](http://qudt.org/) by QUDT.org ([CC BY 4.0](https://creativecommons.org/licenses/by/4.0/))
	* [SWEET 3](https://github.com/ESIPFed/sweet) ([CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/))
	* [Wikidata](https://wikidata.org) ([CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/))
