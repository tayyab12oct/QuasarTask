<template>
<div class="main q-ma-0 text-center">
    <div class="row items-start example-container">
        <div class="example-cell text-center col-1" tabindex="0">
            <div class="text-white q-pb-md q-pt-sm q-mx-md" style="font-size: 2.5em; border-bottom: 1px solid #999999">
                <img src="~/assets/images/search-pic.png" class="left-img" alt="" />
            </div>
            <div class="q-pa-sm md:q-pa-md q-pt-xl">
                <div class="text-white q-gutter-md" style="font-size: 2.2em">
                    <q-icon name="dashboard" class="q-pb-md" />
                    <q-icon name="warning" class="q-pb-md" />
                    <q-icon name="print" class="q-pb-md" />
                    <q-icon name="today" class="q-pb-md" />
                    <q-icon name="settings" class="q-pb-md" />
                </div>
            </div>
            <div class="bottom">
                <div class="text-white q-gutter-md" style="font-size: 2.2em">
                    <q-icon name="dashboard" class="q-pb-md" />
                </div>
            </div>

        </div>
        <div class="main-div col-11 q-pa-lg text-left" tabindex="0">
            <div class="flex justify-between">
                <div class="">
                    <p class="number-text">Dedicated hotline number</p>
                    <h6>800-000-0911</h6>
                </div>
                <div class="flex items-center">
                    <q-btn round>
                        <q-avatar size="46px">
                            <img src="https://cdn.quasar.dev/img/avatar2.jpg" />
                        </q-avatar>
                    </q-btn>
                    <q-icon name="settings" class="q-mr-md q-ml-xs" />
                    <!-- <q-btn-dropdown >
      <q-list>
        <q-item clickable v-close-popup @click="onItemClick">
          <q-item-section>
            <q-item-label>Photos</q-item-label>
          </q-item-section>
        </q-item>

        <q-item clickable v-close-popup @click="onItemClick">
          <q-item-section>
            <q-item-label>Videos</q-item-label>
          </q-item-section>
        </q-item>

        <q-item clickable v-close-popup @click="onItemClick">
          <q-item-section>
            <q-item-label>Articles</q-item-label>
          </q-item-section>
        </q-item>
      </q-list>
    </q-btn-dropdown> -->
                    <q-btn no-caps class="button q-px-md" label="BOOK A SERVICE" />
                </div>
            </div>
            <div class=" q-my-lg">
                <div class="flex font-xs q-mt-lg justify-start" style="color:#7077FB">
                    <q-breadcrumbs>
                        <q-breadcrumbs-el label="My Bookings" style="color:#7077FB" />
                        <q-breadcrumbs-el label="Telemedicine" />
                    </q-breadcrumbs>
                </div>
                <h4>Telemedicine</h4>
            </div>
            <div class="flex justify-between">
                <div class="div-left">
                    <div class="img">
                        <img src="../assets/images/rOGdWY.jpg" />
                    </div>
                    <div class="q-py-lg bottom-icons flex justify-between" style="font-size: 2.2em">
                        <div class="flex column justify-center items-center">
                            <div class="icons q-mb-sm">
                                <q-icon name="call" class="" />
                            </div>
                            <p class="icon-text">Cancel call</p>
                        </div>
                        <div class="flex column justify-center items-center">
                            <div class="icons q-mb-sm">
                                <q-icon name="mic" class="" />
                            </div>
                            <p class="icon-text">Mute mic</p>
                        </div>
                        <div class="flex column justify-center items-center">
                            <div class="icons q-mb-sm">
                                <q-icon name="call" class="" />
                            </div>
                            <p class="icon-text">Hide video</p>
                        </div>
                        <div class="flex column justify-center items-center">
                            <div class="icons q-mb-sm">
                                <q-icon name="call" class="" />
                            </div>
                            <p class="icon-text">Full screen</p>
                        </div>
                    </div>
                </div>
                <div class="div-right q-mb-md">
                    <div class="flex justify-between tab shadow q-mb-lg">
                        <q-card class="q-card q-pt-md">
                            <q-tabs v-model="tab" class="text-grey-800 tabs q-px-sm" align="justify" narrow-indicator>
                                <q-tab class="tab-label" name="following" label="Messages" no-caps />
                                <q-tab class="tab-label" name="world-innovation" label="Documents" no-caps />
                                <q-tab class="tab-label" name="blog" label="Prescription" no-caps />
                            </q-tabs>

                        </q-card>
                        <q-tab-panels class="tab-panels" v-model="tab" animated>
                            <q-tab-panel class="tab-panel" name="following">
                                <div class="flex column items-center justify-center q-pt-xl q-pa-md">
                                    <div class="" style="height:527px; overflow:auto">
                                        <q-infinite-scroll @load="onLoad" :offset="250">
                                            <div v-for="(item, index) in items" :key="index" class="caption">
                                                <div class="q-pa-sm q-px-md rounded" style="background:#FEE6B2">
                                                    Load previous messages
                                                </div>
                                                <div class="q-pa-xs q-px-sm q-my-md rounded-lg  text-white" style="background:#A3A8FC">
                                                    02 September
                                                </div>
                                                <div class="q-mb-md" style="width:100%;">
                                                    <div class="q-pa-sm q-px-md rounded-md text-left" style="width:100%;background:#fff;border:2px solid #FEE6B2 ">
                                                        Telemedicine session has started.
                                                    </div>
                                                    <div class="q-px-md q-pt-xs" style="font-size:9px; color:#cccccc">
                                                        11:00 AM</div>
                                                </div>
                                                <div class="search text-left">
                                                    <div class="q-mb-md flex column items-end" style="width:100%;">
                                                        <div class="q-pa-md rounded-msg-right">
                                                            Lorem ipsum dolor sit amet consectetur adipisicing elit. Velit perferendis rerum vitae ipsam deleniti obcaecati similique neque doloribus necessitatibus.
                                                        </div>
                                                        <div class="flex justify-end q-pt-xs" style="font-size:9px; color:#cccccc">
                                                            11:00 AM
                                                            <q-icon v-if="text !== ''" name="check" @click="text = ''" class="cursor-pointer q-pl-xs" style="color:green; font-size:12px" />
                                                        </div>
                                                    </div>
                                                    <div class="q-mb-md flex column items-start" style="width:100%;">
                                                        <div class="q-pa-md rounded-msg-left">
                                                            Lorem ipsum dolor sit amet consectetur adipisicing elit. Velit perferendis rerum vitae ipsam deleniti obcaecati similique neque doloribus necessitatibus.
                                                        </div>
                                                        <div class="flex justify-start q-pt-xs" style="font-size:9px; color:#cccccc">
                                                            11:00 AM
                                                        </div>
                                                    </div>
                                                </div>
                                                <div style="width:100%;">
                                                    <div class="q-pa-sm q-px-md rounded-md text-left" style="width:100%;background:#fff;border:2px solid #FEE6B2 ">
                                                        Telemedicine session has ended.
                                                    </div>
                                                    <div class="q-px-md q-pt-xs" style="font-size:9px; color:#cccccc">
                                                        12:00 AM</div>
                                                </div>
                                            </div>
                                            <template v-slot:loading>
                                                <div class="row justify-center q-my-md">
                                                    <q-spinner-dots color="primary" size="40px" />
                                                </div>
                                            </template>
                                        </q-infinite-scroll>
                                    </div>
                                </div>

                                <div class="bg-white shadow q-pa-md">
                                    <q-input v-model="text" placeholder="Type Something" style="background:#F7F8FF; border-radius:5px; padding-left:10px; font-size:12px; height:40px">
                                        <template v-slot:append>
                                            <q-icon v-if="text !== ''" name="mic" @click="text = ''" class="cursor-pointer" />
                                        </template>
                                    </q-input>
                                </div>
                            </q-tab-panel>

                            <q-tab-panel class="tab-panel" name="world-innovation">
                                <div class="flex column items-center justify-center q-pt-xl q-pa-md">
                                    <div class="q-pa-sm q-px-md rounded" style="background:#FEE6B2">
                                        Load previous messages
                                    </div>
                                    <div class="q-pa-xs q-px-sm q-my-md rounded-lg  text-white" style="background:#A3A8FC">
                                        02 September
                                    </div>
                                    <div class="q-mb-md" style="width:100%;">
                                        <div class="q-pa-sm q-px-md rounded-md text-left" style="width:100%;background:#fff;border:2px solid #FEE6B2 ">
                                            Telemedicine session has started.
                                        </div>
                                        <div class="q-px-md q-pt-xs" style="font-size:9px; color:#cccccc">
                                            11:00 AM</div>
                                    </div>
                                    <div class="search text-left">
                                        <div class="q-mb-md flex column items-end" style="width:100%;">
                                            <div class="q-pa-md rounded-msg-right">
                                                Lorem ipsum dolor sit amet consectetur adipisicing elit. Velit perferendis rerum vitae ipsam deleniti obcaecati similique neque doloribus necessitatibus.
                                            </div>
                                            <div class="flex justify-end q-pt-xs" style="font-size:9px; color:#cccccc">
                                                11:00 AM
                                                <q-icon v-if="text !== ''" name="check" @click="text = ''" class="cursor-pointer q-pl-xs" style="color:green; font-size:12px" />
                                            </div>
                                        </div>
                                        <div class="q-mb-md flex column items-start" style="width:100%;">
                                            <div class="q-pa-md rounded-msg-left">
                                                Lorem ipsum dolor sit amet consectetur adipisicing elit. Velit perferendis rerum vitae ipsam deleniti obcaecati similique neque doloribus necessitatibus.
                                            </div>
                                            <div class="flex justify-start q-pt-xs" style="font-size:9px; color:#cccccc">
                                                11:00 AM
                                            </div>
                                        </div>
                                    </div>
                                    <div style="width:100%;">
                                        <div class="q-pa-sm q-px-md rounded-md text-left" style="width:100%;background:#fff;border:2px solid #FEE6B2 ">
                                            Telemedicine session has ended.
                                        </div>
                                        <div class="q-px-md q-pt-xs" style="font-size:9px; color:#cccccc">
                                            12:00 AM</div>
                                    </div>
                                </div>
                            </q-tab-panel>

                            <q-tab-panel class="tab-panel" rounded name="blog">
                                <div class="flex column items-center justify-center q-pt-xl q-pa-md">
                                    <div class="q-pa-sm q-px-md rounded" style="background:#FEE6B2">
                                        Load previous messages
                                    </div>
                                    <div class="q-pa-xs q-px-sm q-my-md rounded-lg  text-white" style="background:#A3A8FC">
                                        02 September
                                    </div>
                                    <div class="q-mb-md" style="width:100%;">
                                        <div class="q-pa-sm q-px-md rounded-md text-left" style="width:100%;background:#fff;border:2px solid #FEE6B2 ">
                                            Telemedicine session has started.
                                        </div>
                                        <div class="q-px-md q-pt-xs" style="font-size:9px; color:#cccccc">
                                            11:00 AM</div>
                                    </div>
                                    <div class="search text-left">
                                        <div class="q-mb-md flex column items-end" style="width:100%;">
                                            <div class="q-pa-md rounded-msg-right">
                                                Lorem ipsum dolor sit amet consectetur adipisicing elit. Velit perferendis rerum vitae ipsam deleniti obcaecati similique neque doloribus necessitatibus.
                                            </div>
                                            <div class="flex justify-end q-pt-xs" style="font-size:9px; color:#cccccc">
                                                11:00 AM
                                                <q-icon v-if="text !== ''" name="check" @click="text = ''" class="cursor-pointer q-pl-xs" style="color:green; font-size:12px" />
                                            </div>
                                        </div>
                                        <div class="q-mb-md flex column items-start" style="width:100%;">
                                            <div class="q-pa-md rounded-msg-left">
                                                Lorem ipsum dolor sit amet consectetur adipisicing elit. Velit perferendis rerum vitae ipsam deleniti obcaecati similique neque doloribus necessitatibus.
                                            </div>
                                            <div class="flex justify-start q-pt-xs" style="font-size:9px; color:#cccccc">
                                                11:00 AM
                                            </div>
                                        </div>
                                    </div>
                                    <div style="width:100%;">
                                        <div class="q-pa-sm q-px-md rounded-md text-left" style="width:100%;background:#fff;border:2px solid #FEE6B2 ">
                                            Telemedicine session has ended.
                                        </div>
                                        <div class="q-px-md q-pt-xs" style="font-size:9px; color:#cccccc">
                                            12:00 AM</div>
                                    </div>
                                </div>
                            </q-tab-panel>
                        </q-tab-panels>
                    </div>
                </div>
            </div>
            <div class="flex justify-end">
                <p class="q-mx-sm footer-text">Terms of Service</p>
                <p class="q-mx-sm footer-text">Privacy</p>
                <p class="copyright q-mx-sm q-pl-sm footer-text">&copy; 2020 National Coronavirus Hotline</p>
                <img src="https://cdn.quasar.dev/img/avatar2.jpg" class="img-footer" />
            </div>
        </div>
    </div>
</div>
</template>

<script>
export default {
    name: "PageIndex",
    data() {
        return {
            password: "",
            isPwd: true,
            items: [{}, {}, {}, {}, {}, {}, {}],
            email: "",
            search: "",
            tel: "",
            url: "",
            time: "",
            date: "",
            val: true,
            tab: 'mails',
        };
    },
    methods: {
        onItemClick() {
            // console.log('Clicked on an Item')
        },
        onLoad(index, done) {
            setTimeout(() => {
                if (this.items) {
                    this.items.push({}, {}, {}, {}, {}, {}, {})
                    done()
                }
            }, 2000)
        }
    }
};
</script>

<style scoped>
.main {
    overflow-x: hidden;
    background: #6970fb;
    width: 100%;
    color: white;

}

.main-img {
    height: 300px;
    max-height: 300px;
    width: 100%;
}

.flex-break {
    flex: 1 0 100% !important;
    height: 0 !important;
}

.main-div {
    background: #f0f1ff;
    color: #676668;
    border-top-left-radius: 2rem;
    border-bottom-left-radius: 2rem;
}

.q-gutter-md {
    flex-direction: column;
    display: flex;
    justify-content: center;
    align-items: center;
}

.left-img {
    border-radius: 5px;
    width: 34px !important;
    height: 34px !important;
}

.number-text {
    color: #555555;
    font-size: 11px;
    padding-left: 2px;
    margin: 0;
}

h6 {
    margin: 0;
    font-size: 18px;
    font-weight: bold;
}

h4 {
    margin: 0;
    font-weight: bold;
    font-size: 29px;
    color: #555555;
}

.button {
    background: #6970fb;
    color: white;
    border-radius: 0.5rem;
    line-height: 2.515em;
    font-weight: bold;
}

.q-btn .q-icon {
    font-size: 2.5em !important;
    color: #c3c5fe;
}

.font-xs {
    font-size: 10px;
}

.div-left {
    width: 70%;
}

.div-right {
    width: 28.5%;
}

div.img {
    height: 500px;
    border-radius: 1.2rem;
    overflow: hidden;
}

div.img img {
    width: 100%;
    height: 100%;
}

.bottom-icons {
    width: 40%;
    margin: auto;
}

.icons {
    background: white;
    border-radius: 0.4rem;
    height: 40px;
    width: 40px;
    display: flex;
    justify-content: center;
    align-items: center;
    cursor: pointer;
    color: #626262;
    transition: all 0.4s;
}

.icons:hover {
    background: #FF5F56;
    color: white;
    height: 40px;
    width: 40px;
    display: flex;
    justify-content: center;
    align-items: center;
}

.icon-text {
    color: #555555;
    font-size: 11px;
    margin: 0;
}

.copyright {
    border-left: 1px solid #999999;
}

.footer-text {
    font-size: 11px;
    color: #333333;
    margin-bottom: 0;
}

.img-footer {
    height: 17px;
    width: 30px;
    border-radius: 0.2rem;
}

.bottom {
    position: absolute;
    bottom: 0;
    left: 0px;
    width: 107px;
}

.q-card {
    border-radius: 0px !important;
    width: 100%;
}

.tabs.active {
    font-size: 16px;
    border: 2px solid transparent;
    padding: 0 7px;
}

.q-tab__label {}

.tab {
    border-radius: 15px;
    overflow: hidden;
}

.q-field--filled .q-field__control {
    padding: 0 12px;
    background: #F7F8FF !important;
    border-radius: 4px !important;
}

.q-tab-panel {
    padding: 0px;
}

.shadow {
    box-shadow: 0 1px 6px 0 rgba(0, 0, 0, 0.1), 0 1px 2px 0 rgba(0, 0, 0, 0.06);
}

.rounded {
    border-radius: 0.5rem;
    font-size: 13px;
}

.rounded-lg {
    border-radius: 1.5rem;
    font-size: 11px;
}

.rounded-md {
    border-radius: 0.7rem;
    font-size: 12px;
    color: #333333;
}

.rounded-msg-right {
    background: #F0F1FF;
    max-width: 80%;
    text-align: left;
    font-size: 12px;
    border-radius: 0.7rem;
    border-bottom-right-radius: 0;
}

.rounded-msg-left {
    background: #FFF9EC;
    max-width: 80%;
    text-align: left;
    font-size: 12px;
    border-radius: 0.7rem;
    border-bottom-left-radius: 0;
}
</style>
