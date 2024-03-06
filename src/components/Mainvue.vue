<script setup>
import {ref,onMounted} from 'vue'
import Banner from '@/components/Banner.vue'
import Houses from '@/components/Houses.vue'
let tabrent=ref([
  {
    id:0,
    houseimage:"/images/home_min/home3.JPG",
    title1:"RENT A HOME",
    title2:"Rental home",
    title3:"for Everyone",
    title4:"Explore from Apartments, builder floor, villas and more",
    buttontitle:"Explore Renting"
  }
])
let tabsale=ref([
  {
    id:1,
    houseimage:"/images/home_min/home5.JPG",
    title1:"BUY A HOME",
    title2:"Find,Buy & Own Your",
    title3:"Dream Home",
    title4:"Explore Apartments, Villas, Homes and more",
    buttontitle:"Explore Buying"
  }
])
// Rent house data begins here-----------------------------------------------------------------
let renthousedata=ref(
[
  {id:0,
  	description:
  		{
  			price:'25000/monthly',
  			chamber:"3",
  			bathroom:"2",
  			surface:"123.34",
  			titre2:'Exclusive | Affrodable Options Available',
  			fulldescription:'Lorem ipsum dolor sit amet'
  		},
  	img1:'/images/home_min/home1.JPG'
  },
  {id:1,
  	description:
  		{
  			price:'2500/monthly',
  			chamber:"6",
  			bathroom:"2",
  			surface:"321.34",
  			titre2:'Exclusive | Affrodable Options Available',
  			fulldescription:'Lorem ipsum dolor sit amet'
  		},
  	img1:'/images/home_min/home2.JPG'
  },
  {id:2,
  	description:
  		{
  			price:'340/monthly',
  			chamber:"8",
  			bathroom:"3",
  			surface:"231.34",
  			titre2:'Exclusive | Affrodable Options Available',
  			fulldescription:'Lorem ipsum dolor sit amet'
  		},
  	img1:'/images/home_min/home3.JPG'
  },
  {id:3,
  	description:
  		{
  			price:'1234/monthly',
  			chamber:"4",
  			bathroom:"3",
  			surface:"312.34",
  			titre2:'Exclusive | Affrodable Options Available',
  			fulldescription:'Lorem ipsum dolor sit amet'
  		},
  	img1:'/images/home_min/home4.JPG'
  },
  {id:4,
  	description:
  		{
  			price:'450/monthly',
  			chamber:"6",
  			bathroom:"3",
  			surface:"456.34",
  			titre2:'Exclusive | Affrodable Options Available',
  			fulldescription:'Lorem ipsum dolor sit amet'
  		},
  	img1:'/images/home_min/home5.JPG'
  },
  {id:5,
  	description:
  		{
  			price:'789/monthly',
  			chamber:"8",
  			bathroom:"2",
  			surface:"675.65",
  			titre2:'Exclusive | Affrodable Options Available',
  			fulldescription:'Lorem ipsum dolor sit amet'
  		},
  	img1:'/images/home_min/home6.JPG'
  },
  {id:6,
  	description:
  		{
  			price:'890/monthly',
  			chamber:"9",
  			bathroom:"4",
  			surface:"765.32",
  			titre2:'Exclusive | Affrodable Options Available',
  			fulldescription:'Lorem ipsum dolor sit amet'
  		},
  	img1:'/images/home_min/home7.JPG'
  },
  {id:7,
  	description:
  		{
  			price:'567/monthly',
  			chamber:"8",
  			bathroom:"4",
  			surface:"786.14",
  			titre2:'Exclusive | Affrodable Options Available',
  			fulldescription:'Lorem ipsum dolor sit amet'
  		},
  	img1:'/images/home_min/home8.JPG'
  },
  {id:8,
  	description:
  		{
  			price:'3456/monthly',
  			chamber:"7",
  			bathroom:"4",
  			surface:"124.56",
  			titre2:'Exclusive | Affrodable Options Available',
  			fulldescription:'Lorem ipsum dolor sit amet'
  		},
  	img1:'/images/home_min/home9.JPG'
  }
])
// Rent house data ends here----------------------------------------------------------------------
let rentslider0=ref(
[
  '/images/home_max/Home_max1.JPG',
  'images/interior/m1.JPG',
  'images/interior/m2.JPG',
  'images/interior/m3.JPG',
  'images/interior/m4.JPG',
  'images/interior/m5.JPG',
  'images/interior/m6.JPG',
  'images/interior/m7.JPG',
  'images/interior/m8.JPG'
])
let rentdimension0=ref(
[
  {price:'25000/monthly',
  chamber:"3",
  bathroom:"2",
  surface:"123.34",
  titre2:'Exclusive | Affrodable Options Available',
  fulldescription:'Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet'}
])
// ------------------------------------------------------------------------------------------------------
let rentslider1=ref(
[
  '/images/home_max/Home_max2.JPG',
  'images/interior/m1.JPG',
  'images/interior/m2.JPG',
  'images/interior/m3.JPG',
  'images/interior/m4.JPG',
  'images/interior/m5.JPG',
  'images/interior/m6.JPG',
  'images/interior/m7.JPG',
  'images/interior/m8.JPG'
]);
let rentdimension1=ref(
[
  {
  	price:'2500/monthly',
  	chamber:"6",
  	bathroom:"2",
  	surface:"321.34",
  	titre2:'Exclusive | Affrodable Options Available',
  	fulldescription:'Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet'
  }
])
// ------------------------------------------------------------------------------------------------------
let rentslider2=ref(
[
  'images/home_max/Home_max3.JPG',
  'images/interior/m1.JPG',
  'images/interior/m2.JPG',
  'images/interior/m3.JPG',
  'images/interior/m4.JPG',
  'images/interior/m5.JPG',
  'images/interior/m6.JPG',
  'images/interior/m7.JPG',
  'images/interior/m8.JPG'
])
let rentdimension2=ref(
[
  {
    price:'340/monthly',
    chamber:"8",
    bathroom:"3",
    surface:"231.34",
    titre2:'Exclusive | Affrodable Options Available',
    fulldescription:'Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet',
  }
])
// ------------------------------------------------------------------------------------------------------
let rentslider3=ref(
[
  'images/home_max/Home_max4.JPG',
  'images/interior/m1.JPG',
  'images/interior/m2.JPG',
  'images/interior/m3.JPG',
  'images/interior/m4.JPG',
  'images/interior/m5.JPG',
  'images/interior/m6.JPG',
  'images/interior/m7.JPG',
  'images/interior/m8.JPG'
])
let rentdimension3=ref(
[
  {
  	price:'1234/monthly',
  	chamber:"4",
  	bathroom:"3",
  	surface:"312.34",
  	titre2:'Exclusive | Affrodable Options Available',
  	fulldescription:'Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet'
  }
])
// ------------------------------------------------------------------------------------------------------
let rentslider4=ref(
[
  'images/home_max/Home_max5.JPG',
  'images/interior/m1.JPG',
  'images/interior/m2.JPG',
  'images/interior/m3.JPG',
  'images/interior/m4.JPG',
  'images/interior/m5.JPG',
  'images/interior/m6.JPG',
  'images/interior/m7.JPG',
  'images/interior/m8.JPG'
])
let rentdimension4=ref(
[
  {
  	price:'450/monthly',
  	chamber:"6",
  	bathroom:"3",
  	surface:"456.34",
  	titre2:'Exclusive | Affrodable Options Available',
  	fulldescription:'Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet'
  }
])
// ------------------------------------------------------------------------------------------------------
let rentslider5=ref(
[
  'images/home_max/Home_max6.JPG',
  'images/interior/m1.JPG',
  'images/interior/m2.JPG',
  'images/interior/m3.JPG',
  'images/interior/m4.JPG',
  'images/interior/m5.JPG',
  'images/interior/m6.JPG',
  'images/interior/m7.JPG',
  'images/interior/m8.JPG'
])
let rentdimension5=ref(
[
  {
    price:'789/monthly',
    chamber:"8",
    bathroom:"2",
    surface:"675.65",
    titre2:'Exclusive | Affrodable Options Available',
    fulldescription:'Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet'
  }
])
// ------------------------------------------------------------------------------------------------------
let rentslider6=ref(
[
  'images/home_max/Home_max7.JPG',
  'images/interior/m1.JPG',
  'images/interior/m2.JPG',
  'images/interior/m3.JPG',
  'images/interior/m4.JPG',
  'images/interior/m5.JPG',
  'images/interior/m6.JPG',
  'images/interior/m7.JPG',
  'images/interior/m8.JPG'
])
let rentdimension6=ref(
[
  {
  	price:'890/monthly',
  	chamber:"9",
  	bathroom:"4",
  	surface:"765.32",
  	titre2:'Exclusive | Affrodable Options Available',
  	fulldescription:'Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet'
  }
])
// ------------------------------------------------------------------------------------------------------
let rentslider7=ref(
[
  'images/home_max/Home_max8.JPG',
  'images/interior/m1.JPG',
  'images/interior/m2.JPG',
  'images/interior/m3.JPG',
  'images/interior/m4.JPG',
  'images/interior/m5.JPG',
  'images/interior/m6.JPG',
  'images/interior/m7.JPG',
  'images/interior/m8.JPG'
])
let rentdimension7=ref(
[
  {
    price:'567/monthly',
    chamber:"8",
    bathroom:"4",
    surface:"786.14",
    titre2:'Exclusive | Affrodable Options Available',
    fulldescription:'Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet'
  }

])
// ------------------------------------------------------------------------------------------------------
let rentslider8=ref(
[
  'images/home_max/Home_max9.JPG',
  'images/interior/m1.JPG',
  'images/interior/m2.JPG',
  'images/interior/m3.JPG',
  'images/interior/m4.JPG',
  'images/interior/m5.JPG',
  'images/interior/m6.JPG',
  'images/interior/m7.JPG',
  'images/interior/m8.JPG'
])
let rentdimension8=ref(
[
  {
  	price:'3456/monthly',
  	chamber:"7",
  	bathroom:"4",
  	surface:"124.67",
  	titre2:'Exclusive | Affrodable Options Available',
  	fulldescription:'Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet'
  }
])
// For sale Homes data begins here---------------------------------------------------------------------
let salehomesdata=ref(
[
  {id:0,
  	description:
  		{
  			price:'25000',
  			chamber:"3",
  			bathroom:"2",
  			surface:"123.34",
  			titre2:'Exclusive | Affrodable Options Available',
  			fulldescription:'Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet'
  		},
  	img1:'/images/home_min/home1.JPG'
  },
  {id:1,
  	description:
  		{
  			price:'2500',
  			chamber:"6",
  			bathroom:"2",
  			surface:"321.34",
  			titre2:'Exclusive | Affrodable Options Available',
  			fulldescription:'Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet'
  		},
  	img1:'/images/home_min/home2.JPG'
  },
  {id:2,
  	description:
  		{
  			price:'340',
  			chamber:"8",
  			bathroom:"3",
  			surface:"231.34",
  			titre2:'Exclusive | Affrodable Options Available',
  			fulldescription:'Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet'
  		},
  	img1:'/images/home_min/home3.JPG'
  },
  {id:3,
  	description:
  		{
  			price:'1234',
  			chamber:"4",
  			bathroom:"3",
  			surface:"312.34",
  			titre2:'Exclusive | Affrodable Options Available',
  			fulldescription:'Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet'
  		},
  	img1:'/images/home_min/home4.JPG'
  },
  {id:4,
  	description:
  		{
  			price:'450',
  			chamber:"6",
  			bathroom:"3",
  			surface:"456.34",
  			titre2:'Exclusive | Affrodable Options Available',
  			fulldescription:'Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet'
  		},
  	img1:'/images/home_min/home5.JPG'
  },
  {id:5,
  	description:
  		{
  			price:'789',
  			chamber:"8",
  			bathroom:"2",
  			surface:"675.65",
  			titre2:'Exclusive | Affrodable Options Available',
  			fulldescription:'Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet'
  		},
  	img1:'/images/home_min/home6.JPG'
  },
  {id:6,
  	description:
  		{
  			price:'890',
  			chamber:"9",
  			bathroom:"4",
  			surface:"765.32",
  			titre2:'Exclusive | Affrodable Options Available',
  			fulldescription:'Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet'
  		},
  	img1:'/images/home_min/home7.JPG'
  },
  {id:7,
  	description:
  		{
  			price:'567',
  			chamber:"8",
  			bathroom:"4",
  			surface:"786.14",
  			titre2:'Exclusive | Affrodable Options Available',
  			fulldescription:'Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet'
  		},
  	img1:'/images/home_min/home8.JPG'
  },
  {id:8,
  	description:
  		{
  			price:'3456',
  			chamber:"7",
  			bathroom:"4",
  			surface:"124.67",
  			titre2:'Exclusive | Affrodable Options Available',
  			fulldescription:'Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet'
  		},
  	img1:'/images/home_min/home9.JPG'
  }
])
// For sale Homes data ends here------------------------------------------------------------------------
let saledimension0=ref(
[
  {price:'25000',
  chamber:"3",
  bathroom:"2",
  surface:"123.34",
  titre2:'Exclusive | Affrodable Options Available',
  fulldescription:'Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet'}
])
let saledimension1=ref(
[
  {
  	price:'2500',
  	chamber:"6",
  	bathroom:"2",
  	surface:"321.34",
  	titre2:'Exclusive | Affrodable Options Available',
  	fulldescription:'Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet'
  }
])
let saledimension2=ref(
[
  {
    price:'340',
    chamber:"8",
    bathroom:"3",
    surface:"231.34",
    titre2:'Exclusive | Affrodable Options Available',
    fulldescription:'Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet',
  }
])
let saledimension3=ref(
[
  {
  	price:'1234',
  	chamber:"4",
  	bathroom:"3",
  	surface:"312.34",
  	titre2:'Exclusive | Affrodable Options Available',
  	fulldescription:'Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet'
  }
])
let saledimension4=ref(
[
  {
  	price:'450',
  	chamber:"6",
  	bathroom:"3",
  	surface:"456.34",
  	titre2:'Exclusive | Affrodable Options Available',
  	fulldescription:'Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet'
  }
])
let saledimension5=ref(
[
  {
    price:'789',
    chamber:"8",
    bathroom:"2",
    surface:"675.65",
    titre2:'Exclusive | Affrodable Options Available',
    fulldescription:'Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet'
  }
])
let saledimension6=ref(
[
  {
  	price:'890',
  	chamber:"9",
  	bathroom:"4",
  	surface:"765.32",
  	titre2:'Exclusive | Affrodable Options Available',
  	fulldescription:'Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet'
  }
])
let saledimension7=ref(
[
  {
    price:'567',
    chamber:"8",
    bathroom:"4",
    surface:"786.14",
    titre2:'Exclusive | Affrodable Options Available',
    fulldescription:'Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet'
  }
])
let saledimension8=ref(
[
  {
  	price:'3456',
  	chamber:"7",
  	bathroom:"4",
  	surface:"1234.567",
  	titre2:'Exclusive | Affrodable Options Available',
  	fulldescription:'Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet'
  }
])
let dialog=ref(false);
let rentcaroussel=ref([]);
let rentdescription=ref([]);
let owner=ref();
function scroll(refName)
{
  const elt=document.getElementById(refName);
  elt.scrollIntoView({behavior:"smooth"});
}
function describer(id)
{
  owner.value="Meet the Owner";
switch(id)
    {
      case 0:
        dialog.value=true;
        rentcaroussel=rentslider0.value;
        rentdescription=rentdimension0.value;
        break;
      case 1:
        dialog.value=true;
        rentcaroussel=rentslider1.value;
        rentdescription=rentdimension1.value;
        break;
      case 2:
        dialog.value=true;
        rentcaroussel=rentslider2.value;
        rentdescription=rentdimension2.value;
        break;
      case 3:
        dialog.value=true;
        rentcaroussel=rentslider3.value;
        rentdescription=rentdimension3.value;
        break;
      case 4:
        dialog.value=true;
        rentcaroussel=rentslider4.value;
        rentdescription=rentdimension4.value;
        break;
      case 5:
        dialog.value=true;
        rentcaroussel=rentslider5.value;
        rentdescription=rentdimension5.value;
        break;
      case 6:
        dialog.value=true;
        rentcaroussel=rentslider6.value;
        rentdescription=rentdimension6.value;
        break;
      case 7:
        dialog.value=true;
        rentcaroussel=rentslider7.value;
        rentdescription=rentdimension7.value;
        break;
      case 8:
        dialog.value=true;
        rentcaroussel=rentslider8.value;
        rentdescription=rentdimension8.value;
        break;
    }
}
function saledescriber(id)
{
  owner.value="Meet the Seller";
  switch(id)
  {
    case 0:
      dialog.value=true;
      rentcaroussel=rentslider0.value;
      rentdescription=saledimension0.value;
      break;
    case 1:
      dialog.value=true;
      rentcaroussel=rentslider1.value;
      rentdescription=saledimension1.value;
      break;
    case 2:
      dialog.value=true;
      rentcaroussel=rentslider2.value;
      rentdescription=saledimension2.value;
      break;
    case 3:
      dialog.value=true;
      rentcaroussel=rentslider3.value;
      rentdescription=saledimension3.value;
      break;
    case 4:
      dialog.value=true;
      rentcaroussel=rentslider4.value;
      rentdescription=saledimension4.value;
      break;
    case 5:
      dialog.value=true;
      rentcaroussel=rentslider5.value;
      rentdescription=saledimension5.value;
      break;
    case 6:
      dialog.value=true;
      rentcaroussel=rentslider6.value;
      rentdescription=saledimension6.value;
      break;
    case 7:
      dialog.value=true;
      rentcaroussel=rentslider7.value;
      rentdescription=saledimension7.value;
      break;
    case 8:
      dialog.value=true;
      rentcaroussel=rentslider8.value;
      rentdescription=saledimension8.value;
      break;
  }
}

function fermerdialog()
{
  dialog.value=false;
  issuggestionshow.value=false;
}
let isloadedpage=ref(false);
let isrentbannerloaded=ref(false);
let isrentcontainerloaded=ref(false);
let issalebannerloaded=ref(false);
let issalecontainerloaded=ref(false);
let isfootershow=ref(false);
let iscontactshow=ref(false);
onMounted
{
  isloadedpage.value=true;
  isrentbannerloaded.value=false;
  isrentcontainerloaded.value=false;
  issalebannerloaded.value=false;
  issalecontainerloaded.value=false;
  isfootershow.value=false;
  iscontactshow.value=false;
  setTimeout(()=>
  {
      stoploading();
  },2000);
}
function stoploading()
{
  isloadedpage.value=false;
  isrentbannerloaded.value=true;
  isrentcontainerloaded.value=true;
  issalebannerloaded.value=true;
  issalecontainerloaded.value=true;
  isfootershow.value=true;
  iscontactshow.value=true;
}
let issuggestionshow=ref(false);
function showsuggestion()
{
  issuggestionshow.value=true;
  setTimeout(()=>
  {
     gotosuggestion();
  },500);

}
function gotosuggestion()
{
  const elt=document.getElementById('contactsuggestion');
  elt.scrollIntoView({behavior:"smooth"});
}
</script>
<template>
<v-app-bar id="navmain">
  <v-spacer></v-spacer>
    <v-btn
       class="btnav text-h6 mt-2" @click="scroll('home')">Home</v-btn>
    <v-btn
       class="btnav text-h6 mt-2" @click="scroll('rent')">Rent</v-btn>
    <v-btn
       class="btnav text-h6 mt-2" @click="scroll('sales')">Sale</v-btn>
    <v-btn
       class="btnav text-h6 mt-2" @click="scroll('contact')">Contact</v-btn>
  </v-app-bar>
  <div class="circleloadercontainer" v-if="isloadedpage">
      <v-progress-circular class="circleloader"
            indeterminate
            color="#15a2ff"
      ></v-progress-circular>
  </div>
  <v-conainer id="home">
    <Banner v-for="doss in tabrent" :key="doss.id" v-if="isrentbannerloaded"
            :houseimage="doss.houseimage"
            :title1="doss.title1"
            :title2="doss.title2"
            :title3="doss.title3"
            :title4="doss.title4"
            :buttontitle="doss.buttontitle"
            @exploring="scroll('rent')">
    </Banner>
  </v-conainer>

    <v-container id="rent" v-if="isrentcontainerloaded">
      <div class="renthousecontainer">
        <Houses v-for="docs in renthousedata" :key="docs.id"
          :houseimage="docs.img1"
          :houseprice="docs.description.price"
          :chamber="docs.description.chamber"
          :bathroom="docs.description.bathroom"
          :squarefeet="docs.description.surface"
          :housedescription="docs.description.fulldescription"
          @click="describer(docs.id)">
        </Houses>
      </div>
    </v-container>
    <Banner v-for="doss in tabsale" :key="doss.id" v-if="issalebannerloaded"
            :houseimage="doss.houseimage"
            :title1="doss.title1"
            :title2="doss.title2"
            :title3="doss.title3"
            :title4="doss.title4"
            :buttontitle="doss.buttontitle"
            @exploring="scroll('sales')">
    </Banner>
    <v-container id="sales" v-if="issalecontainerloaded">
          <div class="renthousecontainer">
            <Houses v-for="docs in salehomesdata"
              :key="docs.id"
              :houseimage="docs.img1"
              :houseprice="docs.description.price"
              :chamber="docs.description.chamber"
              :bathroom="docs.description.bathroom"
              :squarefeet="docs.description.surface"
              :housedescription="docs.description.fulldescription"
              @click="saledescriber(docs.id)">
            </Houses>
          </div>
    </v-container>
    <v-container>
      <div class="describer text-center pa-4">
         <v-dialog
                v-model="dialog"
                transition="dialog-bottom-transition"
                fullscreen
              >
            <v-card>
              <v-toolbar>
                <v-btn
                  icon="mdi-close"
                  @click="fermerdialog"
                ></v-btn>

              </v-toolbar>
              <div class="carousselcontainer">
                <div class="carousselcontent">
                  <v-carousel
                        height="400"
                        progress="primary"
                        hide-delimiters
                        cycle
                      >
                        <v-carousel-item
                          v-for="techimg in rentcaroussel"
                          :key="techimg.id"
                        >
                          <v-img :src="techimg" alt="House images" class="mt-10" width="950">

                          </v-img>
                        </v-carousel-item>
                      </v-carousel>
                </div>
                <v-card class="mt-5">
                  <div class="descriptioncontainer mt-5">
                    <div class="descriptioncontent" v-for="docs in rentdescription">
                      <h6 class="text-h6 descprice">AED {{docs.price}}</h6>
                      <h6 class="text-h6">{{docs.chamber}} <v-icon
                            size="x-small"
                            color="#002600"
                            icon="mdi-bed"
                            class="ms-1 mb-1"
                          ></v-icon>| {{docs.bathroom}}
                          <v-icon
                            size="x-small"
                            color="#002600"
                            icon="mdi-scale-bathroom"
                            class="ms-1 mb-1"
                          ></v-icon>| {{docs.surface}} Sqrft</h6>
                      <h6 class="text-h6">{{docs.titre2}}</h6>
                      <p class="text-h6 mt-4">{{docs.fulldescription}}</p>
                      <div class="ownercontact mt-10">
                        <v-btn @click="showsuggestion" class="mb-5" color="#15a2ff">
                          {{owner}}
                        </v-btn>
                      </div>
                      <div class="suggestioncontainer mt-1" v-if="issuggestionshow" id="contactsuggestion">
                        <h6 class="text-h6 mb-5">
                          This action shows any link to the Owner / Seller.
                        </h6>
                      </div>
                    </div>
                  </div>
                </v-card>
              </div>
            </v-card>
          </v-dialog>
      </div>
    </v-container>
    <v-container v-if="iscontactshow" id="contact">
      <div class="contactcontainer">
        <div class="contactcontent">
            <h4 class="text-h4 mt-16 ms-8">
              See also the Mainpage.
            </h4>
            <h6 class="text-subtitle-1 ms-8">
              This will redirect to the main page that contains the link to this project.
            </h6>
            <v-btn color="#002600" class="ms-8 mb-8 mt-8" size="large" href="https://doriaarnaud.online">
                Go to the Mainpage
            </v-btn>
        </div>
      </div>
    </v-container>
    <v-footer v-if="isfootershow" color="#000000">

    </v-footer>
</template>

<script>
  export default
  {
  data: () => ({

      })
  }
</script>
<style>
  @media (min-width: 1200px)
  {
    #navmain
    {
      height:90px;
    }
    .btnav
    {
      margin:0;
      padding:0;
      width:90px;
      text-decoration:underline;
    }
    .circleloadercontainer
    {
      margin-top:50px;
      width:100px;
      margin-left:auto;
      margin-right:auto;
      height:500px;
    }
    .circleloader
    {
      margin-top:20px;
      width:80px;
      height:80px;
      margin-left:auto;
      margin-right:auto;
    }
    .renthousecontainer
    {
      display:flex;
      align-content: center;
      justify-content: center;
      flex-wrap: wrap;
      text-align: left;
      margin-top: 50px;
    }
    .carousselcontent,.descriptioncontent
    {
      width:800px;
      margin-left:auto;
      margin-right:auto;
    }
    h6.descprice
    {
      color:#15a2ff;
    }
    .contactcontainer
    {
      min-height:200px;
      padding-top:50px;
    }
    .contactcontent
    {
      width:950px;
      margin-left:auto;
      margin-right:auto;
      border:1px solid #9f9f9f;
      min-height: 200px;
      background-color:#666666;
      border-radius:10px;
      color:#ffffff;
    }
  }
  @media (min-width: 992px) and (max-width: 1199px)
  {
    #navmain
    {
      height:70px;
    }
    .btnav
    {
      margin:0;
      padding:0;
      width:90px;
      text-decoration:underline;
    }
    .circleloadercontainer
    {
      width:100px;
      margin-left:auto;
      margin-right:auto;
      height:500px;
    }
    .circleloader
    {
      margin-top:20px;
      width:80px;
      height:80px;
      margin-left:auto;
      margin-right:auto;
    }
    .renthousecontainer
    {
      display:flex;
      align-content: center;
      justify-content: center;
      flex-wrap: wrap;
      text-align: left;
      margin-top: 50px;
    }
    .carousselcontent,.descriptioncontent
    {
      width:800px;
      margin-left:auto;
      margin-right:auto;
    }
    .descprice
    {
      color:#15a2ff;
    }
    .contactcontainer
    {
      min-height:200px;
      padding-top:50px;
    }
    .contactcontent
    {
      width:800px;
      margin-left:auto;
      margin-right:auto;
      border:1px solid #9f9f9f;
      min-height: 200px;
      background-color:#666666;
      border-radius:10px;
      color:#ffffff;
    }
  }
  @media (min-width: 768px) and (max-width: 991px)
  {
    #navmain
    {
      height:70px;
    }
    .btnav
    {
      margin:0;
      padding:0;
      width:90px;
      text-decoration:underline;
    }
    .circleloadercontainer
    {
      width:100px;
      margin-left:auto;
      margin-right:auto;
      height:500px;
    }
    .circleloader
    {
      margin-top:20px;
      width:80px;
      height:80px;
      margin-left:auto;
      margin-right:auto;
    }
    .renthousecontainer
    {
      display:flex;
      align-content: center;
      justify-content: center;
      flex-wrap: wrap;
      text-align: left;
      margin-top: 50px;
    }
    .carousselcontent,.descriptioncontent
    {
      width:800px;
      margin-left:auto;
      margin-right:auto;
      padding-left: 20px;
    }
    .descprice
    {
      color:#15a2ff;
    }
    .contactcontainer
    {
      min-height:200px;
      padding-top:50px;
    }
    .contactcontent
    {
      width:700px;
      margin-left:auto;
      margin-right:auto;
      border:1px solid #9f9f9f;
      min-height: 200px;
      background-color:#666666;
      border-radius:10px;
      color:#ffffff;
    }
  }
  @media (min-width: 576px) and (max-width: 767px)
  {
    #navmain
    {
      height:70px;
    }
    .btnav
    {
      margin:0;
      padding:0;
      width:90px;
      text-decoration:underline;
    }
    .circleloadercontainer
    {
      width:100px;
      margin-left:auto;
      margin-right:auto;
      height:500px;
    }
    .circleloader
    {
      margin-top:20px;
      width:80px;
      height:80px;
      margin-left:auto;
      margin-right:auto;
    }
    .renthousecontainer
    {
      display:flex;
      align-content: center;
      justify-content: center;
      flex-wrap: wrap;
      text-align: left;
      margin-top: 50px;
    }
    .descriptioncontent
    {
      margin-left:auto;
      margin-right:auto;
      padding-left:20px;
      padding-right:20px;
    }
    .descprice
    {
      color:#15a2ff;
    }
    .contactcontainer
    {
      min-height:200px;
      padding-top:50px;
    }
    .contactcontent
    {
      width:550px;
      margin-left:auto;
      margin-right:auto;
      border:1px solid #9f9f9f;
      min-height: 200px;
      background-color:#666666;
      border-radius:10px;
      color:#ffffff;
    }
  }
  @media (max-width: 575px)
  {
    #navmain
    {
      height:70px;
    }
    .btnav
    {
      margin:0;
      padding:0;
      width:90px;
      text-decoration:underline;
    }
    .circleloadercontainer
    {
      width:100px;
      margin-left:auto;
      margin-right:auto;
      height:500px;
    }
    .circleloader
    {
      margin-top:20px;
      width:80px;
      height:80px;
      margin-left:auto;
      margin-right:auto;
    }
    .renthousecontainer
    {
      display:flex;
      align-content: center;
      justify-content: center;
      flex-wrap: wrap;
      text-align: left;
      margin-top: 50px;
    }
    .descriptioncontent
    {
      margin-top:-20px;
      margin-left:auto;
      margin-right:auto;
      padding-left:20px;
      padding-right:20px;
    }
    .descprice
    {
      color:#15a2ff;
    }
    .contactcontainer
    {
      min-height:200px;
      padding-top:50px;
    }
    .contactcontent
    {
      width:350px;
      margin-left:auto;
      margin-right:auto;
      border:1px solid #9f9f9f;
      min-height: 200px;
      background-color:#666666;
      border-radius:10px;
      color:#ffffff;
    }
  }
</style>
