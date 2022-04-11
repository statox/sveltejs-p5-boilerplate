<script lang="ts">
    import P5 from 'p5';
    import {externalCommand} from '../services/service';
    export let data;

    const sketch = (p5: P5) => {
        let mover, time;
        p5.setup = () => {
            const canvas = p5.createCanvas(500, 500);
            canvas.parent('canvasDiv');

            mover = {x: 0, y: p5.width/3};
            time = 0;
        };

        // The sketch draw method
        p5.draw = () => {
            p5.background(30, 200, 30);
            p5.fill('black');
            p5.text(data.ruleNumber, p5.width/2, p5.height/2 - 10);
            p5.text(externalCommand(), p5.width/2, p5.height/2 + 10);

            mover.x = (mover.x+1) % p5.width;
            p5.fill('red');
            p5.circle(mover.x, mover.y, 10, 10);
            time++;
        };
    };

    new P5(sketch);
</script>

<main>
    <div id="canvasDiv"></div>
</main>
