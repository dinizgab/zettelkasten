10-02-2023 - 15:15
Status: #idea
Tags: [[ideas]]

# Context Provider

A ideia dessa nota aqui é só pra me lembrar de como se implementar um provider de um contexto em react, pra caso eu precise eu voltar aqui e ler de novo até entender direito 

**Todos os códigos serão feitos usando TypeScript e eu vou usar o exemplo da nota de [[100 - zettelkasten/Context API|Context API]] para fazer o contexto.**

---
#### Primeiro precisa criar o contexto que eu preciso
```tsx
type NameContextType = {
	name: string;
	setName: (name: string) => void;
}

export const NameContext = createContext<NameContextType>({
	name: "",
	setName: () => {}
})
```

No bloco de cima eu defini o tipo dos valores que estarão dentro do contexto em `NameContextType` e criei o contexto setando seus valores iniciais como o `name` sendo uma string vazia e `setName` sendo uma função que não faz nada por enquanto. (Esses valores serão sobrescritos quando criar o provider) 

### Depois é preciso criar o Provider
```tsx
interface NameProviderProps {
	children: ReactNode;
}

export function NameProvider({ children }: NameProviderProps) {
	const [name, setName] = useState("") // Coloca aqui o valor padrão

	return (
		<NameContext.Provider value={name, setName}>
			{children}
		</NameContext.Provider>
	)
}
```

Nesse bloco é criado o contexto com as propriedades contendo os Nós filhos que ele terá dentro da tag, e dentro do Provider, eu crio os estados globais da aplicação e passo ele como a propriedade `value` de `NameContext.Provider`.

Depois disso, é só cobrir as tags que terão acesso a esse contexto (Geralmente eu cubro a tag App direto, já que a maioria das vezes são valores globais mesmo, como autenticação de usuário ou algo que todas as páginas usarão).

E para usar o contexto em outro componente é só usar o hook `useContext` e fazer destructuring do que vai ser usado:
```tsx
import { useContext } from "react";
import { NameContext } from "./providers/NameContext"

export default function Componente2() {
	const { name } = useContext(NameContext)

	return (
		<div>
			{name}
		</div>
	)
}
```

---
# Referências

- Se eu quiser outros exemplos mais práticos, tem o meu projeto Todo-It (A lista de tarefas) e o desafio da Woovi para o frontend
	- Woovi Challenge - https://github.com/dinizgab/woovi-frontend-challenge
	- Todo-It - https://github.com/dinizgab/Todo-It