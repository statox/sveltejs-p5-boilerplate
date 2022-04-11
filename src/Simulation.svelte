<script lang="ts">
    import P5 from 'p5';
    export let data;

    const sketch = (p5: P5) => {
        let mover: Mover;
        p5.setup = () => {
            const canvas = p5.createCanvas(500, 500);
            canvas.parent('canvasDiv');
        };

        // The sketch draw method
        p5.draw = () => {
            p5.background(30, 200, 30);
            p5.text(data.ruleNumber, p5.width/2, p5.height/2);
        };
    };

    new P5(sketch);
</script>

<main>
    <div id="canvasDiv"></div>
</main>
