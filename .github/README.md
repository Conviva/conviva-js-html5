# conviva-js-html5
Conviva HTML5 Video Element module auto-detects events emitted by HTML5 and &lt;video&gt; tag (HTMLVideoElement).

## Offline Library
The Conviva JavaScript HTML5 Video Element module is built on top of <a href="https://github.com/Conviva/conviva-js-coresdk">conviva-core-sdk</a>, is shared as offline library and should be included via the <script> tag in the application.

Via html:
```
<script type="text/javascript" src="<PATH>/conviva-core-sdk.js"></script>
<script type="text/javascript" src="<PATH>/conviva-html5native-impl.js"></script>
```

## Install via npm 

```
npm install @convivainc/conviva-js-html5 --save
```

## Install via yarn 

```
yarn add @convivainc/conviva-js-html5
```
Refer to following sample code to include HTML5 Video Element components followed by Conviva modules.

Via import/require:
```
import Conviva from '@convivainc/conviva-js-coresdk'
import ConvivaHtml5Module from'@convivainc/conviva-js-html5'
```
```
const Conviva = require('<path>/conviva-js-coresdk');
const ConvivaHtml5Module = require('<path>/conviva-js-html5');
```


## Note:
* Refer https://community.conviva.com/ for integration guidelines.
