<template>
  <div>
    <tree :tree-data="tree"></tree>
  </div>
</template>

<script>
import Tree from "./Tree";

export default {
  name: "App",
  components: {
    Tree,
  },
  data() {
    return {
      tree: {
        label: "A cool folder",
        children: [
          {
            label: "A cool sub-folder 1",
            children: [
              {
                label: "A cool sub-sub-folder 1",
                children: [
                  {
                    label: "A cool sub-folder 1",
                    children: [
                      {
                        label: "A cool sub-sub-folder 1",
                        children: [
                          {
                            label: "A cool sub-folder 1",
                            children: [
                              { label: "A cool sub-sub-folder 1" },
                              { label: "A cool sub-sub-folder 2" },
                            ],
                          },
                          { label: "This one is not that cool" },
                        ],
                      },
                      { label: "A cool sub-sub-folder 2" },
                    ],
                  },
                  { label: "This one is not that cool" },
                ],
              },
              { label: "A cool sub-sub-folder 2" },
            ],
          },
          { label: "This one is not that cool" },
        ],
      },
    };
  },
};
</script>

<style lang="scss">
li {
 display: block;
 transition-duration: 0.5s;
}

li:hover {
  cursor: pointer;
}

ul li ul {
  visibility: hidden;
  opacity: 0;
  position: absolute;
  transition: all 0.5s ease;
  margin-top: 1rem;
  left: 0;
  display: none;
}

ul li:hover > ul,
ul li ul:hover {
  visibility: visible;
  opacity: 1;
  display: block;
}

ul li ul li {
  clear: both;
  width: 100%;
}
</style>
