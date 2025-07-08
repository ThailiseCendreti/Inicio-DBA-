create table clientes (
id serial primary key,
nome varchar (100) not null,
email varchar (100) unique not null,
cidade varchar (100)
);


create table produtos (
id serial primary key ,
nome varchar (100) not null, 
preco numeric (10,2) not null check (preco >0) , 
estoque int default 0 check (estoque >= 0)
);


create table pedidos (
id serial primary key,
data_pedido date not null default current_date,
cliente_id int not null,
constraint fk_cliente
   foreign key (cliente_id)
   references clientes(id)
   );



insert into clientes (nome, email, cidade) values
('Marceline da Cunha', 'marceline@email.com', 'Jacareí'),
('Pakita da Silva', 'paki_kiki@rmail.com', 'São Paulo'),
('Jorginho Cendreti', 'jorginho@email.com', 'Jacareí'),
('Jane be Good', 'janecunha@email.com', 'Santa Branca'),
('Derby da Silva', 'derby@email.com', 'Santa Branca'),
('Cristian Cunha', 'cristian@email.com', 'Santa Branca'),
('Thailise Cendreti Cunha','thailise@email.com', 'Guararema'),
('Silvia Cendreti', 'silvia@email.com', 'Caraguatatuba'),
('Marcos Cendreti', 'marcos@email.com', 'Caraguatatuba'),
('Juliana da Silva', 'jujuba@email.com', 'Caraguatatuba'),
('Cleiton Rasta','cleitinho@email.com','Caraguatatuba'),
('Marcos Junior', 'juninho@email.com','Jacareí'),
('Francisca Ferreira', 'fran@email.com', 'Santa Branca'),
('José Apolinario', 'jose@email.com', 'Santa Branca'),
('Cristiane Dulce', 'cristiane@email.com', 'Santa Branca'),
('Lucky da Silva', 'lucky@email.com', 'Santa Branca'),
('Luna luninha', 'luna@email.com', 'Santa Branca'),
('Jonatas Tainha', 'tainha@email.com', 'Santa Branca');
('Adriana Guedes', 'Dri@email.com', 'São Paulo'),
('Grazy Guedes', 'grazy@email.com','São Paulo'),
('Gaby Guedes', 'gabiiiii@email.com', 'São Paulo'),
('Elcio Guedes', 'elcio@email.com', 'São Paulo'),
('Jeferson Silva', 'jeferson@email.com', 'São José dos Campos'),
('Mariana Castro', 'mariana@email.com', 'São José dos Campos'),
('Gustavo Castro', 'gustavo@email.com', 'São José dos Campos'),
('Renata Tavares', 'renata.tavares@email.com', 'Taubaté'),
('Bruno Oliveira', 'bruno.oliveira@email.com', 'São Paulo'),
('Larissa Moura', 'larissa.moura@email.com', 'Jacareí'),
('Carlos Henrique', 'carlos.henrique@email.com', 'Santa Branca'),
('Tatiane Lima', 'tatiane.lima@email.com', 'Caçapava'),
('Igor Almeida', 'igor.almeida@email.com', 'São José dos Campos'),
('Débora Santos', 'debora.santos@email.com', 'Jacareí'),
('Alex Meireles', 'alex.meireles@email.com', 'Guararema'),
('Viviane Rocha', 'viviane.rocha@email.com', 'Pindamonhangaba'),
('Leandro Reis', 'leandro.reis@email.com', 'Caraguatatuba'),
('Bárbara Costa', 'barbara.costa@email.com', 'São José dos Campos'),
('André Ramos', 'andre.ramos@email.com', 'São Paulo'),
('Paula Azevedo', 'paula.azevedo@email.com', 'Santa Branca'),
('Mateus Vieira', 'mateus.vieira@email.com', 'Jacareí'),
('Nathalia Prado', 'nathalia.prado@email.com', 'São José dos Campos'),
('Sérgio Antunes', 'sergio.antunes@email.com', 'Guaratinguetá'),
('Helena Teixeira', 'helena.teixeira@email.com', 'São Paulo'),
('William Torres', 'william.torres@email.com', 'Caçapava'),
('Lívia Fernandes', 'livia.fernandes@email.com', 'Pindamonhangaba'),
('Douglas Nogueira', 'douglas.nogueira@email.com', 'Taubaté'),
('Cristina Amaral', 'cristina.amaral@email.com', 'São José dos Campos'),
('Felipe Cunha', 'felipe.cunha@email.com', 'São Paulo'),
('Mônica Barreto', 'monica.barreto@email.com', 'Jacareí'),
('Luciano Ribeiro', 'luciano.ribeiro@email.com', 'Guararema'),
('Amanda Freitas', 'amanda.freitas@email.com', 'Caraguatatuba'),
('Eduarda Luz', 'eduarda.luz@email.com', 'Guaratinguetá'),
('Raul Torres', 'raul.torres@email.com', 'Jacareí'),
('Isadora Mendes', 'isadora.mendes@email.com', 'São José dos Campos'),
('Fernando Peixoto', 'fernando.peixoto@email.com', 'Taubaté'),
('Jéssica Antunes', 'jessica.antunes@email.com', 'São Paulo'),
('Samuel Brito', 'samuel.brito@email.com', 'Santa Branca'),
('Camila Vargas', 'camila.vargas@email.com', 'Caçapava'),
('Rogério Macedo', 'rogerio.macedo@email.com', 'Guararema'),
('Clarice Bittencourt', 'clarice.bittencourt@email.com', 'Caraguatatuba'),
('Diego Araújo', 'diego.araujo@email.com', 'São Paulo'),
('Tatiane Sales', 'tatiane.sales@email.com', 'São José dos Campos'),
('Ricardo Cunha', 'ricardo.cunha@email.com', 'Taubaté'),
('Talita Ribeiro', 'talita.ribeiro@email.com', 'Pindamonhangaba'),
('Murilo Sanches', 'murilo.sanches@email.com', 'Jacareí'),
('Yasmin Moura', 'yasmin.moura@email.com', 'Guararema'),
('Rafael Godoy', 'rafael.godoy@email.com', 'São Paulo'),
('Daniele Lopes', 'daniele.lopes@email.com', 'Santa Branca'),
('Otávio Campos', 'otavio.campos@email.com', 'São José dos Campos'),
('Vanessa Rocha', 'vanessa.rocha@email.com', 'Lorena'),
('Thiago Duarte', 'thiago.duarte@email.com', 'Guaratinguetá'),
('Brenda Ferreira', 'brenda.ferreira@email.com', 'Jacareí'),
('Matheus Alves', 'matheus.alves@email.com', 'São Paulo'),
('Sabrina Lima', 'sabrina.lima@email.com', 'Caraguatatuba'),
('Danilo Costa', 'danilo.costa@email.com', 'Caçapava'),
('Milena Teixeira', 'milena.teixeira@email.com', 'São José dos Campos');



insert into produtos (nome, preco, estoque) values
('Ração para cães - 5kg', 120.00, 20),
('Ração para gatos - 3kg', 95.50, 30),
('Brinquedo para cães', 45.00, 50),
('Arranhador para gatos', 70.00, 15),
('Coleira para cães', 35.00, 40),
('Areia sanitária perfumada', 28.00, 25),
('Petiscos naturais para cães', 22.50, 60),
('Camisa para cachorro', 55.00, 10),
('Cama para gatos', 150.00, 8),
('Shampoo antialérgico para pets', 40.00, 35),
('Ração premium para cães adultos - 10kg', 230.00, 15),
('Ração para filhotes de gatos - 2kg', 85.00, 20),
('Brinquedo de corda para cães', 38.00, 45),
('Arranhador com brinquedo para gatos', 80.00, 12),
('Coleira com GPS para cães', 250.00, 5),
('Areia sanitária biodegradável', 35.00, 20),
('Petiscos de frango para cães', 18.00, 70),
('Capa de chuva para cachorro', 60.00, 8),
('Caminha ortopédica para cães', 220.00, 6),
('Shampoo antipulgas para cães', 42.00, 30),
('Ração light para cães idosos - 5kg', 130.00, 18),
('Ração para gatos sênior - 3kg', 100.00, 22),
('Bola de brinquedo para cães', 25.00, 55),
('Arranhador de parede para gatos', 65.00, 14),
('Coleira de nylon para cães', 20.00, 50),
('Areia sanitária com controle de odor', 33.00, 27),
('Petiscos dentais para cães', 27.00, 60),
('Moletom para cachorro', 70.00, 9),
('Cama dobrável para gatos', 140.00, 7),
('Condicionador para pelagem de pets', 38.00, 40),
('Ração para cães com alergia - 5kg', 160.00, 13),
('Ração para gatos filhotes - 4kg', 90.00, 18),
('Brinquedo interativo para cães', 55.00, 35),
('Arranhador com plataforma para gatos', 85.00, 11),
('Coleira refletiva para cães', 30.00, 45),
('Areia sanitária aglomerante', 29.00, 28),
('Petiscos de carne para cães', 24.00, 65),
('Capa impermeável para cachorro', 58.00, 12),
('Caminha para gatos pequena', 135.00, 6),
('Shampoo neutro para pets', 35.00, 38),
('Ração para cães de pequeno porte - 3kg', 110.00, 25),
('Ração para gatos adultos - 5kg', 120.00, 20),
('Brinquedo para mastigar cães', 40.00, 48),
('Arranhador vertical para gatos', 75.00, 13),
('Coleira anti-pulgas para cães', 28.00, 35),
('Areia sanitária sem perfume', 27.00, 30),
('Petiscos de peixe para cães', 26.00, 55),
('Moletom com capuz para cachorro', 75.00, 7),
('Cama aquecida para gatos', 160.00, 5),
('Condicionador antipulgas para pets', 40.00, 32),
('Ração hipoalergênica para cães - 5kg', 170.00, 14),
('Ração para gatos obesos - 3kg', 95.00, 19),
('Brinquedo de borracha para cães', 35.00, 50),
('Arranhador com túnel para gatos', 90.00, 10),
('Coleira ajustável para cães', 22.00, 42),
('Areia sanitária com perfume floral', 31.00, 26),
('Petiscos para treinamento de cães', 20.00, 65),
('Capa de chuva refletiva para cachorro', 62.00, 9),
('Caminha portátil para gatos', 145.00, 7),
('Shampoo antiácaro para pets', 45.00, 30),
('Ração para cães ativos - 7kg', 140.00, 16),
('Ração para gatos com taurina - 4kg', 115.00, 18),
('Brinquedo eletrônico para cães', 60.00, 20),
('Arranhador multiandares para gatos', 95.00, 9),
('Coleira de couro para cães', 55.00, 15),
('Areia sanitária para gatos sensíveis', 34.00, 22),
('Petiscos orgânicos para cães', 28.00, 60),
('Moletom esportivo para cachorro', 80.00, 8),
('Cama ortopédica para gatos', 180.00, 6),
('Condicionador para pelos claros', 37.00, 35),
('Ração para cães com vitaminas - 5kg', 125.00, 20),
('Ração para gatos castrados - 3kg', 105.00, 21),
('Brinquedo de pelúcia para cães', 30.00, 40),
('Arranhador com brinquedos pendurados', 85.00, 11),
('Coleira com sininho para gatos', 25.00, 38),
('Areia sanitária com controle de odor forte', 36.00, 24),
('Petiscos sabor bacon para cães', 23.00, 55),
('Capa protetora para carro - cachorro', 90.00, 5),
('Caminha com proteção lateral para gatos', 155.00, 6);


create table itens_pedido (
  id serial primary key,
  pedido_id int not null,
  produto_id int not null,
  quantidade int not null check (quantidade > 0),
  preco_unitario numeric(10,2) not null check (preco_unitario >= 0),
  constraint fk_pedido foreign key (pedido_id) references pedidos(id),
  constraint fk_produto foreign key (produto_id) references produtos(id)
);



insert into pedidos (cliente_id) values (1), (2), (3);


select id, cliente_id, data_pedido from pedidos order by id limit 10;


insert into itens_pedido (pedido_id, produto_id, quantidade, preco_unitario) values
(1, 1, 2, 120.00),
(1, 10, 1, 40.00),
(2, 25, 2, 22.50),
(3, 7, 1, 35.00),
(3, 50, 2, 80.00),
(4, 4, 1, 70.00),
(4, 12, 2, 70.00),
(5, 15, 3, 250.00),
(5, 18, 1, 28.00),
(6, 20, 2, 28.00),
(6, 30, 1, 220.00);


  
  
select
 p.id as pedido_id,
 c.nome as cliente,
 pr.nome as produto,
 ip.quantidade,
 ip.preco_unitario,
 ip.quantidade * ip.preco_unitario as total_item,
 p.data_pedido
from pedidos p 
join clientes c on p.cliente_id = c.id
join itens_pedido ip on ip.pedido_id = p.id
join produtos pr on pr.id = ip.produto_id
order by p.id;



select
 p.id as pedido_id,
 c.nome as cliente,
 sum (ip.quantidade * ip.preco_unitario) as total_pedido,
 p.data_pedido
from pedidos p 
join clientes c on p.cliente_id = c.id
join itens_pedido ip on ip.pedido_id = p.id
group by p.id, c.nome, p.data_pedido
order by p.id; 


select 
 c.nome as cliente,
 sum (ip.quantidade * ip.preco_unitario) as total_gasto
from clientes c  
join pedidos p on p.cliente_id = c.id
join itens_pedido ip on ip.pedido_id = p.id
group by c.nome
order by total_gasto desc; 















 
















