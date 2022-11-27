# Socket/Websocket

É importe ressaltarmos as diferenças entre socket e websocket.
WebSocket é o protocolo de comunicação que fornece comunicação bidirecional entre o Cliente e o Servidor através de uma conexão TCP. O WebSocket permanece aberto o tempo todo, permitindo a transferência de dados em tempo real. 

# POC

Para a criação de uma conexão Servidor/Cliente de um Socket é necessário a utilização de alguns métodos, os principais deles são:

1-) Criando um Socket:

int sockfd = socket(dominio, conexao, protocolo)

Onde dominio corresponde a AF_ LOCAL, conexao = SOCK_STREAM: TCP ou SOCK_DGRAM: UDP e protocolo = 0, que corresponde ao valor do Procolo Internet.


2-) Fornecer o endereço e a porta para o Socket:

int bind(int sockfd, const struct sockaddr *addr, socklen_t addrlen);


3-) Esperar o cliente chamar o servidor:

int listen(int sockfd, int backlog);


4-) Criação de uma nova conexao de Socket:

int new_socket= accept(int sockfd, struct sockaddr *addr, socklen_t *addrlen);



