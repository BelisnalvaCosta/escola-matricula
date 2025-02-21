function cadastrarAluno() {
    const nome = document.getElementById('nome').value;
    const cpf = document.getElementById('cpf').value;
    const curso = document.getElementById('curso').value;
    
    if (nome === '' || cpf === '' || curso === '') {
        alert('Preencha todos os campos!');
        return;
    }
    
    let alunos = JSON.parse(localStorage.getItem('alunos')) || [];
    alunos.push({ nome, cpf, curso });
    localStorage.setItem('alunos', JSON.stringify(alunos));
    alert('Aluno cadastrado com sucesso!');
    
    document.getElementById('nome').value = '';
    document.getElementById('cpf').value = '';
    document.getElementById('curso').value = '';
}

function mostrarRelatorio() {
    let alunos = JSON.parse(localStorage.getItem('alunos')) || [];
    const lista = document.getElementById('listaAlunos');
    lista.innerHTML = '';
    alunos.forEach(aluno => {
        let li = document.createElement('li');
        li.textContent = `${aluno.nome} - ${aluno.cpf} - ${aluno.curso}`;
        lista.appendChild(li);
    });
}