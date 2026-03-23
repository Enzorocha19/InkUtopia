Documento de Regras de Negócio

Sistema de Plataforma de Tatuagens
1. Descrição Geral
A plataforma tem como objetivo conectar clientes, artistas tatuadores e estúdios, permitindo:
divulgação de portfólios

interação social (curtidas, comentários, salvamentos)

comunicação entre usuários

avaliações de serviços

agendamento de tatuagens

O sistema funciona como uma rede social especializada em tatuagem, permitindo que artistas divulguem seus trabalhos e clientes encontrem profissionais e estúdios.
Tecnologia escolhida: PostgreSQL

2. Tipos de Usuários
O sistema possui três tipos principais de usuários:
Cliente
Usuário que acessa a plataforma para:
visualizar trabalhos de artistas

interagir com publicações

entrar em contato com artistas ou estúdios

realizar agendamentos

avaliar serviços

Artista
Usuário profissional que pode:
publicar seus trabalhos

oferecer serviços

participar de um estúdio

receber avaliações

interagir com clientes

Administrador do Estúdio
Usuário artista que criou um estúdio e possui permissões administrativas dentro dele.

3. Regras de Cadastro
RN01 – Cadastro de Usuário
Qualquer pessoa pode criar uma conta na plataforma fornecendo:
nome

email

senha

telefone

Após o cadastro, o usuário deve escolher entre:
Cliente

Artista

RN02 – Alteração de Perfil
Usuários podem atualizar informações do perfil como:
foto

biografia

contato

4. Regras de Estúdio
RN03 – Criação de Estúdio
Apenas usuários do tipo artista podem criar um estúdio.
Ao criar um estúdio, o artista automaticamente se torna:
Administrador do estúdio.

RN04 – Administração do Estúdio
O administrador do estúdio pode:
editar informações do estúdio

aprovar artistas solicitando entrada

remover artistas do estúdio

RN05 – Associação de Artistas
Um artista pode estar associado a apenas um estúdio.
Um estúdio pode possuir vários artistas associados.

RN06 – Solicitação de Entrada no Estúdio
Um artista pode solicitar participação em um estúdio.
A entrada só ocorre após aprovação do administrador do estúdio.

5. Regras de Postagens
RN07 – Postagem de Conteúdo
Artistas podem criar publicações contendo:
imagens

vídeos

descrição do trabalho

preço estimado

RN08 – Postagem do Estúdio
Estúdios também podem realizar postagens.
Essas postagens podem estar relacionadas a:
um artista específico do estúdio

trabalhos realizados no estúdio

RN09 – Portfólio
Cada artista possui um portfólio composto por:
imagens

vídeos

descrições de trabalhos

6. Interações na Plataforma
RN10 – Curtidas
Clientes podem curtir postagens de artistas ou estúdios.
Um usuário pode curtir uma postagem apenas uma vez.

RN11 – Comentários
Usuários podem comentar nas postagens.
Comentários devem estar vinculados a:
usuário autor

postagem

RN12 – Salvamento de Postagens
Clientes podem salvar postagens para visualização posterior.
Essas postagens ficam armazenadas em uma lista de favoritos do usuário.

7. Comunicação
RN13 – Sistema de Mensagens
Clientes podem enviar mensagens para:
artistas

estúdios

Artistas também podem responder às mensagens.

8. Avaliações
RN14 – Avaliação de Artistas
Clientes podem avaliar artistas após interação ou serviço realizado.
A avaliação deve conter:
nota (1 a 5)

comentário opcional

RN15 – Avaliação de Estúdios
Clientes também podem avaliar estúdios.

9. Regras de Agendamento
RN16 – Solicitação de Agendamento
Clientes podem solicitar agendamentos com artistas.
O pedido deve conter:
artista

serviço

data e horário desejados

observações

RN17 – Confirmação do Agendamento
O artista deve confirmar ou recusar o agendamento.
Status possíveis:
pendente

confirmado

cancelado

concluído

10. Moderação e Segurança
RN18 – Conteúdo Inadequado
A plataforma poderá remover conteúdos que:
violem regras da comunidade

contenham material ofensivo

RN19 – Autenticidade
Cada conta deve estar vinculada a um email único.

11. Outras funcionalidades desejáveis para o projeto
Sistema de seguidores
Usuários podem seguir artistas.
Isso permite:
feed personalizado

notificações de novas postagens

Feed personalizado
O sistema mostra:
posts de artistas seguidos

posts populares

artistas próximos da localização

Localização de estúdios
Integração com mapa para mostrar:
estúdios próximos

endereço

rota até o local

Notificações
Usuários recebem notificações quando:
alguém curte sua postagem

alguém comenta

recebe mensagem

agendamento é confirmado

Agenda do artista
Artistas possuem um calendário com:
horários disponíveis

agendamentos marcados

Denúncia de conteúdo
Usuários podem denunciar:
perfis

postagens

comentários

12. Exclusão de conta, postagens
RN20 – Exclusão de conta
Usuários podem excluir suas contas.
Ao excluir a conta:
seus dados são removidos do banco de dados
as postagens relacionadas a conta excluída serão também excluídas
RN21 – Exclusão de post
Artistas e estúdios podem excluir postagens feitas
Ao excluir a postagem:
Os dados relacionados a postagem serão excluídos
