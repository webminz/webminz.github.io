---
layout: plain
title: God jul
permalink: /xmas20/
---

<div id="godjol">
    <style>
        .msg {
            font-size: 1.2em;
            font-weight: bold;
        }
        .btn {
            height: 44px;
            background-color: #349e63;
            color:white;
            border:0;
        }
    </style>
    <h1 class="pageTitle">Hei!</h1>
    <p>
    Und Herzlich willkommen! Wenn du diese Seite gefunden hast, hast du wahrscheinlich eine Weihnachts-Postkarte von mir bekommen und zählst zu meinen engsten Freunden! &lt;3 Alternativ, bist du sehr gut darin wahllos zufällige URLs in deine Browserzeile einzugeben... Anyways! Ich gehe mal von ersterem aus und möchte dir ganz herzlich <b>"Frohe Weihnachten, ein Frohes Neues Jahr, und alles erdenklich Gute wünschen"!</b> Zur Zeit ist es ja schwierig euch alle persönlich in die Arme zu schließen und daher muss ich das jetzt auf elektronischen Wege tun. Ich hoffe einfach, dass wir uns bald wiedersehen! Für die Zwischenzeit habe ich hier mal einen Ausschnitt aus meinem "Daily Life" hier oben (roh und unkommentiert!) zusammengeschnitten, für alle diejenigen, die sich immer gefragt haben, was ich hier eigentlich mache: 
    </p>

    <iframe width="560" height="315" src="https://www.youtube.com/embed/ixtJXunTiDk" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

    <p>
    Die Postkarte die du erhalten hast, sollte noch einen personalisierten Code enthalten. Gib diesen in das Feld hier drunter ein und lass dich überraschen!
    </p>

    <form action="#" onsubmit="doIt(this); return false">
        <input id="kodeFelt" type="text" name="code" placeholder="Dein personalisierter Code hier...">
        <input class="btn" type="submit" value="Und los!">
    </form>

    <p class="msg"><span id="messageBoks"></span><a id="linken" style="visibility:hidden" href="#">Hier klicken</a></p>

    <script>
        var secret = "eyJhUnc0M0oiOiJodHRwczovL3lvdXR1LmJlLzI0LUV4eThsS213IiwidDJ1eXIxIjoiaHR0cHM6Ly95b3V0dS5iZS84aWNWLVdSSm1XSSIsIm1uN2FzNyI6Imh0dHBzOi8veW91dHUuYmUvU1ZEQnR1dHdtMG8iLCJjbzFuNHEiOiJodHRwczovL3lvdXR1LmJlL29wbkFab2lBc2FNIiwibWhqMzZ4IjoiaHR0cHM6Ly95b3V0dS5iZS8tU0piX2NnV3lNUSIsImYyM240NXUiOiJodHRwczovL3lvdXR1LmJlL2k1UlBOdVE3akQ0IiwiaG53NDdnIjoiaHR0cHM6Ly95b3V0dS5iZS9VZnJZTS1WZDJRSSIsImJtbjMyNiI6Imh0dHBzOi8veW91dHUuYmUvM1puNktkSGlvSkEiLCJ5dTQ2eXZwIjoiaHR0cHM6Ly95b3V0dS5iZS9pUnpXOTdPR2g0byIsImR4aG80cCI6Imh0dHBzOi8veW91dHUuYmUvMVN6RlRKRV8wRDQiLCJucWczdjkiOiJodHRwczovL3lvdXR1LmJlL3ZBZExaVjRHOWpzIiwidHJ5YmkzIjoiaHR0cHM6Ly95b3V0dS5iZS81UlV6c3RRUFdGcyIsIjNibjh1ZyI6Imh0dHBzOi8veW91dHUuYmUvUk1DMmc1eGU3R0EiLCJ2eWY2NzgiOiJodHRwczovL3lvdXR1LmJlL2pfUEMtNVpURG8wIiwiODdkZjJ5IjoiaHR0cHM6Ly95b3V0dS5iZS9UUkFMNVBKS2xuUSJ9";

        
        function doIt() {
            var code = document.getElementById("kodeFelt").value;

            if (code) {
                var o = JSON.parse(atob(secret));
                
                if (o[code]) {
                    document.getElementById("messageBoks").innerHTML = "Falls die automatische Weiterleitung nicht funktioniert ";
                    document.getElementById("linken").style.visibility = "visible";
                    document.getElementById("linken").href = o[code];
                    window.location.href = o[code];
                } else {
                     document.getElementById("messageBoks").innerHTML = "Hmm... sieht so aus als ob der Code nicht stimmt. Schau nochmal und sende mir sonst notfalls eine WhatsApp!";
                }
            } else {
                document.getElementById("messageBoks").innerHTML = "";
                document.getElementById("linken").style.visibility = "hidden";
            }
        }
    </script>

    <p>(c) Euer Paddy!</p>
    
</div>
