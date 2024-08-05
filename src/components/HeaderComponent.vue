<template>
   <v-app-bar app dark>
        <v-container>
            <v-row>
               <div v-if="userRole === 'ADMIN'">
                  <v-col class="d-flex justify-start">
                     <v-btn :to="{path:'/member/list'}">회원관리</v-btn>
                     <v-btn :to="{path:'/product/manage'}">상품관리</v-btn>
                     <v-btn :to="{path:'/order/list'}">실시간주문</v-btn>
                  </v-col>
               </div>
               <v-col class="text-center">
                  <v-btn :to="{path:'/'}">java shop</v-btn>
               </v-col>
               <v-col class="d-flex justify-end">
                  <v-btn :to="{path:'/product/list'}">상품목록</v-btn>
                  <v-btn :to="{path:'/mypage'}">MyPage</v-btn>
                  <v-btn :to="{path:'/member/create'}">회원가입</v-btn>
                  <v-btn :to="{path:'/login'}">로그인</v-btn>
                  
               </v-col>

            </v-row>
        </v-container>



   </v-app-bar>
</template>

<script>
export default{};
</script>