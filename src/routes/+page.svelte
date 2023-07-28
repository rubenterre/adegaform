<script>
	import Header from './Components/Header.svelte';
	import Footer from './Components/Footer.svelte';

	export let data;


</script>

<Header />

<section class="formulario_inicial">
	<div class="container">
		<form id="DenunciaAmbiental">
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
					<label for="deteccion">Recentemente, membros de ADEGA detectaron:</label>
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
							<h5>DATOS DE UBICACIÓN</h5>
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
							<h5>LEIS INCUMPRIDAS</h5>
							{#each data.articulos as articulo}
								<p class="formulario">
									<label>
										<input type="checkbox" id={articulo.id} />
										<span><b>{articulo.articulo}</b> {articulo.contenido}</span>
									</label>
								</p>
							{/each}
						</div>
					</div>
					<div class="leis-incumpridas">
						<div class="leis-incumpridas-datos">
							{#each data.leis as lei}
								<p class="formulario">
									<label>
										<input type="checkbox" id={lei.id} />
										<span><b>{lei.articulo}</b> {lei.contenido}</span>
									</label>
								</p>
							{/each}
						</div>
					</div>

					<div class="leis-incumpridas">
						<div class="leis-incumpridas-datos">
							<h5>ELIXE DESTINATARIO</h5>
							<p class="formulario">
								<label>
									<input name="seprona" type="radio" />
									<span>SERVIZO DE PROTECCIÓN DA NATUREZA (SEPRONA)</span>
								</label>
							</p>
							<p class="formulario">
								<label>
									<input name="policia_autonomica" type="radio" />
									<span>POLICÍA AUTONÓMICA</span>
								</label>
							</p>
							<p class="formulario">
								<label>
									<input name="ministerio" type="radio" />
									<span
										>MINISTERIO PARA A TRANSICIÓN ECOLÓXICA E O RETO DEMOGRÁFICO,CONFEDERACIÓN
										HIDROGRÁFICA MIÑO SIL</span
									>
								</label>
							</p>
							<p class="formulario">
								<label>
									<input name="conselleria" type="radio" />
									<span>CONSELLERÍA DE INFRAESTRUCTURAS E MOBILIDADE- AUGAS DE GALICIA</span>
								</label>
							</p>
							<div class="row">
								<div class="col s6">
									<div class="leis-incumpridas">
										<div class="leis-incumpridas-datos">
											<h5>XEFATURAS TERRITORIAIS</h5>
											<p class="formulario">
												<label>
													<input name="mediorural" type="radio" />
													<span>CONSELLERÍA DE MEDIO RURAL</span>
												</label>
											</p>
											<p class="formulario">
												<label>
													<input name="medioambiente" type="radio" />
													<span>CONSELLARÍA DE MEDIO AMBIENTE TERRITORIO E VIVENDA</span>
												</label>
											</p>
											<p class="formulario">
												<label>
													<input name="cultura" type="radio" />
													<span>CONSELLARÍA DE CULTURA, EDUCACIÓN E UNIVERSIDADE</span>
												</label>
											</p>
										</div>
									</div>
								</div>
								<div class="col s6">
									<div class="leis-incumpridas">
										<div class="leis-incumpridas-datos">
											<h5>PROVINCIA</h5>
											<p class="formulario">
												<label>
													<input name="lugo" type="radio" />
													<span>LUGO</span>
												</label>
											</p>
											<p class="formulario">
												<label>
													<input name="coruna" type="radio" />
													<span>A CORUÑA</span>
												</label>
											</p>
											<p class="formulario">
												<label>
													<input name="pontevedra" type="radio" />
													<span>PONTEVEDRA</span>
												</label>
											</p>
											<p class="formulario">
												<label>
													<input name="ourense" type="radio" />
													<span>OURENSE</span>
												</label>
											</p>
										</div>
									</div>
								</div>
							</div>
						</div>
					</div>
					<div class="documentacion">
						<p class="formulario">
							<label>
								<input type="checkbox" id="documentacion" />
								<span> Acompáñanse outra documentación </span>
							</label>
						</p>
					</div>
					<div class="imprimir">
						<a class="white-text waves-effect waves-light btn" onclick= ""
							>IMPRIMIR DOCUMENTO</a
						>
					</div>
				</div>
			</div>
		</form>
	</div>
</section>

<Footer />

<style>
	form {
		margin-bottom: 10%;
	}

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
		max-height: 890px;
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

	.leis-incumpridas {
		margin-top: 20px;
		margin-left: 20px;
		border-left: 2px #428165 solid;
	}
	span {
		font-family: Poppins-Regular;
	}

	/* Documentacion */

	.documentacion {
		margin-top: 20px;
		margin-left: 20px;
	}

	/* Imprimir */

	.imprimir a {
		margin-top: 20px;
		margin-bottom: 20px;
		width: 100%;
		background-color: #428165;
	}
</style>
