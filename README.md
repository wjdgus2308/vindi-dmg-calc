<script src="calc.js"></script>
<div id='calc' style='width: 360px;'>
    <div id='input'>
        <table style='table-layout:fixed;'>
            <col width="205px" />
            <col width="200px" />
            <tr>
                <td nowrap>대상 (보스)</td>
                <td>
                    <select id="boss" style='width:100%;' onchange="if(this.value == 'custom') {document.querySelectorAll('.customstat')[0].style.display='';document.querySelectorAll('.customstat')[1].style.display='';} else {document.querySelectorAll('.customstat')[0].style.display='none';document.querySelectorAll('.customstat')[1].style.display='none';}">
                        <option label="6종" value="lvl90raids"></option>
                        <option label="듀라한" value="dullahan"></option>
                        <option label="에스 시더" value="aessidhe"></option>
                        <option label="아르카나" value="arcana"></option>
                        <option label="루파키투스" value="rupacitus"></option>
                        <option label="클레르" value="claire"></option>
                        <option label="폭주한 엘쿨루스" value="elchulus"></option>
                        <option label="마하" value="macha"></option>
                        <option label="아가레스" value="agares"></option>
                        <option label="루(팔라라)" value="lugh"></option>
                        <option label="스페셜 던전" value="special"></option>
                        <option label="네반" value="neamhain"></option>
                        <option label="발로르" value="balor"></option>
                        <option label="[헬] 결사대" value="hell"></option>
                        <option label="사용자 지정" value="custom"></option>
                    </select>
                </td>
            </tr>
            <tr class='customstat' style='display: none;'>
                <td nowrap>보스 방어력</td>
                <td><input id='bossdef' value='0'></td>
            </tr>
            <tr class='customstat' style='display: none;'>
                <td nowrap>보스 크리티컬 저항</td>
                <td><input id='bossres' value='0'></td>
            </tr>
            <tr>
                <td nowrap>공격력</td>
                <td><input id='atk' value='0'></td>
            </tr>
            <tr>
                <td nowrap>추가피해</td>
                <td><input id='add' value='0'></td>
            </tr>
            <tr>
                <td nowrap>공격력 제한 해제</td>
                <td><input id='alr' value='0'></td>
            </tr>
            <tr>
                <td nowrap>밸런스</td>
                <td><input id='bal' value='0'></td>
            </tr>
            <tr>
                <td nowrap>크리티컬</td>
                <td><input id='cri' value='0'></td>
            </tr>
        </table>
        <button style='width: 100%;' onclick='calc();'>계산</button>
    </div>
    <div id='output'>
        <table style='table-layout:fixed;'>
            <col width="205px" />
            <col width="200px" />
            <tr>
                <td nowrap>유효전투력(크리 미적용)</td>
                <td><input id='nocritdmg' readonly></td>
            </tr>
            <tr>
                <td nowrap>유효전투력(크리 적용)</td>
                <td><input id='critdmg' readonly></td>
            </tr>
        </table>
    </div>
</div>
