<template>
    <div>
        <div id="brand-discount-slider">
            <div class="brand-arrow-next">
                &#10095;
            </div>
            <div class="brand-arrow-prev">
                &#10094;
            </div>
            <ul>
                <li>
                    <a href="https://www.instagram.com/petsiufsm">
                        <div class="brand-logo-container">
                            <img src="https://www.ufsm.br/cursos/graduacao/santa-maria/sistemas-de-informacao/wp-content/uploads/sites/424/2018/11/logo-pet-si-300x110.png" alt="">
                        </div>
                    </a>
                </li>
                <li>
                    <a href="https://www.ufsm.br/pet/ciencia-da-computacao">
                        <div class="brand-logo-container">
                            <img src="https://www.ufsm.br/app/uploads/sites/499/2021/07/LOGO-2-300x178.png" alt="">
                        </div>
                    </a>
                </li>
                <li>
                    <a href="https://www.instagram.com/petflorestalufsm">
                        <div class="brand-logo-container">
                            <img src="https://www.ufsm.br/app/uploads/sites/499/2021/07/logo-pet-png-300x212.png" alt="">
                        </div>
                    </a>
                </li>
                <li>
                    <a href="https://www.instagram.com/petodontoufsm/">
                        <div class="brand-logo-container">
                            <img src="https://www.ufsm.br/app/uploads/sites/499/2021/07/PET-ODONTO-LOGO_Final-Copia-768x207.png" alt="">
                        </div>
                    </a>
                </li>
                <li>
                    <a href="https://www.instagram.com/petcivilufsm">
                        <div class="brand-logo-container">
                            <img src="https://www.ufsm.br/cursos/graduacao/santa-maria/engenharia-civil/wp-content/uploads/sites/434/2020/06/Logo-2019-Preto-HD-300x188.png" alt="">
                        </div>
                    </a>
                </li>
                <li>
                    <a href="https://www.instagram.com/petletraslabcorpus">
                        <div class="brand-logo-container">
                            <img src="https://www.ufsm.br/app/uploads/sites/499/2021/07/Pet-Letras-300x101.png" alt="">
                        </div>
                    </a>
                </li>
                <li>
                    <a href="https://www.instagram.com/petzootecnia_ufsm">
                        <div class="brand-logo-container">
                            <img src="https://www.ufsm.br/app/uploads/sites/499/2021/07/logo-pet-300x117.png" alt="">
                        </div>
                    </a>
                </li>
                <li>
                    <a href="https://www.instagram.com/petmatematicaufsm">
                        <div class="brand-logo-container">
                            <img src="https://www.ufsm.br/app/uploads/sites/499/2021/07/pet-Matematica-300x101.png" alt="">
                        </div>
                    </a>
                </li>
                <li>
                    <a href="https://www.instagram.com/petfisicaufsm">
                        <div class="brand-logo-container">
                            <img src="https://www.ufsm.br/app/uploads/sites/499/2021/07/logo-300x175.png" alt="">
                        </div>
                    </a>
                </li>
                <li>
                    <a href="https://www.instagram.com/petenfermagemufsm">
                        <div class="brand-logo-container">
                            <img src="https://www.ufsm.br/app/uploads/sites/499/2021/07/logo-pet-1-300x233.png" alt="">
                        </div>
                    </a>
                </li>
                <li>
                    <a href="https://www.instagram.com/petcomufsm/">
                        <div class="brand-logo-container">
                            <img src="https://www.ufsm.br/app/uploads/sites/499/2021/07/Marca_PETCom-300x212.png" alt="">
                        </div>
                    </a>
                </li>
                <li>
                    <a href="https://www.instagram.com/petbioufsm/">
                        <div class="brand-logo-container">
                            <img src="https://www.ufsm.br/app/uploads/sites/499/2021/07/Adesivo_branco_modelo_1-removebg-preview-300x276.png" alt="">
                        </div>
                    </a>
                </li>
                <li>
                    <a href="https://www.instagram.com/petagronomiaufsm/">
                        <div class="brand-logo-container">
                            <img src="https://www.ufsm.br/app/uploads/sites/499/2021/07/Logo-PET-Agronomia-2018-300x88.png" alt="">
                        </div>
                    </a>
                </li>
                <li>
                    <a href="https://www.instagram.com/petengenhariaeletrica/">
                        <div class="brand-logo-container">
                            <img src="https://www.ufsm.br/app/uploads/sites/499/2021/07/1.-Padrao-com-degrade-300x157.png" alt="">
                        </div>
                    </a>
                </li>
            </ul>
        </div>
    </div>
</template>

<script>
$(document).ready(function () {

    let slideCount = $('#brand-discount-slider ul li').length;
    let slideWidth = $('#brand-discount-slider ul li').width();
    let slideHeight = $('#brand-discount-slider ul li').height();
    let sliderUlWidth = slideCount * slideWidth;

    $('#brand-discount-slider').css({ width: slideWidth, height: slideHeight });
    $('#brand-discount-slider ul').css({ width: sliderUlWidth, marginLeft: - slideWidth });
    $('#brand-discount-slider ul li:last-child').prependTo('#brand-discount-slider ul');

    function moveLeft() {
        $('#brand-discount-slider ul').animate({
            left: + slideWidth + 30
        }, 200, function () {
            $('#brand-discount-slider ul li:last-child').prependTo('#brand-discount-slider ul');
            $('#brand-discount-slider ul').css('left', '');
        });
    }

    function moveRight() {
        $('#brand-discount-slider ul').animate({
            left: - slideWidth - 30
        }, 200, function () {
            $('#brand-discount-slider ul li:first-child').appendTo('#brand-discount-slider ul');
            $('#brand-discount-slider ul').css('left', '');
        });
    }

    $('.brand-arrow-prev').click(function () {
        moveLeft();
    });

    $('.brand-arrow-next').click(function () {
        moveRight();
    });

    setTimeout(moveLeft(), 1000);
});

export default {
    name: 'Carousel',
}
</script>

<style lang="scss">
.brand-logo-container {
    width: 150px;
    display: flex;
    align-items: center;
}
.brand-logo-container:hover {
    transform: scale(1.1);
    transition-duration: .5s;
}
#brand-discount-slider {
    position: relative;
    overflow: hidden;
    width: 100% !important;
    height: 200px !important;
    border-top: 1px solid #ccc;
    border-bottom: 1px solid #ccc;
}
#brand-discount-slider ul {
    position: relative;
    margin: 0 !important;
    padding: 0 60px !important;
    height: 100% !important;
    display: flex;
}
#brand-discount-slider ul li {
    display: flex;
    align-items: center;
    margin: 20px;
}
#brand-discount-slider ul li img {
    width: 100%;
}
.brand-arrow-prev {
    width: 40px;
    height: 80%;
    background: #000;
    text-align: center;
    line-height: 177px;
    color: #fff;
    position: absolute;
    top: 0;
    left: 0;
    z-index: 25;
    cursor: pointer;
    margin: 20px 0;
}
.brand-arrow-next {
    width: 40px;
    height: 80%;
    background: #000;
    color: #fff;
    position: absolute;
    right: 0;
    z-index: 25;
    cursor: pointer;
    margin: 20px 0;
    display: flex;
    align-items: center;
    justify-content: center;
}

.brand-arrow-next:hover, .brand-arrow-prev:hover {
    color: #cccccc;
    transform: scale(1.3);
    transition-duration: 1s;
}
</style>
