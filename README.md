### Oppia-gulp-optimizer [![Build Status](https://travis-ci.org/MAKOSCAFEE/Oppia-gulp-optimizer.svg?branch=master)](MAKOSCAFEE/Oppia-gulp-optimizer)
---

This is a customized gulp for google-app-engine experimenting to optimize the
performance of Oppia.

### Installation
``` npm install -g oppia-gulp ```

# Usage
```javascript
var gulp = require('gulp');
var gae = require('gulp-oppia');

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

For a working example see the `example` folder.
