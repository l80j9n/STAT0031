java c
Speciﬁc information for this piece of coursework 
• Answer   ALL   questions.
• Students   must   work   alone.
• AI   tools   cannot   be   used.
• You   may   submit   only   one   answer   to   each   question.
• The   total   number   of marks   is   50.
•   The   numbers   in   square   brackets   indicate   the   relative   weights   attached   to   each   part   question.
•   Marks   are   awarded   not   only   for   a   ﬁnal   answer   but   also   for   the   clarity   and   coherence   of your   solution. Do not include   large   amounts   of R   output.
•   Your      answers   should   be   submitted      as   one   pdf   document    (no   larger   than    100MB)   through   the   submission   link   on   the   STAT0031   moodle   page,   within   the      ‘In-course
Assessment’   section.   Your   answers   may   include   hand-written   and/or   type   sections.
•   You must complete   an ICA   cover   sheet to   include   as   the   ﬁrst   page   of your   submitted   document.    The   cover   sheet   can   be   found   within   the   ‘In-course   Assessment’   section   of   the   STAT0031   moodle   page.
•   Your   answers   will   be   marked   anonymously.    Please   DO   NOT   include   your   name   in   any   submitted   material.
• You   may   use   your   course   materials   to   answer   questions.
•   You   may   contact   the   course   lecturer   to   ask   questions   concerning   the   ICA   using   the   ‘In-course   assessment   discussion   forum’   on   the   course   moodle   page.   Please   note,   the   lecturer   will   limit   the   amount   of   help   ofered   to   students   and   cannot   check   answers
(or   part-answers)   or   give   detailed   guidance.
You may use the following notation and results: 
The Poisson distribution,   Poisson(λ),   has   probability   mass   function

where λ > 0.   The   mean   is λ .
The Gamma distribution,   Gamma(Q,   β),   has   probability   density   function

where   Q   > 0   and   β   > 0.    The   mean   is   Q/β   and   the   variance   is   Q/β2.
A multinational electrical components manufacturer   wants   to   limit   the   number   of   faulty components   that   it   produces.   The   company   chooses C factories   for   the   experiment.   At   each         factory, B   large batches of   components are   tested.   The number of   faulty   components   in   the         i-th   batch   at   the   j-th   factory   is   Yi,j .   Let   Y   = (Y1,1, . . . ,   YB,1,   Y1,2, . . . ,   YB,2, . . . ,   Y1,C, . . . ,   YB,C   ).   The   data   can   be   downloaded   in   the   ﬁle   faulty_comp   . txt   from   the   ICA   section   of the         STAT0031 Moodle page and   contains results for   10 batches taken   at   60 factories.
The company’s Bayesian statistician proposes the model
Yi,jjθj    ~ Poisson(θj   ),                      i   = 1,   2, . . . ,   B,    代 写STAT0031 AssessmentR
代做程序编程语言      j   =   1,   2, . . . ,   C 
where Yi,j      are independent given   θj      and 
θj    i..d.    Gamma(Q,   β),                      j   =   1,   2, . . . , C.

1. Choose appropriate hyperpriors for α and β and briefly justify your choice.                        [3]
2. Derive the full conditional distribution of θj .                        [6]
3.   Use   NIMBLE   to   implement a Gibbs   sampler   to   sample   from   the   posterior   distribution   of   this   model   with   the   data   in   the ﬁle   faulty_comp   . txt.   In   your   answer   include all R code needed to run the sampler with two chains and to monitor the chains for Q   and β   ,   i.e.    all steps needed to use the   function   nimbleMCMC.                                                                                  [13]
4.   Draw trace plots and densities of   Q and β   using the ﬁrst 1000 iterations   of   your Gibbs   sampler and comment   on the convergence   and   mixing.                                                                                                             [4]
5.   Decide on an appropriate burn-in (using graphs of   the Gelman-Rubin diagnostic)   and   a   suitable   run   length to   answer the   next   question   (question   6)   (briefly justify your   choices).                                                                                                                       [7]
6.   Use   your   code   to   provide   estimates   (by   reporting   the   posterior   mean   and   a   95%   central credible interval for each parameter) of the following:
7.   The company’s Bayesian statistician is   worried   that   some   batches   have   been   incor-   rectly tested.    She proposes extending the   model by   introducing   the   parameter   Zi,j   which   indicates   whether   the   i-th   batch   at   the   j-th   factory   was   accurately   tested   (Zi,j    = 0) or   inaccurately   tested   (Zi,j      = 1).   The   new   model   is
Yi,jjθj ,   Zi,j    ~ Poisson((1   +   2Zi,j   )θj   ),                      i = 1,   2, . .   . ,   B,          j   = 1,   2, . . . ,   C 
Zi,j    ~ Bernoulli(φ),                      i   = 1,   2, . . . ,   B,          j   =   1,   2, . . . ,   C 
θj    ~   Gamma(2,   β),                      j   = 1,   2, . . . ,   C 
β   ~ Gamma(1,   0.001) 
(a)   Choose   a prior for   φ   and extend   your   NIMBLE   code   in   Question   3   to   sample   from   the   posterior   of   this   model   with   the   data   in   ﬁle   faulty_comp   . txt.    You should only include the model deﬁnition   (i.e.   the nimbleCode   part).                               [4]
(b)   Consider   the   ﬁrst 3 factories (j   = 1;   2;   3) and use   your model and   MCMC   output   to decide which batches are faulty.   Briefly justify your answer.                                                       [7]





         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
