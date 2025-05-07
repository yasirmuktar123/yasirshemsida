<script>
    import Question from '$lib/Ask.svelte';
    let totalPoints = 0;
    let currentQuestion = 0;
    
    const questions = [
        {
            question: "Who is the best player?",
            answer1: "Me",
            answer2: "You",
            answer3: "Them",
            answer4: "Nobody",
            correctAnswer: 2, // Index of correct answer (1-4)
            pointGain: 0
        },
        
        {
            question: "Who is the all-time best goalkeeper??",
            answer1: "Someone",
            answer2: "You",
            answer3: "Them",
            answer4: "Nobody",
            correctAnswer: 2, // Index of correct answer (1-4)
            pointGain: 0
        },
    ];
    
    function handleAnswer(e) {
        totalPoints += e.detail.points;
        // Move to next question or show results
        if(currentQuestion < questions.length - 1) {
            currentQuestion++;
        }
    }
</script>

<div class="container mx-auto px-4">
    <div class="text-center mb-8">
        <h1 class="text-4xl font-bold mb-4">Quiz Game</h1>
        <p class="text-2xl">Total Points: {totalPoints}</p>
    </div>
    
    {#if currentQuestion < questions.length}
        <Question
            {...questions[currentQuestion]}
            on:answer={handleAnswer}
        />
    {:else}
        <div class="text-center">
            <h2 class="text-3xl mb-4">Game Over!</h2>
            <p class="text-2xl">Final Score: {totalPoints}</p>
        </div>
    {/if}
</div>