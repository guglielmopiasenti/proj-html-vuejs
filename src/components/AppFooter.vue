<template>
    <footer class="footer">
        <div class="top-container">
            <img class="logo" src="../assets/img/logotype-2-139x23.png" alt="Company Logo" />
            <ul class="nav-links">
                <li><a href="#">HOME</a></li>
                <li><a href="#">ABOUT</a></li>
                <li><a href="#">PROJECTS</a></li>
                <li><a href="#">SERVICES</a></li>
                <li><a href="#">BLOG</a></li>
                <li><a href="#">CONTACT</a></li>
            </ul>
            <div class="social-icons">
                <i class="fab fa-instagram"></i>
                <i class="fab fa-linkedin-in"></i>
                <i class="fab fa-facebook-f"></i>
                <i class="fab fa-twitter"></i>
            </div>
        </div>
        <div class="divider"></div>
        <div class="bottom-container">
            <div class="policy-links">
                <p><a href="#">Terms of use</a></p>
                <p><a href="#">Privacy Environmental Policy</a></p>
            </div>
            <div class="copyright">
                <p>Copyright © 2023 Phlox Consulting. All Rights Reserved.</p>
            </div>
        </div>
    </footer>
</template>

<style scoped lang="scss">
@use '../assets/scss/var' as *;
@use '../assets/scss/mixins' as *;

.footer {
    @include container-lg;
    padding: 50px 20px;
    color: grey;

    .top-container,
    .bottom-container {
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding-top: 30px;
    }

    a {
        color: grey;
    }

    .nav-links {
        display: flex;
        justify-content: space-between;
        list-style: none;

        li {
            margin: 0 10px;

            a {

                &:hover {
                    color: $c-r;
                }
            }

        }

    }

    .divider {
        border-bottom: 1px solid grey;
        margin: 20px auto;
        padding: 30px 0;
    }

    .social-icons {
        i {
            margin: 0 10px;
            color: white;
        }
    }

    .policy-links {
        p {
            margin: 0;
        }
    }
}
</style>
