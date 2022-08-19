# Comparison and Evaluation of Unit Ontologies with ABECTO

This is a project to compare and evaluate the unit ontologies [OM 2](https://github.com/HajoRijgersberg/OM), [QUDT 2](http://qudt.org/), [SWEET 3](https://github.com/ESIPFed/sweet) and [Wikidata](https://wikidata.org) using [ABECTO](https://github.com/fusion-jena/abecto).

## Execution on GitHub Actions

There is a GitHub Actions Workflow configured in [.github/workflows/unit-ontology-comparison.yml](.github/workflows/unit-ontology-comparison.yml) that can be manually started on [Actions > Unit Ontology Comparison](https://github.com/fusion-jena/abecto-unit-ontology-comparison/actions/workflows/unit-ontology-comparison.yml) by users with sufficient privileges. (You might fork this repository, to try it.)

## Execution on Your Machine

To running the project on your machine, please take the following steps:

1. clone and build ABECTO

	```
	git clone --depth 1 -b v1.0.1 git@github.com:fusion-jena/abecto.git
	mvn -f abecto -B -Dmaven.test.skip=true package
	```

2. clone this project

	```
	git clone git@github.com:fusion-jena/abecto-unit-ontology-comparison.git
	```

3. execute the comparison pipeline defined in [unit-ontology-comparison.trig](unit-ontology-comparison.trig)

	```
	java -jar abecto/target/abecto.jar --trig abecto-unit-ontology-comparison/unit-ontology-comparison-result.trig abecto-unit-ontology-comparison/unit-ontology-comparison.trig
	```

4. create several reports

	```
	java -jar abecto/target/abecto.jar --loadOnly --export wdMismatchFinder=abecto-unit-ontology-comparison/unit-ontology-comparison-wdMismatchFinder.csv abecto-unit-ontology-comparison/unit-ontology-comparison-result.trig
	java -jar abecto/target/abecto.jar --loadOnly --reportOn "http://www.ontology-of-units-of-measure.org/resource/om-2/" --export deviations=abecto-unit-ontology-comparison/unit-ontology-comparison-deviations-om2.csv abecto-unit-ontology-comparison/unit-ontology-comparison-result.trig
	java -jar abecto/target/abecto.jar --loadOnly --reportOn "http://qudt.org/" --export deviations=abecto-unit-ontology-comparison/unit-ontology-comparison-deviations-qudt.csv abecto-unit-ontology-comparison/unit-ontology-comparison-result.trig
	java -jar abecto/target/abecto.jar --loadOnly --reportOn "http://sweetontology.net/" --export deviations=abecto-unit-ontology-comparison/unit-ontology-comparison-deviations-sweet.csv abecto-unit-ontology-comparison/unit-ontology-comparison-result.trig
	java -jar abecto/target/abecto.jar --loadOnly --export wdMismatchFinder=abecto-unit-ontology-comparison/unit-ontology-comparison-wdMismatchFinder.csv abecto-unit-ontology-comparison/unit-ontology-comparison-result.trig
	java -jar abecto/target/abecto.jar --loadOnly --export measurementsMarkdown=abecto-unit-ontology-comparison/unit-ontology-comparison-measurementsMarkdown.md abecto-unit-ontology-comparison/unit-ontology-comparison-result.trig
	```

## Licenses

* This comparison project is licensed under a [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0)
* [ABECTO](https://github.com/fusion-jena/abecto) is licensed under a [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0)
* The generated result data are derived from the compared ontologies, which are licensed as follows:
	* [OM 2](https://github.com/HajoRijgersberg/OM) by Hajo Rijgersberg, Don Willems, Jan Top ([CC BY 4.0](https://creativecommons.org/licenses/by/4.0/))
	* [QUDT 2](http://qudt.org/) by QUDT.org ([CC BY 4.0](https://creativecommons.org/licenses/by/4.0/))
	* [SWEET 3](https://github.com/ESIPFed/sweet) ([CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/))
	* [Wikidata](https://wikidata.org) ([CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/))
