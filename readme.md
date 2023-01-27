<h1 align="center">Gatinhos Petistas</h1>

<img src="https://pbs.twimg.com/media/E4SMu0KWEBAwlJs?format=jpg&name=large">

<div class="section">
<p align="center">Projeto Gatinho Petistas é uma pequena e até mesmo micro landing page. Que surgiu mais de uma brincadeira boba se eu conseguiria fazer em uma madrugada.</p>
</div>


## Relatório de como foi o código 🍜

Único processo que foi meio trabalhoso foi fazer a estrela pois demorei pra achar um site ou software para exportar como iframe sem me preocupar de texturizar e todo o processo ardoso que é a modelagem 3D. Por sorte encontrei o [Spline](https://spline.design/).  
Escolhi o objeto "estrela", foi aí que passei maior parte do tempo texturizando e mudando cada objeto de luz cada degradê de ponto de cor.

No fim deu tudo certo e esse foi o [resultado](https://my.spline.design/3dtextcopy-eb707fd6eea05ceed5d78f331048a25a/)

O resto do código foi como esperado muito tranquilo.
Básico de html e css.

Como eu usei um arquivo 3D que tecnicamente importa da web, o que leva tempo. Fiz uma linha de javascript com GSAP pra criar um ```preloader```. Que é como se fosse uma tela de carregamento. Pra garantir que tudo está pronto nos devidos lugares até o cliente ter carregado.

Vou estar deixando aqui o que eu gostaria de deixar aqui pequenos "destaques" como o import e a transição do ```preloader```



```html
<iframe src="https://my.spline.design/3dtextcopy-eb707fd6eea05ceed5d78f331048a25a/">

```

```js
gsap.from(".text", 0.8, {
            y:40,
            opacity:0,
            ease:"power2.inOut",
            delay: 1,
        });

        gsap.from(".loader", 2, {
            width: 0,
            ease: "power4.inOut",
            delay: 2,
        });

        gsap.to(".pre-loader", 2, {
            top: "-100%",
            ease: "power4.inOut",
            delay: 4,
        });

        gsap.from(".row", 0.9, {
            y:50,
            opacity: 0,
            ease: "power4.inOut",
            delay: 4.5,
            stagger: {
                amount: 0.3,
            }
        });
```