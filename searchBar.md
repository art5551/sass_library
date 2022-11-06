 <!-- From youtube video https://www.youtube.com/watch?v=TlP5WIxVirU&t=662s -->

<body>
    <div class="search">
        <label for="search">Search for Artist</label>
        <input type="search" id="search" data-search><br><br>
    </div>

    <div class="user-cards"></div>

</body>


const userCardContainer = document.querySelector('.user-cards')
const searchInput = document.querySelector('[data-search]')

let users = []

searchInput.addEventListener("input", (e) => {
  const value = e.target.value.toLowerCase()
  users.forEach(user => {
    const isVisible = user.name.toLowerCase().includes(value) || user.email.toLowerCase().includes(value)
    user.element.classList.toggle("hide", !isVisible)
  })
  
})

fetch("https://jsonplaceholder.typicode.com/users")
  .then(res => res.json())
  .then(data => {
    users = data.map(user => {
      const card = document.createElement('div')
      card.className = 'card'
      userCardContainer.appendChild(card)
      const header = document.createElement('div')
      header.className = 'header'
      card.appendChild(header)
      const body = document.createElement('div')
      body.className = 'body'
      card.appendChild(body)
     
      header.innerHTML = user.name
      body.innerHTML = user.email 
      return {name: user.name, email: user.email, element: card}
    })

  })


body {
  display: block;
  background: black;
  color: white;
  height: 100vh;
  width: 80vw;
  margin: auto;
}


.search {
  display: flex;
  flex-direction: column;
  width: 300px;
}

.user-cards {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(190px, 1fr));
  gap: .25rem;
  margin-top: 1rem;
}

.card {
  border: 1px solid white;
  background-color: black;
  color: white;
  padding: .5rem;
}

.hide {
  display: none;
}
