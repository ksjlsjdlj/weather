# weather
<!DOCTYPE html>
<html lang="pl">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
<div class="container"></div>
<script>
const container = document.querySelector('.container');

fetch('https://picsum.photos/v2/list?page=2&limit=10')
.then((response)=>response.json())
.then((data) =>{
console.log(data);
data.forEach((elem) => {
    const imagSrc = elem.download_url; 
    const author = elem.author;
    const content = `<figure><img src="${imagSrc}" alt="some foto"/><figcapion> Autor: ${author} </figcaption></figure>`;
    container.innerHTML += content;
});
console.log(data);
})
.catch((err)=>)




</script>

    
</body>
</html>