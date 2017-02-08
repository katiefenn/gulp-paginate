# gulp-paginate
A Gulp plugin for collating multiple files into one or more pages. Files piped into this plugin are held until the number of articles reaches an optional amount of files. Content is then piped out into a new file with incrementing file names.

## Installation
This package is installed using [npm](https://www.npmjs.com/):

```
npm install gulp-paginate
```

## Options
### itemsPerPage
Determines the maximum number of files to collate onto a single page.

## Examples
```
// articles/article1.html
// articles/article2.html
// articles/article3.html
// articles/article4.html

gulp.task('index-pages', function() {
  return gulp.src('articles/*')
    .pipe(paginate(3))
    .pipe(gulp.dest('./dist'));
});

// Out:
// dist/1.html
// dist/2.html
