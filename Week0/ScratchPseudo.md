# Plancaster 
<br>
Lancaster Sprite

Define Introduction <br>
  show Lancaster costume <br>
  set rotation style to don't rotate <br>
  set x = 0 and y = 0 <br>
  set Score = 0 <br>
  print No cellphones in the hallway, and please don't have coffee delivered for you! <br>
  print Catch all the cellphones to avoid Saturday detention. <br>
  print If you bump into a smiley face, you will be banished to Saturday detention! <br>
  print The smiley faces move faster as the game goes on. <br>
  print Press the space bar to begin. <br>
  wait until space bar pressed <br>
  <br>
When green arrow clicked <br>
  call Introduction <br>
<br>  
When space bar pressed <br>
  begin game <br>
  forever <br>
    if left arrow pressed <br>
      set x = x - 12 <br>
    if right arrow pressed <br>
      set x = x + 12 <br>
    if down arrow pressed <br>
      set y = y - 12 <br>
    if up arrow pressed <br>
      set y = y + 12 <br>
    if on edge <br>
      bounce <br>
      <br>
When game begins <br>
  forever <br>
    play Power until done <br>
    <br>
When game is over <br>
  stop other scripts <br>
  switch costume to Cogdill <br>
  start sound Lose <br>
  print GAME OVER! <br>
  print I would've gotten away with it if it weren't for you meddling kids! <br>
  print Your score is + Score <br>
  if Score >= 20 <br>
    print You're safe from Saturday detention...for now. <br>
  else <br>
    print Not enough to avoid Saturday detention....see you there <br>
    play Laugh3 until done <br>
    <br>
Cellphone Sprite <br>
<br>
  When green arrow clicked <br>
    hide Cellphone <br>
  <br>
  When game begins <br>
    show Cellphone <br>
    set rotation style to don't rotate <br>
    forever <br>
      glide to rand position for one second <br>
      if on edge <br>
        bounce <br>
      if touching Lancaster <br>
        set Score = Score + 1 <br>
        hide Cellphone <br>
        go to rand position <br>
        wait 0.8 seconds <br>
        show Cellphone <br>
         <br>
  When game is over <br>
    hide Cellphone <br>
    <br>
Smile Sprite <br>
<br>
  When play button clicked <br>
    hide Smille <br>
    <br>
  When game begins <br>
    show Smile <br>
    set rotation style to don't rotate <br>
    set Time = 1.75 <br>
    forever <br>
      glide to rand position in Time seconds <br>
      if on edge <br>
        bounce <br>
      Set Time = Time - 0.02 <br>
      if touching Lancaster <br>
        end game <br>
        hide Smile <br>
   
 
