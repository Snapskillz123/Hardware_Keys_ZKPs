# ZKPs
  ## Definition
  A Zero-Knowledge Proof (ZKP) is a cryptographic method that allows one party (the prover) to prove to another (the verifier) that they know a specific piece of information without revealing the information itself.
  It ensures privacy while still verifying the truth of a statement.
  ## Simple Examples
  ### Cave example
  Two friends,say Mario and Luigi, go out for a trek and find an intriguing cave with two paths(A and B) that connect to each other with a door present where the paths meet. This door has a secret password where if you whisper the magic words,it opens.
  Luigi wants to prove that he knows the password without actually telling Mario the password.

  ![image](https://github.com/user-attachments/assets/121fb001-888c-4dce-84d7-61e8deb9ffed)

  While Mario is outside the cave, Luigi goes inside and picks either path A or B to enter the cave. Mario doesn't know which path Luigi has picked as he was outside.
  
  Now Mario shouts from outside and tells Luigi to come out of a path (Let's say A). Luigi comes out of path A. Luigi could have anyways entered though A so Mario is still unsaure whether luigi actually knows the passwords or not.
  So without looking, Mario tells Luigi to enter a path again randomly and come out of a path that Mario shouts, and obviously Luigi comes out of this path. Mario is in disbelief and keeps telling Luigi to repeat the process.

  After a point the chance that Luigi doesn't know the password and is getting lucky with his choice is very low. So now Mario is convinced that Luigi knows the password, but Luigi hasn't told him what the password actually is.

  ### Pen Example
  We have two friends playing a game with pens, say Alice and Bob.
  Alice is colourblind and has 2 pens of colours red and blue in her handand to her the pens are identical. Bob tells her to either swap the pens behind her back or not and Bob will guess what she has done.

  Bob wants to prove that he knows the colours of the pen without actually telling Alice which pen is which colour.
  
  Bob can clearly see whether she has switched the pens or not but alice cannot verify it for sure whether he guessed or he knows because she is colourblind. So Alice puts the pens behind her back again and repeats the process.
  
  If Bob guess her action again she'd become more certain that he knows the colour of the pens even though she doesn't actually know the colour of the pens.
  ## Three Main Properties of ZKP:
  ### Completeness
  If the statement is true, an honest prover can convince an honest verifier.
  ### Soundness
  If the statement is false, no dishonest prover can convince the verifier that it’s true (except with a tiny probability).
  ### Zero-Knowledge
  If the statement is true, the verifier learns nothing other than that it is true (i.e., no additional information is revealed).
  
  ## Applications
  ZKP is widely used for secure authentication, privacy-preserving transactions, and blockchain applications.
