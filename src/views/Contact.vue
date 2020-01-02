<template>
  <div id='contact'>
    <div id='form' class="flex-itemC">
      <v-row align="center">
      <v-form
        ref="form"
        v-model="valid"
      >
        <v-text-field
          :rules="emailRules"
          label="E-mail"
          value='ani789yagnik@gmail.com'
          :disabled="true"
          required
        ></v-text-field>
        <v-text-field
          v-model="email"
          :rules="emailRules"
          label=" Your E-mail"
          required
        ></v-text-field>
        <v-text-field
          v-model="subject"
          :counter="10"
          :rules="subjectRules"
          label="Subject"
          required
        ></v-text-field>
        <v-textarea
            subject="input-7-1"
            label="message"
            value=""
            hint="body"
          ></v-textarea>
        <v-btn
          color="success"
          class="mr-4"
          @click="validate"
        >
          send
        </v-btn>
        <v-btn
          color="error"
          class="mr-4"
          @click="reset"
        >
          Reset Form
        </v-btn>
      </v-form>
    </v-row>
    </div>
    <div class='flex-itemC white--text' style='background-color:crimson'>
      <p style='font-size:1.5em' class=' text-center font-weight-bold text-capitalize' id='head'>contacts</p>
      <p style='font-size:0.85em' >
        <v-icon dark left >mdi-cellphone</v-icon>
        <a style='text-decoration:none;color:white' href="tel:+9898778871">91+9898778871</a>
      </p>
      <p style='font-size:0.85em' >
        <v-icon dark left >mdi-home</v-icon>
        <a style='text-decoration:none;color:white'
        href="https://maps.google.com/maps?f=q&source=embed&hl=en&geocode=&q=Janakpuri,+New+Delhi,+Delhi,+India&aq=0&oq=janapuri+new+delhi&sll=37.0625,-95.677068&sspn=42.987658,86.572266&ie=UTF8&hq=&hnear=Janakpuri,+New+Delhi,+West+Delhi,+Delhi,+India&ll=28.620123,77.093858&spn=0.186865,0.338173&t=m&z=12"
        >
          A block,red spot,southern jupiter (40 km from epicenter)
          </a>
      </p>
      <p style='font-size:0.85em' >
        <v-icon dark left >mdi-domain</v-icon>
        <a style='text-decoration:none;color:white'
        href="https://maps.google.com/maps?f=q&source=embed&hl=en&geocode=&q=Janakpuri,+New+Delhi,+Delhi,+India&aq=0&oq=janapuri+new+delhi&sll=37.0625,-95.677068&sspn=42.987658,86.572266&ie=UTF8&hq=&hnear=Janakpuri,+New+Delhi,+West+Delhi,+Delhi,+India&ll=28.620123,77.093858&spn=0.186865,0.338173&t=m&z=12"
        >
        C-4, Janakpuri, Delhi, India
        </a>
      </p>
      <p style='font-size:0.85em' >
        <v-icon dark left >mdi-contact-mail</v-icon>
        <a style='text-decoration:none;color:white'
        href="mailto:ani789yagnik@gmail.com"
        >
        ani789yagnik@gmail.com
        </a>
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'contact',
  data: () => ({
    valid: false,
    subject: '',
    subjectRules: [
      v => !!v || 'Subject is required'
    ],
    email: '',
    emailRules: [
      v => !!v || 'E-mail is required',
      v => /.+@.+\..+/.test(v) || 'E-mail must be valid'
    ]
  }),

  methods: {
    validate () {
      if (this.$refs.form.validate()) {
        this.snackbar = true
      } else {
        alert('sfd')
      }
    },
    reset () {
      this.$refs.form.reset()
    }
  }
}
</script>
<style lang="scss">
#contact{
  background-image: url('../assets/28171.jpg');
  background-attachment: fixed;
  background-position: center;
  background-repeat: no-repeat;
  display: flex;
  justify-content: space-evenly;
  align-items: center;
  flex-wrap: wrap;
  height: 92.5vh;
  .flex-itemC{
    border:1px solid rgb(220, 255, 25);
    margin: 1vw;
    margin-top: 4vw;
    margin-bottom: 4vw;
  }
  #head{
    padding: 5px 8px;
    font-weight: 600;
    background: url('../assets/bg.jpg') repeat #696666;
    box-shadow: 0px 6px 10px black;
    border: 1px solid chartreuse;
  }
}
#form{
  padding:7vw;
  padding-top: 3vw;
  padding-bottom: 3vw;
  background-image: linear-gradient(to right top, #c5e5ad, #b4ebcb, #b2ede4, #c0edf4, #d5ecf8, #cfdfe9, #c9d3da, #c2c7cb, #a4abaf, #879092, #6b7577, #515c5c);
}
</style>
