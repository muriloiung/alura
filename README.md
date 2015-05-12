<canvas id="tela" width="600" height="450"></canvas>

<script>

var tela = document.getElementById("tela");
var c = tela.getContext("2d");

var imagem = new Image();
imagem.src = "http://www.caelum.com.br/imagens/instrutores/fotos/paulo-silveira-90.jpg";

var desenhaImagem = function(x, y) {
    c.drawImage(imagem, x, y);
};

var limpaTela = function() {
	c.clearRect(0, 0, 600, 400);
};

var x = 1;

var desenha = function() {
	limpaTela();
	desenhaImagem(x, 100);
	x = x + 1;
};

setInterval(desenha, 1);

</script>
