# **GreatPages Instagram Float**

<a href="https://www.buymeacoffee.com/claitonllemes" target="_blank" rel="noopener noreferrer"><img src="https://user-images.githubusercontent.com/99222756/210368404-216273fb-c930-453e-b32b-e3614872eba3.png" width="100%"/></a><br>

## **Configurações**
O código abaixo adiciona um botão flutuante do Instagram a uma página na plataforma Greatpages. Copie e cole no menu de configurações da página.

<br><a href="https://www.buymeacoffee.com/claitonllemes" target="_blank" rel="noopener noreferrer"><img src="https://user-images.githubusercontent.com/99222756/210372197-a1d41894-8acc-470b-ac38-2bd1ee0a4ed9.png" width="100%"/></a><br>

```Html
<!-- Instagram Float for Greatpages v. 1.0.0 - Ⓒ Copyright 2023 Claiton Lemes. -->

<a target="_blank" href="LINKAQUI" class="float">
    <svg class="icon">
        <path
            d="M5 2C4.20435 2 3.44129 2.31607 2.87868 2.87868C2.31607 3.44129 2 4.20435 2 5V13C2 13.7956 2.31607 14.5587 2.87868 15.1213C3.44129 15.6839 4.20435 16 5 16H13C13.7956 16 14.5587 15.6839 15.1213 15.1213C15.6839 14.5587 16 13.7956 16 13V5C16 4.20435 15.6839 3.44129 15.1213 2.87868C14.5587 2.31607 13.7956 2 13 2H5ZM1.46447 1.46447C2.40215 0.526784 3.67392 0 5 0H13C14.3261 0 15.5979 0.526784 16.5355 1.46447C17.4732 2.40215 18 3.67392 18 5V13C18 14.3261 17.4732 15.5979 16.5355 16.5355C15.5979 17.4732 14.3261 18 13 18H5C3.67392 18 2.40215 17.4732 1.46447 16.5355C0.526784 15.5979 0 14.3261 0 13V5C0 3.67392 0.526784 2.40215 1.46447 1.46447ZM13.5 3.5C14.0523 3.5 14.5 3.94772 14.5 4.5V4.51C14.5 5.06228 14.0523 5.51 13.5 5.51C12.9477 5.51 12.5 5.06228 12.5 4.51V4.5C12.5 3.94772 12.9477 3.5 13.5 3.5ZM6.17157 6.17157C6.92172 5.42143 7.93913 5 9 5C10.0609 5 11.0783 5.42143 11.8284 6.17157C12.5786 6.92172 13 7.93913 13 9C13 10.0609 12.5786 11.0783 11.8284 11.8284C11.0783 12.5786 10.0609 13 9 13C7.93913 13 6.92172 12.5786 6.17157 11.8284C5.42143 11.0783 5 10.0609 5 9C5 7.93913 5.42143 6.92172 6.17157 6.17157ZM9 7C8.46957 7 7.96086 7.21071 7.58579 7.58579C7.21071 7.96086 7 8.46957 7 9C7 9.53043 7.21071 10.0391 7.58579 10.4142C7.96086 10.7893 8.46957 11 9 11C9.53043 11 10.0391 10.7893 10.4142 10.4142C10.7893 10.0391 11 9.53043 11 9C11 8.46957 10.7893 7.96086 10.4142 7.58579C10.0391 7.21071 9.53043 7 9 7Z" />
    </svg>
</a>

<style>
    :root {
        --icon-color: #ffffff;
        --gradient-normal: #E9A61D, #EF3738, #9D24CE;
        --gradient-hover: #cb8f17, #bc2323, #721597;
        --pulse-color: #EF3738;
    }

    .icon {
        width: 120px;
        height: 120px;
        transform: scale(2) translate(30%, 30%);
        fill: var(--icon-color);
    }

    .float {
        position: fixed;
        cursor: pointer;
        width: 60px;
        height: 60px;
        bottom: 30px;
        right: 30px;
        transition: background 2s;
        background: linear-gradient(45deg, var(--gradient-normal));
        border-radius: 20px;
        z-index: 9000;
    }

    .float:hover {
        background: linear-gradient(45deg, var(--gradient-hover));
    }

    .float:hover .icon {
        fill: var(--icon-color);
    }
</style>

<script>
    const floatBtn = document.querySelector('.float');

    function pulseAnimation() {
        const animation = floatBtn.animate(
            [
                { boxShadow: `0 0 0 0 var(--pulse-color)` },
                { boxShadow: `0 0 0 20px rgba(0, 200, 0, 0)` },
            ],
            {
                duration: 2000,
                easing: 'ease-out',
                iterations: Infinity,
            }
        );

        animation.addEventListener('iteration', (event) => {
            if (event.elapsedTime > 0) {
                floatBtn.style.boxShadow = '0 0 0 0 var(--pulse-color)';
            }
        });
    }

    pulseAnimation();
</script>
```
