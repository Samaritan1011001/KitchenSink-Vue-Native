<template>
  <nb-container :style="{backgroundColor: '#fff'}">
        <nb-header>
          <nb-left>
            <nb-button
              transparent
              :onPress="() => this.props.navigation.goBack()"
            >
              <nb-icon name="arrow-back" />
            </nb-button>
          </nb-left>
          <nb-body>
            <nb-title>Badge Footer</nb-title>
          </nb-body>
          <nb-right />
        </nb-header>

        <nb-content padder></nb-content>

        <nb-footer>
          <nb-footer-tab>
            <nb-button 
                :active="tab1" 
                :onPress="toggleTab1"
                vertical
                badge
            >
                <nb-badge>
                    <nb-text>2</nb-text>
                </nb-badge>
                <nb-icon name="apps" :active="tab1" />
                <nb-text>Apps</nb-text>
            </nb-button>
            
            <nb-button 
                :active="tab2" 
                :onPress="toggleTab2"
            >
                <nb-icon name="camera" :active="tab2" />
                <nb-text>Camera</nb-text>
            </nb-button>
            
            <nb-button 
                :active="tab3" 
                :onPress="toggleTab3"
                vertical
                badge
            >
                <nb-badge class="badge-3-bg">
                    <nb-text>51</nb-text>
                </nb-badge>
                <nb-icon name="compass" :active="tab3" />
                <nb-text>Compass</nb-text>
            </nb-button>
            
            <nb-button 
                :active="tab4" 
                :onPress="toggleTab4"
            >
                <nb-icon name="contact" :active="tab4" />
                <nb-text>Contact</nb-text>
            </nb-button>
          </nb-footer-tab>
        </nb-footer>
      </nb-container>
</template>


<script>
export default {
  data: function() {
    return {
      tab1: true,
      tab2: false,
      tab3: false,
      tab4: false
    };
  },
  methods: {
    toggleTab1: function() {
      this.tab1 = true;
      this.tab2 = false;
      this.tab3 = false;
      this.tab4 = false;
    },
    toggleTab2: function() {
      this.tab1 = false;
      this.tab2 = true;
      this.tab3 = false;
      this.tab4 = false;
    },
    toggleTab3: function() {
      this.tab1 = false;
      this.tab2 = false;
      this.tab3 = true;
      this.tab4 = false;
    },
    toggleTab4: function() {
      this.tab1 = false;
      this.tab2 = false;
      this.tab3 = false;
      this.tab4 = true;
    }
  }
};
</script>

<style>
.badge-3-bg {
  background-color: green;
}
</style>

