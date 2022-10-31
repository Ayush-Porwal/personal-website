<script>
	export let email = 'xyz@abcmail.com';
</script>

<div>
	<div class="social-icon github icon-github" />
	<div class="social-icon linkedin icon-linkedin" />
	<div class="social-icon instagram icon-instagram" />
	<div class="right-line" />
</div>

<div>
	<div class="email">{email}</div>
	<div class="left-line" />
</div>

<style lang="scss">
	.right-line {
		height: 8vh;
		margin-left: 60px;
		border: 1px solid white;
		position: absolute;
		top: calc(100% - 8vh);
		&:hover {
			border: 1px solid #64ffda;
		}
	}

	.social-icon {
		height: 8vh;
		margin-left: 60px;
		position: absolute;
		left: -9px;
		font-size: 24px;
		color: #fff;
		&:hover {
			color: #64ffda;
		}
	}

	.github {
		top: calc(100% - 8vh - 120px);
	}

	.linkedin {
		top: calc(100% - 8vh - 80px);
	}

	.instagram {
		top: calc(100% - 8vh - 40px);
	}

	.email {
		color: #fff;
		font-size: 12px;
		font-family: roboto-regular;
		position: absolute;
		left: calc(100% - 130px);
		top: calc(100% - 8vh - 100px);
		transform: rotate(90deg);
		&:hover {
			color: #64ffda;
		}
	}

	.left-line {
		height: 8vh;
		margin-left: 60px;
		border: 1px solid white;
		position: absolute;
		top: calc(100% - 8vh);
		left: calc(100% - 120px);
		&:hover {
			border: 1px solid #64ffda;
		}
	}
</style>
