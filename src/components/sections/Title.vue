<script lang="ts" setup>

import { ElIcon } from 'element-plus'
import { Document, Notebook, MagicStick } from '@element-plus/icons-vue'

// 论文 logo
const logo = 'resources/logo_full.png'

// 标题（顶部 logo 已承载 "Micro-Defects Expose Macro-Fakes:" 主题，这里只放副标）
const title = ''

// 标题颜色
const title_color = '#000000'

// 标题副标题
const title_supp = 'Detecting AI-Generated Images via Local Distributional Shifts'

// 副标题颜色
const title_supp_color = '#000000'

// 按钮颜色
const btn_color = '#444444'

// 作者
const authors = [
  {
    name: 'Boxuan Zhang',
    homepage: 'https://zbox1005.github.io/',
    address_flag: '1',
  },
  {
    name: 'Jianing Zhu',
    homepage: 'https://zfancy.github.io/',
    address_flag: '2',
  },
  {
    name: 'Qifan Wang',
    homepage: 'https://wqfcr.github.io/',
    address_flag: '3',
  },
  {
    name: 'Jiang Liu',
    homepage: 'https://joellliu.github.io/',
    address_flag: '4',
  },
  {
    name: 'Ruixiang Tang',
    homepage: 'https://www.ruixiangtang.net/',
    address_flag: '1,*',
  },
]

// 单位
const addresses = [
  {
    address_flag: '1',
    name: 'Rutgers University',
    icon: 'resources/ru_logo.png',
    homepage: 'https://www.rutgers.edu/',
  },
  {
    address_flag: '2',
    name: 'The University of Texas at Austin',
    icon: 'resources/ut_logo.png',
    homepage: 'https://www.utexas.edu/',
  },
  {
    address_flag: '3',
    name: 'Meta AI',
    icon: 'resources/Meta_logo.png',
    homepage: 'https://about.meta.com/',
  },
  {
    address_flag: '4',
    name: 'Advanced Micro Devices',
    icon: 'resources/AMD_logo.png',
    homepage: 'https://www.amd.com/',
  },
]

// 共一/通讯
const con_and_corresponding_author = '* Corresponding Author.'

// 最新消息
const news = ''

// 强调内容
const emphases = []

// 引导按钮
const buttons = [
  // {
  //   disabled: false,
  //   name: 'Paper',
  //   link: 'resources/9781_Micro_Defects_Expose_Macr.pdf',
  //   component: Document,
  // },
  {
    disabled: false,
    name: 'arXiv',
    link: '#',
    iconImg: 'resources/arxiv_logo.svg',
  },
  {
    disabled: false,
    name: 'Code',
    link: '#',
    iconImg: 'resources/github_logo.svg',
  },
  {
    disabled: false,
    name: 'Demo',
    link: 'https://kevinc6986.github.io/mdmf_project/MDMF.html',
    component: MagicStick,
  },
  {
    disabled: false,
    name: 'BibTeX',
    link: '#bibtex',
    component: Notebook,
  },
]

</script>

<template>
  <div>

    <el-row v-if="news" justify="center">
      <el-col :span="24">
        <el-alert :title="news" type="success" />
      </el-col>
    </el-row>

    <el-row v-if="logo" justify="center">
      <el-image :src="logo" class="logo" fit="contain" />
    </el-row>

    <el-row justify="center">
      <el-col :span="22">
        <h1 class="paper-title">
          <span v-if="title" :style="{color: title_color}">{{ title }}</span>
          <br v-if="title && title_supp" />
          <span v-if="title_supp" :style="{color: title_supp_color}">{{ title_supp }}</span>
        </h1>
      </el-col>
    </el-row>

    <el-row justify="center">
      <a v-for="author in authors" :key="author.name" :href="author.homepage">
        <el-button class="title-button" type="primary" text>
          <span class="author">
            {{ author.name }}<sup v-if="author.address_flag" class="name_sup">{{ author.address_flag }}</sup>
          </span>
        </el-button>
      </a>
    </el-row>

    <el-row justify="center">
      <a v-for="address in addresses" :key="address.address_flag" :href="address.homepage">
        <el-button class="title-button" type="primary" text>
          <img v-if="address.icon" :src="address.icon" :alt="address.name" class="address-logo" />
          <span class="address">
            <sup v-if="address.address_flag" class="address_sup">{{ address.address_flag }}</sup>{{ address.name }}
          </span>
        </el-button>
      </a>
    </el-row>

    <el-row justify="center" class="con-cor">
      {{ con_and_corresponding_author }}
    </el-row>

    <el-row justify="center" class="emphasis" v-for="emphasis in emphases" :key="emphasis">
      {{ emphasis }}
    </el-row>

    <el-row justify="center" style="margin-bottom: 20px;">
      <el-col :span="22">
        <el-row justify="center">
          <a v-for="button in buttons" :key="button.name" :href="button.link">
            <el-button class="guidance-button" size="default" :color="btn_color" :disabled="button.disabled" round>
              <el-icon :size="18">
                <component v-if="button.component" :is="button.component" />
                <img v-else-if="button.iconImg" :src="button.iconImg" :alt="button.name" class="btn-icon-img" />
              </el-icon>
              <span class="btn-text">{{ button.name }}</span>
            </el-button>
          </a>
        </el-row>
      </el-col>
    </el-row>

  </div>
</template>

<style scoped>

.paper-title {
  font-family: 'MyFont', Verdana, sans-serif;
  letter-spacing: 1px;
  font-size: 38px;
  line-height: 1.25;
  margin: 8px 0 24px;
  text-align: center;
}

.title-button {
  margin: 8px 3px;
}

.title-button:hover {
  margin: 8px 8px;
}

.guidance-button {
  margin: 8px 5px;
  box-shadow: #d8d8d8 1px 1px 1px 1px;
}

.author {
  font-size: 18px;
  margin-left: 3px;
}

.name_sup {
  color: #606266;
  margin-left: 3px;
}

.address {
  font-size: 17px;
}

.address_sup {
  color: #606266;
  margin-right: 2px;
}

.address-logo {
  height: 36px;
  width: auto;
  max-width: 54px;
  object-fit: contain;
  margin-right: 8px;
  vertical-align: middle;
}

.con-cor {
  font-family: Arial;
  font-size: 14px;
  margin: 18px 0;
  text-align: center;
}

.emphasis {
  color: chocolate;
  font-weight: bold;
  margin: 8px;
  font-size: 22px;
  text-align: center;
}

.btn-text {
  font-size: 18px;
  color: #ffffff;
}

.btn-icon-img {
  width: 100%;
  height: 100%;
  object-fit: contain;
}

.el-alert {
  margin: 10px 0 0;
}

.el-alert:first-child {
  margin: 0;
}

.logo {
  width: 520px;
  max-width: 90%;
  height: auto;
  margin-top: 40px;
}

a:-webkit-any-link {
  text-decoration: none;
}

a:hover {
  color: inherit;
  border-bottom: none;
}

a {
  text-decoration: none;
  color: inherit;
}

</style>
