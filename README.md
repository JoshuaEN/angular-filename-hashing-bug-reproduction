# AngularBugReportMinimalExample

1. Run `npm ci` to install dependencies.

2. Run `ng build --configuration=production` (with the default `es2017` target in `tsconfig.json`).

3. Observe the contents of the output `dist/angular-filename-hashing-bug-reproduction/scripts.{revhash_1}.js` file to be `try{console.log()}catch(c){}`.

4. Change the `compilerOptions.target` to `es2019` (or `es2020` or `es2021`) from `es2017` in `tsconfig.json`.

5. Run `ng build --configuration=production`.

6. Observe the contents of the output `dist/angular-filename-hashing-bug-reproduction/scripts.{revhash_2}.js` file to be `try{console.log()}catch{}` (different from the output from step 3).

7. Observe that `revhash_1` equals `revhash_2`.
