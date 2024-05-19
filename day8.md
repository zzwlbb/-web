## 分页器
1.知道当前是第几页：pageNo
知道分页器一共需要多少数据 total
每一页展示的数据个数 pageSize
一共多少业  totalPage 【计算得来的】
2.计算出连续的页码数

## 放大图
let mask = this.$refs.mask;
let big = this.$refs.big;
let left = e.offsetX - mask.offsetWidth / 2;
let top = e.offsetY - mask.offsetHeight / 2;
//约束范围
if (left <= 0) left = 0;
if (left >= mask.offsetWidth) left = mask.offsetWidth;
if (top <= 0) top = 0;
if (top >= mask.offsetHeight) top = mask.offsetHeight;
mask.style.left = left + "px";
mask.style.top = top + "px";
//big 为是-2 因为大图比小图大两倍而且你鼠标滑动的时候大图的方向相反
big.style.left = -2 * left + "px";
big.style.top = -2 * top + "px";