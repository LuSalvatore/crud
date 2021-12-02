# crud
//Este Crud foi feito em php se quiser pode dar um fork para ver o codigo funcionar em sua maquina 
Porém enfatizo que este crud não está perfeito... mas dá pro gasto ;-D

As // São para demarcar a mudança de páginas dentro do code por que não entendi como criar paginas 
no neste git talvez fique um pouco bagunçado rsrsrs...

///////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
///////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
//index.php < Pagina 1//
<!DOCTYPE html>
<html>
<head>
<title>Cronos Marvel</title>

<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-1BmE4kWBq78iYhFldvKuhfTAU6auU8tT94WrHftjDbrCEXSU1oBoqyl2QvZ6jIW3" crossorigin="anonymous">
<script src="https://kit.fontawesome.com/8786c39b09.js"></script>

</head>
<body>

<div class="container">
	<div class="row">
  <div class="col-sm-6">
    <div class="card">
      <div class="card-body">
        <h5 class="card-title">Adicionar Lançamento</h5>
        <p class="card-text">Adicione um Novo Filme a linha do tempo Marvel</p>
        <a href="_adicionar_filme.php" class="btn btn-primary">Novo Lançamento</a>
      </div>
    </div>
  </div>
  <div class="col-sm-6">
    <div class="card">
      <div class="card-body">
        <h5 class="card-title">Listar Filmes</h5>
        <p class="card-text">Visualizar e Editar linha Cronológica.</p>
        <a href="_listar_filme.php" class="btn btn-primary">Ver Todos os Filmes Marvel</a>
      </div>
    </div>
  </div>
</div>
</div>

<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-ka7Sk0Gln4gmtz2MlQnikT1wXgYsOg+OMhuP+IlRH9sENBO0LRn5q+8nbTov4+1p" crossorigin="anonymous"></script>
</body>
</html>

///////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
//_adicionar_filme.php < Pagina 2//
<!DOCTYPE html>
<html>
<head>
	<meta charset="utf-8">
	<title>Linha Cronológica Marvel</title>
	<!-- CSS only -->
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-1BmE4kWBq78iYhFldvKuhfTAU6auU8tT94WrHftjDbrCEXSU1oBoqyl2QvZ6jIW3" crossorigin="anonymous">

	<style type="text/css">
		#tamanhoContainer {width: 500px}
	</style>

</head>
<body>

<div class="container" id="tamanhoContainer" style="margin-top: 50px">
	<h4>Cronologia Marvel</h4>
<form action="_inserir_filme.php" method="post" style="margin-top: 20px">
		<div class="mb-3">
		    <label class="form-label">Insira seu Email</label>
		    <input type="email" class="form-control" name="nomeemail" placeholder="Insira seu Email">
		</div>
		<div class="mb-3">
		    <label class="form-label">Seu Id</label>
		    <input type="text" class="form-control" name="nomeid" placeholder="Nome de Usuário">
		</div>
		<div class="mb-3">
		    <label class="form-label">Nome do Filme</label>
		    <input type="text" class="form-control" name="nomefilme" placeholder="Qual o nome do Filme">
		</div>
		<div class="mb-3">
		    <label class="form-label">Data de Lançamento</label>
		    <input type="number" class="form-control" name="Data" placeholder="Data de Lançamento">
		</div>
		<div class="mb-3">
		    <label class="form-label">Ordem Cronológica</label>
		    <input type="text" class="form-control" name="nomeordem" placeholder="Este filme vem depois de...">
		</div>
		 <div class="form-group" name="categoria">
		    <label>Selecione a Franquia</label>
		    <select class="form-control">
				      <option></option>
				      <option>Capitão America</option>
				      <option>Thor</option>
				      <option>Hulk</option>
				      <option>Homem de Ferro</option>
				      <option>Gavião</option>
				      <option>Vilva</option>
				      <option>Spider Verse</option>
				      <option>Wanda and Vision</option>
				      <option>Mutantes</option>
				      <option>Eternals</option>
				      <option>Quantun Verse</option>
				      <option>Wakanda</option>
				      <option>Espaço</option>
				      <option>Loki</option>
				      <option>Doutor Estranho</option>
				      <option>Quarteto Fantastico</option>
		    </select>
 		 </div>
 		 <div class="form-group" name="Segmento">
		    <label>Selecione o Segmento</label>
		    <select class="form-control">
				      <option></option>
				      <option>MCU</option>
				      <option>SONY</option>
				      <option>DISNEY+</option>
		    </select>
 		 </div>
 		 <div style="text-align: right; margin-top: 20px">
		 	<a href="_adicionado_filme.php" type="submit" class="btn btn-sucess" style=" background-color: #069">Cadastrar</a>
		 </div>
		  <div style="text-align: left; margin-top: 20px">
		 	<a type="submit" class="btn btn-sucess" href="index.php" style=" background-color: #069">Voltar</a>
		 </div>
</form>
</div>

<!-- JavaScript Bundle with Popper -->
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-ka7Sk0Gln4gmtz2MlQnikT1wXgYsOg+OMhuP+IlRH9sENBO0LRn5q+8nbTov4+1p" crossorigin="anonymous"></script>

</body>
</html>

///////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
//_adicionado_filme.php < Pagina 3//

<!DOCTYPE html>
<html>
<head>

<title>Linha Cronológica</title>
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-1BmE4kWBq78iYhFldvKuhfTAU6auU8tT94WrHftjDbrCEXSU1oBoqyl2QvZ6jIW3" crossorigin="anonymous">

</head>
<body>

<?php
include 'conexao.php';

$nomeemail = $_POST['nomeemail'];
$nomeid = $_POST['nomeid'];
$nomefilme = $_POST['nomefilme'];
$Data = $_POST['Data'];
$nomeordem = $_POST['nomeordem'];
$categoria = $_POST['categoria'];
$Segmento = $_POST['Segmento'];
$sql = "INSERT INFO 'estoque'('nomeordem', 'nomefilme', 'nomeid', 'nomeemail', 'categoria', 'Segmento', 'Data') 
	 VALUES ('$nomeordem', '$nomefilme', '$nomeid', '$nomeemail', '$categoria', '$Segmento', '$Data')";
$inserir = mysqli_query($conexao,$sqli);
?>

<link rel="stylesheet" type="text/css" href="" integrity="" crossorigin="anonymus">

<div class="container" style="width: 500px, margin-top: 20px">
	<center>
	<h4>Filme Adicionado</h4>
	</center>
	<div style="padding-top: 20px">
		<center>
		   <a href="_adicionar_filme.php" role="button" class="btn btn-sucess btn-primary">Cadastre um Novo Filme</a>
		   <a href="_listar_filme.php" class="btn btn-primary">Ver Linha Marvel</a>
		</center>
	</div>
</div>

<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-ka7Sk0Gln4gmtz2MlQnikT1wXgYsOg+OMhuP+IlRH9sENBO0LRn5q+8nbTov4+1p" crossorigin="anonymous"></script>
</body>
</html>

///////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
//_listar_filme.php < Pagina 4//

<!DOCTYPE html>
<html>
<head>

<title>Linha Cronológica</title>
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-1BmE4kWBq78iYhFldvKuhfTAU6auU8tT94WrHftjDbrCEXSU1oBoqyl2QvZ6jIW3" crossorigin="anonymous">
<script src="https://kit.fontawesome.com/8786c39b09.js"></script>

</head>
<body>

<table class="table table-dark">
  <thead>
 	<tr>
    <th scope="col">Filme</th>
    <th scope="col">Data</th>
    <th scope="col">Sequencia</th>
    <th scope="col">Segmento</th>
    <th scope="col">Id</th>
    <th scope="col">Ação</th>

	</tr>
  </thead>

    	<?php
    	include 'conaxão.php';
    	$sql = "SELECT * FROM 'Filme'"
    	$buscar = mysqli_query($conexão,$sql);

    	while ($array = mysqli_fetch_array($buscar)){
    		
    		$nomefilme = $array['nomefilme']
            $Data = $array['Data']
    		$Sequencia = $array['Sequencia']
    		$Segmento = $array['Segmento']
            $nomeid = $array['nomeid']
    	?>
    <tr>
    	<td><?php $Filme ?></td>
    	<td><?php $Data ?></td>
    	<td><?php $Sequencia ?></td>
    	<td><?php $Segmento ?></td>
    	<td><?php $Id ?></td>
    	<td><?php $Assistir ?></td>
    	<td><a type="button" class="btn btn-primary" href="_editar_filme.php?id=<?php echo $nomeid ?>" role="button">
            <i class="far fa-edit"></i>&nbsp;Editar</a>
            <a type="button" class="btn btn-danger" href="_deletar_filme.php?id=<?php echo $nomeid ?>" role="button">
            <i class="far fa-trash-alt"></i>&nbsp;Deletar</a>
        </td>

    	<?php } ?>
    </tr>
</table>

<!-- JavaScript Bundle with Popper -->
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-ka7Sk0Gln4gmtz2MlQnikT1wXgYsOg+OMhuP+IlRH9sENBO0LRn5q+8nbTov4+1p" crossorigin="anonymous"></script>
</body>
</html>

///////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
//_editar_filme.php < Pagina 5//

<?php 
include 'conexao.php';

echo $id = $_GET['id']

?>

<!DOCTYPE html>
<html>
<head>
	<meta charset="utf-8">
	<title>Editar Filme</title>
	<!-- CSS only -->
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-1BmE4kWBq78iYhFldvKuhfTAU6auU8tT94WrHftjDbrCEXSU1oBoqyl2QvZ6jIW3" crossorigin="anonymous">

	<style type="text/css">
		#tamanhoContainer {width: 500px}
	</style>

</head>
<body>

<div class="container" id="tamanhoContainer" style="margin-top: 50px">
	<h4>Cronologia Marvel</h4>
<form action="_inserir_filme.php" method="post" style="margin-top: 20px">
		<?php 
		$sql = "SELECT * FROM 'estoque' WHERE nomeid = $id";
		$buscar = mysql_query($conexao, $sql);
		while ($array = mysqli_fetch_array($buscar)) {
			$nomefilme = $array['nomefilme']
    		$nomeid = $array['nomeid']
    		$Data = $array['Data']
    		$Sequencia = $array['Sequencia']
    		$Segmento = $array['Segmento']
    		$nomeordem = $array['nomeordem']
		?>


		<div class="mb-3">
		    <label class="form-label">Insira seu Email</label>
		    <input type="email" class="form-control" name="nomeemail" value="<?php echo $nomeemail ?>" disabled >
		</div>
		<div class="mb-3">
		    <label class="form-label">Seu Id</label>
		    <input type="text" class="form-control" name="nomeid" value="<?php echo $nomeid ?>" disabled>
		</div>
		<div class="mb-3">
		    <label class="form-label">Nome do Filme</label>
		    <input type="text" class="form-control" name="nomefilme" value="<?php echo $nomefilme ?>"disabled>
		     <input type="text" class="form-control" name="id" value="<?php echo $id ?>" style="display: none;">
		</div>
		<div class="mb-3">
		    <label class="form-label">Data de Lançamento</label>
		    <input type="number" class="form-control" name="Data" value="<?php echo $Data ?>">
		</div>
		<div class="mb-3">
		    <label class="form-label">Ordem Cronológica</label>
		    <input type="text" class="form-control" name="nomeordem" value="<?php echo $nomeordem ?>">
		</div>
		 <div class="form-group" name="categoria">
		    <label>Selecione a Franquia</label>
		    <select class="form-control">
				      <option></option>
				      <option>Capitão America</option>
				      <option>Thor</option>
				      <option>Hulk</option>
				      <option>Homem de Ferro</option>
				      <option>Gavião</option>
				      <option>Vilva</option>
				      <option>Spider Verse</option>
				      <option>Wanda and Vision</option>
				      <option>Mutantes</option>
				      <option>Eternals</option>
				      <option>Quantun Verse</option>
				      <option>Wakanda</option>
				      <option>Espaço</option>
				      <option>Loki</option>
				      <option>Doutor Estranho</option>
				      <option>Quarteto Fantastico</option>
		    </select>
 		 </div>
 		 <div class="form-group" name="Segmento">
		    <label>Selecione o Segmento</label>
		    <select class="form-control">
				      <option></option>
				      <option>MCU</option>
				      <option>SONY</option>
				      <option>DISNEY+</option>
		    </select>
 		 </div>
 		 <div style="text-align: center; margin-top: 20px">
		 	<a href="_atualizar_filme.php" type="submit" class="btn btn-sucess" style=" background-color:#069">Atualizar</a>
		 </div>
		<?php } ?>
</form>
</div>

<!-- JavaScript Bundle with Popper -->
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-ka7Sk0Gln4gmtz2MlQnikT1wXgYsOg+OMhuP+IlRH9sENBO0LRn5q+8nbTov4+1p" crossorigin="anonymous"></script>

</body>
</html>

///////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
//_atualizar_filme.php < Pagina 6//

<?php

include 'conexao.php';
$id = $_POST['id'];
$nomeid = $_POST['nomeid'];
$nomeordem = $_POST['nomeordem'];
$Data = $_POST['Data'];
$Segmento = $_POST['Segmento'];
$nomeemail = $_POST['nomeemail'];
$categoria = $_POST['categoria'];
$sql = "UPDATE 'filme' SET 'nomeemail'='$nomeemail', 'nomeordem'='$nomeordem', 'Data'='$Data', 'Segmento'='$Segmento', 'nomeid'='$nomeid', 'categoria'='$categoria' WHERE id_nomefilme = $id";
$Atualizar = msqli_query($conexao, $sql);

?>
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-1BmE4kWBq78iYhFldvKuhfTAU6auU8tT94WrHftjDbrCEXSU1oBoqyl2QvZ6jIW3" crossorigin="anonymous">
<div class="container" style="widht:400px">
	<center>
		<h3>Atuaizado Brabo</h3>
		<div style="margin-top: 10px"></div>
		<a href="_listar_filme.php" class="btn btn-sucess btn btn-primary">Ver Lista de Filmes</a>
	</center>
	
</div>

///////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
//_deletar_filme.php < Pagina 7//

<?php
include 'conexao.php'
$id = $_GET['id']

$sql = "DELETE FROM 'Filmes' WHERE id_nomefilme = $id";
$deltar = mysqli_query($conexao, $sql)
?>
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-1BmE4kWBq78iYhFldvKuhfTAU6auU8tT94WrHftjDbrCEXSU1oBoqyl2QvZ6jIW3" crossorigin="anonymous">
<div class="container" style="widht:400px">
	<center>
		<h3>Deletar Brabo</h3>
		<div style="margin-top: 10px"></div>
		<a href="_listar_filme.php" class="btn btn-sucess btn btn-primary">Listar Filmes</a>
	</center>
	
</div>

///////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
// # THE AND # //
