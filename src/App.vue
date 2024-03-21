<template>
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Josefin+Sans:ital,wght@0,100..700;1,100..700&display=swap" rel="stylesheet"> 
  <div>
    <div class="hero">
      <nav>
        <h2 class="logo">Daffa Finanda</h2>
        <ul>
          <li><router-link to="/home">Home</router-link></li>
          <li><router-link to="/biodata">Biodata</router-link></li>
          <li><router-link to="/prestasi">Prestasi</router-link></li>
          <li><router-link to="/galeri">Galeri</router-link></li>
          <li><router-link to="/portofolio">Portofolio</router-link></li>
        </ul>
      </nav>
      <div class="content">
        <h4>Hai, nama saya</h4>
        <h1>Daffa Finanda</h1>
        <h3>Selamat datang di Web saya</h3>
      </div>
    </div>

      <div class="bio">
        
        <div class="img">
            <img src="./assets/daffa.jpg" alt="daffa">
        </div>
        <div class="biodata">
          <h1>Biodata</h1>
            <p>Nama : Daffa Finanda</p>
            <p>Tanggal Lahir: 14 Februari 2004</p>
            <p>Pendidikan: S1 Tekhnik Informartika</p>
            <p>Pekerjaan: Mahasiswa</p>
            <p>Email: daffafinanda15@gmail.com</p>
            <p>Telepon: 0895634907444</p>
        </div>
      </div>

    <div class="contact-form">
      <div class="contact-info">
        <h2>Informasi Kontak</h2>
        <p>Email: {{ email }}</p>
        <p>Telepon: {{ phone }}</p>
        <p>Alamat: {{ address }}</p>
      </div>
      <div class="message-form">
        <h2>Kirim Pesan</h2>
        <form @submit.prevent="sendMessage">
          <label for="name"></label>
          <input type="text" id="name" name="name" placeholder="Nama" required>

          <label for="email"></label>
          <input type="email" id="email" name="email" placeholder="Email" required>

          <label for="message"></label>
          <textarea id="message" name="message" rows="4" placeholder="Pesan"></textarea>

          <button type="submit">Kirim</button>
        </form>
      </div>     
    </div>
  </div>  

    <footer>
      <div>
        <p>&copy; {{ author }} | {{ studentId }}</p>
      </div>
    </footer>
</template>

<script>
export default {
  data() {
    return {
      name: 'Daffa Finanda',
      email: 'daffafinanda15@gmail.com',
      phone: '+62 896-6349-07444',
      address: 'Pekanbaru, Riau',
      message: '',
      author: 'Daffa Finanda',
      studentId: '12250111603'
    };
  },
  methods: {
    sendMessage() {
    
      console.log('Message sent:', this.message);
    
    }
  }
};
</script>

<style scoped>
div{
  font-family: 'Josefin Sans';
  color: white;
}
/*Bar Navigasi */
.hero{
  height: 100vh;
  width: 100%;
  background-color: black;
  background-size: cover;
  background-position: center;
}

nav{
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding-top: 3vh;
  padding-left: 8%;
  padding-right: 8%;
}

.logo {
  color: white;
  font-size: 20px;
  letter-spacing: 1px;
  cursor: pointer;
}

nav ul li{
  list-style-type: none;
  display: inline-block;
  padding: 10px 25px;
}

nav ul li router-link{
  text-decoration: none;
  font-weight: bold;
  text-transform: capitalize;
}

nav ul li router-link:hover{
  color: rgb(24, 24, 24);
  transition: .4s;
}
/* Akhir Bar Navigasi */

.content {
  padding-top:25vh;
  align-items: center;
  text-align: center;
  color: white;
  justify-content: center;
}

/* Bio */
.bio {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh; 
    background-color: #131313; 
}

.img {
    margin-right: 20px; 
}

.img img {
    width: 150px; 
    height: 150px;
    border-radius: 50%; 
}

.biodata {
    color: #fff; 
}

.biodata p {
    margin: 5px 0; 
}

.contact-form {
    justify-content: space-around;
    align-items: flex-start;
    margin-top: 20px;
}


.contact-info {
    background-color: #f4f4f4;
    padding: 20px;
    color: black
}
.contact-info  p {
    text-align: left;
}

.message-form {
    background-color: #f9f9f9;
    padding: 20px;
    color: black;
}

.message-form form {
    display: flex;
    flex-direction: column;
}

.message-form label {
    margin-bottom: 10px;
}

.message-form input[type="text"],
.message-form input[type="email"],
.message-form textarea {
    width: 95%;
    padding: 10px;
    margin-bottom: 15px;
    border: 1px solid #ccc;
    border-radius: 3px;
}

.message-form button[type="submit"] {
    padding: 10px 20px;
    background-color: #007bff;
    color: white;
    border: none;
    border-radius: 3px;
    cursor: pointer;
}

.message-form button[type="submit"]:hover {
    background-color: #0056b3;
}
/* Akhir HOME */

footer {
    background-color: black; 
    padding: 5px;
    text-align: center;
    color: #f0f0f0;
}

</style>
