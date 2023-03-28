1. Initiall performance was 16.
2.  Added some compression to `server.js`. 
    Put const 
    ```
      compression = require('compression');
      app.use(compression());
     ```
    before `app.use(express.static('build'))`.

After that performance changed to 23.

3. In `src/model.js`, replace `const dir = 'big'` with `const dir = 'small'`

   After that performance is changed to 30.

4. Delete unused scripts `<script src="/libs/lodash.js">` and `<script src="/libs/jquery.js"></script>` from template.html

After that performance is changed to 31.

5. In `webpack.config.js` change `"mode":"development"` to `"mode":"production"`.

After that performance is changed to 43.

6. In `src/App.jsx` remove the call to `this.mineBitcoin(1500)` in the `constructor` and `mineBitcoin` method

After that performance is changed to 98.