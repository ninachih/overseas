<template>
    <div class="travelTheme" id="travelTheme">
        <div class="container scrollContainer">
            <div class="travel-nav-container">
                            <div class="travel-nav-fixed">
                                <div class="title-wrapper center">
                                    <h2 class="title">跟著旅遊主題買 旅行保險好簡單</h2>
                                </div>
                                <ul class="travel-nav">
                                    <li data-anchor="rails" class="active">
                                        <a href="#rails" v-smooth-scroll="{ duration: 1000, offset: -321, container: '.scrollContainer' }">鐵道客運遊</a>
                                    </li>
                                    <li data-anchor="moto">
                                        <a href="#moto" v-smooth-scroll="{ duration: 1000, offset: -321, container: '.scrollContainer' }">離島租車遊</a>
                                    </li>
                                    <li data-anchor="car">
                                        <a href="#car" v-smooth-scroll="{ duration: 1000, offset: -321, container: '.scrollContainer' }">租車自駕遊</a>
                                    </li>
                                    <li data-anchor="basic">
                                        <a href="#basic" v-smooth-scroll="{ duration: 1000, offset: -321, container: '.scrollContainer' }">基本保障款</a>
                                    </li>
                                    <li data-anchor="camp">
                                        <a href="#camp" v-smooth-scroll="{ duration: 1000, offset: -321, container: '.scrollContainer' }">自然露營趣</a>
                                    </li>
                                </ul>
                            </div>
            </div>
            <div class="theme-container">
                            <div id="rails" class="item">
                                <div class="image-wrapper">
                                    <img src="../assets/travel-rails.svg" alt="鐵道客運遊">
                                    <div class="title">
                                        <h3>鐵道客運遊</h3>
                                    </div>
                                </div>

                                <div class="item-content">
                                    <div class="head">
                                        <div class="title">
                                            <h3>鐵道客運遊</h3>
                                        </div>
                                        <div class="prize">
                                            <p>一日保費<br>只要</p>
                                            <p class="hightlight"><span>$</span>130</p>
                                            <p>起</p>
                                        </div>
                                    </div>
                                    <div class="body">
                                        <p>
                                            國道或大眾運輸交通事故險<br>
                                            鐵路客運旅程延誤補償<br>
                                            旅行平安險額度300萬<br>
                                            傷害醫療險額度30萬<br>
                                            個人賠償責任險
                                        </p>
                                        <div class="prize">
                                            <p>一日保費<br>只要</p>
                                            <p class="hightlight"><span>$</span>130</p>
                                            <p>起</p>
                                        </div>
                                    </div>
                                    <a class="btn" id="railsContent" @click="popupShow($event)">
                                        <p>瞭解完整保障</p>
                                    </a>
                                </div>
                            </div>
                            <div id="moto" class="item">
                                <div class="image-wrapper">
                                    <img src="../assets/travel-moto.svg" alt="離島租車遊">
                                    <div class="title">
                                        <h3>離島租車遊</h3>
                                    </div>
                                </div>

                                <div class="item-content">
                                    <div class="head">
                                        <div class="title">
                                            <h3>離島租車遊</h3>
                                        </div>
                                        <div class="prize">
                                            <p>一日保費<br>只要</p>
                                            <p class="hightlight"><span>$</span>217</p>
                                            <p>起</p>
                                        </div>
                                    </div>
                                    <div class="body">
                                        <p>
                                            國內租車旅遊險(機車)<br>
                                            境內飛機旅程延誤補償<br>
                                            旅行平安險額度500萬<br>
                                            傷害醫療險額度50萬<br>
                                            個人賠償責任險
                                        </p>
                                        <div class="prize">
                                            <p>一日保費<br>只要</p>
                                            <p class="hightlight"><span>$</span>217</p>
                                            <p>起</p>
                                        </div>
                                    </div>
                                    <a class="btn" id="motoContent"  @click="popupShow($event)">
                                        <p>瞭解完整保障</p>
                                    </a>
                                </div>
                            </div>
                            <div id="car" class="item">
                                <div class="image-wrapper">
                                    <img src="../assets/travel-car.svg" alt="租車自駕遊">
                                    <div class="title">
                                        <h3>租車自駕遊</h3>
                                    </div>
                                </div>

                                <div class="item-content">
                                    <div class="head">
                                        <div class="title">
                                            <h3>租車自駕遊</h3>
                                        </div>
                                        <div class="prize">
                                            <p>一日保費<br>只要</p>
                                            <p class="hightlight"><span>$</span>370</p>
                                            <p>起</p>
                                        </div>
                                    </div>
                                    <div class="body">
                                        <p>
                                            國內租車旅遊險(汽車)<br>
                                            國道或大眾運輸交通事故險<br>
                                            旅行平安險額度500萬<br>
                                            傷害醫療險額度50萬<br>
                                            個人賠償責任險
                                        </p>
                                        <div class="prize">
                                            <p>一日保費<br>只要</p>
                                            <p class="hightlight"><span>$</span>370</p>
                                            <p>起</p>
                                        </div>
                                    </div>
                                    <a class="btn" id="carContent"  @click="popupShow($event)">
                                        <p>瞭解完整保障</p>
                                    </a>
                                </div>
                            </div>
                            <div id="basic" class="item">
                                <div class="image-wrapper">
                                    <img src="../assets/travel-basic.svg" alt="基本保障款">
                                    <div class="title">
                                        <h3>基本保障款</h3>
                                    </div>
                                </div>
                                <div class="item-content">
                                    <div class="head">
                                        <div class="title">
                                            <h3>基本保障款</h3>
                                        </div>
                                        <div class="prize">
                                            <p>一日保費<br>只要</p>
                                            <p class="hightlight"><span>$</span>68</p>
                                            <p>起</p>
                                        </div>
                                    </div>
                                    <div class="body">
                                        <p>
                                            旅行平安險額度200萬<br>
                                            傷害醫療險額度20萬<br>
                                            個人賠償責任險
                                        </p>
                                        <div class="prize">
                                            <p>一日保費<br>只要</p>
                                            <p class="hightlight"><span>$</span>68</p>
                                            <p>起</p>
                                        </div>
                                    </div>
                                    <a class="btn" id="basicContent" @click="popupShow($event)" >
                                        <p>瞭解完整保障</p>
                                    </a>
                                </div>
                            </div>
                            <div id="camp" class="item">
                                <div class="image-wrapper">
                                    <img src="../assets/travel-camp.svg" alt="自然露營趣">
                                    <div class="title">
                                        <h3>自然露營趣</h3>
                                    </div>
                                </div>
                                <div class="item-content">
                                    <div class="head">
                                        <div class="title">
                                            <h3>自然露營趣</h3>
                                        </div>
                                        <div class="prize">
                                            <p>一日保費<br>只要</p>
                                            <p class="hightlight"><span>$</span>166</p>
                                            <p>起</p>
                                        </div>
                                    </div>
                                    <div class="body">
                                        <p class="">
                                            重大燒燙傷保險<br>
                                            國道或大眾運輸交通事故險<br>
                                            旅行平安險額度500萬<br>
                                            傷害醫療險額度50萬<br>
                                            個人賠償責任險
                                        </p>
                                        <div class="prize">
                                            <p>一日保費<br>只要</p>
                                            <p class="hightlight"><span>$</span>166</p>
                                            <p>起</p>
                                        </div>
                                    </div>
                                    <a class="btn" id="campContent"  @click="popupShow($event)">
                                        <p>瞭解完整保障</p>
                                    </a>
                                </div>
                            </div>
            </div>
            <p class="note center">(保費金額以投保試算頁面為準，保費將依保額、天數、人數調整)</p>
        </div>
        <div class="popup-wrapper" style="display: none;">
            <div class="popup-content popup-railsContent">
                        <div class="head">
                            <h3>鐵道客運遊 <span>保險方案推薦</span></h3>
                        </div>
                        <div class="close popup-close" @click="popupClose">
                            <img src="../assets/close.svg" alt="">
                        </div>
                        <div class="overFrame">
                            <div class="body">
                                <div class="list">
                                    <div class="list-icon">
                                        <p>推薦<br><span>1</span></p>
                                        <img src="../assets/popup-yellow-icon.svg" alt="">
                                    </div>
                                    <div class="list-content">
                                        <p class="title">鐵道客運旅程延誤險(含在國內旅遊不便險內) </p>
                                        <p class="listCon">若因台鐵、客運誤點達4小時以上即可獲得定額2,000元補償。</p>
                                    </div>
                                </div>
                                <div class="list">
                                    <div class="list-icon">
                                        <p>推薦<br><span>2</span></p>
                                        <img src="../assets/popup-yellow-icon.svg" alt="">
                                    </div>
                                    <div class="list-content">
                                        <p class="title">國道或大眾運輸事故保險 </p>
                                        <p class="listCon">在國道上發生意外或是搭乘大眾運輸工具發生意外，導致不幸身故，最高理賠200萬元。</p>
                                    </div>
                                </div>
                                <div class="list">
                                    <div class="list-icon">
                                        <p class="color-black">必保<br><span>1</span></p>
                                        <img src="../assets/popup-green-icon.svg" alt="">
                                    </div>
                                    <div class="list-content">
                                        <p class="title">旅行平安保險</p>
                                        <p class="listCon">旅行期間因意外事故造成身亡或失能，依保額提供定額給付。</p>
                                    </div>
                                </div>
                                <div class="list">
                                    <div class="list-icon">
                                        <p class="color-black">必保<br><span>2</span></p>
                                        <img src="../assets/popup-green-icon.svg" alt="">
                                    </div>
                                    <div class="list-content">
                                        <p class="title">傷害醫療保險</p>
                                        <p class="listCon">若因旅程期間騎乘腳踏車不慎摔傷，以實際醫療費用給付醫療保險金。</p>
                                    </div>
                                </div>
                                <div class="list">
                                    <div class="list-icon">
                                        <p class="color-black">必保<br><span>3</span></p>
                                        <img src="../assets/popup-green-icon.svg" alt="">
                                    </div>
                                    <div class="list-content">
                                        <p class="title">個人賠償責任保險</p>
                                        <p class="listCon">餐廳吃飯不慎將咖啡潑灑到鄰桌客人身上，導致需要賠償衣物、包包，提供保險金賠償。</p>
                                    </div>
                                </div>
                            </div>
                        </div>
                        <div class="footer">
                            <div class="prize">
                                <p>一日保費</p>
                                <p class="hightlight"><span>$</span>130</p>
                                <p>起</p>
                            </div>
                            <p class="safe-terms">(保費依旅平保額3百萬、傷害醫療30萬計算，保費將依保額、天數、人數變動)</p>
                            <div class="btnArea">
                                <a href="/portal/tmnewaAPI/v1/goTripIns?amount31=300&amount32=30&over15count=1&planCode=I00&travelArea=A&buyTrafficAccidentDomestic=true&buyUneasyPolicyDomestic=true" target="_blank" class="btn">
                                立即投保
                                <img src="../assets/go.svg" alt="">
                                </a>
                            </div>
                        </div>
            </div>
            <div class="popup-content  popup-motoContent">
                        <div class="head">
                            <h3>離島租車遊 <span>保險方案推薦</span></h3>
                        </div>
                        <div class="close popup-close" @click="popupClose">
                            <img src="../assets/close.svg" alt="">
                        </div>
                        <div class="overFrame">
                            <div class="body">
                                <div class="list">
                                    <div class="list-icon">
                                        <p>推薦<br><span>1</span></p>
                                        <img src="../assets/popup-yellow-icon.svg" alt="">
                                    </div>
                                    <div class="list-content">
                                        <p class="title">境內旅程延誤險(含在國內旅遊不便險)</p>
                                        <p class="listCon">若因飛機、船班誤點達4小時，以上即可獲得定額2,000元補償。</p>
                                    </div>
                                </div>
                                <div class="list">
                                    <div class="list-icon">
                                        <p>推薦<br><span>2</span></p>
                                        <img src="../assets/popup-yellow-icon.svg" alt="">
                                    </div>
                                    <div class="list-content">
                                        <p class="title">國內租車旅遊險(機車)</p>
                                        <p class="listCon">於綠島騎乘機車，不慎與對向機車對撞，提供機車維修費用與他人財損、受傷限額補償。</p>
                                    </div>
                                </div>
                                <div class="list">
                                    <div class="list-icon">
                                        <p class="color-black">必保<br><span>1</span></p>
                                        <img src="../assets/popup-green-icon.svg" alt="">
                                    </div>
                                    <div class="list-content">
                                        <p class="title">旅行平安保險</p>
                                        <p class="listCon">旅行期間因意外事故造成身亡或失能，依保額提供定額給付。</p>
                                    </div>
                                </div>
                                <div class="list">
                                    <div class="list-icon">
                                        <p class="color-black">必保<br><span>2</span></p>
                                        <img src="../assets/popup-green-icon.svg" alt="">
                                    </div>
                                    <div class="list-content">
                                        <p class="title">傷害醫療保險</p>
                                        <p class="listCon">若因旅程期間騎乘腳踏車不慎摔傷，以實際醫療費用給付醫療保險金。</p>
                                    </div>
                                </div>
                                <div class="list">
                                    <div class="list-icon">
                                        <p class="color-black">必保<br><span>3</span></p>
                                        <img src="../assets/popup-green-icon.svg" alt="">
                                    </div>
                                    <div class="list-content">
                                        <p class="title">個人賠償責任保險</p>
                                        <p class="listCon">餐廳吃飯不慎將咖啡潑灑到鄰桌客人身上，導致需要賠償衣物、包包等，提供保險金賠償。</p>
                                    </div>
                                </div>
                            </div>
                        </div>
                        <div class="footer">
                                <div class="prize">
                                    <p>一日保費</p>
                                    <p class="hightlight"><span>$</span>217</p>
                                    <p>起</p>
                                </div>
                                <p class="safe-terms">(保費依旅平保額5百萬、傷害醫療50萬計算，保費將依保額、天數、人數變動)</p>
                                <div class="btnArea">
                                    <a  href="/portal/tmnewaAPI/v1/goTripIns?amount31=500&amount32=50&over15count=1&planCode=I00&travelArea=A&buyUneasyPolicyDomestic=true&buyMotorPolicy=true" target="_blank" class="btn" data-title="離島租車遊_立即投保">
                                        立即投保
                                        <img src="../assets/go.svg" alt="">
                                    </a>
                                </div>
                        </div>
                        
            </div>
            <div class="popup-content  popup-carContent">
                        <div class="head">
                            <h3>租車自駕遊 <span>保險方案推薦</span></h3>
                        </div>
                        <div class="close popup-close" @click="popupClose">
                            <img src="../assets/close.svg" alt="">
                        </div>
                        <div class="overFrame">
                            <div class="body">
                                <div class="list">
                                    <div class="list-icon">
                                        <p>推薦<br><span>1</span></p>
                                        <img src="../assets/popup-yellow-icon.svg" alt="">
                                    </div>
                                    <div class="list-content">
                                        <p class="title">國內租車旅遊險(汽車)</p>
                                        <p class="listCon">於國內租車與其他車輛發生碰撞事故，提供車輛維修費用與他人財損受傷限額保險金。</p>
                                    </div>
                                </div>
                                <div class="list">
                                    <div class="list-icon">
                                        <p>推薦<br><span>2</span></p>
                                        <img src="../assets/popup-yellow-icon.svg" alt="">
                                    </div>
                                    <div class="list-content">
                                        <p class="title">國道或大眾運輸交通事故保險</p>
                                        <p class="listCon">在國道上發生意外或是搭乘大眾運輸工具發生意外，導致不幸身故，最高理賠200萬元。</p>
                                    </div>
                                </div>
                                <div class="list">
                                    <div class="list-icon">
                                        <p class="color-black">必保<br><span>1</span></p>
                                        <img src="../assets/popup-green-icon.svg" alt="">
                                    </div>
                                    <div class="list-content">
                                        <p class="title">旅行平安保險</p>
                                        <p class="listCon">旅行期間因意外事故造成身亡或失能，依保額提供定額給付。</p>
                                    </div>
                                </div>
                                <div class="list">
                                    <div class="list-icon">
                                        <p class="color-black">必保<br><span>2</span></p>
                                        <img src="../assets/popup-green-icon.svg" alt="">
                                    </div>
                                    <div class="list-content">
                                        <p class="title">傷害醫療保險</p>
                                        <p class="listCon">若因旅程期間騎乘腳踏車不慎摔傷，以實際醫療費用給付醫療保險金。</p>
                                    </div>
                                </div>
                                <div class="list">
                                    <div class="list-icon">
                                        <p class="color-black">必保<br><span>3</span></p>
                                        <img src="../assets/popup-green-icon.svg" alt="">
                                    </div>
                                    <div class="list-content">
                                        <p class="title">個人賠償責任保險</p>
                                        <p class="listCon">餐廳吃飯不慎將咖啡潑灑到鄰桌客人身上，導致需要賠償衣物、包包，提供保險金賠償。</p>
                                    </div>
                                </div>
                            </div>
                        </div>
                        <div class="footer">
                            <div class="prize">
                                <p>一日保費</p>
                                <p class="hightlight"><span>$</span>370</p>
                                <p>起</p>
                            </div>
                            <p class="safe-terms">(保費依旅平保額5百萬、傷害醫療50萬計算，保費將依保額、天數、人數變動)</p>
                            <div class="btnArea">
                                <a href="/portal/tmnewaAPI/v1/goTripIns?amount31=500&amount32=50&over15count=1&planCode=I00&travelArea=A&buyTrafficAccidentDomestic=true&buyCarPolicy=true" target="_blank" class="btn" data-title="租車自駕遊_立即投保">
                                   立即投保
                                   <img src="../assets/go.svg" alt="">
                                </a>
                            </div>
                        </div>
            </div>
            <div class="popup-content  popup-basicContent">
                        <div class="head">
                            <h3>基本保障款 <span>保險方案推薦</span></h3>
                        </div>
                        <div class="close popup-close" @click="popupClose">
                            <img src="../assets/close.svg" alt="">
                        </div>
                        <div class="overFrame">
                            <div class="body">
                                <div class="list">
                                    <div class="list-icon">
                                        <p class="color-black">必保<br><span>1</span></p>
                                        <img src="../assets/popup-green-icon.svg" alt="">
                                    </div>
                                    <div class="list-content">
                                        <p class="title">旅行平安保險</p>
                                        <p class="listCon">旅行期間因意外事故造成身亡或失能，依保額提供定額給付。</p>
                                    </div>
                                </div>
                                <div class="list">
                                    <div class="list-icon">
                                        <p class="color-black">必保<br><span>2</span></p>
                                        <img src="../assets/popup-green-icon.svg" alt="">
                                    </div>
                                    <div class="list-content">
                                        <p class="title">傷害醫療保險</p>
                                        <p class="listCon">若因旅程期間騎乘腳踏車不慎摔傷，以實際醫療費用給付醫療保險金。</p>
                                    </div>
                                </div>
                                <div class="list">
                                    <div class="list-icon">
                                        <p class="color-black">必保<br><span>3</span></p>
                                        <img src="../assets/popup-green-icon.svg" alt="">
                                    </div>
                                    <div class="list-content">
                                        <p class="title">個人賠償責任保險</p>
                                        <p class="listCon">餐廳吃飯不慎將咖啡潑灑到鄰桌客人身上，導致需要賠償衣物、包包，提供保險金賠償。</p>
                                    </div>
                                </div>
                            </div>
                        </div>
                        <div class="footer">
                            <div class="prize">
                                <p>一日保費</p>
                                <p class="hightlight"><span>$</span>68</p>
                                <p>起</p>
                            </div>
                            <p class="safe-terms">(保費依旅平保額2百萬、傷害醫療20萬計算，保費將依保額、天數、人數變動)</p>
                            <div class="btnArea">
                                <a href="/portal/tmnewaAPI/v1/goTripIns?amount31=200&amount32=20&over15count=1&planCode=I00&travelArea=A" target="_blank" class="btn" data-title="基本保障款_立即投保">
                                    立即投保
                                    <img src="../assets/go.svg" alt="">
                                </a>
                            </div>
                        </div>
            </div>
            <div class="popup-content  popup-campContent">
                        <div class="head">
                            <h3>自然露營趣 <span>保險方案推薦</span></h3>
                        </div>
                        <div class="close popup-close" @click="popupClose">
                            <img src="../assets/close.svg" alt="">
                        </div>
                        <div class="overFrame">
                            <div class="body">
                                <div class="list">
                                    <div class="list-icon">
                                        <p>推薦<br><span>1</span></p>
                                        <img src="../assets/popup-yellow-icon.svg" alt="">
                                    </div>
                                    <div class="list-content">
                                        <p class="title">重大燒燙傷保險</p>
                                        <p class="listCon">露營不免烤肉、野炊、升營火，活動期間若不慎造成燒燙傷，依100萬保額按燒傷程度的比例給付保險金。</p>
                                    </div>
                                </div>
                                <div class="list">
                                    <div class="list-icon">
                                        <p>推薦<br><span>2</span></p>
                                        <img src="../assets/popup-yellow-icon.svg" alt="">
                                    </div>
                                    <div class="list-content">
                                        <p class="title">國道或大眾運輸交通事故險</p>
                                        <p class="listCon">前往營地不免路經國道，若不幸因意外造成身故提供定額保險金。</p>
                                    </div>
                                </div>
                                <div class="list">
                                    <div class="list-icon">
                                        <p class="color-black">必保<br><span>1</span></p>
                                        <img src="../assets/popup-green-icon.svg" alt="">
                                    </div>
                                    <div class="list-content">
                                        <p class="title">旅行平安保險</p>
                                        <p class="listCon">旅行期間因意外事故造成身亡或失能，依保額提供定額給付。</p>
                                    </div>
                                </div>
                                <div class="list">
                                    <div class="list-icon">
                                        <p class="color-black">必保<br><span>2</span></p>
                                        <img src="../assets/popup-green-icon.svg" alt="">
                                    </div>
                                    <div class="list-content">
                                        <p class="title">傷害醫療保險</p>
                                        <p class="listCon">若因旅程期間騎乘腳踏車不慎摔傷，以實際醫療費用給付醫療保險金。</p>
                                    </div>
                                </div>
                                <div class="list">
                                    <div class="list-icon">
                                        <p class="color-black">必保<br><span>3</span></p>
                                        <img src="../assets/popup-green-icon.svg" alt="">
                                    </div>
                                    <div class="list-content">
                                        <p class="title">個人賠償責任保險</p>
                                        <p class="listCon">餐廳吃飯不慎將咖啡潑灑到鄰桌客人身上，導致需要賠償衣物、包包，提供保險金賠償。</p>
                                    </div>
                                </div>
                                <a href=""></a>
                            </div>
                        </div>
                        <div class="footer">
                            <div class="prize">
                                <p>一日保費</p>
                                <p class="hightlight"><span>$</span>166</p>
                                <p>起</p>
                            </div>
                            <p class="safe-terms">(保費依旅平保額5百萬、傷害醫療50萬計算，保費將依保額、天數、人數變動)</p>
                            <div class="btnArea">
                                <a href="/portal/tmnewaAPI/v1/goTripIns?amount31=500&amount32=50&over15count=1&planCode=I00&travelArea=A&buyTrafficAccidentDomestic=true&buyBurnPolicyDomestic=true" target="_blank" class="btn" data-title="自然露營趣_立即投保">
                                    立即投保
                                    <img src="../assets/go.svg" alt="">
                                </a>
                            </div>
                        </div>
            </div>
        </div>
    </div>
</template>

<script>

export default {
  name: "travelTheme",
  mounted(){
   this.initNavFixedEvent()
    
  },
  data(){
    return{
       popupData:''
    }
  },
  methods:{
    initNavFixedEvent() {
        var travelNavFixedTop;
        var themeitem = $('.theme-container > .item').last();
        var themeLast = $(themeitem).last().position().top + $(themeitem).height() / 2;
        var isFixed = false;
        travelNavFixedTop = $('.travel-nav-fixed').offset().top;
        $(window).on('resize', function () {
        $('.travel-nav-fixed').removeClass('fixed');
        travelNavFixedTop = $('.travel-nav-fixed').position().top;
        });
        $(window).on('scroll', function (event) {
      if ($(this).scrollTop() + 320 > travelNavFixedTop && $(this).scrollTop() + 320 < themeLast) {
        $('.travel-nav-fixed').addClass('fixed');
        isFixed = true;
        var triggerAry = [];
        $('.theme-container > .item').each(function (index, item) {
          if ($(window).scrollTop() + 320 + $('.travel-nav-fixed').height() > $(item).position().top) {
            triggerAry.push($(item).attr('id'));
          }
        });

        if (triggerAry.length > 0) {
          $("[data-anchor=".concat(triggerAry[triggerAry.length - 1], "]")).addClass('active').siblings().removeClass('active');
          $('.travel-nav').scrollLeft($("[data-anchor=".concat(triggerAry[triggerAry.length - 1], "]")).position().left + $('.travel-nav').scrollLeft());
        }
      } else {
        isFixed = false;
        $('.travel-nav-fixed').removeClass('fixed');
        $('.travel-nav').scrollLeft(0);
        travelNavFixedTop = $('.travel-nav-fixed').position().top;
        themeLast = $(themeitem).last().position().top + $(themeitem).height() / 2;
      }
    });
    },
    popupShow(event){
       var popupTarget = event.currentTarget.id;
       $('.popup-wrapper').find(".popup-".concat(popupTarget)).addClass('active').siblings().removeClass('active').end().end().fadeIn();
       $('body').css('overflow', 'hidden');
    },
    popupClose(){     
        $('.popup-wrapper').fadeOut();
        $('body').css('overflow', 'initial');
    }
  }
 
  
};
</script>

<style lang="scss">
.travelTheme  {
    padding-top: 60px;
    padding-bottom: 85px;
    .travel-nav-container{
        .travel-nav-fixed {
            padding-top: 20px;
            &.fixed {
                position: fixed;
                top: 93px;
                z-index: 10;
                left: 50%;
                -webkit-transform: translateX(-50%);
                transform: translateX(-50%);
                background-color: #e8e8e8;
                width: 100%;            
            }
        }
        .travel-nav {
            display: -webkit-box;
            display: -ms-flexbox;
            display: flex;
            padding-bottom: 25px;
            padding-top: 40px;
            -webkit-box-pack: center;
            -ms-flex-pack: center;
            justify-content: center;
            li {
                background: white;
                -ms-flex-negative: 0;
                flex-shrink: 0;
                border-radius: 20px;
                cursor: pointer;
                -webkit-transition: .3s all;
                transition: .3s all;
                border: 2px solid #B6B6B7;
                a{color:$mainBlue;  padding: 20px 20px;display:block;font-weight:bold}
               
                & ~ li{
                    margin-left: 20px;
                }
                &:hover{
                    background: $mainBlue;
                    border: 2px solid  $mainBlue;
                    a {color:#fff}
                }
                &.active{
                    background: $mainBlue;
                    border: 2px solid  $mainBlue;
                    a {color:#fff}
                }
            }
            p {
                color: #a8a39a;
                margin: 0px;
                font-weight: 600;
                line-height: 1em;
            }
        }
    }
    .theme-container {
        width: 100%;
        max-width: 900px;
        margin: 0px auto;
        margin-bottom: 60px;
        .item {
            display: -webkit-box;
            display: -ms-flexbox;
            display: flex;
            position: relative;
            & ~ .item {
                margin-top: 75px;
            }
            .image-wrapper {
            display: block;
            position: relative;
            z-index: 3;
            width: 370px;
            -ms-flex-negative: 0;
            flex-shrink: 0;
            
                .title {
                    display: none;
                }
                img {
                    width: 100%;
                }
            }
            .item-content {
                width: 100%;
                position: relative;
                padding-right: 20px;
                -webkit-box-sizing: border-box;
                box-sizing: border-box;
                &::before {
                    content: "";
                    position: absolute;
                    background-color: white;
                    border: 2px solid #EBECED;
                    top: 0px;
                    width: calc(100% + 276px);
                    height: calc(100% + 35px);
                    border-radius: 10px;
                    right: 0px;
                    box-shadow: 0px 4px 4px #CACCCF;
                }
                .title {
                    color: #fff;
                    padding: 15px 25px 15px 40px;
                    background-color: $mainBlue;
                    -webkit-transform: translateX(-10px);
                    transform: translateX(-10px);
                    position: relative;
                    left:-15px;
                    border-top-right-radius: 50px;
                    border-bottom-right-radius:50px;
                    
                    h3{
                        margin: 0px;
                        line-height: 1em;
                        position: relative;
                        font-size:24px;
                    }
                }
                .head {
                    display: -webkit-box;
                    display: -ms-flexbox;
                    display: flex;
                    -webkit-box-pack: justify;
                    -ms-flex-pack: justify;
                    justify-content: space-between;
                    -webkit-box-align: end;
                    -ms-flex-align: end;
                    align-items: flex-end;
                    position: relative;
                }
                .body {
                    padding-left: 25px;
                    padding-top: 25px;
                    position: relative;
                    p {
                        margin: 0px;
                        font-size: 16px;
                        line-height: 32px;
                        color:$deepGray;
                        font-weight:bold;
                    }
                    .prize {
                        display: none;
                    }
                }
                a {
                    position: absolute;
                    right: 20px;
                    bottom: 5px;
                    &.btn{
                        padding:16px;
                        width:auto;
                        margin:0;
                        p {
                        font-size: 20px;
                        color: white;
                        font-weight: 900;
                        margin: 0px;
                        position: relative;
                        z-index: 2;
                        line-height: 1em;
                        }
                    }
                    
                }
                .prize {
                    display: -webkit-box;
                    display: -ms-flexbox;
                    display: flex;
                    -webkit-box-align: end;
                    -ms-flex-align: end;
                    align-items: flex-end;
                    margin-bottom: 2px;
                    p {
                        font-size: 16px;
                        line-height: 20px;
                        color: $mainBlue;
                        text-align: right;
                        margin: 0px;
                        font-weight: 600;
                        &:nth-of-type(3){
                            color:$pink;
                            font-size:20px;
                            line-height: 24px;
                        }
                    }
                    .hightlight {
                        font-size: 48px;
                        color: $pink;
                        font-weight: 600;
                        margin-left: 4px;
                        margin-right: 2px;
                        -webkit-transform: translateY(5px);
                        transform: translateY(5px);
                        span {
                            font-size: 24px;
                            line-height: 32px;
                        }
                    }
                }
                
            }
            
        }  
    }
    .note{
        color:$gray;
        font-weight:bold;
    }
    .popup-wrapper {
        position: fixed;
        left: 0px;
        top: 0px;
        background-color: rgba(0, 0, 0, 0.5);
        width: 100%;
        height: 100%;
        z-index: 1000;
        .popup-content {
            padding: 105px 80px 30px 80px;
            position: relative;
            background: #FFFFFF;
            box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
            border-radius: 20px;
            position: absolute;
            left: 50%;
            top: 50%;
            -webkit-transform: translate(-50%, -50%);
            transform: translate(-50%, -50%);
            width: 1024px;
            display: none;
            -webkit-box-sizing: border-box;
            box-sizing: border-box;
            scroll-behavior: smooth;
            &.active {
                display: inline;
                display: initial;
            }
          
            .head {
                position: absolute;
                left: 0px;
                top: 0px;
                background-color: $mainBlue;
                border-top-right-radius:50px;
                border-bottom-right-radius:50px;
                padding: 12px 50px 12px 27px;
                h3 {
                    font-size: 30px;
                    margin: 0px;
                    line-height: 1em;
                    color: $popupYellow;
                    span {
                        color: white;
                    }
                }
            }
            .close {
                position: absolute;
                right: 20px;
                top: 20px;
                cursor: pointer;
            }
            .overFrame{
                height:400px;
                overflow-y:scroll;
                box-sizing: border-box;
                padding: 15px 40px;
                border: 2px solid $mainBlue;
                &::-webkit-scrollbar {
                    width: 5px;
                    height: 8px;
                    background: $btnGray;
                    border-radius:10px
                }
                &::-webkit-scrollbar-thumb {
                    border-radius:10px;
                    background-color: $mainBlue; 
                    margin-right:10px;
                }
            }
            .body {
                margin-bottom: 27px;
                .list {
                    display: -webkit-box;
                    display: -ms-flexbox;
                    display: flex;
                    -webkit-box-align: center;
                    -ms-flex-align: center;
                    align-items: center;
                    margin:20px 0;
                    .list-icon {
                        position: relative;
                        p {
                            position: absolute;
                            color: white;
                            left: 50%;
                            top: 50%;
                            -webkit-transform: translate(-50%, -50%);
                            transform: translate(-50%, -50%);
                            margin: 0px;
                            font-size: 22px;
                            font-weight: bold;
                            text-align: center;
                            span {
                                font-size: 36px;
                                line-height: 30px;
                                font-family: 'Noto Sans TC', '微軟正黑體', sans-serif;
                            }
                        }
                    }
                    .list-content {
                        margin-left: 20px;
                        .title {
                            font-size: 24px;
                            margin: 0px;
                            margin-bottom: 9px;
                            font-weight: bold;
                            color: $deepGray;
                            text-align:left;
                            padding:0;
                        }
                        .listCon{
                            font-size: 20px;
                            margin: 0px;
                            color: #000;
                        }
                    }
                }
            }
            .footer {
                text-align: center;
                margin:15px 0;
                .prize {
                    display: -webkit-box;
                    display: -ms-flexbox;
                    display: flex;
                    -webkit-box-align: end;
                    -ms-flex-align: end;
                    align-items: flex-end;
                    margin-bottom: 2px;
                    -webkit-box-pack: center;
                    -ms-flex-pack: center;
                    justify-content: center;
                    p {
                        font-size: 24px;
                        line-height: 35px;
                        color: $mainBlue;
                        text-align: right;
                        margin: 0px;
                        font-weight: 600;     
                    }
                    .hightlight {
                        font-size: 40px;
                        line-height:50px;
                        color: $pink;
                        font-weight: 600;
                        margin-left: 4px;
                        margin-right: 2px;
                        -webkit-transform: translateY(5px);
                        transform: translateY(5px);
                    }
                }
                .safe-terms{
                    font-size: 18px;
                    line-height: 50px;
                }
            }
        }
    }
    
}

</style>