<script>
    import FormularioInicial from "./FormularioInicial.svelte";
</script>
<section class="formulario_tit">
	<div class="container">
		<div class="row">
			<div class="col s12 m6 valign-wrapper">
				<h1>Formulario de<br /> denuncia</h1>
			</div>
			<div class="col s12 m6 valign-wrapper">
				<p>
					En ADEGA estamos comprometidos con preservar a riqueza ecolóxica que define a nosa terra e
					asegurar un futuro sostible para as xeracións vindeiras.
				</p>
			</div>
		</div>
	</div>
</section>

 <FormularioInicial/>


<style>
    .formulario_tit{
        margin-top: 5vh;
    }
	h1 {
		font-family: Poppins-SemiBold;
		font-size: 2rem;
		color: #0a2010;
		letter-spacing: 0;
		line-height: 40px;
	}

	p {
		font-family: Poppins-SemiBold;
		font-size: 14px;
		color: rgba(0, 0, 0, 0.6);
		letter-spacing: 0;
		line-height: 25px;
	}
</style>
