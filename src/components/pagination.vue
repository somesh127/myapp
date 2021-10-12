<div id="app">
  <v-app class="container">
    <v-card>
      <v-card-title>

      </v-card-title>
      <v-data-table
        :headers="headers"
        :items="items"
        show-expand
        single-expand
        item-key="name"
        :search="search"
        @item-expanded="loadDetails">
        <template v-slot:expanded-item="{ headers, item }">
            <td :colspan="headers.length">
                <div class="row">
                    <div v-for="p in item.details">
                            <div class="col">
                                {{ p.name }}
                             </div>  
                             <div class="col">
                                {{ p.Url }}
                             </div>   
                    </div>
                    
                </div>
            </td>
        </template>
      </v-data-table>
    </v-card>
  </v-app>
</div>