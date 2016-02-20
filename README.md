# Ultimate Parser
This module was created for use in [**Powder Player**](https://github.com/jaruba/PowderPlayer).

Various parsing utilities for Node.js

## Usage
```
var parser = require('parser');

parser('C:\\Downloads\\wow.avi').webize()
// result: 'file:///C:/Downloads/wow.avi'

parser('file:///C:/Downloads/wow.avi').deWebize()
// result: 'C:\\Downloads\\wow.avi'

parser('http%3A%2F%2Fdecoded.com%2Furi.html').decodeURI()
// result: 'http://decoded.com/uri.html'

parser('C:\\Downloads\\wow.avi').filename()
// result: 'wow.avi'

parser('C:\\Downloads\\wow.avi').extension()
// result: 'avi'

parser('C:\\Downloads\\such.a.lovely.movie_2016.avi').name()
// result: 'Such a lovely movie 2016'

// TV Show specific parsing
// supported tag types: 'S01E01', 'S01E01-E02', '01x01', '[01x01]', '[01 01]', 'season 1 episode 5', '105', '1005', '10005'

parser('C:\\Downloads\\such.a.nice.show_s05e12.avi').showName()
// result: 'such a nice show'

parser('C:\\Downloads\\such.a.nice.show.1021.avi').shortSzEp()
// result: 's10e21'

parser('C:\\Downloads\\such.a.nice.show.1021.avi').season()
// result: '10'

parser('C:\\Downloads\\such.a.nice.show.1021.avi').episode()
// result: '21'
```
