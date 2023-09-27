# shimmer

```
<style>
        .shimmer {
            border-radius: 8px;
            background: gray !important;
            color: grey !important;
            background-color: transparent;
            display: inline-block;
            -webkit-mask: linear-gradient(-60deg, #000 30%, #0005, #000 70%) right/300% 100%;
            background-repeat: no-repeat;
            animation: shimmer 2.5s infinite;
            font-size: 50px;
            opacity: 0.5;
            max-width: fit-content;
            border: solid;
        }
        .shimmer div {
            visibility: hidden !important;
        }
        @keyframes shimmer {
            100% {
                -webkit-mask-position: left
            }
        }
    </style>
```

```
<script type="text/javascript">

    const delay = ms => new Promise(res => setTimeout(res, ms));
    const parentDiv = document.getElementById('parents');
    const divs = parentDiv.querySelectorAll('div');
    async function removClassFromDivs(className) {
        await delay(3000);
        divs.forEach(div => {
            div.classList.remove(className);
        });
    }
    removClassFromDivs('shimmer');

</script>
```
