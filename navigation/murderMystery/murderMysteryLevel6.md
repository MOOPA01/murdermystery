---
layout: opencs
title: Murder Mystery Boss Fight
permalink: /murdermystery6
microblog: true
---

<div id="gameContainer" style="position: relative;">
    <div id="promptDropDown" class="promptDropDown" style="z-index: 9999"></div>
    <canvas id='gameCanvas'></canvas>
</div>

<script type="module">
    // Mansion Game assets locations
    import Core from "{{site.baseurl}}/assets/js/mansionGame/MansionLogic/Game.js";
    import GameControl from "{{site.baseurl}}/assets/js/mansionGame/GameControl.js";
    import MurderMysteryBossFight from "{{site.baseurl}}/assets/js/mansionGame/murderMysteryBossFight.js";
    import { pythonURI, javaURI, fetchOptions } from '{{site.baseurl}}/assets/js/api/config.js';

    // Web Server Environment data
    const environment = {
        path: "{{site.baseurl}}",
        pythonURI: pythonURI,
        javaURI: javaURI,
        fetchOptions: fetchOptions,
        gameContainer: document.getElementById("gameContainer"),
        gameCanvas: document.getElementById("gameCanvas"),
        gameLevelClasses: [MurderMysteryBossFight]
    }
    
    // Launch Boss Fight using the central core and mansion GameControl
    Core.main(environment, GameControl);
</script>