<img alt="GoStack" src="https://storage.googleapis.com/golden-wind/bootcamp-gostack/header-desafios.png" />

<h3 align="center">
  Challenge 09: Database relationships in Node.js
</h3>

<p align="center">
  <a href="#rocket-about-the-challenge">About the Challenge</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#technologies">Technologies</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#routes">Routes</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#installation">Installation</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#memo-license">License</a>
</p>

## :rocket: About the Challenge

Application that allows the creation of customers, products and orders, where the customer can generate new purchase orders for certain products, such as a small e-commerce.

## Technologies

- [Node.js](https://nodejs.org/en/)
- [Express](https://expressjs.com/)
- [Typescript](https://www.typescriptlang.org/)
- [TypeORM](https://typeorm.io/#/)

## Routes

- **`POST /customers`**

```json
{
	"name": "Customer name",
	"email": "email@example.com"
}
```
- **`POST /products`**

```json
{
	"name": "Product name",
	"price": 1500,
	"quantity": 5
}
```

- **`POST /orders`**

```json
{
  "customer_id": "836d6d54-e8c3-4b07-ab2b-4e21360aac58",
  "products": [
		{
      "id": "dcd0915f-4495-48a5-adfc-57ac51cee17d",
      "quantity": 5
    },
    {
      "id": "55fe82fe-3420-4df5-9965-da49a5d9bb15",
      "quantity": 2
    }
  ]
}
```

- **`GET /orders/:id`**


## Installation

### Database

1. Install Docker https://www.docker.com/get-started and check if was installed with the command: `docker version`
2. Run the command `docker run --name gostack_postgres -e POSTGRES_PASSWORD=docker -p 5432:5432 -d postgres`
3. Verify if container was created `docker ps -a`
4. Create a database with name `gostack_challenge09`

### Run Server

1. Clone the repository: `git@github.com:matheus-neves/challenge-typeorm-relations.git`
2. Access the directory: `cd challenge-typeorm-relations`
3. Install the dependencies: `yarn`
4. Run migrations: `yarn typeorm migration:run`
5. Run the server: `yarn dev:server`
6. Server running in `http://localhost:3333/`




## :memo: License

This challenge is under license from MIT. See the archive [LICENSE](https://github.com/Rocketseat/bootcamp-gostack-desafios/blob/master/LICENSE) for more details.

---
Challenge completed ✔️by Matheus Neves and created with 💜by Rocketseat 👋 [Join the community!](https://discordapp.com/invite/gCRAFhc)
