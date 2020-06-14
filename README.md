# Configuração do Ambiente (React)

## 1- Criar um projeto React

```bash
npx create-react-app style_guide_react
cd style_guide_react
code .
```

## 2- Instalar e Configurar o ESLint

```bash
npm i -D eslint
npx eslint --init
```

**2.1. Responder o questionário para criar o arquivo .eslintrc.json**

- How would you like to use ESLint?<br>
  `To check syntax, find problems, and enforce code style`

- What type of modules does your project use?<br>
  `JavaScript modules (import/export)`

- Which framework does your project use?<br>
  `React`

- Does your project use TypeScript?<br>
  `No`

- Where does your code run?<br>
  `Browser`

- How would you like to define a style for your project?<br>
  `Use a popular style guide`

- Which style guide do you want to follow?<br>
  `Airbnb: https://github.com/airbnb/javascript`

- What format do you want your config file to be in?<br>
  `JSON`

**2.2. Instalar os pacotes necessários**

Instalar os pacotes que são apresentados durante a criação do arquivo .eslintrc.json

**2.3 Instalar os pacotes para integração com Prettier**

```bash
npm i -D prettier eslint-plugin-prettier eslint-config-prettier
```

**2.4 Atualizar o arquivo .eslintrc.json**

```json
{
	"env": {
		"browser": true,
		"jest": true
	},
	"extends": ["airbnb", "prettier"],
	"plugins": ["react", "prettier"],
	"rules": {
		"prettier/prettier": "error",
		"react/jsx-filename-extension": [
			"error",
			{
				"extensions": [".js", ".jsx"]
			}
		],
		"quotes": [
			"error",
			"single",
			{
				"avoidEscape": true,
				"allowTemplateLiterals": true
			}
		],
		"no-unused-vars": "warn",
		"no-use-before-define": "warn",
		"no-console": "warn",
		"func-names": "off",
		"object-shorthand": "off",
		"global-require": "off",
		"import/prefer-default-export": "off",
		"react/jsx-indent": "off",
		"react/jsx-indent-props": "off"
	}
}
```

**2.5 Criar o arquivo .prettierrc**

```json
{
	"singleQuote": true,
	"useTabs": true
}
```

## 3- Pesquisar por mais opções de configuração

- [ESLint](https://eslint.org/)<br>
- [Preetier](https://prettier.io/)
