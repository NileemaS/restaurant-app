# restaurant-app

<h3>How to use the restaurant-app:</h3>

 - fork the app
 - cd
 - run: node index.js
 - app will run on localhost:5500/graphql
 
 
 <h3>Use these Quesries to test the app</h3>
 
 - mutation editrestaurants($idd: Int = 1, $name: String = "OLDO") {
  editrestaurant(id: $idd, name: $name) {
    id
    name
    description
  }
}

- mutation setrestaurants ($idd: Int = 7, $price: Int=11, $pprice: Int=15){
  setrestaurant(input: {
    id: $idd
    name: "Granite123",
    description: "American123",
    dishes: [{name: "Rice", price: $price} {name: "pasta", price: $pprice}]
  }) {
    id
    name
    description
    dishes {
      name
      price
    }
  }
}

- mutation deleterestaurants($iid: Int = 2) {
  deleterestaurant(id: $iid) {
    ok
  }
}

- query getrestaurants {
  restaurants {
    id
    name
    description
    dishes {
      name
      price
    }
  }
}

- query getrestaurant($iid: Int = 3) {
  restaurant(id: $iid) {
    id
    name
    description
    dishes {
      name
      price
    }
  }
}



<footer> License by MIT @2022 </footer>
