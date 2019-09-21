# Plancaster <break>
<break>
Lancaster Sprite <break>

Define Introduction <break>
  show Lancaster costume <break>
  set rotation style to don't rotate <break>
  set x = 0 and y = 0 <break>
  set Score = 0 <break>
  print No cellphones in the hallway, and please don't have coffee delivered for you! <break>
  print Catch all the cellphones to avoid Saturday detention. <break>
  print If you bump into a smiley face, you will be banished to Saturday detention! <break>
  print The smiley faces move faster as the game goes on. <break>
  print Press the space bar to begin. <break>
  wait until space bar pressed <break>
  <break>
When green arrow clicked <break>
  call Introduction <break>
<break>  
When space bar pressed <break>
  begin game <break>
  forever <break>
    if left arrow pressed <break>
      set x = x - 12 <break>
    if right arrow pressed <break>
      set x = x + 12 <break>
    if down arrow pressed <break>
      set y = y - 12 <break>
    if up arrow pressed <break>
      set y = y + 12 <break>
    if on edge <break>
      bounce <break>
      <break>
When game begins <break>
  forever <break>
    play Power until done <break>
    <break>
When game is over <break>
  stop other scripts <break>
  switch costume to Cogdill <break>
  start sound Lose <break>
  print GAME OVER! <break>
  print I would've gotten away with it if it weren't for you meddling kids! <break>
  print Your score is + Score <break>
  if Score >= 30 <break>
    print You're safe from Saturday detention...for now. <break>
  else <break>
    print Not enough to avoid Saturday detention....see you there <break>
    play Laugh3 until done <break>
    <break>
Cellphone Sprite <break>
<break>
  When green arrow clicked <break>
    hide Cellphone <break>
  <break>
  When game begins <break>
    show Cellphone <break>
    set rotation style to don't rotate <break>
    forever <break>
      glide to rand position for one second <break>
      if on edge <break>
        bounce <break>
      if touching Lancaster <break>
        set Score = Score + 1 <break>
        hide Cellphone <break>
        go to rand position <break>
        wait 0.8 seconds <break>
        show Cellphone <break>
         <break>
  When game is over <break>
    hide Cellphone <break>
    <break>
Smile Sprite <break>
<break>
  When play button clicked <break>
    hide Smille <break>
    <break>
  When game begins <break>
    show Smile <break>
    set rotation style to don't rotate <break>
    set Time = 2 <break>
    forever <break>
      glide to rand position in Time seconds <break>
      if on edge <break>
        bounce <break>
      Set Time = Time - 0.02 <break>
      if touching Lancaster <break>
        end game <break>
        hide Smile <break>
   
 
