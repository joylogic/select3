this is a js control depending on jquery，using this control ，you do not need to create many filter input control any more.
in another word ,this is an all-in-one filter control.

这是一个js控件，使用这个控件后，你不再需要在页面上创建很多过滤条件的输入框，换句话说，这是一个ALL-IN-ONE 的过滤控件。
# select3  usage

1. 包含js 和css

    <script src="../lib/jquery/dist/jquery.js"></script> 
    <script src="../js/jquery.timer.js"></script>  
    <script src="../js/select3.js"></script>
    <link rel="stylesheet" href="../css/select3.css">    


	2.定义一个filter
 <div id="editme" >
     <select id="filter" class="form-control select3 select3-hidden-accessible" multiple="" data-placeholder="请筛选.." style="width: 100%;" tabindex="-1" aria-hidden="true">
         <option format="^[1-9]\d{3}-(0?[1-9]|1[0-2])-(0?[1-9]|[1-2][0-9]|3[0-1])$" selected="selected" value="startTime" >开始时间:2016-1-1</option>
         <option value="endTime">结束时间</option>
         <option value="user">用户</option>
         <option value="desc">备注</option>
       
     </select>
 </div>

 
 3.初始化和获取值

       $("#filter").select3();
  
        //{id,filter,content,selected,format}
        // $.select3InitValue("#filter", [{ "id": "hello", "filter": "hello2", "content": "xx" }])

        //{ id,filter,content }
        var selectValues = $.select3Value("#filter");
