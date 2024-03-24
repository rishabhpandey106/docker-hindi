# docker
1. **What's Docker?**

   Docker ek platform hai jisse aap applications develop, ship, aur run kar sakte hain. Docker aapko aapke applications ko aapke infrastructure se alag rakhne ki suvidha deta hai, jisse aap software ko tezi se deliver kar sakte hain. Docker ke madhyam se aap apne infrastructure ko waise hi manage kar sakte hain jaise aap aapke applications ko manage karte hain. Docker ke methodologies ka istemal karke aap code ko ship, test, aur deploy karne mein delay ko kam kar sakte hain, jisse code likhne aur use production mein chalane mein kam samay lagta hai.

2. **Why do we need Docker?**

   - Like agar aap kisi company me developer ho aur man lo aapne ek project bnaya pr ab aap project bada ho gya h or suppose company ne aur bande allot kr diye ki aap bhi isi project pe kam kro to maan lo aapne project bnaya tha kuch apni configuration pe like -

     Your configuration-
     - os - windows 10
     - tech - node 18.0.1

     lekin agar aapke project pe kam krne wale kisi aur bande ka config. -
     - os - mac
     - tech - node 16.1.2

     hai to project kbhi kam krega hi n phir aap usko bologe ki bhai tum bhi node k version ko upgrade kar lo pr man lo uske apne projects jo k usne node 16.1.2 pe banye h phir wo kam n krenge agar usne upgrade kiya to.

     in conditions se bachne ke liye docker use krte h. 

3. **How does Docker work?**

   like agar layman language me bolu to hame docker engine ki jrurt padti h jo ki alg-alg containers banata krta h jiske andar hame kya tech stack use krna kya os use krna h etc install krte h images k form me jo har container k andar images installed hote h jo ki aapke host/original config pe asar nhi krte nahi uspe depended rahte h (ha space pe depended rahte h as jo images ham install krte h ho kbhi kbhar kafo sapce consume krte h).
     To agar 4 log milke ek project bana rhe h to phle hi docker container bna lete h phir uske andar apne hisab se images install krke project ko bnate h taki sabk config. same rahe aur kisi ko dikkat na ho.

4. **Docker Architecture?**

   ![Docker Architecture](https://docs.docker.com/get-started/images/docker-architecture.webp)
   - docker waise client-server achitecture use krta h. docker client sabse phle docker daemon se contact krta h joki normally sare heavy tasks jaise building, distributions etc sambhalta hai.
   docker client ___(docker)___ and docker daemon REST api use krte h connections ke liye.
   - ab docker daemon ___(dockerd)___ listen krta h sare docker api requests ko aur manage bhi karta h docker images/containers ko.
   
   - suppose aapne ___"docker run"___ command likha to sabse phle client phle command ko docker daemon ke pas bhejta h joki use execue krta h.
   - ek docker client kayi docker daemon se communicate kar sakta h.
   
   - ___docker deskop___ ek gui application h jisse docker daemon , contaner , images etc install hote h aapke local pc pe aur is application k madad se aap manage bhi kar sakte h apne docker container/volumes/images ko aasani se.
   
   - ___docker registries___ store karti h docker images ko.
   - ___docker hub___ bilkul hithub h pr docker images ka like agar ham koi image run krte h aur wo install nhi h to wo automatic docker hub se install ho jata h.
