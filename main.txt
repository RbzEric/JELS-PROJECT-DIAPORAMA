const images = [
    {src :'image1.jpg', title :'Image 1'},
    {src :'image2.jpg' , title :'Image 2'},
    {src :'image3.jpg' , title :'Image 3'},
    {src :'image4.jpg' , title : 'Image 4'},
    {src :'image5.jpg' , title : 'Image 5'},
    {src :'image6.jpg', title : 'Image 6' }
];


let currentIndex = 0;
let button = document.querySelector('#suivant');
let nextImage = document.querySelector('#image');
let title = document.querySelector('figcaption');


button.addEventListener('click',() =>{
    button.textContent = 'Image suivante';
    let image = images[currentIndex];
    currentIndex = (currentIndex + 1) % images.length;
    nextImage.src = image.src;
    title.textContent = image.title;
});