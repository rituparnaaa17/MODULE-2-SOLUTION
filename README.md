# MODULE-2-SOLUTION
mkdir module2-solution
cd module2-solution
mkdir css
touch index.html css/styles.css
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Responsive Layout</title>
  <link rel="stylesheet" href="css/styles.css">
</head>
<body>
  <h1>Delicious Foods</h1>
  <div class="container">
    <section class="section" id="chicken">
      <div class="title">Chicken</div>
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
    </section>
    <section class="section" id="beef">
      <div class="title">Beef</div>
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
    </section>
    <section class="section" id="sushi">
      <div class="title">Sushi</div>
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
    </section>
  </div>
</body>
</html>
* {
  box-sizing: border-box;
}

body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
}

h1 {
  text-align: center;
  margin: 20px 0;
}

.container {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  padding: 10px;
}

.section {
  position: relative;
  border: 1px solid black;
  padding: 20px;
  margin: 10px 0;
  background-color: #f0f0f0;
}

.title {
  position: absolute;
  top: 10px;
  right: 10px;
  background-color: #e0e0e0;
  padding: 5px 10px;
  border: 1px solid black;
  font-weight: bold;
}

#chicken {
  background-color: #ffcccc;
}

#chicken .title {
  background-color: #ff9999;
}

#beef {
  background-color: #ccffcc;
}

#beef .title {
  background-color: #99ff99;
}

#sushi {
  background-color: #ccccff;
}

#sushi .title {
  background-color: #9999ff;
}

@media (min-width: 992px) {
  .section {
    width: 32%;
  }
}

@media (min-width: 768px) and (max-width: 991px) {
  .section {
    width: 48%;
  }
  
  #sushi {
    width: 100%;
  }
}

@media (max-width: 767px) {
  .section {
    width: 100%;
  }
}
