---
layout: default
title: Copy Code
nav_order: 99
search_exclude: true
nav_exclude: true
---

<style>
    code {
        font-family: 'Consolas', Courier, monospace;
        background-color: #FFF;
        padding: 8px !important;
        border-radius: 3px;
        font-size: 150%;
        line-height: 150%;
    }
    h1 {
        font-size: 150%;
        text-align: center;
    }
</style>

<body onload="
    (function() {
        const searchParams = new URLSearchParams(window.location.search);
        const copy = searchParams.get('code');
        document.getElementById('copy').innerHTML = copy;
    })();
">
    <h1 onclick="
            (function() {
                const textArea = document.createElement('textarea');
                textArea.value = document.getElementById('copy').innerHTML;
                textArea.style.opacity = 0;
                document.body.appendChild(textArea);
                textArea.focus();
                textArea.select();
                try {
                    const success = document.execCommand('copy');
                    alert(`${success ? `Success! Copied ${textArea.value} to clipboard.` : 'Something went wrong, please manually copy.'}`);
                } catch (err) {
                    console.error(err.name, err.message);
                }
                document.body.removeChild(textArea);
            })();
        ">Click or tap here to copy <br><code id="copy"></code><br> to your clipboard</h1>
</body>
