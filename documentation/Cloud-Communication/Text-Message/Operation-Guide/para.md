## 模板变量规则<br>
  
短信模板=固定文本+变量，或短信模板=固定文本。  
变量为每次发送短信时的可变内容。  

**变量规则**  
每个模板中最多包含20个变量，最多连续2个变量在一起。（变量间包含文字则为不连续变量）  
系统支持以下四种变量格式，请按照要求填写，并选择合适的变量格式及长度。  
    
<table>
     <tr align="center">
        <th width="150">变量格式</th>
        <th width="150">类型</th>
        <th width="150">填写示例</th>
        <th width="400">说明</th>
     </tr>
      <tr>
         <td>${TXT_数字}</td>
         <td>字符，即文本</td>
         <td>${TXT_20}</td>
         <td>“数字”指最大长度，取值范围：1~20，单位：字符数。<br>
1个汉字、中文标点符号、其他非英文字符，或1个英文字母、数字、英文标点符号均按1个字符数计算。<br>  
请就实际业务进行取值，勿取值过大。<br>
注：变量取值不能包含字符“{”和“}”，即大括号。否则，可能导致模板变量解析异常。</td>
      </tr>
      <tr>
         <td>${NUM_数字}</td>
         <td>数字</td>
         <td>${NUM_8}</td>
         <td>“数字”指最大长度，取值范围：1~20，单位：字符数。1个数字按1个字符数计算。<br> 
发送短信时，只能填0到9的数字，不能带其他字符，如“-”。<br> 
请就实际业务进行取值，勿取值过大。</td>
      </tr>
      <tr>
         <td>${DATE}</td>
         <td>日期</td>
         <td>${DATE}</td>
         <td>发送短信时，格式为“YYYY/MM/DD”，例如2017/07/16、2017/7/16、2017/7/1。</td
      </tr>
      <tr>
         <td>${TIME}</td>
         <td>时间</td>
         <td>${TIME}</td>
         <td>发送短信时，有两种格式。<br> 
•	HH:MM，时 : 分，例如14:30。<br> 
•	HH:MM:SS，时 : 分 : 秒，例如14:30:30。  </td>
      </tr>      
</table>  

模板类型特定规范  

除公共规范外，短信的每种模板类型还有以下特定规范：  

<table>
     <tr align="center">
        <th width="150">类别</th>
        <th width="300">变量规范</th>
        <th width="400">内容规范</th>
     </tr>
      <tr>
         <td>验证码短信</td>
         <td>仅支持一个变量，用于填写数字验证码。<br> 
         验证码变量的“最大长度”只能8位及以下。</td>
         <td>国内短信必须含有验证码，注册码，校验码，动态码这4个词其中之一。</td>
      </tr>
      <tr>
         <td>通知短信</td>
         <td>链接不支持使用变量发送，请填写在模板的固定文本中。</td>
         <td>不支持带营销推广的内容。</td>
      </tr>
      <tr>
         <td>推广短信</td>
         <td>不支持变量，模板只能为纯固定文本。</td>
         <td>推广短信除公共规范外，另禁止发送涉及以下信息的短信：培训、招商加盟类、团购会、装修（含建材，家私）、烟、酒、茶、捐款献血、迷信色彩、人工或软件刷单、做任务、虚拟货币、人民币收藏、钱币买卖、沙发翻新、工商代办、代开发票、买卖黑车、非法钓鱼、会展、网站、优惠券类推广、卡类、保险、税票、APP推广、办证、回收、医疗保健、POS机相关、信用卡、交友、猎头、直播及其他违反法律法规的内容。<br>
         只支持发送给有订购关系的会员用户，模板必须体现是发送给会员。<br>
         不支持发送给国际/港澳台地区。</td
      </tr> 
</table>  

注意：  
模板规范可能随运营商规则变化实时调整，最终以模板审核结果为准。  