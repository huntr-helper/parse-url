<!---------------------------------------------------------------------------->
<!-- STOP, LOOK & LISTEN!                                                   -->
<!-- ====================                                                   -->
<!-- Do NOT edit this file directly since it's generated from a template    -->
<!-- file, using https://github.com/IonicaBizau/node-blah                   -->
<!--                                                                        -->
<!-- If you found a typo in documentation, fix it in the source files       -->
<!-- (`lib/*.js`) and make a pull request.                                  -->
<!--                                                                        -->
<!-- If you have any other ideas, open an issue.                            -->
<!--                                                                        -->
<!-- Please consider reading the contribution steps (CONTRIBUTING.md).      -->
<!-- * * * Thanks! * * *                                                    -->
<!---------------------------------------------------------------------------->

# parse-url [![Donate now][donate-now]][paypal-donations]

An advanced url parser supporting git urls too.

## Installation

```sh
$ npm i parse-url
```

## Example

```js
// Dependencies
var ParseUrl = require("parse-url");

console.log(ParseUrl("http://ionicabizau.net/blog"));
// => {
//     protocols: [ "http" ]
//   , port: null
//   , resource: "ionicabizau.net"
//   , user: ""
//   , pathname: "/blog"
//   , hash: ""
//   , search: ""
// }

console.log(ParseUrl("http://domain.com/path/name?foo=bar&bar=42#some-hash"));
// => {
//     protocols: ["http"]
//   , port: null
//   , resource: "domain.com"
//   , user: ""
//   , pathname: "/path/name"
//   , hash: "some-hash"
//   , search: "foo=bar&bar=42"
// }

console.log(ParseUrl("git+ssh://git@host.xz/path/name.git"));
// => {
//     protocols: ["git", "ssh"]
//   , port: null
//   , resource: "host.xz"
//   , user: "git"
//   , pathname: "/path/name.git"
//   , hash: ""
//   , search: ""
// }

console.log(ParseUrl("git@github.com:IonicaBizau/git-stats.git"));
// => {
//     protocols: []
//   , port: null
//   , resource: "github.com"
//   , user: "git"
//   , pathname: "/IonicaBizau/git-stats.git"
//   , hash: ""
//   , search: ""
// }

```

## Documentation

### `ParseUrl(url)`
Parses the input url.

#### Params
- **String** `url`: The input url.

#### Return
- **Object** An object containing the following fields:

## How to contribute
Have an idea? Found a bug? See [how to contribute][contributing].

## License
[KINDLY][license] © [Ionică Bizău][website]–The [LICENSE](/LICENSE) file contains
a copy of the license.

[license]: http://ionicabizau.github.io/kindly-license/?author=Ionic%C4%83%20Biz%C4%83u%20%3Cbizauionica@gmail.com%3E&year=2015
[contributing]: /CONTRIBUTING.md
[website]: http://ionicabizau.net
[docs]: /DOCUMENTATION.md
[paypal-donations]: https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=MG98D7NPFZ3MG
[donate-now]: http://i.imgur.com/jioicaN.png