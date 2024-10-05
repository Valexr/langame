<script lang="ts">
	import '../app.css';
</script>

<section>
	<a href="_#" class="logo">
		<img src="logo.svg" alt="" />
	</a>
	<form action="POST" on:submit|preventDefault>
		<fieldset>
			<label for="" style="--input-icon: url('./tel.svg')">
				<input name="tel" type="tel" placeholder="Введите номер телефона" pattern="\d" />
			</label>
			<label for="" style="--input-icon: url('./password.svg')">
				<input name="password" type="password" placeholder="Введите пароль" />
			</label>
			<label for="">
				<a href="">Забыли пароль</a>
			</label>
		</fieldset>
		<fieldset>
			<button>Войти</button>
		</fieldset>
	</form>
	<p>Если у вас ещё нет аккаунта<br /><a href=""><strong>Зарегистрируйтесь</strong></a></p>
	<p></p>
	<p>
		Установите приложение<br /><br />
		<a href=""><img src="app-store.svg" alt="" /></a>
		<a href=""><img src="google-play.svg" alt="" /></a>
	</p>
</section>

<footer>
	<menu>
		<a href="">Информация</a>
		<a href="">Вакансии</a>
		<a href="">Помощь</a>
		<a href="">Конфиденциальность</a>
		<a href="">Правила</a>
		<a href="">FAQ</a>
		<a href="">Прайс-лист</a>
	</menu>
	<a href=""><img src="powered.svg" alt="" /></a>
</footer>

<style>
	/* @import '../app.css'; */
	@import url('https://fonts.googleapis.com/css2?family=Lato:ital,wght@0,100;0,300;0,400;0,700;0,900;1,100;1,300;1,400;1,700;1,900&display=swap');

	section {
		height: calc(100vh - 72px);
		display: grid;
		text-align: center;
		place-content: center;
		gap: 1em;
	}
	form {
		margin: auto;
		max-width: 500px;
		min-width: 300px;
	}
	.logo {
		display: block;
		width: 124px;
		margin: auto;
		aspect-ratio: 1.65/1;
	}
	fieldset {
		display: flex;
		flex-flow: column nowrap;
		border: 0;
		gap: 1em;
	}
	input {
		background-color: #efefef;
		line-height: 60px;
		border: 0;
		border-radius: 5px;
		padding: 0 3em;
		width: 100%;
	}
	label[style]::before {
		content: '';
		width: 60px;
		height: 60px;
		position: absolute;
		background: var(--input-icon) no-repeat 1em;
	}
	button {
		text-transform: uppercase;
		background-color: #dc0000;
		color: #fff;
		border: 0;
		border-radius: 25px;
		width: fit-content;
		padding: 1em 2em;
		cursor: pointer;
	}
	fieldset button {
		width: 100%;
	}
	::placeholder {
		color: #909090;
	}
	:invalid {
		color: #dc0000;
	}
	menu {
		display: flex;
		gap: 1em;
		align-items: center;
		justify-content: center;
		padding: 0;
	}

	footer {
		text-align: center;
	}
</style>
