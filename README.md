# openwrt-sub-web

仅个人修改使用

```bash
cd openwrt
make package/openwrt-sub-web/{clean,prepare} -j"$(nproc)" QUILT=1
cd build_dir/target-*/*sub-web*
quilt push patches/020-views-add-examples-from-ACL4SSR-and-Subconverter.patch
quilt edit src/views/Subconverter.vue

ggvG
dG

quilt refresh
cd ../../../
make package/openwrt-sub-web/update -j"$(nproc)"
make package/openwrt-sub-web/{clean,compile} package/index -j"$(nproc)"

```





## 参考
* [CTCGFW](https://github.com/project-openwrt/openwrt/tree/548764d28283bce9293da157a8c06af06385c0e9/package/ctcgfw/sub-web)
