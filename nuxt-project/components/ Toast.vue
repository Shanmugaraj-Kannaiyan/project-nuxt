<template>
  <div>
      <div id="toastbar">{{name}}</div>
  </div>
</template>

<script>
export default {
    data(){
        return {
            name :'',
        }
    },
    methods: {
        toast(value, color){
            var colorcode;
            if(color === 'success'){
                colorcode = 'green'
            } else if(color === 'danger'){
                colorcode = 'red'
            } else {
                colorcode = 'black'
            }
            this.name = value   
            var x  = document.getElementById('toastbar');
            x.className = 'toast'
            x.style.backgroundColor = colorcode
            setTimeout(() => x.className = x.className.replace('toast', ''), 2800)
        }
    }
}
</script>

<style>
#toastbar{
    visibility: hidden;
    background-color: black;
    color: white;
    padding: 16px;
    position: fixed;
    bottom: 30px;
    min-width:250px;
    left:50%;
    margin-left: -125px;
    text-align: center;
    border-radius: 4px;
}
#toastbar.showtoast {
    visibility: visible;
    animation: beginToast 0.5s, endToast 0.5s 2.5s;
}

@keyframes beginToast {
    from{bottom:0;opacity: 0;}
    to{bottom:30px;opacity: 1;}    
}

@keyframes endToast {
    from{bottom:30px;opacity: 1}
    to{bottom:0; opacity:0}
}

</style>