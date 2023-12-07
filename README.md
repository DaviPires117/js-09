
const funcionarios = [
  { nome: 'Wally', salario: 4800 },
  { nome: 'Funcionario1', salario: 6000 },
  { nome: 'Funcionario2', salario: 4500 },
  { nome: 'Funcionario3', salario: 5200 },
  { nome: 'Funcionario4', salario: 4800 }
];


console.log("Lista de Funcionários e Salários antes do reajuste:");
funcionarios.forEach(funcionario => {
  console.log(`${funcionario.nome}: R$ ${funcionario.salario}`);
});


const funcionariosReajustados = funcionarios.map(funcionario => ({
  nome: funcionario.nome,
  salario: funcionario.salario * 1.05
}));


console.log("\nLista de Funcionários e Salários após o reajuste:");
funcionariosReajustados.forEach(funcionario => {
  console.log(`${funcionario.nome}: R$ ${funcionario.salario.toFixed(2)}`);
});


const funcionariosAcimaDe5000 = funcionariosReajustados.filter(funcionario => funcionario.salario > 5000);


console.log("\nFuncionários que recebem mais de 5000 após o reajuste:");
funcionariosAcimaDe5000.forEach(funcionario => {
  console.log(`${funcionario.nome}: R$ ${funcionario.salario.toFixed(2)}`);
});

 funcionariosAcimaDe5000.find(funcionario => funcionario.nome === 'Wally');
console.log(`\nVocê encontrou o funcionário Wally? ${wallyEncontrado ? 'Sim' : 'Não'}`);
```
