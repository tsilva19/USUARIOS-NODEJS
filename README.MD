## COMEÇO provisiona api e o postgres

- docker-compose up

## SE PRECISAR RESTART O CONTAINERda api se por ventura alterações de codigo

- docker  restart apiContainer

## COMANDO TYPEORM para criar as migrations

- yarn typeorm migration:create -n CreateCategories

- yarn typeorm migration:create -n CreateSpecifications


## comando para criar entity no postgres

- yarn typeorm migration:run

## comando para deletar entity

- yarn typeorm migration:revert

## USANDO a api por contrato SWEGGER OPEN API

- Acesse http://localhost:3333/api-docs

## USANDO no postman

- Acesse GET E POST http://localhost:3333/categories

- Acesse GET E POST http://localhost:3333/specifications


## Exemplo de requisição

`
curl -X 'POST' \
  'http://localhost:3333/categories' \
  -H 'accept: */*' \
  -H 'Content-Type: application/json' \
  -d '{
  "name": "SVU 2",
  "description": "SVU EXEMPLO 2"
}'
`