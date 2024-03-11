<script>


export default {

    name: 'AppTopBar',



}

</script>

<template>

    <div id="top-bar">
        <div class="container">
            <div id="contacts" class="d-flex justify-content-between align-items-center">
                <div id="address" class="d-flex">
                    <div id="place" class="d-flex align-items-center">
                        <i class="fa-solid fa-location-dot"></i>
                        <span>7087 Richmond hwy, Alexandria, VA</span>
                    </div>
                    <div id="number" class="d-flex align-items-center">
                        <i class="fa-solid fa-phone"></i>
                        <span>800-2345-6789</span>
                    </div>
                </div>

                <div id="socials" class="d-flex">
                    <div id="social-container" class="d-flex align-items-center justify-content-center">
                        <i class="fa-brands fa-facebook-f">
                            <a href="#"></a>
                        </i>
                    </div>

                    <div id="social-container" class="d-flex align-items-center justify-content-center">
                        <i class="fa-brands fa-twitter">
                            <a href="#"></a>
                        </i>
                    </div>

                    <div id="social-container" class="d-flex align-items-center justify-content-center">
                        <i class="fa-brands fa-instagram">
                            <a href="#"></a>
                        </i>
                    </div>


                </div>
            </div>

        </div>
    </div>

</template>

<style lang="scss">
@use '../styles/mixins' as *;
@use '../styles/variables' as *;

#top-bar {
    padding: 10px 0;
}

.container {
    @include styleContainer;

    #contacts {

        #address {
            color: #6a6c71;
            gap: 60px;

            #place {

                gap: 15px;

            }

            i {
                color: $PrimaryColor;
            }

            #number {
                gap: 15px;
            }

        }

        #socials {

            gap: 20px;
            color: white;

            #social-container{
                width: 20px;
                height: 20px;
                border-radius: 50%;
                background-color: #6a6c71;

                i{
                    font-size: 12px;
                }
            }


        }

    }

}
</style>