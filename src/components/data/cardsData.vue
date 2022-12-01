<script>
    import article1 from "../../assets/article1.png";
    import article2 from "../../assets/article2.png";
    import article3 from "../../assets/article3.png";
    
    export default {
        data() {
            return {
                cardsContent: {
                    card1: {
                        image: article1 ,
                        title: 'Disease detection, check up in the laboratory',
                        text: 'In this case, the role of the health laboratory is very important to do a disease detection...',
                    },
                    card2: {
                        image: article2,
                        title: 'Herbal medicines that are safe for consumption',
                        text: 'Herbal medicine is very widely used at this time because of its very good for your health...',
                    },
                    card3: {
                        image: article3,
                        title: 'Natural care for healthy facial skin',
                        text: 'A healthy lifestyle should start from now and also for your skin health. There are some...',
                    }
                }
            }
        },  
    }
</script>