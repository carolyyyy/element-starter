<template>
<div>
    <el-tabs v-model="activeName" @tab-click="handleClick">
        <el-tab-pane label="gui" name="gui">
            <el-row :gutter="12" >
                <el-col :span="8">
                    <el-button>gui</el-button>
                </el-col>
                <el-col :span="8">
                    <el-card shadow="hover">
                        gui.desktopAgent
                    <el-checkbox v-model="checked_guidesktop"></el-checkbox>
                    </el-card>
                </el-col>
                <el-col :span="8">
                    <el-card shadow="hover">
                    gui.webBrowserAgent
                <el-checkbox v-model="checked_guiweb"></el-checkbox>
                    </el-card>
                </el-col>
                <el-col :span="8">
                    <el-card shadow="hover">
                    gui.jiraUploader
                <el-checkbox v-model="checked_guijira"></el-checkbox>
                    </el-card>
                </el-col>
            </el-row>
        </el-tab-pane>
        <el-tab-pane label="nongui" name="nongui">
            <el-row :gutter="12" >
                <el-col :span="8">
                    <el-card shadow="hover">
                        nongui
                    <el-checkbox v-model="checked_nongui"></el-checkbox>
                    </el-card>
                </el-col>
                <el-col :span="8">
                    <el-card shadow="hover">
                        nongui.elkAgent
                    <el-checkbox v-model="checked_nonguielk"></el-checkbox>
                    </el-card>
                </el-col>
                <el-col :span="8">
                    <el-card shadow="hover">
                    nongui.sshAgent
                <el-checkbox v-model="checked_nonguissh"></el-checkbox>
                    </el-card>
                </el-col>
                <el-col :span="8">
                    <el-card shadow="hover">
                    nongui.webapiAgent
                <el-checkbox v-model="checked_nonguiweb"></el-checkbox>
                    </el-card>
                </el-col>
            </el-row>
        </el-tab-pane>
    </el-tabs>
    
</div>
</template>

<script>
  export default {
    data() {
      return {
        activeName: 'gui',
        checked_gui: false,
        checked_guidesktop: false,
        checked_guiweb: false,
        checked_guijira: false,
        checked_nongui: false,
        checked_nonguielk: false,
        checked_nonguissh: false,
        checked_nonguiweb: false
      };
    },
    methods: {
      handleClick(tab, event) {
        console.log(tab, event);
      }
    }
  };
</script>

<style lang='less' scoped>
.el-button {
    
}

.el-row {
    margin-bottom: 20px;
    &:last-child {
        margin-bottom: 0;
    }
}

.el-col {
    border-radius: 4px;
    line-height: 100px;
}

.bg-purple-dark {
    background: #99a9bf;
}

.bg-purple {
    background: #d3dce6;
}

.bg-purple-light {
    background: #e5e9f2;
}
.grid-content {
    border-radius: 4px;
    min-height: 36px;
}
.row-bg {
    padding: 10px 0;
    background-color: #f9fafc;
}
</style>