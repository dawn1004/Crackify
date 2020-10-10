<template>
      <div 
      class="offer-container" v-for="(product, index) in state.products" 
      :key="index"
      data-aos="fade-up"
      data-aos-offset="300"
      data-aos-duration="1000"
      >
        <div class="title">
            <h1>{{product.title}}</h1>
        </div>
        <div class="right">
            
            <img :src="product.url" alt="">
            <div class="discription">
                <p>{{product.description}}</p>
                <p class="price">₱{{product.price}}  <h3>Original Price :</h3>  <span class="discount" v-if="product.discount">₱{{product.discount}}  </span> </p>
            </div>
        </div>

    </div>
</template>


<script>
//dito sa script tag yung products array edit mo yung price
import { reactive } from 'vue'
export default {
    name: "Offer",
    setup(){
        const state = reactive({
            counts: [1,2,3,4,5],
            products: [
                {
                    title:'Adobe Master Collection CC 2020',
                    description: 'Adobe Master Collection CC 2020 is a collection of applications from the Creative Cloud 2020 line and a number of junior version programs combined by a single installer with the ability to select the installation path and the language of the installed programs.In terms of functionality',
                    url: require("../assets/logos/adobe.jpg"),
                    price: '150',
                    discount: '400'
                },{
                    title:'Driver Easy Pro',
                    description: 'Driver Easy is a free driver update program. ... Buy a PRO subscription, install, activate, scan and update drivers in one click!',
                    url:  require('../assets/logos/de.jpg'),
                    price: '50',
                    discount: '200'
                },{
                    title:'Magix Vegas Pro 18 Video Editor for PC',
                    description: 'Magix VEGAS Pro 18 Edit is an excellent, streamlined solution for video and audio production. Benefit from lightning-fast operation, thanks to nestled timelines and a unified color grading layout.',
                    url:  require('../assets/logos/Magix.jpg'),
                    price: '100',
                    discount: '400'
                },{
                    title:'Avast Premium',
                    description: 'Avast Premium Security is an upgrade to your current Antivirus protection. It includes all the features included in Avast Internet Security, and additionally includes Webcam Shield, Data Shredder, and automatic updates in Software Updater.',
                    url:  require('../assets/logos/Avast.jpg'),
                    price: '80',
                    discount: '600'
                },{
                    title:'Canva Pro',
                    description: "What is Canva Pro? Canva Pro is the premium plan of Canva that comes with additional features including unlimited storage for photos and assets. You can upload your own images and access millions of photos. You'll also get exclusive access to 400,000 free photos, illustrations, and templates.",
                    url:  require('../assets/logos/Canva_Logo.jpg'),
                    price: '80',
                    discount: '500'
                },{
                    title:'CCleaner Professional',
                    description: "CCleaner Professional is the most powerful version of Piriform's celebrated PC cleaner. It makes it easy to speed up a slow computer and keep your activity private — automatically and in the background.",
                    url:  require('../assets/logos/cc.jpg'),
                    price: '150',
                    discount: '700'
                },{
                    title:'Adobe Acrobat Pro DC 2020',
                    description: ' Acrobat 2020 is the latest perpetual desktop version of Acrobat. It simplifies everyday PDF tasks and includes many productivity enhancements when working with PDFs from your desktop.',
                    url:  require('../assets/logos/adobe2.jpg'),
                    price: '80',
                    discount: '600'
                },{
                    title:'Adobe Photoshop CC 2020',
                    description: "the latest update to its flagship image-editing application. The new version brings some seriously useful new features, including new Warp capabilities, better automatic selection, and a range of minor interface changes that combine to make you more productive.",
                    url:  require('../assets/logos/adobe3.jpg'),
                    price: '100',
                    discount: '600'
                },{
                    title:'MS Office 2019',
                    description: 'Microsoft Office 2019 is the current version of Microsoft Office, a productivity suite, succeeding Office 2016. It was released to general availability for Windows 10 and for macOS on September 24, 2018.',
                    url:  require('../assets/logos/ms.jpg'),
                    price: '120',
                    discount: '900'
                },{
                    title:'Filmora 9',
                    description: 'Filmora9 is designed for all video content creators, whether a beginner, an amateur or a professional. It has a simple interface that lets you find the features and tools you need easily. ... It has plans for individuals, businesses, educators, and students, making it an attractive choice for video editing.',
                    url:  require('../assets/logos/filmora_9.jpg'),
                    price: '80',
                    discount: '500'
                },{
                    title:'WinZip Professional',
                    description: 'The new WinZip 25 product family provides individual, business, and enterprise customers powerful encryption, file management, and compression tools that make it easy to safely save and share files on email, the network, and the cloud.',
                    url:  require('../assets/logos/wr.png'),
                    price: '80',
                    discount: '500'
                },{
                    title:'Krisp Noise Cancelling App ',
                    description: "With a single button, Krisp removes all background noises for incoming and outgoing calls. Increase your productivity by having professional and noiseless ...",
                    url:  require('../assets/logos/Krisp.jpg'),
                    price: '80',
                    discount: '300'
                },{
                    title:'Adobe Illustrator',
                    description: 'Adobe Illustrator is a software application for creating drawings, illustrations, and artwork using a Windows or MacOS computer. Illustrator is widely used by graphic designers, web designers, visual artists, and professional illustrators throughout the world to create high quality artwork. Illustrator includes many sophisticated drawing tools that can reduce the time need to create illustrations.',
                    url:  require('../assets/logos/Adobe Illustrator.jpg'),
                    price: '80',
                    discount: '400'
                },{
                    title:'Premiere Pro',
                    description: 'Adobe Premiere Pro is a video editing program that is part of the Adobe Creative Cloud software collection, as well as Adobe CS6 – or Adobe Creative Suite. Premiere Pro is used to edit videos, including movies, and is quickly becoming the go-to program for filmmakers all over the world, both amateur and pro. ',
                    url:  require('../assets/logos/Premiere Pro.jpg'),
                    price: '100',
                    discount: '400'
                },{
                    title:'Adobe Indesign',
                    description: 'Adobe InDesign CC is part of the Creative Cloud, a collection of applications used for design, marketing, and communications in print, video, and online.',
                    url:  require('../assets/logos/Adobe Indesign.png'),
                    price: '150',
                    discount: '400'
                },{
                    title:'Adobe After Effects',
                    description: 'Adobe After Effects is a 2.5D animation software used for animation, visual effects, and motion picture compositing. After Effects is used in film, TV, and web video creation.',
                    url:  require('../assets/logos/Adobe After Effects.png'),
                    price: '80',
                    discount: '400'
                },{
                    title:'Sketch Up Pro',
                    description: 'Pro. SketchUp Pro includes the functionality of SketchUp Make plus importers and exporters to common 2D and 3D formats, access to LayOut (2D documentation software) and Style Builder (create custom edge styles for SketchUp models).',
                    url:  require('../assets/logos/Sketch.jpg'),
                    price: '100',
                    discount: '500'
                },{
                    title:'AutoCAD 2018 ',
                    description: 'AutoCAD 2018 continues to improve graphics and performance while ensuring the TrustedDWG technology you rely on. The DWG format has been updated to provide improvements in the efficiency of open and save operations, especially for drawings that contain many annotative objects and viewports',
                    url:  require('../assets/logos/autocad-2018.jpg'),
                    price: '100',
                    discount: '700'
                },
                {
                    title:'IBM SPSS Statistics 25',
                    description: "IBM SPSS Statistics is the world's leading statistical software used to solve business and research problems by means of ad-hoc analysis, hypothesis testing, and predictive analytics.",
                    url:  require('../assets/logos/IBM.jpg'),
                    price: '100',
                    discount: '900'
                }
            ]
        })

        return {state}
    }
}
</script>




<style>
.offer-container{
    margin: 100px;
    margin-top: 80px;
    margin-bottom: 0px;
}
.offer-container .title{
    color: #0A274A;
}
.offer-container .right{
    display: flex;
    align-items: center;
    margin-top: 20px;
}
.offer-container .right p{
    font-size: 26px;
    color: rgb(47, 47, 47);
    text-align: justify;
}
.offer-container .right .price{
    font-style: italic;
    color: rgb(47, 47, 47);
    margin-top: 10px;
}
.offer-container .right .price span{
    font-style: italic;
    color: rgb(88, 88, 88);
    font-size: 18px;
    text-decoration: line-through;
}
.offer-container .right img{
    max-width: 250px;
    min-width: 250px;
    margin-right: 20px;
}

@media only screen and (max-width: 500px) {
    .offer-container{
        margin: 40px;
        margin-top: 100px;
    }
    .offer-container .title{
        font-size: 14px;
    }
    .offer-container .right{
        flex-direction: column;
        align-items: flex-start;
    }
    .offer-container .right p{
        font-size: 18px;
        margin-top: 15px;
    }
    .offer-container .right img{
           max-width: 180px;
    min-width: 180px;
        margin-right: 0px;
    }
}
</style>



