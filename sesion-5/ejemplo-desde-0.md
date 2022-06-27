# 🖥 Ejemplo: desde 0

_Que no se nos olvide_

* testing
* linter
* jsConfig (y después tsConfig)
* CI (GitHub Actions)
* Storybook

{% embed url="https://www.typescriptlang.org/tsconfig" %}

```json
	"ts-component": {
		"scope": "typescriptreact",
		"prefix": "\\new",
		"body": [
			"import './${TM_FILENAME_BASE}.scss';",
			"",
			"interface Props {",
			"\tfoo?: string;",
			"}",
			"",
			"function ${TM_FILENAME_BASE/(.*)/${1:/pascalcase}/}({ foo }: Props): JSX.Element {",
			"\treturn <div className='${TM_FILENAME_BASE}'>{foo}</div>;",
			"}",
			"",
			"export default ${TM_FILENAME_BASE/(.*)/${1:/pascalcase}/};"
		]
	},
```
