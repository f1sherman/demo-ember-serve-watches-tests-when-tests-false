# demo-ember-serve-watches-tests-when-tests-false

Sample app for reproduction of https://github.com/ember-cli/ember-cli/issues/8173

To reproduce:
1. Clone this repository
2. `npm install ember@3.5.0`
3. `ember serve`
4. (In another terminal session once `ember serve` has completed building) `touch tests/unit/routes/demo-test.js`
5. Note that the `ember serve` process rebuilds even though `tests: false` in `ember-cli-build.js`
