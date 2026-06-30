const senha = document.getElementById("senha");

senha.addEventListener("keyup", verificar);

function mostrarSenha(){

    if(senha.type==="password"){
        senha.type="text";
    }else{
        senha.type="password";
    }

}

function verificar(){

let valor = senha.value;

let pontos = 0;

let maiuscula = /[A-Z]/.test(valor);
let minuscula = /[a-z]/.test(valor);
let numero = /[0-9]/.test(valor);
let especial = /[!@#$%^&*(),.?":{}|<>]/.test(valor);

document.getElementById("c1").style.color = valor.length>=8?"lime":"white";
document.getElementById("c2").style.color = maiuscula?"lime":"white";
document.getElementById("c3").style.color = minuscula?"lime":"white";
document.getElementById("c4").style.color = numero?"lime":"white";
document.getElementById("c5").style.color = especial?"lime":"white";

if(valor.length>=8)pontos++;
if(maiuscula)pontos++;
if(minuscula)pontos++;
if(numero)pontos++;
if(especial)pontos++;

let barra=document.getElementById("forca");
let texto=document.getElementById("textoForca");

switch(pontos){

case 1:
barra.style.width="20%";
barra.style.background="red";
texto.innerHTML="Senha muito fraca";
break;

case 2:
barra.style.width="40%";
barra.style.background="orange";
texto.innerHTML="Senha fraca";
break;

case 3:
barra.style.width="60%";
barra.style.background="yellow";
texto.innerHTML="Senha média";
break;

case 4:
barra.style.width="80%";
barra.style.background="lime";
texto.innerHTML="Senha forte";
break;

case 5:
barra.style.width="100%";
barra.style.background="green";
texto.innerHTML="Senha muito forte";
break;

default:
barra.style.width="0%";
texto.innerHTML="Digite uma senha";
}

}
