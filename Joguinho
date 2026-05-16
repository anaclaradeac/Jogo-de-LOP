# Jogo-de-LOP
Jogo criado para a disciplina de Lógica de Programação
//Link do vídeo: https://youtu.be/t6dqhriVWY8
//Descrisão: https://docs.google.com/document/d/1IPl-2uLw8L66Nolsl9cl4dY1M4Tn69FqoUkyXpb2zsM/edit?usp=sharing

// tela 
// 0 = Menu 
// 1 = Jogar 
// 2 = Instruções 
// 3 = Creditos 
// 4 = Jogo
// 5 = Perdeuuu 
// 6 = Parabéns ganhouu

var tela = 0
var x = 300 
var y = 360 
var x1
var y1 = 0
var l = 25
var pontuacao = 0
var vida = 3
var imagem1
var imagem2 
var imagem3 
var imagem4 
var imagem5 
var imagem6
var imagem7
var imagem8 
var imagem9
var dataInicial;
var tempoInicial;
var tempo; 
var colisao = false;
var pose = 0;
var poseTime=0;
var mode = 0;
var idle = [];
var walk = [];
var jump = [];
var gojo = []

let pulo;
let tempo_pulo=0;
let pulando;
let pulo_posicao_y_jogador = y;
let varpulo;
var yChao = 200
var yc = yChao
var estapulando=false

function preload(){
    
    idle[0] = loadImage('assets_itadori/yuji0.png');
    idle[1] = loadImage('assets_itadori/yuji1.png');
    idle[2] = loadImage('assets_itadori/yuji2.png');
    idle[3] = loadImage('assets_itadori/yuji3.png');
    idle[4] = loadImage('assets_itadori/yuji4.png');
  
    walk[0] = loadImage('assets_itadori/yujirun0.png');
    walk[1] = loadImage('assets_itadori/yujirun1.png');
    walk[2] = loadImage('assets_itadori/yujirun2.png');
    walk[3] = loadImage('assets_itadori/yujirun3.png');
    walk[4] = loadImage('assets_itadori/yujirun4.png');
    walk[5] = loadImage('assets_itadori/yujirun5.png');

    jump[0] = loadImage('assets_itadori/yujijump0.png');
    jump[1] = loadImage('assets_itadori/yujijump1.png');
    jump[2] = loadImage('assets_itadori/yujijump2.png');
    jump[3] = loadImage('assets_itadori/yujijump3.png');
  
    gojo[0] = loadImage('satoru/gojo0.png');
    gojo[1] = loadImage('satoru/gojo1.png');
    gojo[2] = loadImage('satoru/gojo2.png');
    gojo[3] = loadImage('satoru/gojo3.png');
    gojo[4] = loadImage('satoru/gojo4.png');
    gojo[5] = loadImage('satoru/gojo5.png');
    gojo[6] = loadImage('satoru/gojo6.png');
    gojo[7] = loadImage('satoru/gojo7.png');
    gojo[8] = loadImage('satoru/gojo8.png');  
  
  imagem1 = loadImage("assets/AnaClara.jpg")
  imagem2 = loadImage("assets/Aquiles.png")
  imagem3 = loadImage("assets/Tela0.png")
  imagem4 = loadImage("assets/Tela1.png")
  imagem5 = loadImage("assets/Tela2.png")
  imagem6 = loadImage("assets/Tela3.png")
  imagem7 = loadImage("assets/Tela4.png")
  imagem8 = loadImage("dedosukuna.png")
  imagem9 = loadImage("assets/roxo.png")
  
}

function setup() {
  createCanvas(650,450); 
  x1 = random(25,625); 
  entrada = createInput();
  
}

function draw(){
  if(tela==0){
    image(imagem3,0,0,650,450)  
    textSize(20)
    rect(190,210,270,50,15)  
    text("INSTRUÇÕES",265,240) 

    rect(190,130,270,50,15)
    text("JOGAR",295,160)
    
    rect(190,290,270,50,15)  
    text("CRÉDITOS",275,320)
    entrada.position(0, 470);
 
    
  }else if(tela==1){
    image (imagem4,0,0,650,450) 
    rect(20,380,100,50,15)  //Forma de voltar
    text("Voltar",45,410) 
    rect(330,150,180,50,50) //Forma do BORA LÁ  
    text("BORA LÁ",375,180)
    
    rect(140,65,335,30,0) //Forma da frase
    
    text("Digite seu nome:",150,85)
    entrada.position(290, 70);
    
    msg = entrada.value();
    
    textSize(20) //Tamanho do texto
    
    
    }else if(tela==2){
    image(imagem5,0,0,650,450)
    textSize(20)
    rect(60,50,530,210,30) //Forma do texto 
    rect(20,380,100,50,15) //Forma do voltar 
    text("Voltar",45,410)
    text("Olá e seja bem vindo(a)!",230,85) 
    text("Esta é a criação do meu primeiro jogo!!!",180,110) 
    text("Para mais informações sobre a descrição do jogo click:",100,135) 
    
    textSize(11)
    text("https://docs.google.com/document/d/1IPl-2uLw8L66Nolsl9cl4dY1M4Tn69FqoUkyXpb2zsM/edit?usp=sharing",72,160)
    
    textSize(20)
    text("Espero que você se divirta.",220,200) 
    
    text("Aproveite o jogo!",250,235)

  }else if(tela==3){
    image(imagem6,0,0,650,450)
    rect(20,380,100,50,15) 
    text("Voltar",45,410) 
    rect(220,30,160,30,30) 
    text("Desenvolvedores:",230,50) 
    textSize (20) 
    rect(90,70,170,220,10)
    image(imagem1,100,80,150,200) 
    rect(340,70,170,220,10)
    image(imagem2,350,80,150,200) 
    rect(50,300,250,55,0) 
    text("Ana Clara de Almeida Cabral",55,320) 
    text("Discente e programadora",75,345) 
    rect(330,300,190,80,0)
    text("Aquiles Medeiros",355,320) 
    text("Filgueira Burlamaqui",340,345) 
    text("Professor responsável",340,370)
           
    
  }else if(tela==4){
    image(imagem7,0,0,650,450)
    rect(560,30, 60,30,5) //Forma do voltar 
    text ("Voltar",565,50)
    textSize (20)
    entrada.position(0,470);
     
  if(keyIsDown(LEFT_ARROW))
    if(x>0) //A bola vai pra esquerda se x for maior que 25 
      x-=8;  

  if(keyIsDown(RIGHT_ARROW))
    if(x<600) // A bola vai pra direita se x for maior que 575 
      x+=8;  

  if(keyIsDown(UP_ARROW) && !estaPulando )
    yc = yChao-120
    estaPulando=true
  
    if(estaPulando){
    if(y<yChao){
      y = y + 12
    }
    }else{
      estaPulando=false
      y = yChao
    }
    
  if(mode==0){
    image(idle[pose%5], x, pulo_posicao_y_jogador,50,50)
  }else if(mode==1){
      image(walk[pose%6], x, pulo_posicao_y_jogador,70,50) 
    }else if(mode==2){
       image(jump[pose%4], x, pulo_posicao_y_jogador,50,50) 
  } 
    
  if(poseTime==8){
    pose++
    poseTime=0
  }else{
    poseTime++
  }
    
  if(keyIsPressed===true){
    if(pulando)
      mode=2
    else
      mode=1  
  }else{
   mode=0
  }
    
    function pular(){
   if(pulando){
     varpulo = tempo_pulo-230
     pulo =-tempo_pulo*varpulo
     
     tempo_pulo = tempo_pulo + 0.5
     if(pulo<0){
       pulando=false
       pulo=0
       tempo_pulo=0
    }
    pulo_posicao_y_jogador = y - pulo 
   }   
}
   
    
  image(imagem8,x1,y1,l,50,70,100)
  //ellipse(x1,y1,l)
    
  y1=y1+3
    
  if(pontuacao>10){
    y1=y1+4
  }
    
  if(pontuacao==20){
    tela=6
  }
    
  if(colisao==true){
    x1=random(25,625)
    y1=0
    colisao=false
  }
    if(y1>450){
    x1=random(25,625)
    y1=0
    vida--
    colisao=false
  }
    
  //colisão
    
  c = dist(x,y,x1,y1)
    
  if(c>10 && c<35){
    colisao = true
    pontuacao++
  } 
    if(vida==0){
      tela=5
    } 
    
    dataAtual = new Date()
    tempoAtual = dataAtual.getTime()
    tempo = tempoAtual - tempoInicial
    
  if(tempo>30001){
    dataAtual = new Date()
    tempoInicial = dataAtual.getTime()
    tela=5
  }
      
    rect(340,30,130,30)
    text("Pontuação: " + pontuacao ,350,50); 
    
    rect(230,30, 90, 30)
    text("Vida = " + vida, 240,50)
    
    rect(95,30, 110, 30)
    text("Tempo: " + parseInt(tempo/1000) + "s",100,50)
    
  }else if(tela==5){
    background(220)
    text("FIM DE JOGO, VOCÊ PERDEUUU",180,150)
    rect(190,210,270,50,15)  
    text("Jogar novamente",265,240)
    rect(190,290,270,50,15)  
    text("Voltar ao Menu",265,320)
    
  }else if(tela==6){
    image(imagem9,0,0,650,450)
    rect(175,120,300,30,15)
    text("PARABÉNS, VOCÊ GANHOU!",190,140)
    
  
    rect(190,210,270,50,15)  
    text("Voltar ao menu",265,240)
  
    
  }text( mouseX + "/" + mouseY + "/" + tela,10,15)
  
}

function mouseClicked(){
  if (tela==0){
    if(mouseX>=190 && mouseX<=460 && mouseY>=130 && mouseY<=180){
      console.log("Clicou em Jogar")  
      tela=1  
 
    }else if(mouseX>=190 && mouseX<=460 && mouseY>=210 && mouseY<=260){
      console.log("Instruções") 
      tela=2

    }else if(mouseX>=190 && mouseX<=460 && mouseY>=290 && mouseY<=340){
      console.log("Créditos")
      tela=3  
    
    }
 }
  
  else if (tela==1){
    if(mouseX>=330 && mouseX<=510 && mouseY>=150 && mouseY<=200){
      console.log("BORA LÁ " + msg) 
      dataInicial = new Date();
      tempoInicial = dataInicial.getTime();
      tempo = 0
      pontuacao = 0
      vida = 3
      tela = 4
    
    }
  }
  if(tela==1 || tela==2 || tela==3){
    if(mouseX>=20 && mouseX<=120 && mouseY>=380 && mouseY<=430){
      console.log("Voltar") 
      tela=0 
    }

  }else if(tela==4){
    if(mouseX>=560 && mouseX<=620 && mouseY>=30 && mouseY<=60){
      console.log ("Voltar") 
      tela=1
    }
  }
    if(tela==5){
      if(mouseX>=190 && mouseX<=460 && mouseY>=210 && mouseY<=260){
        console.log("Jogar novamente")
        dataInicial = new Date();
        tempoInicial = dataInicial.getTime();
        tempo = 0 
        vida = 3
        pontuacao = 0
        tela=4
      
      }else if(mouseX>=190 && mouseX<=460 && mouseY>=290 && mouseY<=340){
           console.log("Voltar ao menu") 
           tela=0
      }
    }
  if(tela==6){
     if(mouseX>=190 && mouseX<=460 && mouseY>=210 && mouseY<=260){
         console.log("Voltar ao menu")
         tela=0
    }
  }
}
