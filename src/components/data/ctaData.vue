<script>
    import image1 from '../../assets/trafalgar-illustration-1.png'
    import image2 from '../../assets/trafalgar-illustration-2.png'
    import icon_ from '../../assets/Vector.svg'

    export default {
        data() {
            return {
                cta1: {
                    link: image1,
                    title: 'Leading healthcare providers',
                    buttonTxt: 'Learn more',
                    text: 'Trafalgar provides progressive, and affordable healthcare, accessible onmobile and online for everyone. To us, it’s not just work. We take pridein the solutions we deliver',
                    none: 'hidden',
                },

                cta2: {
                    link: image2,
                    title: 'Download our mobile apps',
                    buttonTxt: 'Download',
                    text: 'Our dedicated patient engagement app and web portal allow you to access information instantaneously (no tedeous form, long calls, or administrative hassle) and securely',
                    reverse: 'flex-row-reverse',
                    icon: icon_,
                    
                }
            }
        }
    }
</script>

<style>
</style>