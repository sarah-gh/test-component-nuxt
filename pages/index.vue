<template>
  <div>
      <saragh-table-component-sample
    :tablehead="thead"
    :items="items"
    :modal="false"
    @showItem="showItem"
    @deleteItem="deleteItem"
    :operations="operations"
    :pageSize="pageSize"
      >
      <template slot="table-header">
          card header
      </template> 
      <template slot="table-footer">
          card footer
      </template> 
      <!-- <template slot="global-arrow-sort-icon-up">
         
      </template>  -->
      <template slot="header_column_fname" slot-scope="props">
          <i>
              {{props.item.text}}
          </i>
      </template>
      <template slot="modal-main" slot-scope="props">
        <div class="text">
          <div class="content">
            <p v-for="(item, x) in props.modalData" :key="x">
              <span>lable :</span>
              {{item}}
            </p>
          </div>
        </div>
      </template>
      <template slot="column_1" slot-scope="props">
          <i>
            {{props.item[props.i.name]}}
          </i>
      </template>
      <template slot="operate_icon_delete">
        <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-trash" viewBox="0 0 16 16">
          <path d="M5.5 5.5A.5.5 0 0 1 6 6v6a.5.5 0 0 1-1 0V6a.5.5 0 0 1 .5-.5zm2.5 0a.5.5 0 0 1 .5.5v6a.5.5 0 0 1-1 0V6a.5.5 0 0 1 .5-.5zm3 .5a.5.5 0 0 0-1 0v6a.5.5 0 0 0 1 0V6z"/>
          <path fill-rule="evenodd" d="M14.5 3a1 1 0 0 1-1 1H13v9a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V4h-.5a1 1 0 0 1-1-1V2a1 1 0 0 1 1-1H6a1 1 0 0 1 1-1h2a1 1 0 0 1 1 1h3.5a1 1 0 0 1 1 1v1zM4.118 4 4 4.059V13a1 1 0 0 0 1 1h6a1 1 0 0 0 1-1V4.059L11.882 4H4.118zM2.5 3V2h11v1h-11z"/>
        </svg>
      </template>
      <template slot="operate_icon_showing">
        <img src="https://cdn1.iconfinder.com/data/icons/freeline/32/eye_preview_see_seen_view-256.png">
      </template>
    </saragh-table-component-sample>
  </div>
</template>

<script>
import { SaraghTableComponentSample } from 'saragh-table-component';

export default {
    components: {
      SaraghTableComponentSample,
    },
   data () {
    return {
      items: [
          {
              id: "111fdfv",
              parent: "saraghotbzadeh",
              administratorName: "سارا قطب زاده",
              education: "vdfvdfv",
              jobSkills: "dfvdf",
              jobTitle: "fdvfdv",
              fname: "dfgvdfgd",
              lname: "fvdfvd",
              nationalCode: "dfdfv",
              phone: "09158854527",
              username: "fdfv"
          },
          {
              id: "222fgbfgb",
              parent: "saraghotbzadeh",
              administratorName: "سارا قطب زاده",
              education: "fgbfgb",
              jobSkills: "bfgbfgb",
              jobTitle: "fgbfgb",
              fname: "fghfgg",
              lname: "bfgb",
              nationalCode: "gbfgbfg",
              phone: "09145556644",
              username: "fgbfgb"
          },
          {
              id: "333fgh",
              parent: "saraghotbzadeh",
              administratorName: "سارا قطب زاده",
              education: "بلابلا",
              jobSkills: "بلابلا",
              jobTitle: "بلابلا",
              fname: "فغغات",
              lname: "فغالبا",
              nationalCode: "بلابلا",
              phone: "09158889977",
              username: "بلابلا"
          },
          {
              id: "444dfdfv",
              parent: "saraghotbzadeh",
              administratorName: "سارا قطب زاده",
              education: "dfvdfv",
              jobSkills: "dfvdfv",
              jobTitle: "dfvdfv",
              fname: "dfgdfg",
              lname: "dfgdfv",
              nationalCode: "dfvdfv",
              phone: "09158845522",
              username: "dfdfv"
          },
          {
              id: "555gfhfghn",
              parent: "saraghotbzadeh",
              administratorName: "سارا قطب زاده",
              education: "fghfgh",
              jobSkills: "fghfgh",
              jobTitle: "fghfgh",
              fname: "rthglkmb",
              lname: "fgfghg",
              nationalCode: "fghfgh",
              phone: "09158975489",
              username: "gfhfghn"
          },
          {
              id: "666fghfg",
              parent: "saraghotbzadeh",
              administratorName: "سارا قطب زاده",
              education: "بلابلا",
              jobSkills: "بلابلا",
              jobTitle: "بلابلا",
              fname: "نتمت",
              lname: "سیبیت",
              nationalCode: "بلابلا",
              phone: "09158889977",
              username: "بلابلافغا"
          },
          {
              id: "777fdfv",
              parent: "saraghotbzadeh",
              administratorName: "سارا قطب زاده",
              education: "vdfvdfv",
              jobSkills: "dfvdf",
              jobTitle: "fdvfdv",
              fname: "dfgvdfgd",
              lname: "fvdfvd",
              nationalCode: "dfdfv",
              phone: "09158854527",
              username: "fdfv"
          },
          {
              id: "888fgbfgb",
              parent: "saraghotbzadeh",
              administratorName: "سارا قطب زاده",
              education: "fgbfgb",
              jobSkills: "bfgbfgb",
              jobTitle: "fgbfgb",
              fname: "fghfgg",
              lname: "bfgb",
              nationalCode: "gbfgbfg",
              phone: "09145556644",
              username: "fgbfgb"
          },
          {
              id: "999fghth",
              parent: "saraghotbzadeh",
              administratorName: "سارا قطب زاده",
              education: "بلابلا",
              jobSkills: "بلابلا",
              jobTitle: "بلابلا",
              fname: "فغغات",
              lname: "فغالبا",
              nationalCode: "بلابلا",
              phone: "09158889977",
              username: "بلابلا"
          },
          {
              id: "1010dfdfv",
              parent: "saraghotbzadeh",
              administratorName: "سارا قطب زاده",
              education: "dfvdfv",
              jobSkills: "dfvdfv",
              jobTitle: "dfvdfv",
              fname: "dfgdfg",
              lname: "dfgdfv",
              nationalCode: "dfvdfv",
              phone: "09158845522",
              username: "dfdfv"
          },
          {
              id: "1111gfhfghn",
              parent: "saraghotbzadeh",
              administratorName: "سارا قطب زاده",
              education: "fghfgh",
              jobSkills: "fghfgh",
              jobTitle: "fghfgh",
              fname: "rthglkmb",
              lname: "fgfghg",
              nationalCode: "fghfgh",
              phone: "09158975489",
              username: "gfhfghn"
          },
          {
              id: "1212sdegtr",
              parent: "saraghotbzadeh",
              administratorName: "سارا قطب زاده",
              education: "بلابلا",
              jobSkills: "بلابلا",
              jobTitle: "بلابلا",
              fname: "نتمت",
              lname: "سیبیت",
              nationalCode: "بلابلا",
              phone: "09158889977",
              username: "بلابلافغا"
          },
          {
              id: "1313fdfv",
              parent: "saraghotbzadeh",
              administratorName: "سارا قطب زاده",
              education: "vdfvdfv",
              jobSkills: "dfvdf",
              jobTitle: "fdvfdv",
              fname: "dfgvdfgd",
              lname: "fvdfvd",
              nationalCode: "dfdfv",
              phone: "09158854527",
              username: "fdfv"
          },
          {
              id: "1414fgbfgb",
              parent: "saraghotbzadeh",
              administratorName: "سارا قطب زاده",
              education: "fgbfgb",
              jobSkills: "bfgbfgb",
              jobTitle: "fgbfgb",
              fname: "fghfgg",
              lname: "bfgb",
              nationalCode: "gbfgbfg",
              phone: "09145556644",
              username: "fgbfgb"
          },
          {
              id: "1515fghyh",
              parent: "saraghotbzadeh",
              administratorName: "سارا قطب زاده",
              education: "بلابلا",
              jobSkills: "بلابلا",
              jobTitle: "بلابلا",
              fname: "فغغات",
              lname: "فغالبا",
              nationalCode: "بلابلا",
              phone: "09158889977",
              username: "بلابلا"
          },
          {
              id: "dfdfv",
              parent: "saraghotbzadeh",
              administratorName: "سارا قطب زاده",
              education: "dfvdfv",
              jobSkills: "dfvdfv",
              jobTitle: "dfvdfv",
              fname: "dfgdfg",
              lname: "dfgdfv",
              nationalCode: "dfvdfv",
              phone: "09158845522",
              username: "dfdfv"
          },
          {
              id: "gfhfghn",
              parent: "saraghotbzadeh",
              administratorName: "سارا قطب زاده",
              education: "fghfgh",
              jobSkills: "fghfgh",
              jobTitle: "fghfgh",
              fname: "rthglkmb",
              lname: "fgfghg",
              nationalCode: "fghfgh",
              phone: "09158975489",
              username: "gfhfghn"
          },
          {
              id: "gytyu",
              parent: "saraghotbzadeh",
              administratorName: "سارا قطب زاده",
              education: "بلابلا",
              jobSkills: "بلابلا",
              jobTitle: "بلابلا",
              fname: "نتمت",
              lname: "سیبیت",
              nationalCode: "بلابلا",
              phone: "09158889977",
              username: "بلابلافغا"
          }
      ],
      pageSize: 3,
      operations: [true, true],
      thead: [
        {
          text: 'نام',
          name: 'fname',
          typeof: 'fa'
        },
        {
          text: 'نام خانوادگی',
          name: 'lname',
          typeof: 'fa'
        },
        {
          text: 'نام کاربری',
          name: 'id',
          typeof: 'en'
        },
        {
          text: 'تلفن',
          name: 'phone',
          typeof: 'phone'
        }
      ],
    }
  },
  methods: {
    deleteItem() {
      console.log('deleteItem');
    },
    showItem() {
      console.log('showItem');
    },
    addElement (employee) {
      this.items.push(employee)
    },
    onEnterModal (value) {
      this.showModal = false
    }
  }
}
</script>
