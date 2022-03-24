<template>
    <div class="section-wrapper">
        <div class="container-small">
            <div class="footer-info">
                <div class="address">
                    <div class="title">Address</div>
                    <ul>
                        <FooterCol v-for="el in address" 
                            :key="el.id"
                            :text="el.text"/>
                    </ul>

                    <ul class="social">
                        <li><i class="fa-brands fa-facebook-square"></i></li>
                        <li><i class="fa-brands fa-twitter"></i></li>
                        <li><i class="fa-brands fa-instagram"></i></li>
                        <li><i class="fa-brands fa-linkedin"></i></li>
                    </ul>
                </div>

                <div class="info">
                    <div class="explore">
                        <div class="title">Explore</div>
                        <ul class="list-explore">
                            <FooterCol v-for="el in explore" 
                            :key="el.id"
                            :text="el.text"/>
                        </ul>
                    </div>
                    <div>
                        <div class="title">Information</div>
                        <ul>
                            <FooterCol v-for="el in information" 
                            :key="el.id"
                            :text="el.text"/>
                        </ul>
                    </div>
                </div>
            </div>

            <div class="rights">© 2020 Maxcoach. All Rights Reserved</div>
        </div>
    </div>
</template>

<script>
import FooterCol from './FooterCol.vue'

export default {
  name: 'FooterContent',
  components:{
    FooterCol
  },
  data () {
    return {
      explore:[
        {
          text: 'Start here',
          id: 0,
        },
        {
          text: 'Blog',
          id: 1,
        },
        {
          text: 'About us',
          id: 2,
        },
        {
          text: 'Success Story',
          id: 3,
        },
        {
          text: 'Courses',
          id: 4,
        },
        {
          text: 'Contact us',
          id: 5,
        },
      ],
      information: [
        {
          text: 'Membership',
          id: 0,
        },
        {
          text: 'Purchase guide',
          id: 1,
        },
        {
          text: 'Privacy policy',
          id: 2,
        },
        {
          text: 'Terms of service',
          id: 3,
        },
      ],
      address:[
        {
          text: '382 NE 191st St # 87394 Miami, FL 33179-3899',
          id: 0
        },
        {
          text: '+1 (305) 547-9909 (9am - 5pm EST, Monday - Friday)',
          id: 1
        },
        {
          text: 'support@maxcoach.com',
          id: 2
        },
      ]
    }
  }
}
</script>

<style scoped lang="scss">
    .section-wrapper{
        background-color: #171621;
        padding: 110px 0px;

        .container-small{
            display: flex;
            flex-direction: column;
            align-content: center;

            .rights{
                color: #fff;
                text-align: center;
                padding-top: 40px;
            }

            .footer-info{
                display: flex;

                .title{
                    font-size: 18px;
                    font-weight: 700;
                    color: #fff;
                    margin-bottom: 25px;
                }

                

                .address{
                    width: 50%;

                    .social{
                        display: flex;
                        gap: 30px;
                        margin-top: 40px;
                        color: #ababab;
                        
                        i{
                            font-size: 24px;  
                            cursor: pointer;
                        }

                        li:hover{
                            transition: 300ms;
                            color: #fff;
                        }
                    }
                }

                .info{
                    width: 50%;
                    display: flex;

                    .explore{
                        width: 55%;

                        .list-explore{
                           display: flex;
                           flex-direction: column;
                           flex-wrap: wrap;
                           
                           max-height: 150px;
                        }
                    }
                }
            }
        }
    }
</style>
