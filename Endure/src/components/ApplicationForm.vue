<template>
  <div class="application-form">
    <h3 class="application-form__title">Apply for the position of purchasing assistant</h3>
    <form class="application-form__envelope">
      <div class="application-form__personal-details">
        <p>Personal Details</p>
      </div>
      <div class="application-form__details-row">
        <div class="application-form__details-col --right form-group">
          <div class="--cell">
            <input
              v-model="contact.name"
              type="text"
              name="name"
              class="form-control application-form__field"
              required>
            <span
              v-if="errors.name"
              class="text-danger">
              {{ errors.name }}
            </span>
          </div>
          <div class="--cell">
            <input
              v-model="contact.place"
              type="text"
              name="place"
              class="form-control application-form__field"
              required>
            <span
              v-if="errors.place"
              class="text-danger">
              {{ errors.place }}
            </span>
          </div>
          <div class="--cell">
            <input
              v-model="contact.email"
              type="email"
              name="email"
              class="form-control application-form__field"
              required>
            <span
              v-if="errors.email"
              class="text-danger">
              {{ errors.email }}
            </span>
          </div>
        </div>
        <div class="application-form__details-col --left form-group">
          <div class="--cell">
            <input
              v-model="contact.surname"
              type="text"
              name="surname"
              class="form-control application-form__field"
              required>
            <span
              v-if="errors.surname"
              class="text-danger">
              {{ errors.surname }}
            </span>
          </div>
          <div class="--cell">
            <input
              v-model="contact.country"
              type="text"
              name="country"
              class="form-control application-form__field"
              required>
            <span
              v-if="errors.country"
              class="text-danger">
              {{ errors.country }}
            </span>
          </div>
          <div class="--cell">
            <input
              v-model="contact.telephone"
              type="text"
              name="telephone"
              class="form-control application-form__field"
              required>
            <span
              v-if="errors.telephone"
              class="text-danger">
              {{ errors.telephone }}
            </span>
          </div>
        </div>
      </div>
      <div class="application-form__details-row">
        <div class="application-form__details-col --right form-group">
          <p class="--section-title">Your motivation</p>
          <textarea class="application-form__motivation" type="free-text" />
        </div>
        <div class="application-form__details-col --left form-group">
          <p class="--section-title">Attach your documents (pdf, doc(x), jpg max. 4Mb)</p>
          <div>
            <div class="application-form__documents-row">
              <div class="--title">
                <span>Resume</span>
              </div>
              <button class="application-form-btn mr">
                <em class="fas fa-desktop" />
                <span>Upload</span>
              </button>
              <button class="application-form-btn">
                <em class="fab fa-dropbox" />
                <span>DropBox</span>
              </button>
            </div>
            <div class="application-form__documents-row">
              <div class="--title">
                <span>Portfolio</span>
              </div>
              <button class="application-form-btn mr">
                <em class="fas fa-desktop" />
                <span>Upload</span>
              </button>
              <button class="application-form-btn">
                <em class="fab fa-dropbox" />
                <span>DropBox</span>
              </button>
            </div>
            <div class="application-form__documents-row">
              <div class="--title">
                <span>Photo</span>
              </div>
              <button class="application-form-btn mr">
                <em class="fas fa-desktop" />
                <span>Upload</span>
              </button>
              <button class="application-form-btn">
                <em class="fab fa-dropbox" />
                <span>DropBox</span>
              </button>
            </div>
          </div>
        </div>
      </div>
      <div class="application-form__details-row --last-section">
        <div class="application-form__details-col --title"><span> &lt; Back to job description</span></div>
        <div class="application-form__details-col">
          <div class="--auto">
            <div class="--checkbox">
              <input type="checkbox" name="copy" />
              <label for="copy" class="application-form__send-copy">Send me a copy</label>
            </div>

              <button class="application-form-btn --apply">
                <span>Apply for this job</span>
              </button>

          </div>
        </div>
      </div>
    </form>
  </div>
</template>

<script>
export default {
  name: 'ApplicationForm',
  data () {
    return {
      contact: {},
      errors: {}
    }
  },
  mounted () {
    this.contact = {
      name: 'Sybren',
      surname: 'van Putten',
      place: 'Amsterdam',
      email: 'sybren@netwerven.nl',
      country: '',
      telephone: '20240024'
    }
  }
}
</script>

<style lang="scss" scoped>
.application-form{
  display: flex;
  flex-direction: column;
  padding: 10px;
  @media screen and (min-width: 760px) {
    width: 700px;
    margin: auto;
  }
}
.application-form__personal-details{
  display: flex;
}
.application-form__title{
  text-transform: uppercase;
  font-size: 25px;
  text-align: left;
}
.application-form__envelope{
  @media screen and (min-width: 760px){
    flex-direction: row;
  }
}
.application-form__details-col{
  flex-direction: column;
  &.--right{
    margin-right: 2%;
  }
  &.--left{
    margin-left: 2%;
  }
  .--section-title{
    font-size: 14px;
    font-weight: 600;
  }
  .--cell{
    display: flex;
  }
  .--auto{
    display: flex;
  }
  .--checkbox{
    display: flex;
    margin-right: auto;
    margin-top: auto;
    margin-bottom: auto;
  }
  @media screen and (min-width: 760px){
    display: inline-flex;
    width: 48%;
  }
}
.application-form__field{
  width: 100%;
  padding: 13px;
  border: none;
  margin-bottom: 15px;
  font-weight: bold;
}
.application-form__motivation{
  height: 100%;
  width: 100%;
  min-height: 100px;
}
.application-form-btn{
  min-width: 100px;
  color: white;
  background-color: #1c448d;
  width: 50%;
  text-transform: uppercase;
  font-weight: 600;
  &.mr{
    margin-right: 10px;
  }
  em{
    margin-right: 5px;
  }
  &.--apply{
    min-height: 40px;
  }
}
.application-form__documents-row{
  display: flex;
  flex-direction: row;
  min-height: 40px;
  padding: 5px;
  &:last-child{
    padding-bottom: 0px;
  }
  .--title{
    justify-content: flex-start;
    font-size: 12px;
    margin-right: 5px;
    min-width: 20%;
    margin-top: auto;
    margin-bottom: auto;
  }
}
.application-form__details-row{
  margin-top: 50px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  text-align: left;
  @media screen and (min-width: 760px){
    flex-direction: row;
  }
  .--title{
    justify-content: flex-start;
    font-size: 12px;
    margin-top: 20px;
    @media screen and (min-width: 760px){
      margin-top: auto;
      margin-bottom: auto;
    }
  }
  &.--auto{
    margin: auto;
    display: flex;
  }
  &.--last-section{
    flex-direction: column-reverse;
    @media screen and (min-width: 760px){
      flex-direction: row;
    }
  }
}
.application-form__send-copy{
  font-size: 12px;
}
</style>
