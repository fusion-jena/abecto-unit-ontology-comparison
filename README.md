[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/fusion-jena/abecto-unit-ontology-comparison.git/master?filepath=abecto-unit-ontology-comparison.ipynb)

# Comparison and Evaluation of Unit Ontologies with ABECTO

This is a project to compare and evaluate unit ontologies using  [ABECTO](https://github.com/fusion-jena/abecto).

## Execution
You can [use Binder to execute the project online](https://mybinder.org/v2/gh/fusion-jena/abecto-unit-ontology-comparison.git/master?filepath=abecto-unit-ontology-comparison.ipynb).

To locally running the project, you first need to checkout the project including subproject and compile ABECTO:
```
git clone --recursive https://github.com/fusion-jena/abecto-unit-ontology-comparison.git
mvn -f abecto-unit-ontology-comparison/abecto -B -Dmaven.test.skip=true install
```
Then open the notebook:
```
jupyter notebook abecto-unit-ontology-comparison/abecto-unit-ontology-comparison.ipynb
```

## Licenses

* [ABECTO](https://github.com/fusion-jena/abecto) is licensed under the [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0)
* This comparison project, excluding the data derived from the compared ontologys in [.abecto/](abecto/), is licensed under the [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0)
* The data in [.abecto/](abecto/) are derived from the compared ontologies, which are licensed as follows:
	* [OM 2](https://github.com/HajoRijgersberg/OM) by Hajo Rijgersberg, Don Willems, Jan Top ([CC BY 4.0](https://creativecommons.org/licenses/by/4.0/))
	* [QUDT 2](http://qudt.org/) by QUDT.org ([CC BY 4.0](https://creativecommons.org/licenses/by/4.0/))
	* [SWEET 3](https://github.com/ESIPFed/sweet) is licensed under the [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0)
