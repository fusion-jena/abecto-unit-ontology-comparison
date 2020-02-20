[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/fusion-jena/abecto-unit-ontology-comparison.git/master?filepath=abecto-unit-ontology-comparison.ipynb)

# Comparison and Evaluation of Unit Ontologies with ABECTO

This is a [ABECTO](https://github.com/fusion-jena/abecto) project to compare and evaluate unit ontologies.

## Execution
You can [use Binder to execute the project online](https://mybinder.org/v2/gh/fusion-jena/abecto-unit-ontology-comparison.git/master?filepath=abecto-unit-ontology-comparison.ipynb).

To locally running the project, you first need to checkout the project including subproject and compile ABECTO:
```
git clone https://github.com/fusion-jena/abecto-unit-ontology-comparison.git
mvn -f abecto-unit-ontology-comparison/abecto -B -Dmaven.test.skip=true install
```
Then open the notebook:
```
jupyter notebook abecto-unit-ontology-comparison/abecto-unit-ontology-comparison.ipynb
```

## Licenses

* [ABECTO](https://github.com/fusion-jena/abecto) is licensed under the [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0)
* This comparison project, excluding ontology files in [ontology/](ontology/) and derived data in [.abecto/](abecto/), is licensed under the [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0)
* The ontologies in [ontology/](ontology/) and the respective derived data in [.abecto/](abecto/) are licensed as follows:
	* [OM 2](https://github.com/HajoRijgersberg/OM) by Hajo Rijgersberg, Don Willems, Jan Top ([CC BY 4.0](https://creativecommons.org/licenses/by/4.0/))
	* [QUDT 2](http://qudt.org/) by QUDT.org ([CC BY 4.0](https://creativecommons.org/licenses/by/4.0/))
	* [SWEET 3](https://github.com/ESIPFed/sweet) is licensed under the [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0)
