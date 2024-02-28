<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ArcherySouth</title>

    <link rel="stylesheet" href="index.css">
    <script src="https://code.jquery.com/jquery-3.6.0.js" integrity="sha256-H+K7U5CnXl1h5ywQfKtSj8PCmoN9aaq30gDh27Xc0jk=" crossorigin="anonymous"></script>
    <script src="index.js"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css" integrity="sha512-DTOQO9RWCH3ppGqcWaEA1BIZOC6xxalwEsw9c2QQeAIftl+Vegovlnee1c9QX4TctnWMn13TZye+giMm8e2LwA==" crossorigin="anonymous" referrerpolicy="no-referrer" />
    <script src="//cdn.jsdelivr.net/npm/sweetalert2@11"></script>
</head>
<body>
    <nav>
        <div class="nav-container">
                <img src="LOGO.png" class="logonav">
            <div class="nav-profile">
                <input onkeyup="searchsomething(this)" id="txt_search" class="sidebar-search" placeholder="Search something...">
                <p class="nav-profile-name">Cart</p>
        <div onclick="openCart()" style="cursor: pointer;" class="nav-profile-cart">
          <i class="fas fa-cart-shopping"></i>
          <div id="cartcount" class="cartcount" style="display: none;">
            0
          </div>
        </div>
            </div>
        </div>
    </nav>
    <div class="contianer">
        <div class="sidebar">
            <a onclick="searchproduct('all')" class="sidebar-items">
                All product
              </a>
              <a onclick="searchproduct('Compound')" class="sidebar-items">
                Compound
              </a>
              <a onclick="searchproduct('Recurve')" class="sidebar-items">
                Recurve
              </a>
              <a onclick="searchproduct('Accessories')" class="sidebar-items">
                Bow Accessories
              </a>
        </div>
        <div id="productlist" class="product">
            
        </div>
    </div>
    <div id="modalDesc" class="modal" style="display: none;">
        <div onclick="closeModal()" class="modal-bg"></div>
        <div class="modal-page">
          <h2>Detail</h2>
          <br>
          <div class="modaldesc-content">
            <img id="mdd-img" class="modaldesc-img" src="https://images.unsplash.com/photo-1542291026-7eec264c27ff?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1740&q=80" alt="">
            <div class="modaldesc-detail">
              <p id="mdd-name" style="font-size: 1.5vw;">Product name</p>
              <p id="mdd-price" style="font-size: 1.2vw;">500 THB</p>
              <br>
              <p id="mdd-desc" style="color: #adadad;">Lorem iaudantium harum doloremque alias. Quae, vel ipsum quasi, voluptas, sit optio nemo magni numquam non dicta voluptates porro! Vero eveniet numquam sit aut vel eligendi officiis iste tenetur expedita. Delectus vero quibusdam adipisci in. Esse.</p>
              <br>
              <div class="btn-control">
                <button onclick="closeModal()" class="btn">
                  Close
                </button>
                <button onclick="addtocart()" class="btn btn-buy">
                  Add to cart
                </button>
              </div>
            </div>
          </div>
        </div>
      </div>
    
      <div id="modalCart" class="modal" style="display: none;">
        <div onclick="closeModal()" class="modal-bg"></div>
        <div class="modal-page">
          <h2>My cart</h2>
          <br>
          <div id="mycart" class="cartlist">
    
          </div>
          <div class="btn-control">
            <button onclick="closeModal()" class="btn">
              Cancel
            </button>
            <button class="btn btn-buy">
              Buy
            </button>
          </div>
        </div>
      </div>    
</body>
</html>
