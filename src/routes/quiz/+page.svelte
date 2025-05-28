<script>
    import Question from '$lib/Ask.svelte';
    let totalPoints = 0;
    let currentQuestion = 0;
    
    const questions = [
    {
        question: "Vilket land har vunnit flest VM-titlar i fotboll?",
        answer1: "Tyskland",
        answer2: "Brasilien",
        answer3: "Italien",
        answer4: "Argentina",
        correctAnswer: 2,
        pointGain: 0
    },
    {
        question: "Vem vann Ballon d'Or 2023?",
        answer1: "Lionel Messi",
        answer2: "Kylian Mbappé",
        answer3: "Erling Haaland",
        answer4: "Karim Benzema",
        correctAnswer: 1,
        pointGain: 0
    },
    {
        question: "Vilken klubb har vunnit flest Champions League-titlar?",
        answer1: "AC Milan", 
        answer2: "Bayern München",
        answer3: "Real Madrid",
        answer4: "Liverpool",
        correctAnswer: 3,
        pointGain: 0
    },
    {
        question: "Vilken spelare har gjort flest mål i VM-historien?",
        answer1: "Ronaldo Nazário",
        answer2: "Miroslav Klose",
        answer3: "Pelé",
        answer4: "Messi",
        correctAnswer: 2,
        pointGain: 0
    },
    {
        question: "Vilket år grundades Premier League?",
        answer1: "1992",
        answer2: "1986",
        answer3: "1990",
        answer4: "1994",
        correctAnswer: 1,
        pointGain: 0
    },
    {
        question: "Vilket lag vann EM 2020 (spelades 2021)?",
        answer1: "Spanien",
        answer2: "England",
        answer3: "Italien",
        answer4: "Frankrike",
        correctAnswer: 3,
        pointGain: 0
    },
    {
        question: "Vem är känd som 'El Fenomeno'?",
        answer1: "Cristiano Ronaldo",
        answer2: "Ronaldinho",
        answer3: "Ronaldo Nazário",
        answer4: "Neymar",
        correctAnswer: 3,
        pointGain: 0
    },
    {
        question: "Vilken svensk har gjort flest mål i landslaget?",
        answer1: "Henrik Larsson",
        answer2: "Zlatan Ibrahimović",
        answer3: "Marcus Allbäck",
        answer4: "Gunnar Nordahl",
        correctAnswer: 2,
        pointGain: 0
    },
    {
        question: "Vilken spelare har gjort flest mål i ett kalenderår?",
        answer1: "Cristiano Ronaldo",
        answer2: "Messi",
        answer3: "Lewandowski",
        answer4: "Mbappé",
        correctAnswer: 2,
        pointGain: 0
    },
    {
        question: "Vilken klubb spelar på Old Trafford?",
        answer1: "Liverpool",
        answer2: "Chelsea",
        answer3: "Manchester United",
        answer4: "Arsenal",
        correctAnswer: 3,
        pointGain: 0
    },
    {
        question: "Vem gjorde det berömda 'Hand of God'-målet?",
        answer1: "Pelé",
        answer2: "Maradona",
        answer3: "Messi",
        answer4: "Zidane",
        correctAnswer: 2,
        pointGain: 0
    },
    {
        question: "Vilket land stod värd för VM 2018?",
        answer1: "Brasilien",
        answer2: "Tyskland",
        answer3: "Qatar",
        answer4: "Ryssland",
        correctAnswer: 4,
        pointGain: 0
    },
    {
        question: "Vilket land har aldrig vunnit ett VM?",
        answer1: "England",
        answer2: "Argentina",
        answer3: "Nederländerna",
        answer4: "Frankrike",
        correctAnswer: 3,
        pointGain: 0
    },
    {
        question: "Vem tränade Manchester City 2023?",
        answer1: "Jurgen Klopp",
        answer2: "Pep Guardiola",
        answer3: "Thomas Tuchel",
        answer4: "Carlo Ancelotti",
        correctAnswer: 2,
        pointGain: 0
    },
    {
        question: "Vilken färg har FC Barcelonas hemmatröja?",
        answer1: "Röd och blå",
        answer2: "Gul",
        answer3: "Vit",
        answer4: "Grön",
        correctAnswer: 1,
        pointGain: 0
    },
    {
        question: "Hur många spelare är på planen från ett lag vid matchstart?",
        answer1: "10",
        answer2: "11",
        answer3: "12",
        answer4: "9",
        correctAnswer: 2,
        pointGain: 0
    },
    {
        question: "Vilken position har nummer 1 oftast?",
        answer1: "Mittfältare",
        answer2: "Anfallare",
        answer3: "Målvakt",
        answer4: "Back",
        correctAnswer: 3,
        pointGain: 0
    },
    {
        question: "Vad kallas Europas största klubbtävling?",
        answer1: "Europa League",
        answer2: "Champions League",
        answer3: "Conference League",
        answer4: "Super Cup",
        correctAnswer: 2,
        pointGain: 0
    },
    {
        question: "Vilken klubb är känd som 'The Blues'?",
        answer1: "Chelsea",
        answer2: "Everton",
        answer3: "Manchester City",
        answer4: "Napoli",
        correctAnswer: 1,
        pointGain: 0
    },
    {
        question: "Vilken nation vann VM 2022?",
        answer1: "Frankrike",
        answer2: "Argentina",
        answer3: "Kroatien",
        answer4: "Brasilien",
        correctAnswer: 2,
        pointGain: 0
    }
];

       
    
    function handleAnswer(e) {
        totalPoints += e.detail.points;
        // Move to next question or show results
        if(currentQuestion < questions.length - 1) {
            currentQuestion++;
        }
    }
</script>
<main>
<div class="container mx-auto px-4">
    <div class="text-center mb-8">
        <h1 class="text-4xl font-bold mb-">FotbollsQuiz</h1>
        <p class="text-4xl">Total Points: {totalPoints}</p>
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
</main>
<style>
    main {
        background: linear-gradient(-45deg, #d50ad5, #9b0f0f);
        padding: 20px;
        border-radius: 10px;
        color: white;
    }
    .text-4xl{
        font-size:2.5rem;
        text-align: center;
    }
    </style>