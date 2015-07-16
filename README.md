#***DEPRECATED***

If you want to download a file with gulp, just `npm install --save-dev request vinyl-source-stream` and put this in your gulpfile:

    var request = require('request');
    var source = require('vinyl-source-stream');
    
    request(url)
        .pipe(source('filename.txt'))
        .pipe(gulp.dest('downloads'));
