test時に気付いたこと。  
$がついたプロパティは、マウント後にしか生成されない。

``` javascript
import index from './index.vue'
import { mount } from 'vue-test-utils'

index.$options //これはエラーになる
index.options  //これはOK

const wrapper = mount(index)
wrapper.$options // OK!

```