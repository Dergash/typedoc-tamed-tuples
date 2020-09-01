Reproduction example for typedoc backward compatibility with typescript 3.7.5 and 3.9.7:

```sh
yarn install
yarn typedoc
```
3.7.5
Output
```
Using TypeScript 3.7.5 from C:\projects\typedoc-named-tuples\node_modules\typescript\lib
C:\projects\typedoc-named-tuples\node_modules\typedoc\dist\lib\converter\types\tuple.js:44
        return ts.isNamedTupleMember(node);
                  ^

TypeError: ts.isNamedTupleMember is not a function
    at NamedTupleMemberConverter.supportsNode (C:\projects\typedoc-named-tuples\node_modules\typedoc\dist\lib\converter\types\tuple.js:44:19)
    at Converter.convertType (C:\projects\typedoc-named-tuples\node_modules\typedoc\dist\lib\converter\converter.js:126:31)
    at C:\projects\typedoc-named-tuples\node_modules\typedoc\dist\lib\converter\nodes\alias.js:24:37
    at Context.withScope (C:\projects\typedoc-named-tuples\node_modules\typedoc\dist\lib\converter\context.js:109:9)
    at AliasConverter.convert (C:\projects\typedoc-named-tuples\node_modules\typedoc\dist\lib\converter\nodes\alias.js:23:17)
    at Converter.convertNode (C:\projects\typedoc-named-tuples\node_modules\typedoc\dist\lib\converter\converter.js:117:53)
    at C:\projects\typedoc-named-tuples\node_modules\typedoc\dist\lib\converter\nodes\block.js:66:28
    at Array.forEach (<anonymous>)
    at BlockConverter.convertStatements (C:\projects\typedoc-named-tuples\node_modules\typedoc\dist\lib\converter\nodes\block.js:65:24)
    at C:\projects\typedoc-named-tuples\node_modules\typedoc\dist\lib\converter\nodes\block.js:44:26
error Command failed with exit code 1.
info Visit https://yarnpkg.com/en/docs/cli/run for documentation about this command.
```

3.9.7
Output
```
Using TypeScript 3.9.7 from C:\projects\tesler-ui\node_modules\typescript\lib
C:\projects\tesler-ui\node_modules\typedoc\dist\lib\converter\types\tuple.js:44
        return ts.isNamedTupleMember(node);
                  ^

TypeError: ts.isNamedTupleMember is not a function
    at NamedTupleMemberConverter.supportsNode (C:\projects\tesler-ui\node_modules\typedoc\dist\lib\converter\types\tuple.js:44:19)
    at Converter.convertType (C:\projects\tesler-ui\node_modules\typedoc\dist\lib\converter\converter.js:126:31)
    at C:\projects\tesler-ui\node_modules\typedoc\dist\lib\converter\nodes\variable.js:102:48
    at Context.withScope (C:\projects\tesler-ui\node_modules\typedoc\dist\lib\converter\context.js:109:9)
    at VariableConverter.convert (C:\projects\tesler-ui\node_modules\typedoc\dist\lib\converter\nodes\variable.js:78:17)
    at Converter.convertNode (C:\projects\tesler-ui\node_modules\typedoc\dist\lib\converter\converter.js:117:53)
    at C:\projects\tesler-ui\node_modules\typedoc\dist\lib\converter\nodes\interface.js:33:32
    at Array.forEach (<anonymous>)
    at C:\projects\tesler-ui\node_modules\typedoc\dist\lib\converter\nodes\interface.js:32:30
    at Context.withScope (C:\projects\tesler-ui\node_modules\typedoc\dist\lib\converter\context.js:109:9)
error Command failed with exit code 1.
info Visit https://yarnpkg.com/en/docs/cli/run for documentation about this command.
```