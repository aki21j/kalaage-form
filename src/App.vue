<template>
  <div id="app">
    <nav class="navbar navbar-expand-lg navbar-light bg-white">
      <div class="row nav-row">
        <div class="col-6 text-center">
          <a class="navbar-brand text-danger font-weight-normal" href="#">Kalaage</a>
        </div>  
        <div class="col-6 text-center">
          <button class="btn btn-outline-danger  my-2 my-sm-0 btn-sm" type="button">How it works</button>          
        </div>  
      </div>
    </nav>
    <div class="container py-5">
      <div class="row">
      <div class="col-md-11 col-sm-12 form-div"> 
      <div class="row justify-content-md-center px-3">
        <h2>Just a few questions and you'll be Golden</h2>
        <div class="col-md-6 col-sm-9 col-xs-9">
          <form action="" class="bg-white p-4 my-4">
            
            <div class="form-group">
              <label for="" class="label-text my-3">Why do you want to start your own publication?</label>
              <textarea type="text" placeholder="Type your mind" class="form-control">
              </textarea>
            </div>

            <div class="form-group">
              <label for="" class="label-text my-3">What kind of publication do you want?</label>
              <div class="row">
                <div class="col-lg-4 col-md-6 col-sm-6 col-xs-6 py-1" v-for="(value,index) in publications" :key="index">
                
                  <div class="custom-control custom-checkbox" >
                    <input type="checkbox" class="custom-control-input" :id="'customCheck' + index">
                    <label class="custom-control-label" :for="'customCheck' + index">{{value}}</label>
                  </div>
                </div>

              </div>

            </div>

            <div class="row">
              <div class="col-12 text-right">
                <button type="button" class="btn btn-outline-danger px-5">Next</button>
              </div>
            </div>

          </form>
        </div>
      </div>
      </div>
      <div class="col-md-1 col-sm-12 py-3 check-div text-center">
        <button type="button" class="btn check-circle text-center pt-0 px-1 my-4 mx-2 ">
          <i class="fas fa-check text-success check-circle-text"></i>
        </button>
        <button type="button" class="btn check-circle text-center pt-0 px-1 my-4 mx-2 ">
          <span class="check-circle-text text-danger font-weight-bold">2</span>
        </button>
        <button type="button" class="btn check-circle text-center pt-0 px-1 my-4 mx-2 ">
          <span class="check-circle-text text-danger font-weight-bold">3</span>
        </button>
        <button type="button" class="btn check-circle text-center pt-0 px-1 my-4 mx-2 ">
          <span class="check-circle-text text-danger font-weight-bold">4</span>
        </button>
        <button type="button" class="btn check-circle text-center pt-0 px-1 my-4 mx-2 ">
          <span class="check-circle-text text-danger font-weight-bold">5</span>
        </button>

      </div>
      </div>
    </div>

  </div>
</template>

<script>
export default {
  name: 'app',
  data:() =>({
    publications:[
      'Literature',
      'Fiction',
      'Poetry',
      'News Culture',
      'Travel',
      'Business',
      'Sports',
      'Lifestyle',
      'Technology',
      'Photojournal',
      'Art/Creative',
    ]
    
  })
}
</script>

<style scoped>

  .navbar{
    box-shadow: 6px 0 10px #6b6565;
  }
  .nav-row{
    width: 100%;
  }

  .label-text{
    font-size: 14px;
    color: #381dcc;
  }
  .form-control{
    background-color: #ced4da;
    border-radius: 0;
  }
  .form-control:focus{
    background-color: #fff;
  }
  .custom-control-label{
    font-size: 14px;
  }
  .custom-control-label:hover{
    cursor: pointer;
  }
  
  .custom-checkbox .custom-control-input:checked~.custom-control-label::before {
    background-color: #dc3545;
  }
  
  .custom-checkbox .custom-control-label::before {
      border-radius: 0;
  }
  .check-circle{
    width: 1.8rem;
    height: 1.8rem;
    border-radius: 50%;
    background-color: #fff;
    cursor: pointer;
  }
  .check-circle-text{
    font-size: .8rem;
  }
  @media only screen and (max-device-width: 600px)
    { 
      .check-div{
        position: absolute;
        top: 50px;
      }
      .form-div{
        top: 50px;
      }
    }

</style>
