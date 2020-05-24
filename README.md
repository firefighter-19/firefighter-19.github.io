@import "nullstyle.scss";
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&display=swap');
@font-face {
	font-family: 'Bankir-Retro';
	src: url('fonts/Bankir-Retro.eot');
	src: local('☺'), url('../fonts/fonts/Bankir-Retro.woff') format('woff'), url('fonts/Bankir-Retro.ttf') format('truetype'), url('fonts/Bankir-Retro.svg') format('svg');
	font-weight: 400;
	font-style: normal;
}

@font-face {
	font-family: 'BankGothicMdBT';
	src: url('../fonts/BankGothicMdBT.eot');
	src: local('☺'), url('../fonts/BankGothicMdBT.woff') format('woff'), url('../fonts/BankGothicMdBT.ttf') format('truetype'), url('../fonts/BankGothicMdBT.svg') format('svg');
	font-weight: 400;
	font-style: normal;
}



body.lock {
	overflow: hidden;
}

.wrapper {
// display: flex;
// flex-direction: column;
// flex: 1 1 100%;
background-color: black;
// min-width: 100%;
// min-height: 100%;
}

.container {
	max-width: 1180px;
	margin: 0 auto;

}
.wrapper__background {
  position: fixed;
  display: flex;
  justify-content: space-between;
  width: 100%;
  height: 100%;
	@media (max-width: 968px){
		position: absolute;
	}
}

.wrapper__background__left {
  display: block;
  width: 100%;
	height: 100%;
  background: url('../source/vectors/purple.svg') bottom left/auto 50% no-repeat;
  margin: 0 0 27px 0;
	@media (max-width: 1600px) {
		bottom: 0;
		position: absolute;
	}
	@media (max-width: 968px) {
		height: 70%;
		width: 70%;
		position: absolute;
		left: 0;
		top: -25%;
	}
}

.wrapper__background__right {
  display: block;
  width: 100%;
	height: 100%;
  background: url('../source/vectors/orange.svg') bottom right/auto 100% no-repeat;
	@media (max-width: 1600px) {
		bottom: 0;
		right: 0;
		position: absolute;
	}
	@media (max-width: 968px) {
		height: 70%;
		width: 70%;
		position: absolute;
		right: 0;
		bottom: -7%;
	}
	@media (max-width: 480px) {
		height: 70%;
		width: 70%;
		position: absolute;
		right: 0;
		bottom: -10%;
	}
}

.anchor {
display: inline-block;
position: relative;
height: 1px;
width: 1px;
}

// ---------------HEADER-----------------

.header {
  position: fixed;
  height: 90px;
  width: 100%;
  z-index: 1;
  flex-grow: 1;
	@media (max-width: 968px) {
		height: 80px;
	}
  &:before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    z-index: 3;
	background-color: black;
  }
}

.header__container {
  margin: 0 auto;
  max-width: 1180px;
	z-index: 2;
	@media (max-width: 968px) {
		display: flex;
		flex-direction: column;
		justify-content: center;
		position: fixed;
		z-index: 2;
		transform: translateY(-100%);
		right: 0;
		width: 100%;
		height: 100%;
		overflow: auto;
		background-color: black;
		transition: all 0.5s ease 0s;
		opacity: 0.85;
		&.active {
			transform: translateY(0%);
		}
	}
}

.header__border {
  width: 100%;
  position: absolute;
  top: 90px;
  height: 1.5px;
  background-color: rgb(249,136,22); /* Old browsers */
  background: -moz-linear-gradient(left, rgb(249,136,22) 25%, rgb(255,93,177) 51%, rgb(193,71,171) 78%); /* FF3.6-15 */
  background: -webkit-linear-gradient(left, rgb(249,136,22) 25%,rgb(255,93,177) 51%,rgb(193,71,171) 78%); /* Chrome10-25,Safari5.1-6 */
  background: linear-gradient(to right, rgb(249,136,22) 25%,rgb(255,93,177) 51%,rgb(193,71,171) 78%); /* W3C, IE10+, FF16+, Chrome26+, Opera12+, Safari7+ */
  filter: progid:DXImageTransform.Microsoft.gradient( startColorstr='#f98816', endColorstr='#c147ab',GradientType=1 ); /* IE6-9 */;
  z-index: 3;
	@media (max-width: 968px) {
		top: 80px;
		height: 2px;
	}
	&.active {
		transform: rotate(180deg);
	}
}

.nav__menu {
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 90px;
	@media (max-width: 968px) {
		flex-direction: column;
		height: 100%;
		width: 100%;
		justify-content: space-around;
	}
}

.nav__menu__list {
  display: flex;
  justify-content: flex-end;
}

.nav__menu__list-item {
  font-family: 'BankGothicMdBT';
	font-size: 16px;
  line-height: 17px;
	z-index: 3;
	li {
		@media (max-width: 968px) {
			opacity: 0;
			padding: 135px 0 0 0;
			min-height: 400px;
			display: flex;
			flex-direction: column;
			justify-content: space-between;
			text-align: center;
			font-size: calc(16px + 16 * ((100vw - 320px) / (1180 - 320)));
		}
  }
}

@keyframes navLinksFade {
	from {
		opacity: 0;
	}
	to {
		opacity: 1;
	}
}

.item__link {
  color: rgb(54,201,164);
  padding: 0 15px;
  &:hover {
    color: white;
  }
}

.nav__menu__links {
	z-index: 3;
	display: flex;
	svg {
		margin: 0 20px;
		&:hover {
			transform: scale(1.3);
			-webkit-transform: scale(1.3);
  		-ms-transform: scale(1.3);
		}
	}
	@media (max-width: 968px) {
		display: none;
	}
}


.nav__menu__links-media {
	display: none;
	@media (max-width: 968px) {
		display: block;
		position: fixed;
		top: 33px;
		left: 10px;
		z-index: 4;
		img {
	    padding: 0 18px;
	  }
	}
}

.nav__container__burger {
  display: none;
  @media (max-width: 968px) {
    display: block;
    position: absolute;
    width: 36px;
    height: 36px;
    top: 24px;
    right: 17px;
    cursor: pointer;
    z-index: 4;
		background: linear-gradient(43.78deg, rgba(255, 3, 200, 0.5) 7.14%, rgba(255, 0, 61, 0.5) 105.1%);
		&.active {
			border-radius: 50%;
			overflow: hidden;
			background: linear-gradient(63.9deg, rgba(0, 255, 255, 0.5) 0%, rgba(102, 255, 204, 0.5) 100%);
			width: 36px;
			height: 36px;

			}
    span {
      background: linear-gradient(55.01deg, #00FFFF 0%, #66FFCC 100%);
      position: absolute;
      width: 36px;
      height: 2px;
      top: 17px;
      right: 0px;
      transition: all 0.3s ease 0s;
      z-index: 3;
      &:first-child {
        top: 9px;
        transition: all 0.3s ease 0s;
      }
      &:last-child {
        top: 25px;
        transition: all 0.3s ease 0s;
      }
    }
    &.active {
      span{
				width: 30px;
				left: 2.6px;
				top: 4px;
        transform: scale(0);
				background: linear-gradient(264.69deg, #FF003D -7.43%, #FF03C8 100%);
        &:first-child {
          transform:rotate(45deg);
          top: 16px;


        }
        &:last-child {
          transform:rotate(-45deg);
          top: 17px;

        }
      }
    }
  }
}
// ---------------SECTION-----------------

.section {
	min-height: 100vh;
	@media (max-width: 968px) {
		display: flex;
		justify-content: center;
		flex-direction: column;
	}
}

.section__container {

}

.main {
  display: flex;
	justify-content: space-between;
  position: relative;
	align-items: center;
	@media (max-width: 968px) {
		flex-direction: column;
		padding: 0px;
	}
}

.main__head {
  padding: 230px 60px 0 0;
  color: white;
	@media (max-width: 968px) {
		width: 100%;
		padding: 0;
		order: 2;
	}
}

.main__head__header {
  line-height: 38px;
  font-family: 'BankGothicMdBT';
  letter-spacing: 10px;
  text-transform: capitalize;
  padding: 0 0 0 7px;
	font-size: calc(20px + 26 * ((100vw - 320px) / (1180 - 320)));
	@media (max-width: 968px) {
		text-align: center;
		padding: 15px 0;
		letter-spacing: 5px;
	}
	@media (max-width: 480px) {
		padding: 7px 0;
	}
}

.main__head__description {
  display: flex;
  font-family: 'Montserrat', sans-serif;
  font-size: calc(14px + 16 * ((100vw - 320px) / (1180 - 320)));
  line-height: 42px;
  padding: 15px 40px 0 5px;
	@media (max-width: 968px) {
		text-align: center;
		padding: 0 35px;
		line-height: 23px;
	}
}

.main__head__logo {
  padding: 230px 18px 0 0;
  display: flex;
	flex: 0 0 300px;
	justify-content: center;
	order: 1;
	img {
    height: 100%;
		width: 100%;
		object-fit: cover;
		@media (max-width: 968px) {
			width: 30%;
		}
		@media (max-width: 968px) and (max-height: 420px) {
			width: 25%;
		}
		@media (max-width: 669px) and (max-height: 380px) {
			width: 25%;
		}
  }
	@media (max-width: 968px) {
		flex: 0 0 150px;
		padding: 100px 0 25px 0;
	}
}

//===============================ARTICLE============================
.article {
	display: block;
}

.article__container {
	margin: 0 0 35px 0;
	background-color: #fff;
	position: relative;
	@media (max-width: 968px) {
		background-color: #fff;
		background-image: url('../source/1stPage/mobile/vleft.png'), url('../source/1stPage/mobile/vright.png');
		background-position: top left, right bottom;
		background-size: 100%;
		background-repeat: no-repeat, no-repeat;
	}
}

.article__about {
	padding: 50px 30px;
	max-width: 1000px;
	margin: 0 auto;
	line-height: 20px;
}

.article__about__title {
	font-family: 'BankGothicMdBT';
	font-size: calc(20px + 8 * ((100vw - 320px) / (1180 - 320)));
	text-decoration: underline;
	margin: 0 0 20px 0;
}

.article__about__header {
	display: flex;
	justify-content: space-between;
	margin: 0 0 60px 0;
	font-size: calc(14px + 2 * ((100vw - 320px) / (1180 - 320)));
	font-family: 'Montserrat', sans-serif;
	font-weight: normal;
	@media (max-width: 768px) {
		display: block;
		margin: 0 0 20px 0;
	}
}

.article__about__header-first {
	max-width: 500px;
	padding: 0 10px 0 0;
	text-align: justify;
	@media (max-width: 968px) {
		padding: 0 5px 0 0;
	}

}

.about__header__description {
	display: inline-block;

}

.about__header__description-uppercase{
	display: inline;
	padding: 0 2px;
	font-weight: 700;
}

.article__about__header-second {
	max-width: 500px;
	text-align: justify;
	padding: 0 0 0 10px;
	@media (max-width: 768px) {
		padding: 5px 0 0 0;
	}
}

.article__about__header__image {
	flex: 0 0 1000px;
	img {
		object-fit: cover;
		width: 100%;
		height: 100%;
	}
}

.article__about__header-article {
	margin: 60px 0;
	@media (max-width: 768px) {
		margin: 30px 0;
	}

}

.about__article__text {
	font-family: 'Montserrat', sans-serif;
	font-size: calc(14px + 2 * ((100vw - 320px) / (1180 - 320)));
	text-align: justify;
}

.article__about__footer {
	font-family: 'Montserrat', sans-serif;
	text-align: justify;

}

.article__about__footer-reward {

}

.reward__title {
	font-weight: 700;
	padding: 0 0 10px 0;
	font-size: calc(14px + 4 * ((100vw - 320px) / (1180 - 320)));

}

.about__footer__description {
	padding: 0 0 20px 0;
	font-size: calc(14px + 2 * ((100vw - 320px) / (1180 - 320)));

}

.article__about__footer-image {
	flex: 0 0 1000px;
	img {
		object-fit: cover;
		width: 100%;
		height: 100%;
	}
}

.article__about__footer-important {
	padding: 20px 0;
	font-size: calc(14px + 2 * ((100vw - 320px) / (1180 - 320)));
}

//==========================ARTICLE_ROADMAP=========================

.article__roadmap__container{
	padding: 50px 30px;
	max-width: 1000px;
	margin: 0 auto;
}

.article__roadmap {
	position: relative;
	margin: 0 auto 30px auto;
	background-color: #fff;
	@media (max-width: 968px) {
		background-image: url('../source/1stPage/mobile/vleft.png'), url('../source/1stPage/mobile/vright.png');
		background-position: top left, right bottom;
		background-size: 100%;
		background-repeat: no-repeat, no-repeat;
	}
}

.article__roadmap__title {
	font-family: 'BankGothicMdBT';
	font-size: calc(20px + 8 * ((100vw - 320px) / (1180 - 320)));
	text-decoration: underline;
	margin: 0 0 20px 0;
}


.article__roadmap__description {
	display: flex;
	flex-direction: column;
	align-items: center;
	margin: 0 auto;
	max-width: 500px;
	font-family: 'Montserrat', sans-serif;
	line-height: 35px;
	font-size: calc(14px + 2 * ((100vw - 320px) / (1180 - 320)));
	@media (max-width: 968px) {
		line-height: 30px;
	}
}

.article__roadmap__description-items{
	text-align: center;
	font-family: 'Montserrat', sans-serif;
}

.article__roadmap__whitepaper{
	text-align: right;
	margin: 20px 0 0 0;
	font-family: 'BankGothicMdBT';
	font-size: calc(20px + 8 * ((100vw - 320px) / (1180 - 320)));
	a {
		color: rgb(249,136,22);
		text-decoration: underline;
	}
}

//==========================COMMUNITY=============================

.community {
	margin: 0 auto;
	max-width: 800px;
	padding: 0 5px;
	@media (max-width: 968px) {
		padding: 0 10px;
	}
}

.community__social {
	display: none;
}

.community__social__links {
	display: flex;
	svg {
		object-fit: cover;
		width: 100%;
		height: 100%;
	}
}

//===========================TEAM__MEMBERS=========================

.team__members {
	margin: 0 auto;
	max-width: 800px;
	padding: 0 5px;
	@media (max-width: 968px) {
		padding: 0 10px;

	}
}

.team__community__title {
	color: white;
	font-family: 'BankGothicMdBT';
	font-size: calc(14px + 6 * ((100vw - 320px) / (1180 - 320)));
	text-decoration: underline;
	text-transform: uppercase;
	display: flex;
	justify-content: flex-start;
	padding: 40px 0;
	position: relative;
}

.team__members__list {
	display: flex;
	justify-content: space-around;
	font-family: 'Montserrat', sans-serif;
	font-size: calc(12px + 2 * ((100vw - 320px) / (1180 - 320)));
	position: relative;
	@media (max-width: 768px) {
		flex-direction: column;
		justify-content: space-around;
	}
}

.team__members-list-admins {
	display: flex;
	a {
		padding: 3px 0;
	}
	@media (max-width: 968px) {
		margin: 20px 0;
		justify-content: center;
	}
}

.team {
	color: white;
	padding: 0 20px;
}

.team-links {
	display: flex;
	flex-direction: column;
	// padding: 0 10px 0 0;
	a {
		color: white;
		&:hover{
			color: rgb(54,201,164);
			transform: scale(1.1);
			-webkit-transform: scale(1.1);
  		-ms-transform: scale(1.1);
		}
	}
}

.team-links-twitter {
	position: relative;
	right: 7px;
	bottom: 4px;
}

.team__members-list-helpers {
	display: flex;
	a {
		padding: 3px 0;
	}
	@media (max-width: 968px) {
		justify-content: center;
		margin: 0 14px 0 0;
	}
}





//===============================FOOTER=============================
.footer {
	margin: 40px 0 0 0;
	position: relative;
}

.footer__container {
	max-width: 400px;
	margin: 0 auto;
	@media (max-width: 768px) {
		padding: 10px;
	}

}

.footer__upper {
	display: flex;
	justify-content: center;
}

// .footer__upper__social {
// 	padding: 0 15px;
// 	display: flex;
// 	position: relative;
// 	svg {
// 		margin: 0 0 5px 0;
// 	}
// 	@media (max-width: 767px) {
// 		padding: 0 7px;
// 	}
// }

.footer__lower {
	display: flex;
	flex-direction: column;
	align-items: center;
	justify-content: center;
	margin: 35px 0 0 0;
}

.footer__lower__logo {
	padding: 0 0 10px 0;
	display:flex;
	flex: 0 0 15px;
	img {
		object-fit: cover;
		width: 100%;
		height: 100%;
	}

}

.footer__lower__text {
	text-align: center;
	font-family: 'BankGothicMdBT';
	font-size: 24px;
	line-height: 25px;
	color: white;
	opacity: 0.5;
	padding: 0 0 15px 0;
	font-size: calc(12px + 8 * ((100vw - 320px) / (1180 - 320)));
}
