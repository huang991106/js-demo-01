var div1 = document.createElement('div');

document.body.appendChild(div1);
var lastX
var lastY
div1.className = 'demo';
var e = false
div1.onmousedown = function (a) {
    lastX = a.clientX /*上次鼠标落点水平位置 */
    lastX = a.clientX /*上次鼠标落点垂直位置 */
    e = true

}
document.onmouseup = function () {
    e = false
}
document.onmousemove = function (x) {
    if (e === true) {
        var deltaX = x.clientX - lastX /*这次鼠标水平位置减去之前水平位置得出移动的距离 */
        var deltaY = x.clientY - lastY
        var top = parseInt(div1.style.top) || 0 /*需要将结果转化为整数 */
        var left = parseInt(div1.style.left) || 0
        div1.style.top = top + deltaY + 'px' /*单位是重中之重 */
        div1.style.left = left + deltaX + 'px'
        lastX = x.clientX /*鼠标移动位置之后将水平位置更新，否则会一直是初始的水平位置 */
        lastY = x.clientY
    }

}
/*思路
    1.用JS添加一个div,设置绝对定位
    2.给div绑定事件
    3.取到鼠标在body中的坐标，让div根据鼠标的坐标进行移动
*/
