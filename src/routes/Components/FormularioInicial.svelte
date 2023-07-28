<section class="formulario_inicial">
	<div class="container">
		<form action="">
			<div class="row">
				<div class="input-field outlined col s12 m6 valign-wrapper formulario">
					<input id="codigoadega" type="text" class="validate" />
					<label for="codigoadega">Código de ADEGA: DF</label>
				</div>
				<div class="input-field outlined col s12 m6 valign-wrapper formulario">
					<input id="asuntorelacionado" type="text" class="validate" />
					<label for="asuntorelacionado">Asunto relacionado:</label>
				</div>
				<div class="input-field outlined col s12 formulario">
					<textarea
						id="deteccion"
						class="materialize-textarea"
						placeholder="Incluír a data aproximada, unha descrición dos feitos denunciados, e indicar a referencia catastral e/ou cordeadas X/Y se as houbese."
					/>
					<label for="textarea2">Recentemente, membros de ADEGA detectaron:</label>
				</div>
			</div>
			<div class="row formulario_denuncia">
				<div class="col m3 l3 hide-on-small-only">
					<div class="denunciaambiental">
						<h4>Denuncia ambiental</h4>
						<p class="white-text">
							Se foste testemuña de calquera actividade que atente contra o medio ambiente en
							Galiza, animámoste a informarnos ao respecto. A túa valiosa denuncia permitiranos
							tomar accións enérxicas contra calquera infracción ambiental e loitar pola xustiza
							ecolóxica.
						</p>

						<p class="white-text">
							Sabemos que a protección do noso entorno é unha tarefa conxunta e que cada voz conta.
							Agradecemos profundamente o teu compromiso coa preservación da beleza natural que nos
							rodea.
						</p>

						<p class="white-text">
							Por favor, completa este formulario con todos os detalles pertinentes e calquera
							evidencia que poidas proporcionar. Coa túa colaboración, podemos manter viva a esencia
							única de Galiza e traballar incansabelmente para preservar a súa biodiversidade e o
							equilibrio ecolóxico.
						</p>

						<p class="white-text">
							Grazas por ser parte activa na defensa da ecoloxía de Galiza! Xuntos, lograremos un
							impacto significativo na protección do noso amado fogar natural.
						</p>
					</div>
				</div>

				<div class="col s12 m9">
					<div class="ubicacion">
						<div class="ubicacion-datos">
							<h5>Datos de ubicación</h5>
							<div class="input-field outlined col s12 m6 valign-wrapper formulario">
								<input id="poligono" type="text" class="validate" />
								<label for="poligono">Polígono</label>
							</div>
							<div class="input-field outlined col s12 m6 valign-wrapper formulario">
								<input id="parcela" type="text" class="validate" />
								<label for="parcela">Parcela</label>
							</div>
							<div class="input-field outlined col s12 m6 valign-wrapper formulario">
								<input id="concello" type="text" class="validate" />
								<label for="concello">Concello</label>
							</div>
							<div class="input-field outlined col s12 m6 valign-wrapper formulario">
								<input id="provincia" type="text" class="validate" />
								<label for="provincia">Provincia</label>
							</div>
						</div>
					</div>
					<div class="leis-incumpridas">
						<div class="leis-incumpridas-datos">
							<h5>Leis incumpridas</h5>
							<div class="input-field outlined col s12 m6 valign-wrapper formulario">
								<input id="poligono" type="text" class="validate" />
								<label for="poligono">Polígono</label>
							</div>
							<div class="input-field outlined col s12 m6 valign-wrapper formulario">
								<input id="parcela" type="text" class="validate" />
								<label for="parcela">Parcela:</label>
							</div>
						</div>
					</div>
					
				</div>
				
			</div>
		</form>
	</div>
</section>

<style>
	.formulario_inicial {
		margin-top: 5vh;
	}

	.formulario {
		margin: 10px;
	}

	label {
		font-family: Poppins-Medium;
		font-size: 14px;
		color: #0a2010;
		letter-spacing: 0;
	}

	input {
		background: #ffffff;
		border: 2px solid #428165;
	}

	.materialize-textarea {
		height: 300px;
	}

	.formulario_denuncia {
		margin-top: 20px;
	}

	/* Sidebar denuncia ambiental */

	.denunciaambiental {
		background-image: url(./denunicaambiental.png);
		background-size: cover;
		background-position: center;
		position: relative;
		height: 100%;
		padding: 20px;
	}

	h4 {
		font-family: Poppins-SemiBold;
		font-size: 18px;
		color: #ffffff;
		letter-spacing: 0;
	}

	/* Ubicacion */

	.ubicacion {
		
		margin-left: 20px;
		border-left: 2px #428165 solid;

	}

	h5 {
		font-family: Poppins-Medium;
		font-size: 18px;
		color: #0a2010;
		letter-spacing: 0;
		padding-bottom: 10px;
		padding-left: 10px;
		margin: 0px;
	}

	/* Leis incumpridas */

	.leis-incumpridas{
		margin-top: 20px;
		margin-left: 20px;
		border-left: 2px #428165 solid;
	}


</style>
