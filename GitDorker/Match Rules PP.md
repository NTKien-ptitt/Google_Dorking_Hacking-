Bảng phân loại các đoạn mã và lỗ hổng Prototype Pollution 1:

| **Regex**                                                                                  | **Lỗ hổng**                                  | **Thư viện/Ứng dụng**                 | **Mức độ nghiêm trọng** | **Khả năng chắc chắn** |
|-------------------------------------------------------------------------------------------|---------------------------------------------|---------------------------------------|-------------------------|-------------------------|
| `String\(\w+\)\.split\(\/&\|;\/\)\,\s*function\(`                                         | Prototype Pollution                         | Purl (jQuery-URL-Parser)              | High                   | Certain                |
| `\/\(\[\^\\\[\\\]\]\+\)\|\(\\\[\\\]\)\/g\s*`                                              | Prototype Pollution                         | CanJS deparam                        | High                   | Certain                |
| `\.substr\(0,\s*\w+\s*-\s*1\)\.match\(\/\(\[\^\\\]\\?\[\]\+\|\(\\B\)\(\?\=\\\]\)\)\/g\)`  | Prototype Pollution                         | MooTools More                         | High                   | Certain                |
| `\$\.each\(\s*\w+\.replace\(\s*\/\\\+\/g\s*,\s*['"] ['"]\s*\)\.split\(\s*['"]&['"]\s*\)`  | Prototype Pollution                         | jQuery BBQ (deparam)                 | High                   | Certain                |
| `\s*\/\\\[\/\.test\(\s*\w+\[0\]\s*\)\s*&&\s*\/\\\]\$\/\.test\(\s*\w+\[\s*\w+\s*\]\s*\)`  | Prototype Pollution                         | deparam                              | High                   | Certain                |
| `['"]\[\]['"]\s*===\s*\w+\s*\?\s*\w+\.push\(\w+\)\s*:\s*\w+\[\w+\]\s*=\s*\w+`            | Prototype Pollution                         | deparam                              | High                   | Certain                |
| `(\w+)\s*=\s*decodeURIComponent[\w+;,\s\(\)\.\{=\[\]'"-\/\?}]+\b(\w+)\s*=\s*\3\[\2\]...` | Prototype Pollution                         | backbone-query-parameters 2          | High                   | Certain                |
| `\w+\s*=\s*\/\\\[\(\[\^\\\]\]\*\)\]\/g`                                                  | Prototype Pollution                         | V4Fire Core                          | High                   | Certain                |
| `\w+\s*=\s*\w+\.split\(\/\\\&\(amp\\\;\)\?\/\)`                                          | Prototype Pollution                         | jQuery Sparkle                       | High                   | Certain                |
| `\/\^\(\[\^\[\]\+\??\)\(\\\[\.\*\\\]\)\?\$\/\.exec\(\s*\w+\s*\)`                         | Prototype Pollution                         | jQuery query-object                  | High                   | Certain                |
| `\.match\(\/\(\^\[\^\[\]\+\)\(\\\[\.\*\\\]\$\)\?\/\)`                                    | Prototype Pollution                         | queryToObject                        | High                   | Certain                |



Bảng phân loại các đoạn mã bổ sung và các lỗ hổng Prototype Pollution 2:

| **Regex**                                                                                  | **Lỗ hổng**                                  | **Thư viện/Ứng dụng**                 | **Mức độ nghiêm trọng** | **Khả năng chắc chắn** |
|-------------------------------------------------------------------------------------------|---------------------------------------------|---------------------------------------|-------------------------|-------------------------|
| `\?\s*decodeURIComponent\(\s*\w+\.substr\(\s*\w+\s*\+\s*1\)\)\s*:\s*['"]['"]`             | Prototype Pollution                         | getJsonFromUrl                        | High                   | Certain                |
| `\w+\.replace\(\s*['"]\[\]['"]\s*,\s*['"]\[['"]\.concat\(`                                 | Prototype Pollution                         | Unknown lib_0                         | High                   | Certain                |
| `\w+\s*=\s*\/\(\\w\+\)\\\[\(\\d\+\)\\\]\/`                                                | Prototype Pollution                         | component/querystring                 | High                   | Certain                |
| `\(\w+\s*=\s*\w+\.exec\(\w+\)\)\s*\?\s*\(\s*\w+\[\w+\[1\]\]\s*=\s*\w+\[\w+\[1\]\]\s*...`  | Prototype Pollution                         | component/querystring #2             | High                   | Certain                |
| `\/\(\.\*\)\\\[\(\[\^\\\]\]\*\)\\\]\$\/\.exec\(\w+\)`                                     | Prototype Pollution                         | YUI 3 querystring-parse               | High                   | Certain                |
| `\w+\s*=\s*\w+\.split\(\/\\\.\(\.\+\)\?\/\)\[1\]`                                         | Prototype Pollution                         | jquery.parseParams.js                 | High                   | Certain                |
| `\w+\s*=\s*\/\\\[\?\(\[\^\\\]\[\]\+\)\\\]\?\/g`                                           | Prototype Pollution                         | flow.js                               | High                   | Certain                |
| `\w+\s*=\s*\w+\(\w+\[1\]\.slice\(\w+\s*\+\s*1,\s*\w+\[1\]\.indexOf\(['"]\]['"],\s*\w+\)`  | Prototype Pollution                         | wishpond decodeQueryString            | High                   | Certain                |
| `\w+\s*=\s*\w+\.slice\(0,\s*\w+\.indexOf\(['"]\\x?0?0['"]\)\)`                             | Prototype Pollution                         | PHP.js parse_str                      | High                   | Certain                |
| `"\[\]"\s*===\s*\w+\.substring\(\w+\.length\s*-\s*2\)...`                                 | Prototype Pollution                         | Unknown lib_1                         | High                   | Certain                |
| `\w+\.match\(\/\(\^\[\^\\\[\]\+\)\(\\\[\.\*\\\]\$\)\?\/\)`                                | Prototype Pollution                         | Unknown lib_2                         | High                   | Certain                |
| `\(\[\^\\\\\[\^\\\\\]\]\+\)\(\(\\\\\[\(\^\\\\\[\^\\\\\]\)\\\\\]\)\*\)`                    | Prototype Pollution                         | Unknown lib_3                         | High                   | Certain                |


Bảng phân loại các đoạn mã bổ sung và các lỗ hổng Prototype Pollution 3:

| **Regex**                                                                                              | **Lỗ hổng**                              | **Thư viện/Ứng dụng**                     | **Mức độ nghiêm trọng** | **Khả năng chắc chắn** |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------|-------------------------------------------|-------------------------|-------------------------|
| `(['"]-1['"]\s*==\s*\w+\[1\]\.indexOf\(['"]\[['"]\))`                                                 | Prototype Pollution                     | inbound setUrlParams                      | High                   | Certain                |
| `(\w+\s*=\s*\w+\.split\(['"]\.['"]\)\s*[;,]\s*\w+\s*=\s*\w+\.pop\(\)\s*[;,]\s*\w+\s*=\s*\w+\.reduce\()` | Prototype Pollution                     | Unknown lib_4                             | High                   | Certain                |
| `(\w+\s*=\s*\w+\.split\(\/\\\]\\\[\?\|\\\[\/\)[\w\s=\(\;\,<\-]*\w+\.indexOf\(['"]\[['"]\))`            | Prototype Pollution                     | Old mithril.js                            | High                   | Certain                |
| `(\w+\s*=\s*\w+\.split\(['"]\.['"]\)[\s;,\w]+=\s*\w+\.pop\(\)[!\s;,\w]+\(\w+\.length\))`              | Prototype Pollution                     | builder.io QueryString.deepen             | High                   | Certain                |
| `(\w+\s*=\s*\w+\.indexOf\(['"]\]['"],\s*\w+\)[\s\w;,]+=\s*decodeURIComponent\(\w+\.substring\(\w+\s*\+\s*1))` | Prototype Pollution                     | Unknown lib_5                             | High                   | Certain                |
| `(\w+\.replace\(['"]\]['"],\s*['"]['"]\)[\w\s;,\(]+\.search\(\/\[\\\.\\\[\]\/\))`                     | Prototype Pollution                     | arg.js                                   | High                   | Certain                |
| `(\/\^\(\[\$a-zA-z_\]\[\$a-zA-z0-9\]\*\)\\\[\(\[\$a-zA-z0-9\]\*\)\\\]\$\/)`                           | Prototype Pollution                     | R.js                                     | High                   | Certain                |
| `(\/\^\(\\w\+\)\\\[\(\\w\+\)\?\\\]\(\\\[\\\]\)\?\/)`                                                  | Prototype Pollution                     | davis.js                                 | High                   | Certain                |
| `(\.match\(\/\^\[\\\[\\\]\]\*\(\[\^\\\[\\\]\]\+\)\\\]\*\(\.\*\)\/\))`                                 | Prototype Pollution                     | SoundCloud SDK decodeParams               | High                   | Certain                |
| `((\w+)\s*=\s*\w+\.split\(['"]\.['"]\)[\w+;,\s\(\)\.\{=\[\]'"<]+\b(\w+)\s*=\s*\2\[\w+\][\w+;,\s\(\)...` | Prototype Pollution                     | Unknown lib_7                             | High                   | Certain                |

