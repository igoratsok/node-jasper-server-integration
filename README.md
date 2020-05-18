# JasperServer Integration
JSIntegration is a node module that quickly integrates node.js to Jasper Server.

# Usage
Usage is quite simple:
```javascript
var JSIntegration = require('./JSIntegration.js');

var jsIntegration = new  JSIntegration(
  'http://localhost:8080/jasperserver', // URL of the Jasper Server
  'reports/my_report_unit',             // Path to the Report Unit
  'pdf',                                // Export type
  'jasperadmin',                        // User
  'jasperadmin',                        // Password
  {"P_ID_ALUNO" :  1}                   // Optional parameters
);

var data = jsIntegration.execute()
  .then((data) => {
  // Do whatever you want with the binary data
  console.log(data);
  })

  .catch((error) => {
  console.log(error);
  });
```
