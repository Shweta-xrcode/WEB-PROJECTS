let userscore=0;
let compscore=0;

const choices=document.querySelectorAll(".choice");
const msg=document.querySelector("#msg");

const userscorepara = document.querySelector("#user-score");
const compscorepara = document.querySelector("#comp-score");

const computerchoice=()=>{
    const options=["rock","paper","scissor"];
    const randidx=Math.floor(Math.random()*3);
    return options[randidx];
}

const drawgame=() =>{
    
    msg.innerText="game was draw. play again";
    msg.style.background="black";
}

const showWinner= (userwin) =>{
    if(userwin) {
        userscore++;
        userscorepara.innerText= userscore;
        msg.innerText="you win";
        msg.style.background ="green";
    }else{
        compscore++;
        compscorepara.innerText= compscore;
        console.log("you lose");
        msg.innerText="you lose";
        msg.style.background="red";
    }
}

const playgame=(userchoice) =>{
     

     // generate computer choice
     const compchoice=computerchoice();
    

     if(userchoice=== compchoice) {
        //drawgame
        drawgame();
     }else{
        let userwin = true;
        if(userchoice === "rock") {
            //scissors,paper
            userwin= compchoice=== "paper" ? false: true;
        }else if(userchoice==="paper"){
            //rock,scissor
            userwin=compchoice==="scissor" ? false: true;
        }else{
            //rock,paper
            userwin= compchoice==="rock" ? false : true;
        }
        showWinner(userwin , userchoice , compchoice);

     }
}

choices.forEach((choice)=>{
    
    choice.addEventListener("click", () =>{
        const userchoice=choice.getAttribute("id");
        playgame(userchoice);

    })
})