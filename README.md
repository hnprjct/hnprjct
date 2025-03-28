<!DOCTYPE html>
<html>
<meta charset='UTF-8'/><meta content='width=device-width, initial-scale=1, user-scalable=1, minimum-scale=1, maximum-scale=5' name='viewport'/><meta content='IE=edge' http-equiv='X-UA-Compatible'/><link href="https://feeldreams.github.io/withyou/style.css" rel="stylesheet" type="text/css" />
  
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Shippori+Antique:wght@400;700&display=swap" rel="stylesheet">
  <link href="https://fonts.googleapis.com/css2?family=Dancing+Script&display=swap" rel="stylesheet">

  <script>!function(e,t){"object"==typeof exports&&"undefined"!=typeof module?module.exports=t():"function"==typeof define&&define.amd?define(t):(e=e||self).Sweetalert2=t()}(this,function(){"use strict";const l=Object.freeze({cancel:"cancel",backdrop:"backdrop",close:"close",esc:"esc",timer:"timer"}),t="SweetAlert2:",o=e=>e.charAt(0).toUpperCase()+e.slice(1),a=e=>Array.prototype.slice.call(e),s=e=>{console.warn("".concat(t," ").concat("object"==typeof e?e.join(" "):e))},r=e=>{console.error("".concat(t," ").concat(e))},n=[],i=(e,t)=>{t='"'.concat(e,'" is deprecated and will be removed in the next major release. Please use "').concat(t,'" instead.'),n.includes(t)||(n.push(t),s(t))},c=e=>"function"==typeof e?e():e,u=e=>e&&"function"==typeof e.toPromise,d=e=>u(e)?e.toPromise():Promise.resolve(e),p=e=>e&&Promise.resolve(e)===e,m=e=>e instanceof Element||(e=>"object"==typeof e&&e.jquery)(e);var e=e=>{const t={};for(const n in e)t[e[n]]="swal2-"+e[n];return t};const h=e(["container","shown","height-auto","iosfix","popup","modal","no-backdrop","no-transition","toast","toast-shown","show","hide","close","title","html-container","actions","confirm","deny","cancel","default-outline","footer","icon","icon-content","image","input","file","range","select","radio","checkbox","label","textarea","inputerror","input-label","validation-message","progress-steps","active-progress-step","progress-step","progress-step-line","loader","loading","styled","top","top-start","top-end","top-left","top-right","center","center-start","center-end","center-left","center-right","bottom","bottom-start","bottom-end","bottom-left","bottom-right","grow-row","grow-column","grow-fullscreen","rtl","timer-progress-bar","timer-progress-bar-container","scrollbar-measure","icon-success","icon-warning","icon-info","icon-question","icon-error"]),g=e(["success","warning","info","question","error"]),b=()=>document.body.querySelector(".".concat(h.container)),f=e=>{const t=b();return t?t.querySelector(e):null},y=e=>f(".".concat(e)),v=()=>y(h.popup),w=()=>y(h.icon),C=()=>y(h.title),k=()=>y(h["html-container"]),A=()=>y(h.image),B=()=>y(h["progress-steps"]),x=()=>y(h["validation-message"]),E=()=>f(".".concat(h.actions," .").concat(h.confirm)),P=()=>f(".".concat(h.actions," .").concat(h.deny));const S=()=>f(".".concat(h.loader)),T=()=>f(".".concat(h.actions," .").concat(h.cancel)),L=()=>y(h.actions),O=()=>y(h.footer),j=()=>y(h["timer-progress-bar"]),M=()=>y(h.close),D=()=>{const e=a(v().querySelectorAll('[tabindex]:not([tabindex="-1"]):not([tabindex="0"])')).sort((e,t)=>(e=parseInt(e.getAttribute("tabindex")),(t=parseInt(t.getAttribute("tabindex")))<e?1:e<t?-1:0));var t=a(v().querySelectorAll('\n  a[href],\n  area[href],\n  input:not([disabled]),\n  select:not([disabled]),\n  textarea:not([disabled]),\n  button:not([disabled]),\n  iframe,\n  object,\n  embed,\n  [tabindex="0"],\n  [contenteditable],\n  audio[controls],\n  video[controls],\n  summary\n')).filter(e=>"-1"!==e.getAttribute("tabindex"));return(t=>{const n=[];for(let e=0;e<t.length;e++)-1===n.indexOf(t[e])&&n.push(t[e]);return n})(e.concat(t)).filter(e=>G(e))},I=()=>!H()&&!document.body.classList.contains(h["no-backdrop"]),H=()=>document.body.classList.contains(h["toast-shown"]);const q={previousBodyPadding:null},V=(t,e)=>{if(t.textContent="",e){const n=new DOMParser,o=n.parseFromString(e,"text/html");a(o.querySelector("head").childNodes).forEach(e=>{t.appendChild(e)}),a(o.querySelector("body").childNodes).forEach(e=>{t.appendChild(e)})}},N=(t,e)=>{if(!e)return!1;var n=e.split(/\s+/);for(let e=0;e<n.length;e++)if(!t.classList.contains(n[e]))return!1;return!0},U=(e,t,n)=>{var o,i;if(o=e,i=t,a(o.classList).forEach(e=>{Object.values(h).includes(e)||Object.values(g).includes(e)||Object.values(i.showClass).includes(e)||o.classList.remove(e)}),t.customClass&&t.customClass[n]){if("string"!=typeof t.customClass[n]&&!t.customClass[n].forEach)return s("Invalid type of customClass.".concat(n,'! Expected string or iterable object, got "').concat(typeof t.customClass[n],'"'));W(e,t.customClass[n])}},F=(e,t)=>{if(!t)return null;switch(t){case"select":case"textarea":case"file":return K(e,h[t]);case"checkbox":return e.querySelector(".".concat(h.checkbox," input"));case"radio":return e.querySelector(".".concat(h.radio," input:checked"))||e.querySelector(".".concat(h.radio," input:first-child"));case"range":return e.querySelector(".".concat(h.range," input"));default:return K(e,h.input)}},R=e=>{var t;e.focus(),"file"!==e.type&&(t=e.value,e.value="",e.value=t)},z=(e,t,n)=>{e&&t&&(t="string"==typeof t?t.split(/\s+/).filter(Boolean):t).forEach(t=>{e.forEach?e.forEach(e=>{n?e.classList.add(t):e.classList.remove(t)}):n?e.classList.add(t):e.classList.remove(t)})},W=(e,t)=>{z(e,t,!0)},_=(e,t)=>{z(e,t,!1)},K=(t,n)=>{for(let e=0;e<t.childNodes.length;e++)if(N(t.childNodes[e],n))return t.childNodes[e]},Y=(e,t,n)=>{(n=n==="".concat(parseInt(n))?parseInt(n):n)||0===parseInt(n)?e.style[t]="number"==typeof n?"".concat(n,"px"):n:e.style.removeProperty(t)},Z=(e,t="flex")=>{e.style.display=t},J=e=>{e.style.display="none"},X=(e,t,n,o)=>{const i=e.querySelector(t);i&&(i.style[n]=o)},$=(e,t,n)=>{t?Z(e,n):J(e)},G=e=>!(!e||!(e.offsetWidth||e.offsetHeight||e.getClientRects().length)),Q=()=>!G(E())&&!G(P())&&!G(T()),ee=e=>!!(e.scrollHeight>e.clientHeight),te=e=>{const t=window.getComputedStyle(e);var n=parseFloat(t.getPropertyValue("animation-duration")||"0"),e=parseFloat(t.getPropertyValue("transition-duration")||"0");return 0<n||0<e},ne=(e,t=!1)=>{const n=j();G(n)&&(t&&(n.style.transition="none",n.style.width="100%"),setTimeout(()=>{n.style.transition="width ".concat(e/1e3,"s linear"),n.style.width="0%"},10))},oe=()=>"undefined"==typeof window||"undefined"==typeof document,ie='\n <div aria-labelledby="'.concat(h.title,'" aria-describedby="').concat(h["html-container"],'" class="').concat(h.popup,'" tabindex="-1">\n   <button type="button" class="').concat(h.close,'"></button>\n   <ul class="').concat(h["progress-steps"],'"></ul>\n   <div class="').concat(h.icon,'"></div>\n   <img class="').concat(h.image,'" />\n   <h2 class="').concat(h.title,'" id="').concat(h.title,'"></h2>\n   <div class="').concat(h["html-container"],'" id="').concat(h["html-container"],'"></div>\n   <input class="').concat(h.input,'" />\n   <input type="file" class="').concat(h.file,'" />\n   <div class="').concat(h.range,'">\n     <input type="range" />\n     <output></output>\n   </div>\n   <select class="').concat(h.select,'"></select>\n   <div class="').concat(h.radio,'"></div>\n   <label for="').concat(h.checkbox,'" class="').concat(h.checkbox,'">\n     <input type="checkbox" />\n     <span class="').concat(h.label,'"></span>\n   </label>\n   <textarea class="').concat(h.textarea,'"></textarea>\n   <div class="').concat(h["validation-message"],'" id="').concat(h["validation-message"],'"></div>\n   <div class="').concat(h.actions,'">\n     <div class="').concat(h.loader,'"></div>\n     <button type="button" class="').concat(h.confirm,'"></button>\n     <button type="button" class="').concat(h.deny,'"></button>\n     <button type="button" class="').concat(h.cancel,'"></button>\n   </div>\n   <div class="').concat(h.footer,'"></div>\n   <div class="').concat(h["timer-progress-bar-container"],'">\n     <div class="').concat(h["timer-progress-bar"],'"></div>\n   </div>\n </div>\n').replace(/(^|\n)\s*/g,""),ae=()=>{cn.isVisible()&&cn.resetValidationMessage()},se=e=>{var t=(()=>{const e=b();return!!e&&(e.remove(),_([document.documentElement,document.body],[h["no-backdrop"],h["toast-shown"],h["has-column"]]),!0)})();if(oe())r("SweetAlert2 requires document to initialize");else{const n=document.createElement("div");n.className=h.container,t&&W(n,h["no-transition"]),V(n,ie);const o="string"==typeof(t=e.target)?document.querySelector(t):t;o.appendChild(n),(e=>{const t=v();t.setAttribute("role",e.toast?"alert":"dialog"),t.setAttribute("aria-live",e.toast?"polite":"assertive"),e.toast||t.setAttribute("aria-modal","true")})(e),e=o,"rtl"===window.getComputedStyle(e).direction&&W(b(),h.rtl),(()=>{const e=v(),t=K(e,h.input),n=K(e,h.file),o=e.querySelector(".".concat(h.range," input")),i=e.querySelector(".".concat(h.range," output")),a=K(e,h.select),s=e.querySelector(".".concat(h.checkbox," input")),r=K(e,h.textarea);t.oninput=ae,n.onchange=ae,a.onchange=ae,s.onchange=ae,r.oninput=ae,o.oninput=()=>{ae(),i.value=o.value},o.onchange=()=>{ae(),o.nextSibling.value=o.value}})()}},re=(e,t)=>{e instanceof HTMLElement?t.appendChild(e):"object"==typeof e?ce(e,t):e&&V(t,e)},ce=(e,t)=>{e.jquery?le(t,e):V(t,e.toString())},le=(t,n)=>{if(t.textContent="",0 in n)for(let e=0;e in n;e++)t.appendChild(n[e].cloneNode(!0));else t.appendChild(n.cloneNode(!0))},ue=(()=>{if(oe())return!1;var e=document.createElement("div"),t={WebkitAnimation:"webkitAnimationEnd",OAnimation:"oAnimationEnd oanimationend",animation:"animationend"};for(const n in t)if(Object.prototype.hasOwnProperty.call(t,n)&&void 0!==e.style[n])return t[n];return!1})(),de=(e,t)=>{const n=L();var o=S(),i=E(),a=P(),s=T();t.showConfirmButton||t.showDenyButton||t.showCancelButton||J(n),U(n,t,"actions"),pe(i,"confirm",t),pe(a,"deny",t),pe(s,"cancel",t),function(e,t,n,o){if(!o.buttonsStyling)return _([e,t,n],h.styled);W([e,t,n],h.styled),o.confirmButtonColor&&(e.style.backgroundColor=o.confirmButtonColor,W(e,h["default-outline"]));o.denyButtonColor&&(t.style.backgroundColor=o.denyButtonColor,W(t,h["default-outline"]));o.cancelButtonColor&&(n.style.backgroundColor=o.cancelButtonColor,W(n,h["default-outline"]))}(i,a,s,t),t.reverseButtons&&(n.insertBefore(s,o),n.insertBefore(a,o),n.insertBefore(i,o)),V(o,t.loaderHtml),U(o,t,"loader")};function pe(e,t,n){$(e,n["show".concat(o(t),"Button")],"inline-block"),V(e,n["".concat(t,"ButtonText")]),e.setAttribute("aria-label",n["".concat(t,"ButtonAriaLabel")]),e.className=h[t],U(e,n,"".concat(t,"Button")),W(e,n["".concat(t,"ButtonClass")])}const me=(e,t)=>{var n,o,i=b();i&&(o=i,"string"==typeof(n=t.backdrop)?o.style.background=n:n||W([document.documentElement,document.body],h["no-backdrop"]),o=i,(n=t.position)in h?W(o,h[n]):(s('The "position" parameter is not valid, defaulting to "center"'),W(o,h.center)),n=i,!(o=t.grow)||"string"!=typeof o||(o="grow-".concat(o))in h&&W(n,h[o]),U(i,t,"container"))};var he={promise:new WeakMap,innerParams:new WeakMap,domCache:new WeakMap};const ge=["input","file","range","select","radio","checkbox","textarea"],be=e=>{if(!ke[e.input])return r('Unexpected type of input! Expected "text", "email", "password", "number", "tel", "select", "radio", "checkbox", "textarea", "file" or "url", got "'.concat(e.input,'"'));var t=Ce(e.input);const n=ke[e.input](t,e);Z(n),setTimeout(()=>{R(n)})},fe=(e,t)=>{const n=F(v(),e);if(n){(t=>{for(let e=0;e<t.attributes.length;e++){var n=t.attributes[e].name;["type","value","style"].includes(n)||t.removeAttribute(n)}})(n);for(const o in t)n.setAttribute(o,t[o])}},ye=e=>{var t=Ce(e.input);e.customClass&&W(t,e.customClass.input)},ve=(e,t)=>{e.placeholder&&!t.inputPlaceholder||(e.placeholder=t.inputPlaceholder)},we=(e,t,n)=>{if(n.inputLabel){e.id=h.input;const i=document.createElement("label");var o=h["input-label"];i.setAttribute("for",e.id),i.className=o,W(i,n.customClass.inputLabel),i.innerText=n.inputLabel,t.insertAdjacentElement("beforebegin",i)}},Ce=e=>{e=h[e]||h.input;return K(v(),e)},ke={};ke.text=ke.email=ke.password=ke.number=ke.tel=ke.url=(e,t)=>("string"==typeof t.inputValue||"number"==typeof t.inputValue?e.value=t.inputValue:p(t.inputValue)||s('Unexpected type of inputValue! Expected "string", "number" or "Promise", got "'.concat(typeof t.inputValue,'"')),we(e,e,t),ve(e,t),e.type=t.input,e),ke.file=(e,t)=>(we(e,e,t),ve(e,t),e),ke.range=(e,t)=>{const n=e.querySelector("input"),o=e.querySelector("output");return n.value=t.inputValue,n.type=t.input,o.value=t.inputValue,we(n,e,t),e},ke.select=(e,t)=>{if(e.textContent="",t.inputPlaceholder){const n=document.createElement("option");V(n,t.inputPlaceholder),n.value="",n.disabled=!0,n.selected=!0,e.appendChild(n)}return we(e,e,t),e},ke.radio=e=>(e.textContent="",e),ke.checkbox=(e,t)=>{const n=F(v(),"checkbox");n.value=1,n.id=h.checkbox,n.checked=Boolean(t.inputValue);var o=e.querySelector("span");return V(o,t.inputPlaceholder),e},ke.textarea=(n,e)=>{n.value=e.inputValue,ve(n,e),we(n,n,e);return setTimeout(()=>{if("MutationObserver"in window){const t=parseInt(window.getComputedStyle(v()).width);new MutationObserver(()=>{var e,e=n.offsetWidth+(e=n,parseInt(window.getComputedStyle(e).marginLeft)+parseInt(window.getComputedStyle(e).marginRight));e>t?v().style.width="".concat(e,"px"):v().style.width=null}).observe(n,{attributes:!0,attributeFilter:["style"]})}}),n};const Ae=(e,t)=>{const n=k();U(n,t,"htmlContainer"),t.html?(re(t.html,n),Z(n,"block")):t.text?(n.textContent=t.text,Z(n,"block")):J(n),((e,o)=>{const i=v();e=he.innerParams.get(e);const a=!e||o.input!==e.input;ge.forEach(e=>{var t=h[e];const n=K(i,t);fe(e,o.inputAttributes),n.className=t,a&&J(n)}),o.input&&(a&&be(o),ye(o))})(e,t)},Be=(e,t)=>{for(const n in g)t.icon!==n&&_(e,g[n]);W(e,g[t.icon]),Pe(e,t),xe(),U(e,t,"icon")},xe=()=>{const e=v();var t=window.getComputedStyle(e).getPropertyValue("background-color");const n=e.querySelectorAll("[class^=swal2-success-circular-line], .swal2-success-fix");for(let e=0;e<n.length;e++)n[e].style.backgroundColor=t},Ee=(e,t)=>{var n;e.textContent="",t.iconHtml?V(e,Se(t.iconHtml)):"success"===t.icon?V(e,'\n      <div class="swal2-success-circular-line-left"></div>\n      <span class="swal2-success-line-tip"></span> <span class="swal2-success-line-long"></span>\n      <div class="swal2-success-ring"></div> <div class="swal2-success-fix"></div>\n      <div class="swal2-success-circular-line-right"></div>\n    '):"error"===t.icon?V(e,'\n      <span class="swal2-x-mark">\n        <span class="swal2-x-mark-line-left"></span>\n        <span class="swal2-x-mark-line-right"></span>\n      </span>\n    '):(n={question:"?",warning:"!",info:"i"},V(e,Se(n[t.icon])))},Pe=(e,t)=>{if(t.iconColor){e.style.color=t.iconColor,e.style.borderColor=t.iconColor;for(const n of[".swal2-success-line-tip",".swal2-success-line-long",".swal2-x-mark-line-left",".swal2-x-mark-line-right"])X(e,n,"backgroundColor",t.iconColor);X(e,".swal2-success-ring","borderColor",t.iconColor)}},Se=e=>'<div class="'.concat(h["icon-content"],'">').concat(e,"</div>"),Te=(e,o)=>{const i=B();if(!o.progressSteps||0===o.progressSteps.length)return J(i);Z(i),i.textContent="",o.currentProgressStep>=o.progressSteps.length&&s("Invalid currentProgressStep parameter, it should be less than progressSteps.length (currentProgressStep like JS arrays starts from 0)"),o.progressSteps.forEach((e,t)=>{var n,e=(n=e,e=document.createElement("li"),W(e,h["progress-step"]),V(e,n),e);i.appendChild(e),t===o.currentProgressStep&&W(e,h["active-progress-step"]),t!==o.progressSteps.length-1&&(t=(e=>{const t=document.createElement("li");return W(t,h["progress-step-line"]),e.progressStepsDistance&&(t.style.width=e.progressStepsDistance),t})(o),i.appendChild(t))})},Le=(e,t)=>{e.className="".concat(h.popup," ").concat(G(e)?t.showClass.popup:""),t.toast?(W([document.documentElement,document.body],h["toast-shown"]),W(e,h.toast)):W(e,h.modal),U(e,t,"popup"),"string"==typeof t.customClass&&W(e,t.customClass),t.icon&&W(e,h["icon-".concat(t.icon)])},Oe=(e,t)=>{var n,o,i;(e=>{var t=b();const n=v();e.toast?(Y(t,"width",e.width),n.style.width="100%",n.insertBefore(S(),w())):Y(n,"width",e.width),Y(n,"padding",e.padding),e.background&&(n.style.background=e.background),J(x()),Le(n,e)})(t),me(0,t),Te(0,t),i=e,n=t,o=he.innerParams.get(i),i=w(),o&&n.icon===o.icon?(Ee(i,n),Be(i,n)):n.icon||n.iconHtml?n.icon&&-1===Object.keys(g).indexOf(n.icon)?(r('Unknown icon! Expected "success", "error", "warning", "info" or "question", got "'.concat(n.icon,'"')),J(i)):(Z(i),Ee(i,n),Be(i,n),W(i,n.showClass.icon)):J(i),(e=>{const t=A();if(!e.imageUrl)return J(t);Z(t,""),t.setAttribute("src",e.imageUrl),t.setAttribute("alt",e.imageAlt),Y(t,"width",e.imageWidth),Y(t,"height",e.imageHeight),t.className=h.image,U(t,e,"image")})(t),(e=>{const t=C();$(t,e.title||e.titleText,"block"),e.title&&re(e.title,t),e.titleText&&(t.innerText=e.titleText),U(t,e,"title")})(t),(e=>{const t=M();V(t,e.closeButtonHtml),U(t,e,"closeButton"),$(t,e.showCloseButton),t.setAttribute("aria-label",e.closeButtonAriaLabel)})(t),Ae(e,t),de(0,t),i=t,e=O(),$(e,i.footer),i.footer&&re(i.footer,e),U(e,i,"footer"),"function"==typeof t.didRender&&t.didRender(v())};const je=()=>E()&&E().click();const Me=e=>{let t=v();t||cn.fire(),t=v();var n=S();H()?J(w()):De(t,e),Z(n),t.setAttribute("data-loading",!0),t.setAttribute("aria-busy",!0),t.focus()},De=(e,t)=>{var n=L();const o=S();!t&&G(E())&&(t=E()),Z(n),t&&(J(t),o.setAttribute("data-button-to-replace",t.className)),o.parentNode.insertBefore(o,t),W([e,n],h.loading)},Ie={},He=o=>new Promise(e=>{if(!o)return e();var t=window.scrollX,n=window.scrollY;Ie.restoreFocusTimeout=setTimeout(()=>{Ie.previousActiveElement&&Ie.previousActiveElement.focus?(Ie.previousActiveElement.focus(),Ie.previousActiveElement=null):document.body&&document.body.focus(),e()},100),window.scrollTo(t,n)});const qe=()=>{if(Ie.timeout)return(()=>{const e=j();var t=parseInt(window.getComputedStyle(e).width);e.style.removeProperty("transition"),e.style.width="100%";var n=parseInt(window.getComputedStyle(e).width),n=parseInt(t/n*100);e.style.removeProperty("transition"),e.style.width="".concat(n,"%")})(),Ie.timeout.stop()},Ve=()=>{if(Ie.timeout){var e=Ie.timeout.start();return ne(e),e}};let Ne=!1;const Ue={};const Fe=t=>{for(let e=t.target;e&&e!==document;e=e.parentNode)for(const o in Ue){var n=e.getAttribute(o);if(n)return void Ue[o].fire({template:n})}},Re={title:"",titleText:"",text:"",html:"",footer:"",icon:void 0,iconColor:void 0,iconHtml:void 0,template:void 0,toast:!1,showClass:{popup:"swal2-show",backdrop:"swal2-backdrop-show",icon:"swal2-icon-show"},hideClass:{popup:"swal2-hide",backdrop:"swal2-backdrop-hide",icon:"swal2-icon-hide"},customClass:{},target:"body",backdrop:!0,heightAuto:!0,allowOutsideClick:!0,allowEscapeKey:!0,allowEnterKey:!0,stopKeydownPropagation:!0,keydownListenerCapture:!1,showConfirmButton:!0,showDenyButton:!1,showCancelButton:!1,preConfirm:void 0,preDeny:void 0,confirmButtonText:"OK",confirmButtonAriaLabel:"",confirmButtonColor:void 0,denyButtonText:"No",denyButtonAriaLabel:"",denyButtonColor:void 0,cancelButtonText:"Cancel",cancelButtonAriaLabel:"",cancelButtonColor:void 0,buttonsStyling:!0,reverseButtons:!1,focusConfirm:!0,focusDeny:!1,focusCancel:!1,returnFocus:!0,showCloseButton:!1,closeButtonHtml:"&times;",closeButtonAriaLabel:"Close this dialog",loaderHtml:"",showLoaderOnConfirm:!1,showLoaderOnDeny:!1,imageUrl:void 0,imageWidth:void 0,imageHeight:void 0,imageAlt:"",timer:void 0,timerProgressBar:!1,width:void 0,padding:void 0,background:void 0,input:void 0,inputPlaceholder:"",inputLabel:"",inputValue:"",inputOptions:{},inputAutoTrim:!0,inputAttributes:{},inputValidator:void 0,returnInputValueOnDeny:!1,validationMessage:void 0,grow:!1,position:"center",progressSteps:[],currentProgressStep:void 0,progressStepsDistance:void 0,willOpen:void 0,didOpen:void 0,didRender:void 0,willClose:void 0,didClose:void 0,didDestroy:void 0,scrollbarPadding:!0},ze=["allowEscapeKey","allowOutsideClick","background","buttonsStyling","cancelButtonAriaLabel","cancelButtonColor","cancelButtonText","closeButtonAriaLabel","closeButtonHtml","confirmButtonAriaLabel","confirmButtonColor","confirmButtonText","currentProgressStep","customClass","denyButtonAriaLabel","denyButtonColor","denyButtonText","didClose","didDestroy","footer","hideClass","html","icon","iconColor","iconHtml","imageAlt","imageHeight","imageUrl","imageWidth","progressSteps","returnFocus","reverseButtons","showCancelButton","showCloseButton","showConfirmButton","showDenyButton","text","title","titleText","willClose"],We={},_e=["allowOutsideClick","allowEnterKey","backdrop","focusConfirm","focusDeny",</script>
  <script>// TypeIt by Alex MacArthur - https://typeitjs.com
!function(e,t){"object"==typeof exports&&"undefined"!=typeof module?module.exports=t():"function"==typeof define&&define.amd?define(t):(e="undefined"!=typeof globalThis?globalThis:e||self).TypeIt=t()}(this,(function(){"use strict";const e=e=>Array.isArray(e),t=t=>e(t)?t:[t];const n=e=>Array.from(e),r=e=>document.createTextNode(e);let i=e=>([...e.childNodes].forEach((e=>{if(e.nodeValue)return[...e.nodeValue].forEach((t=>{e.parentNode.insertBefore(r(t),e)})),void e.remove();i(e)})),e);const a=e=>{let t=document.implementation.createHTMLDocument();return t.body.innerHTML=e,i(t.body)},o="ti-cursor",s={started:!1,completed:!1,frozen:!1,destroyed:!1},l={breakLines:!0,cursor:{autoPause:!0,autoPauseDelay:500,animation:{frames:[0,0,1].map((e=>({opacity:e}))),options:{iterations:1/0,easing:"steps(2, start)",fill:"forwards"}}},cursorChar:"|",cursorSpeed:1e3,deleteSpeed:null,html:!0,lifeLike:!0,loop:!1,loopDelay:750,nextStringDelay:750,speed:100,startDelay:250,startDelete:!1,strings:[],waitUntilVisible:!1,beforeString:()=>{},afterString:()=>{},beforeStep:()=>{},afterStep:()=>{},afterComplete:()=>{}};function u(e,t=!1,n=!1){let r,i=e.querySelector(".ti-cursor"),a=document.createTreeWalker(e,NodeFilter.SHOW_ALL,{acceptNode:e=>{if(i&&n){if(e.classList?.contains(o))return NodeFilter.FILTER_ACCEPT;if(i.contains(e))return NodeFilter.FILTER_REJECT}return e.classList?.contains(o)?NodeFilter.FILTER_REJECT:NodeFilter.FILTER_ACCEPT}}),s=[];for(;r=a.nextNode();)r.originalParent||(r.originalParent=r.parentNode),s.push(r);return t?s.reverse():s}function c(e,t=!0){return t?u(a(e)):n(e).map(r)}const d=e=>document.createElement(e),f=(e,t="")=>{let n=d("style");n.id=t,n.appendChild(r(e)),document.head.appendChild(n)},h=t=>(e(t)||(t=[t/2,t/2]),t),y=(e,t)=>Math.abs(Math.random()*(e+t-(e-t))+(e-t));let p=e=>e/2;const m=e=>"value"in e;let g=e=>"function"==typeof e?e():e;const b=e=>Number.isInteger(e);let w=(e,t=document,n=!1)=>t["querySelector"+(n?"All":"")](e);const T=(e,t)=>Object.assign({},e,t);let v={"font-family":"","font-weight":"","font-size":"","font-style":"","line-height":"",color:"",transform:"translateX(-.125em)"};const E=(e,t)=>new Array(t).fill(e),P=({queueItems:e,selector:t,cursorPosition:n,to:r})=>{if(b(t))return-1*t;let i=new RegExp("END","i").test(r),a=t?[...e].reverse().findIndex((({char:e})=>{let n=e.parentElement,r=n.matches(t);return!(!i||!r)||r&&n.firstChild.isSameNode(e)})):-1;return a<0&&(a=i?0:e.length-1),a-n+(i?0:1)};let S=e=>new Promise((t=>{requestAnimationFrame((async()=>{t(await e())}))})),N=e=>e?.getAnimations().find((t=>t.id===e.dataset.tiAnimationId)),L=({cursor:e,frames:t,options:n})=>{let r=e.animate(t,n);return r.pause(),r.id=e.dataset.tiAnimationId,S((()=>{S((()=>{r.play()}))})),r},C=e=>e.func?.call(null),D=async({index:e,queueItems:t,wait:n,cursor:r,cursorOptions:i})=>{let a=t[e][1],o=[],s=e,l=a,u=()=>l&&!l.delay,c=a.shouldPauseCursor()&&i.autoPause;for(;u();)o.push(l),u()&&s++,l=t[s]?t[s][1]:null;if(o.length)return await S((async()=>{for(let e of o)await C(e)})),s-1;let d,f=N(r);return f&&(d={...f.effect.getComputedTiming(),delay:c?i.autoPauseDelay:0}),await n((async()=>{f&&c&&f.cancel(),await S((()=>{C(a)}))}),a.delay),await(({cursor:e,options:t,cursorOptions:n})=>{if(!e||!n)return;let r,i=N(e);i&&(t.delay=i.effect.getComputedTiming().delay,r=i.currentTime,i.cancel());let a=L({cursor:e,frames:n.animation.frames,options:t});return r&&(a.currentTime=r),a})({cursor:r,options:d,cursorOptions:i}),e};return function(e,r={}){let S=async(e,t,n=!1)=>{X.frozen&&await new Promise((e=>{this.unfreeze=()=>{X.frozen=!1,e()}})),n||await G.beforeStep(this),await((e,t,n)=>new Promise((r=>{n.push(setTimeout((async()=>{await e(),r()}),t||0))})))(e,t,J),n||await G.afterStep(this)},N=(e,t)=>D({index:e,queueItems:t,wait:S,cursor:ee,cursorOptions:G.cursor}),C=e=>((e,t)=>{if(!e)return;let n=e.parentNode;(n.childNodes.length>1||n.isSameNode(t)?e:n).remove()})(e,V),I=()=>m(V),M=(e=0)=>function(e){let{speed:t,deleteSpeed:n,lifeLike:r}=e;return n=null!==n?n:t/3,r?[y(t,p(t)),y(n,p(n))]:[t,n]}(G)[e],x=()=>(e=>m(e)?n(e.value):u(e,!0).filter((e=>!(e.childNodes.length>0))))(V),A=(e,t)=>(Y.add(e),((e={})=>{let t=e.delay;t&&Y.add({delay:t})})(t),this),H=()=>W??U,O=(e={})=>[{func:()=>B(e)},{func:()=>B(G)}],F=e=>{let t=G.nextStringDelay;Y.add([{delay:t[0]},...e,{delay:t[1]}])},k=async()=>{if(!I()&&ee&&V.appendChild(ee),Z){((e,t)=>{let n=`[data-typeit-id='${e}'] .ti-cursor`,r=getComputedStyle(t),i=Object.entries(v).reduce(((e,[t,n])=>`${e} ${t}: var(--ti-cursor-${t}, ${n||r[t]});`),"");f(`${n} { display: inline-block; width: 0; ${i} }`,e)})(K,V),ee.dataset.tiAnimationId=K;let{animation:e}=G.cursor,{frames:t,options:n}=e;L({frames:t,cursor:ee,options:{duration:G.cursorSpeed,...n}})}},R=()=>{let e=G.strings.filter((e=>!!e));e.forEach(((t,n)=>{if(this.type(t),n+1===e.length)return;let r=G.breakLines?[{func:()=>z(d("BR")),typeable:!0}]:E({func:j,delay:M(1)},Y.getTypeable().length);F(r)}))},$=async(e=!0)=>{X.started=!0;let t=t=>{Y.done(t,!e)};try{let n=[...Y.getQueue()];for(let e=0;e<n.length;e++){let[r,i]=n[e];if(!i.done){if(!i.deletable||i.deletable&&x().length){let r=await N(e,n);Array(r-e).fill(e+1).map(((e,t)=>e+t)).forEach((e=>{let[r]=n[e];t(r)})),e=r}t(r)}}if(!e)return this;if(X.completed=!0,await G.afterComplete(this),!G.loop)throw"";let r=G.loopDelay;S((async()=>{await(async e=>{let t=H();t&&await q({value:t});let n=x().map((e=>[Symbol(),{func:j,delay:M(1),deletable:!0,shouldPauseCursor:()=>!0}]));for(let r=0;r<n.length;r++)await N(r,n);Y.reset(),Y.set(0,{delay:e})})(r[0]),$()}),r[1])}catch(n){}return this},q=async e=>{var t,n,r;t=e,n=U,r=x(),U=Math.min(Math.max(n+t,0),r.length),((e,t,n)=>{let r=t[n-1],i=w(".ti-cursor",e);(e=r?.parentNode||e).insertBefore(i,r||null)})(V,x(),U)},z=e=>((e,t)=>{if(m(e))return void(e.value=`${e.value}${t.textContent}`);t.innerHTML="";let n=(r=t.originalParent,/body/i.test(r?.tagName)?e:t.originalParent||e);var r;n.insertBefore(t,w(".ti-cursor",n)||null)})(V,e),B=async e=>G=T(G,e),_=async()=>{I()?V.value="":x().forEach(C)},j=()=>{let e=x();e.length&&(I()?V.value=V.value.slice(0,-1):C(e[U]))};this.break=function(e){return A({func:()=>z(d("BR")),typeable:!0},e)},this.delete=function(e=null,t={}){e=g(e);let n=O(t),r=e,{instant:i,to:a}=t,o=Y.getTypeable(),s=null===r?o.length:b(r)?r:P({queueItems:o,selector:r,cursorPosition:H(),to:a});return A([n[0],...E({func:j,delay:i?0:M(1),deletable:!0},s),n[1]],t)},this.empty=function(e={}){return A({func:_},e)},this.exec=function(e,t={}){let n=O(t);return A([n[0],{func:()=>e(this)},n[1]],t)},this.move=function(e,t={}){e=g(e);let n=O(t),{instant:r,to:i}=t,a=P({queueItems:Y.getTypeable(),selector:null===e?"":e,to:i,cursorPosition:H()}),o=a<0?-1:1;return W=H()+a,A([n[0],...E({func:()=>q(o),delay:r?0:M(),cursorable:!0},Math.abs(a)),n[1]],t)},this.options=function(e,t={}){return e=g(e),B(e),A({},t)},this.pause=function(e,t={}){return A({delay:g(e)},t)},this.type=function(e,t={}){e=g(e);let{instant:n}=t,r=O(t),i=c(e,G.html).map((e=>{return{func:()=>z(e),char:e,delay:n||(t=e,/<(.+)>(.*?)<\/(.+)>/.test(t.outerHTML))?0:M(),typeable:e.nodeType===Node.TEXT_NODE};var t})),a=[r[0],{func:async()=>await G.beforeString(e,this)},...i,{func:async()=>await G.afterString(e,this)},r[1]];return A(a,t)},this.is=function(e){return X[e]},this.destroy=function(e=!0){J.forEach(clearTimeout),J=[],g(e)&&ee&&C(ee),X.destroyed=!0},this.freeze=function(){X.frozen=!0},this.unfreeze=()=>{},this.reset=function(e){!this.is("destroyed")&&this.destroy(),e?(Y.wipe(),e(this)):Y.reset(),U=0;for(let t in X)X[t]=!1;return V[I()?"value":"innerHTML"]="",this},this.go=function(){return X.started?this:(k(),G.waitUntilVisible?(((e,t)=>{new IntersectionObserver(((n,r)=>{n.forEach((n=>{n.isIntersecting&&(t(),r.unobserve(e))}))}),{threshold:1}).observe(e)})(V,$.bind(this)),this):($(),this))},this.flush=function(e=(()=>{})){return k(),$(!1).then(e),this},this.getQueue=()=>Y,this.getOptions=()=>G,this.updateOptions=e=>B(e),this.getElement=()=>V;let V="string"==typeof(Q=e)?w(Q):Q;var Q;let J=[],U=0,W=null,X=T({},s);r.cursor=(e=>{if("object"==typeof e){let t={},{frames:n,options:r}=l.cursor.animation;return t.animation=e.animation||{},t.animation.frames=e.animation?.frames||n,t.animation.options=T(r,e.animation?.options||{}),t.autoPause=e.autoPause??l.cursor.autoPause,t.autoPauseDelay=e.autoPauseDelay||l.cursor.autoPauseDelay,t}return!0===e?l.cursor:e})(r.cursor??l.cursor);let G=T(l,r);G=T(G,{html:!I()&&G.html,nextStringDelay:h(G.nextStringDelay),loopDelay:h(G.loopDelay)});let K=Math.random().toString().substring(2,9),Y=function(e){let n=function(e){return t(e).forEach((e=>a.set(Symbol(e.char?.innerText),r({...e})))),this},r=e=>(e.shouldPauseCursor=function(){return Boolean(this.typeable||this.cursorable||this.deletable)},e),i=()=>Array.from(a.values()),a=new Map;return n(e),{add:n,set:function(e,t){let n=[...a.keys()];a.set(n[e],r(t))},wipe:function(){a=new Map,n(e)},reset:function(){a.forEach((e=>delete e.done))},destroy:e=>a.delete(e),done:(e,t=!1)=>t?a.delete(e):a.get(e).done=!0,getItems:(e=!1)=>e?i():i().filter((e=>!e.done)),getQueue:()=>a,getTypeable:()=>i().filter((e=>e.typeable))}}([{delay:G.startDelay}]);V.dataset.typeitId=K,f("[data-typeit-id]:before {content: '.'; display: inline-block; width: 0; visibility: hidden;}");let Z=!!G.cursor&&!I(),ee=(()=>{if(I())return;let e=d("span");return e.className=o,Z?(e.innerHTML=a(G.cursorChar).innerHTML,e):(e.style.visibility="hidden",e)})();G.strings=(e=>{let t=V.innerHTML;return t?(V.innerHTML="",G.startDelete?(V.innerHTML=t,i(V),F(E({func:j,delay:M(1),deletable:!0},x().length)),e):t.replace(/<!--(.+?)-->/g,"").trim().split(/<br(?:\s*?)(?:\/)?>/).concat(e)):e})(t(G.strings)),G.strings.length&&R()}}));</script>
  <script src="https://kit.fontawesome.com/4f3ce16e3e.js" crossorigin="anonymous"></script>
  
<head>
<title>Happy Birthday</title>
<!-- 
  
-->
</head>
<body>
	
   <!-- Ganti Audio di sini -->
   <audio loop="true" src="https://feeldreams.github.io/djikhlas.mp3" id="linkmp3" class="sembunyi"></audio>
   
   <div id="bodyblur">
     <!-- Wallpaper --><img src="https://feeldreams.github.io/wp9.jpg" id="wallpaper"/><div id="beneranblur"></div>
   </div>
   
   <div id='Content'>

     <div id="kadoIn">
       <!-- Tombol Surat --><img src="https://i.postimg.cc/pXxhQDbX/1000052683-removebg-preview.png"/>
     </div>
     <p id="ket">Klik Kadonya!</p>

     <div class="kumpulanstiker">
         <!-- Stiker untuk Konten -->
         <img src="https://i.postimg.cc/KvQwh9F3/mimibubu.gif" id="fotostiker"/>
         <img src="https://i.postimg.cc/7Y5St8C3/snuggles-caring-1.gif" id="fotostiker2"/>
         <img src="https://feeldreams.github.io/emawh.gif" id="fotostiker5" id="fotostiker3"/>
     </div>
     <p id="halo" class="halo">Hitaaaa</p>
     <!-- Konten Pesan Setelah Aksi -->
     <p id="halo2" class="halo sty2">🙏Selamat Hari Raya Idul Fitri🙏</p>
     <p id="halo3" class="halo sty3">Minal       Aidzin Walfaizin       Mohon       Maaf       Lahir       Batin        ya        Adek🙏😝                 
      nih ada sedikit THR buat kamu ></p>
     <!-- Tanggal Otomatis Sesuai Hari Ini --><p id="tanggal" class="halo sty3"></p>
     
     <!-- Konten Pesan Akhir -->
     <p id="kalimatbawah"> 🎉Selamat Hari Raya Idul Fitri🎉</p> 
     <p id="kalimatbawah2" class="sembunyi">🙏Mohon Maaf Lahir dan Batin🙏</p> 
     <p id="kalimatbawah3" class="sembunyi">I Love You😝</p>
       
     <div><blockquote id='bq' data-text='&#9829;'>

       <!-- Konten Pembukaan -->
       <p id="kalimat">Hai Cantik 😝</p>
       <p id="kalimatb">Selamat Hari Raya Idul Fitri ya😄</p>
       <p id="kalimatc">Maaf kan aku bila aku pernah berbuat salah kepadamu😅</p>
       <p id="kalimatd">Sebenarnya agak pusing sih bikin ini soal e gak ada sinyal😭</p>
       <p id="kalimate">Tapi gak apa apa lah demi kamu😁</p>
       <p id="kalimatf">Nih Ada THR Buat kamu
       🧧</p>
       
       <p id="opsL">Klik untuk Lanjut</p>
       
     </blockquote></div>

     <!-- Tombol Kirim Pesan -->
     <div id="Tombol"><a id="By">Ambil THR 💸</a></div>

     <!-- Pesan yang dikirim ke WhatsApp -->
     <span id="pesanWA" class="sembunyi">Makasih😝!</span>
     
   </div>

<!-- Jangan Edit Bagian Ini --><script>
  const body = document.querySelector("body"); const style = document.createElement('style'); var today = new Date();var dd = String(today.getDate()).padStart(2, '0');var mm = String(today.getMonth() + 1).padStart(2, '0');var yyyy = today.getFullYear();const monthNames = ["Januari", "Februari", "Maret", "April", "Mei", "Juni", "Juli", "Agustus", "September", "Oktober", "November", "Desember"];today = 33 + ' ' + monthNames[today.getMonth()] + ' ' + yyyy; inikuis=0;ftganti=0;flag=1;flagg=1;fungsi=0;ftfungsi=0;fungsiAwal=0;fungsitimer=0;vketikhalo=halo.innerHTML;halo.innerHTML = "";vketikhalo2=halo2.innerHTML;halo2.innerHTML = "";pesanwhatsapp = pesanWA.innerHTML;deffotostiker=fotostiker.src;Content.style = "opacity:1;margin-top:16vh;";
  audio = new Audio('' + linkmp3.src);tanggal.innerHTML="-2025 M / 1448 H-"; function createHeart() {const heart = document.createElement("div"); heart.className = "fas fa-heart"; heart.style.left = (Math.random() * 90)+"vw"; heart.style.animationDuration = (Math.random()*3)+2+"s"; body.appendChild(heart);} setInterval(function name(params) {var heartArr = document.querySelectorAll(".fa-heart"); if (heartArr.length > 100) {heartArr[0].remove()}},100);
</script>
<script>document.getElementById("kadoIn").onclick = function() {if(fungsiAwal==0){audio.play();fungsiAwal=1;kadoIn.style="transition:all .8s ease;transform:scale(10);opacity:0";wallpaper.style="transform: scale(1.5);";ket.style="display:none";setTimeout(mulainama,700)}}
  
  async function mulainama() {
           kadoIn.style="display:none";ket.style="display:none";
           Content.style = "opacity:1;margin-top:2vh";
           bodyblur.style="opacity:.7";
           wallpaper.style="transform: scale(1);";
           fotostiker.style="display:inline-flex;";
           setTimeout(ftmuncul,200);
           setTimeout(kethalo,500);
  }
  
  function ftmuncul(){
    if(ftganti==0){fotostiker.src = deffotostiker;fotostiker.style="display:inline-flex;opacity:1;transform:scale(1)";}
    if(ftganti==1){fotostiker.src = fotostiker2.src;fotostiker.style="display:inline-flex;opacity:1;transition:all .7s ease;transform:scale(1);";}
    if(ftganti==2){fotostiker.src = fotostiker3.src;fotostiker.style="display:inline-flex;opacity:1;transition:all .7s ease;transform:scale(1);";}
    if(ftganti==3){fotostiker.src = fotostiker4.src;fotostiker.style="display:inline-flex;opacity:1;transition:all .7s ease;transform:scale(1);box-shadow:none;background:none;border:0;width:150px;height:150px";setTimeout(jjfoto,400);}
  }
  function fthilang(){fotostiker.style="display:inline-flex;opacity:1;transition:all .7s ease;transform:scale(.1)";}
  function jjfoto(){fotostiker.style.animation="rto .8s infinite alternate";setInterval(createHeart,200);}
  
  function kethalo(){
  new TypeIt("#halo", {
  strings: ["" + vketikhalo], startDelay: 50, speed: 60, waitUntilVisible: true,
  afterComplete: function(){
    halo.innerHTML = vketikhalo;
    setTimeout(bqmuncul,200);
  },}).go();
  }
  function kethalo2(){
  bqhilang();fthilang();ftganti=1;setTimeout(ftmuncul,400);
  halo.style="display:none";
  new TypeIt("#halo2", {
  strings: ["" + vketikhalo2], startDelay: 50, speed: 60, waitUntilVisible: true,
  afterComplete: function(){
    bq.style="";
    halo2.innerHTML = vketikhalo2;
    setTimeout(mulaiketikAkhir,500);
  },}).go();
  }
  vketikhalo3=halo3.innerHTML;halo3.innerHTML="";
  function mulaiketikAkhir(){
  halo3.style="position:relative !important";
  new TypeIt("#halo3", {
  strings: ["" + vketikhalo3], cursor: false, startDelay: 50, speed: 55, waitUntilVisible: true,
  afterComplete: function(){
    halo3.innerHTML = vketikhalo3;
    setTimeout(showtanggal,300);
    setTimeout(munculbwh,800);
    setTimeout(fthilang,600);ftganti=2;setTimeout(ftmuncul,1000);
    setInterval(createHeart,400);setTimeout(tombol,7000);
  },}).go();
  }
  function showtanggal(){tanggal.style="position:relative !important;opacity:1;transform:scale(1)";}
  defkalimatbawah = kalimatbawah.innerHTML;
  function munculbwh(){kalimatbawah.innerHTML=defkalimatbawah;setTimeout(munculbwh2,2000);otomatis();}
  function munculbwh2(){kalimatbawah.innerHTML=kalimatbawah2.innerHTML;setTimeout(munculbwh3,2000);otomatis();}
  function munculbwh3(){kalimatbawah.innerHTML=kalimatbawah3.innerHTML;setTimeout(munculbwh,2000);otomatis();}
  function otomatis() {kalimatbawah.style="position:relative;opacity:0;transform:scale(.3);";setTimeout(anim,300);} 
  function anim() {kalimatbawah.style="position:relative;opacity:1;transform:scale(1);";}
  
  function bqmuncul(){bq.style = "position:relative;opacity:1;visibility:visible;transform: scale(1);margin-top:0";mulaiketik1();fungsi=1;}
  function bqhilang(){wallpaper.style="transform: scale(2);";bodyblur.style="opacity:.5";bq.style = "position:relative;transition:all .7s ease;";}
  
  function tombol(){Tombol.style="opacity:1;transform: scale(1);";fungsi=1}
  document.getElementById("By").onclick = function() {if(fungsi==1){menuju();}}
  async function menuju(){window.location = "https://link.dana.id/danakaget?c=sjadsfjmz&r=dRMb4I&orderId=20250327101214587515010300166580614927745";}

  opsLclick=0;opsLcheck=0;
  document.getElementById("bq").onclick = function() {
    if(opsLclick==1){
      if(opsLcheck==1){mulaiketik2();}
      if(opsLcheck==2){mulaiketik3();}
      if(opsLcheck==3){mulaiketik4();}
      if(opsLcheck==4){mulaiketik5();}
      if(opsLcheck==5){kethalo2();}
      opsLclick=0;
    }
  }
  
  vketik1=kalimat.innerHTML;kalimat.innerHTML = "";
  function mulaiketik1(){
  new TypeIt("#kalimat", {
  strings: ["" + vketik1], startDelay: 400, speed: 40, deleteSpeed: 20, breakLines: false, waitUntilVisible: true, lifelike: true,
  afterComplete: function(){
    opsL.style.opacity=".8";opsLcheck=1;opsLclick=1;
  },}).go();
  }
  
  vketik2=kalimatb.innerHTML;kalimatb.innerHTML = "";
  function mulaiketik2(){
  kalimat.innerHTML = "";kalimat.style.display="none";
  opsL.style.opacity="0";
  new TypeIt("#kalimatb", {
  strings: ["" + vketik2], startDelay: 100, speed: 40, waitUntilVisible: true,
  afterComplete: function(){
    opsL.style.opacity=".8";opsLcheck=2;opsLclick=1;
  },}).go();
  }
  
  vketik3=kalimatc.innerHTML;kalimatc.innerHTML = "";
  function mulaiketik3(){
  kalimatb.innerHTML = "";kalimatb.style.display="none";
  opsL.style.opacity="0";
  new TypeIt("#kalimatc", {
  strings: ["" + vketik3], startDelay: 100, speed: 40, waitUntilVisible: true,
  afterComplete: function(){
    opsL.style.opacity=".8";opsLcheck=3;opsLclick=1;
  },}).go();
  }

  vketik4=kalimatd.innerHTML;kalimatd.innerHTML = "";
  vketik5=kalimate.innerHTML;kalimate.innerHTML = "";
  function mulaiketik4(){
  kalimatc.innerHTML = "";kalimatc.style.display="none";
  opsL.style.opacity="0";
  new TypeIt("#kalimatd", {
  strings: ["" + vketik4, "" + vketik5], startDelay: 100, speed: 40, deleteSpeed: 10, breakLines: false, waitUntilVisible: true, lifelike: true,
  afterComplete: function(){
    opsL.style.opacity=".8";opsLcheck=4;opsLclick=1;
  },}).go();
  }

  vketik6=kalimatf.innerHTML;kalimatf.innerHTML = "";
  function mulaiketik5(){
  kalimatd.innerHTML = "";kalimatd.style.display="none";
  opsL.style.opacity="0";
  new TypeIt("#kalimatf", {
  strings: ["" + vketik6], startDelay: 100, speed: 40, deleteSpeed: 10, breakLines: false, waitUntilVisible: true, lifelike: true,
  afterComplete: function(){
     kalimatf.innerHTML = vketik6;
    opsLcheck=5;opsLclick=1;
  },}).go();
  }</script>
<!-- Sampai Sini -->
</body>
</html>
