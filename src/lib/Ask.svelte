<!-- lib/Question.svelte -->
<script>
    export let question = "Default Question";
    export let answer1 = "Default Answer 1";
    export let answer2 = "Default Answer 2";
    export let answer3 = "Default Answer 3";
    export let answer4 = "Default Answer 4";
    export let correctAnswer = 1; // 1-4 indicating which answer is correct
    export let pointGain = 0;
    
    // Dispatch events for parent component
    import { createEventDispatcher } from 'svelte';
    const dispatch = createEventDispatcher();
    
    function handleAnswer(selectedNumber) {
        const isCorrect = selectedNumber === correctAnswer;
        pointGain = isCorrect ? 1 : -1;
        dispatch('answer', { correct: isCorrect, points: pointGain });
    }
</script>

<div class="min-h-screen flex items-center justify-center p-4">
    <div class="card w-full max-w-3xl bg-base-100 shadow-xl">
        <div class="card-body items-center text-center">
            <h2 class="card-title text-3xl mb-8">{question}</h2>
            
            <div class="grid grid-cols-1 md:grid-cols-2 gap-4 w-full">
                <button 
                    on:click={() => handleAnswer(1)}
                    class="btn btn-primary h-24 text-lg"
                >
                    {answer1}
                </button>
                <button 
                    on:click={() => handleAnswer(2)}
                    class="btn btn-secondary h-24 text-lg"
                >
                    {answer2}
                </button>
                <button 
                    on:click={() => handleAnswer(3)}
                    class="btn btn-accent h-24 text-lg"
                >
                    {answer3}
                </button>
                <button 
                    on:click={() => handleAnswer(4)}
                    class="btn btn-warning h-24 text-lg"
                >
                    {answer4}
                </button>
            </div>
        </div>
    </div>
</div>