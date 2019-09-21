# Plancaster

Lancaster Sprite

Define Introduction
  show Lancaster costume
  set rotation style to don't rotate
  set x = 0 and y = 0
  set Score = 0
  print No cellphones in the hallway, and please don't have coffee delivered for you!
  print Catch all the cellphones to avoid Saturday detention.
  print If you bump into a smiley face, you will be banished to Saturday detention!
  print The smiley faces move faster as the game goes on.
  print Press the space bar to begin.
  wait until space bar pressed
  
When green arrow clicked
  call Introduction
  
When space bar pressed
  begin game
  forever
    if left arrow pressed
      set x = x - 12
    if right arrow pressed
      set x = x + 12
    if down arrow pressed
      set y = y - 12
    if up arrow pressed
      set y = y + 12
    if on edge
      bounce
      
When game begins
  forever
    play Power until done
    
When game is over
  stop other scripts
  switch costume to Cogdill
  start sound Lose
  print GAME OVER!
  print I would've gotten away with it if it weren't for you meddling kids!
  print Your score is + Score
  if Score >= 30
    print You're safe from Saturday detention...for now.
  else
    print Not enough to avoid Saturday detention....see you there
    play Laugh3 until done
    
Cellphone Sprite

  When green arrow clicked
    hide Cellphone
  
  When game begins
    show Cellphone
    set rotation style to don't rotate
    forever
      glide to rand position for one second
      if on edge
        bounce
      if touching Lancaster
        set Score = Score + 1
        hide Cellphone
        go to rand position
        wait 0.8 seconds
        show Cellphone
        
  When game is over
    hide Cellphone
    
Smile Sprite

  When play button clicked
    hide Smille
    
  When game begins
    show Smile
    set rotation style to don't rotate
    set Time = 2
    forever
      glide to rand position in Time seconds
      if on edge
        bounce
      Set Time = Time - 0.02
      if touching Lancaster
        end game
        hide Smile
   
 
