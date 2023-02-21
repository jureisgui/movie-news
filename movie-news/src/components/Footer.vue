<template>

    <footer>
        <div class="footer-links">
            <h3><a>Contact Us</a></h3>
            <div class="social-media">
                <a><img class="social" src="../assets/images/facebook.png" alt=""></a>
                <a><img class="social" src="../assets/images/instagram.png" alt=""></a>
                <a><img class="social" src="../assets/images/twitter.png" alt=""></a>
            </div>
            <h3>&copy; Movie News, 2023</h3>
        </div>
        <img class="megaphone" src="../assets/images/megaphone.png" alt="">
    </footer>
    
</template>

<style scoped>
    footer{
        background-color: #8C0343;
        display: flex;
        padding: 0.8em 1.5em;
    }

    .social-media{
        display: flex;
        max-width: 20px;
    }

    .social{
        max-width: 30px;
    }

    .footer-links{
        flex: 1;
    }

    .megaphone{
        max-width: 120px;
        flex: 1;
    }
    
</style>

