gulp-gae
========
This is a customized gulp for google-app-engine experimenting to optimize the
performance of Oppia.
# Usage
```javascript
var gulp = require('gulp');
var gae = require('../');

gulp.task('oppia-serve', function() {
  gulp.src('app/app.yaml')
    .pipe(gae('dev_appserver.py', [], {
      admin_host: '0.0.0.0',
      admin_port: 8001,
      host: '0.0.0.0',
      port: 8181
    }));
});

gulp.task('default', ['gae-serve']);

```

For a working example see the `test` folder.