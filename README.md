# Tic Tac Toe 2.0

Ultimate Tic Tac Toe em português europeu, com visual neon, dois jogadores locais, CPU com três dificuldades e lobbies online 1x1.

Joga em https://yvllima.github.io/tic-tac-toe-2/ .

## Jogar com um amigo em PCs diferentes

1. Ambos abrem o site e escolhem **Online · Lobby 1x1**.
2. Um jogador clica em **Criar lobby** e envia o código de 8 caracteres ao amigo.
3. O amigo introduz esse código e clica em **Entrar no lobby**.
4. Quem cria controla X; quem entra controla O. Mantém as páginas abertas.

As jogadas e o placar sincronizam através de um canal WebRTC ordenado. O anfitrião valida as jogadas. Os lobbies têm dois lugares; ao sair ou atualizar a página, a ligação termina. Após o fim, o anfitrião pode iniciar outra partida. Desfazer e reiniciar estão desativados no modo online.

HTML, CSS e JavaScript puro num único index.html, sem bibliotecas externas nem armazenamento persistente. O modo online usa o serviço público gratuito PeerServer (0.peerjs.com) para sinalização e servidores STUN Google/Cloudflare para estabelecer a ligação direta. Depende da disponibilidade desses serviços. Algumas redes ou VPNs impedem WebRTC direto; não existe servidor TURN de retransmissão configurado. Não é necessário criar conta.

A célula escolhida determina o próximo mini-tabuleiro. Conquista três mini-tabuleiros em linha para vencer!
