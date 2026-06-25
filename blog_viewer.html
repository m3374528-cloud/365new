<!DOCTYPE html>
<html lang="ko">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>블로그 원고 기초자료 뷰어</title>
<style>
:root {
  --teal:#004D40;--teal-l:#E0F2F1;--amber:#E65100;--amber-l:#FFF3E0;
  --green:#1B5E20;--blue:#0D47A1;--blue-l:#E3F2FD;
  --border:#E0E0E0;--gray-l:#F5F5F5;--text:#212121;--sub:#757575;
}
*{box-sizing:border-box;margin:0;padding:0}
body{font-family:'Noto Sans KR',-apple-system,sans-serif;background:#F5F7FA;color:var(--text);font-size:14px}
.hdr{background:var(--teal);color:#fff;padding:14px 20px;display:flex;align-items:center;justify-content:space-between}
.hdr-title{font-size:17px;font-weight:700}
.hdr-sub{font-size:11px;opacity:.7;margin-top:2px}
.container{max-width:900px;margin:20px auto;padding:0 16px}
.card{background:#fff;border-radius:12px;box-shadow:0 1px 4px rgba(0,0,0,.08);margin-bottom:16px;overflow:hidden}
.card-head{padding:12px 16px;font-size:13px;font-weight:700;color:#fff;display:flex;align-items:center;gap:8px}
.card-head.teal{background:var(--teal)}
.card-head.green{background:var(--green)}
.card-head.amber{background:var(--amber)}
.card-head.blue{background:var(--blue)}
.card-body{padding:16px}
.field-grid{display:grid;grid-template-columns:1fr 1fr;gap:10px}
.field{margin-bottom:10px}
.field:last-child{margin-bottom:0}
.field-label{font-size:11px;font-weight:600;color:var(--sub);text-transform:uppercase;letter-spacing:.04em;margin-bottom:3px}
.field-value{font-size:13px;color:var(--text);padding:8px 10px;background:var(--gray-l);border-radius:6px;min-height:34px;line-height:1.5}
.field-value.highlight{background:var(--teal-l);color:var(--teal);font-weight:600}
.field-value.amber{background:var(--amber-l);color:var(--amber)}
.field-value.empty{color:var(--sub);font-style:italic}
.tag-list{display:flex;flex-wrap:wrap;gap:4px}
.tag{padding:3px 8px;border-radius:12px;font-size:11px;background:var(--teal);color:#fff;font-weight:600}
.divider{height:1px;background:var(--border);margin:12px 0}
.prompt-box{background:#1A1A2E;border-radius:8px;padding:14px;margin-top:8px}
.prompt-box pre{color:#A8E6CF;font-size:12px;line-height:1.7;white-space:pre-wrap;font-family:'Courier New',monospace}
.section-title{font-size:12px;font-weight:700;color:var(--sub);text-transform:uppercase;letter-spacing:.06em;margin-bottom:8px;padding-left:4px}
.cost-row{display:flex;justify-content:space-between;padding:7px 0;border-bottom:1px solid var(--border);font-size:13px}
.cost-row:last-child{border-bottom:none;font-weight:700;color:var(--teal);font-size:14px;padding-top:10px}
.cost-label{color:var(--sub)}
.cost-value{font-weight:600;font-variant-numeric:tabular-nums}
.badge{display:inline-block;padding:2px 8px;border-radius:10px;font-size:11px;font-weight:700}
.badge-test{background:#FF5252;color:#fff}
.badge-real{background:var(--teal);color:#fff}
input[type=text]{width:100%;padding:9px 12px;border:1.5px solid var(--border);border-radius:8px;font-size:14px;font-family:inherit}
input:focus{outline:none;border-color:var(--teal)}
.btn{padding:9px 18px;background:var(--teal);color:#fff;border:none;border-radius:8px;font-size:13px;font-weight:600;cursor:pointer;font-family:inherit}
.btn:hover{background:#00695C}
.loading{text-align:center;padding:40px;color:var(--sub)}
.spinner{width:32px;height:32px;border:3px solid var(--teal-l);border-top-color:var(--teal);border-radius:50%;animation:spin .8s linear infinite;margin:0 auto 10px}
@keyframes spin{to{transform:rotate(360deg)}}
.empty-state{text-align:center;padding:60px 20px;color:var(--sub)}
.prompt-section{margin-top:16px}
.accordion-btn{width:100%;padding:10px 14px;background:var(--blue-l);border:1px solid #90CAF9;border-radius:8px;font-size:13px;font-weight:600;color:var(--blue);cursor:pointer;text-align:left;font-family:inherit}
.accordion-content{display:none;margin-top:8px}
.accordion-content.open{display:block}
</style>
</head>
<body>

<div class="hdr">
  <div>
    <div class="hdr-title">블로그 원고 기초자료 뷰어</div>
    <div class="hdr-sub">작업지시서 데이터 → 블로그 원고 생성 과정 확인</div>
  </div>
</div>

<div class="container">

  <div class="card">
    <div class="card-head teal">프로젝트번호로 조회</div>
    <div class="card-body">
      <div style="display:flex;gap:8px">
        <input type="text" id="projNumInput" placeholder="예) 00244_01_DA1 또는 00000_02_TEST" onkeydown="if(event.key==='Enter')loadData()">
        <button class="btn" onclick="loadData()">조회</button>
      </div>
    </div>
  </div>

  <div id="result"></div>

</div>

<script>
const SCRIPT_URL = 'https://script.google.com/macros/s/AKfycbxPEGAy6Y9fK7Y2M4XWoCNd6DLPjENfLpamzeg9kM27WyvdNzgvoob374pgC27m3tqBCQ/exec';

function fmt(n) { return n ? Math.round(n).toLocaleString('ko-KR') + '원' : '-'; }
function val(v, fallback) { return (v && String(v).trim() && String(v).trim() !== '0') ? String(v).trim() : (fallback || ''); }
function el(id) { return document.getElementById(id); }

function loadData() {
  const projNum = el('projNumInput').value.trim();
  if (!projNum) return;
  
  const result = el('result');
  result.innerHTML = '<div class="loading"><div class="spinner"></div>데이터를 불러오는 중...</div>';
  
  fetch(SCRIPT_URL + '?action=getWorkOrderDetail&projNum=' + encodeURIComponent(projNum))
    .then(r => r.json())
    .then(data => {
      if (!data || data.error) {
        result.innerHTML = '<div class="card"><div class="card-body empty-state">프로젝트번호를 찾을 수 없습니다.<br><small style="color:#bbb">' + (data.error || '') + '</small></div></div>';
        return;
      }
      renderData(data);
    })
    .catch(e => {
      result.innerHTML = '<div class="card"><div class="card-body empty-state">데이터 조회 오류: ' + e.message + '</div></div>';
    });
}

function renderData(d) {
  const isTest = String(d.projNum || '').indexOf('TEST') !== -1;
  const prompt = buildPromptPreview(d);
  
  el('result').innerHTML = `
    <div class="card">
      <div class="card-head teal">
        기본 정보
        <span class="badge ${isTest ? 'badge-test' : 'badge-real'}">${isTest ? 'TEST' : 'REAL'}</span>
      </div>
      <div class="card-body">
        <div class="field-grid">
          <div class="field">
            <div class="field-label">프로젝트번호</div>
            <div class="field-value highlight">${val(d.projNum)}</div>
          </div>
          <div class="field">
            <div class="field-label">접수일시</div>
            <div class="field-value">${val(d.recvDate)}</div>
          </div>
          <div class="field">
            <div class="field-label">사업자구분</div>
            <div class="field-value">${val(d.bizType)}</div>
          </div>
          <div class="field">
            <div class="field-label">영업담당자</div>
            <div class="field-value">${val(d.salesPerson)}</div>
          </div>
        </div>
      </div>
    </div>

    <div class="card">
      <div class="card-head teal">A탭 — 업무내용 (작업신고 담당자 수신본)</div>
      <div class="card-body">
        <div class="prompt-box">
          <pre>${buildEmailPreview(d)}</pre>
        </div>
      </div>
    </div>

    <div class="card">
      <div class="card-head green">C탭 — 공사상세 (블로그 원고 생성 재료)</div>
      <div class="card-body">
        <div class="field-grid">
          <div class="field">
            <div class="field-label">건물유형</div>
            <div class="field-value">${val(d.buildingType, '<span class="empty">미입력</span>')}</div>
          </div>
          <div class="field">
            <div class="field-label">건물 준공연도</div>
            <div class="field-value">${val(d.buildYear, '<span class="empty">미입력</span>')}</div>
          </div>
          <div class="field">
            <div class="field-label">석면 부위/자재</div>
            <div class="field-value">${val(d.asbestosArea, '<span class="empty">미입력</span>')}</div>
          </div>
          <div class="field">
            <div class="field-label">덧방 유무</div>
            <div class="field-value">${val(d.overCoatYn, '<span class="empty">미입력</span>')}</div>
          </div>
          <div class="field">
            <div class="field-label">의뢰경위</div>
            <div class="field-value">${val(d.contactRoute, '<span class="empty">미입력</span>')}</div>
          </div>
          <div class="field">
            <div class="field-label">공사목적</div>
            <div class="field-value">${val(d.workPurpose, '<span class="empty">미입력</span>')}</div>
          </div>
          <div class="field">
            <div class="field-label">현장상태</div>
            <div class="field-value">${val(d.siteStatus, '<span class="empty">미입력</span>')}</div>
          </div>
          <div class="field">
            <div class="field-label">현장제약조건</div>
            <div class="field-value">${val(d.siteLimit, '<span class="empty">미입력</span>')}</div>
          </div>
        </div>
        <div class="divider"></div>
        <div class="field">
          <div class="field-label">예상 작업 포인트</div>
          <div class="field-value">${val(d.keyPoint, '<span class="empty">미입력</span>')}</div>
        </div>
        <div class="field" style="margin-top:10px">
          <div class="field-label">예상 어려움/주의사항</div>
          <div class="field-value">${val(d.surprise, '<span class="empty">미입력</span>')}</div>
        </div>
        <div class="field" style="margin-top:10px">
          <div class="field-label">고객 관심사</div>
          <div class="field-value">${val(d.satisfaction, '<span class="empty">미입력</span>')}</div>
        </div>
        <div class="field" style="margin-top:10px">
          <div class="field-label">유사경험/참고사항</div>
          <div class="field-value">${val(d.tip, '<span class="empty">미입력</span>')}</div>
        </div>
      </div>
    </div>

    <div class="card">
      <div class="card-head amber">B탭 — 원가계산 초안</div>
      <div class="card-body">
        <div class="cost-row"><span class="cost-label">예상 노무비 🔶임시</span><span class="cost-value">${fmt(d.calcLaborAmt)}</span></div>
        <div class="cost-row"><span class="cost-label">예상 외주장비비 🔶임시</span><span class="cost-value">${fmt(d.calcEquipAmt)}</span></div>
        <div class="cost-row"><span class="cost-label">자재비</span><span class="cost-value">${fmt(d.calcMatFee)}</span></div>
        <div class="cost-row"><span class="cost-label">폐기물 처리비 🔶임시</span><span class="cost-value">${fmt(d.calcWasteFee)}</span></div>
        <div class="cost-row"><span class="cost-label">폐기물 운반비 🔶임시</span><span class="cost-value">${fmt(d.calcTransportFee)}</span></div>
        <div class="cost-row"><span class="cost-label">석면조사비</span><span class="cost-value">${fmt(d.calcSurveyFee)}</span></div>
        <div class="cost-row"><span class="cost-label">후측정비</span><span class="cost-value">${fmt(d.calcPostFee)}</span></div>
        <div class="cost-row"><span class="cost-label">감리비</span><span class="cost-value">${fmt(d.calcSuperFee)}</span></div>
        <div class="cost-row"><span class="cost-label">일반관리비 (10%)</span><span class="cost-value">${fmt(d.calcMgmtFee)}</span></div>
        <div class="cost-row"><span>원가 합계 (임시)</span><span class="cost-value">${fmt(d.calcTotal)}</span></div>
      </div>
    </div>

    <div class="card">
      <div class="card-head blue">Claude API 프롬프트 미리보기 (실제 전달 내용)</div>
      <div class="card-body">
        <div class="section-title">이 내용이 Claude에게 전달되어 블로그 원고가 생성됩니다</div>
        <button class="accordion-btn" onclick="toggleAccordion(this)">📋 프롬프트 내용 보기/접기</button>
        <div class="accordion-content">
          <div class="prompt-box" style="margin-top:8px">
            <pre>${escapeHtml(prompt)}</pre>
          </div>
        </div>
        ${d.docUrl ? `
        <div style="margin-top:12px;padding:10px 14px;background:#E8F5E9;border-radius:8px;border:1px solid #A5D6A7">
          <span style="font-size:13px;font-weight:600;color:#1B5E20">✅ 생성된 원고: </span>
          <a href="${d.docUrl}" target="_blank" style="color:#1B5E20;font-size:13px">${d.docUrl}</a>
        </div>` : '<div style="margin-top:12px;padding:10px 14px;background:#FFF3E0;border-radius:8px;border:1px solid #FFCC80;font-size:13px;color:#E65100">⏳ 원고 아직 생성되지 않음</div>'}
      </div>
    </div>
  `;
}

function buildEmailPreview(d) {
  const date = d.workDate ? new Date(d.workDate).toLocaleDateString('ko-KR', {year:'numeric',month:'long',day:'numeric'}) : '미입력';
  return `[업무내용]
프로젝트번호: ${val(d.projNum)}
사업자: ${val(d.bizType)}

1. 공사명: ${val(d.workTitle || d.workContent)}
2. 주소: ${val(d.address)}
3. 공사내용: ${val(d.workContent)}
4. 공사범위: ${val(d.workScope)}
5. 감리 및 측정: ${val(d.superYnA)}
6. 폐기물: ${val(d.wasteVendor)}
7. 발주자 및 담당자: ${val(d.clientPersonName)} ${val(d.clientPhone)}
8. 영업 담당자: ${val(d.salesPerson)}
9. 특이사항: ${val(d.note, '없음')}
10. 공사예정일: ${date}

— 자동 알림 시스템`;
}

function buildPromptPreview(d) {
  const addr = d.address ? d.address.split(' ').slice(0,3).join(' ') : '';
  return `=== 현장 정보 ===
위치: ${addr}
건물유형: ${val(d.buildingType)}
건물준공연도: ${val(d.buildYear)}
공사명: ${val(d.workTitle || d.workContent)}
공사내용: ${val(d.workContent)}
공사범위: ${val(d.workScope)}
석면부위/자재: ${val(d.asbestosArea)}
작업면적: ${val(d.workArea)}㎡
감리및측정: ${val(d.superYnA)}
예상공사기간: ${val(d.estPeriod)}
공사목적: ${val(d.workPurpose)}
현장상태: ${val(d.siteStatus)}
현장제약: ${val(d.siteLimit)}
민원소지: ${val(d.complaintRisk)}
의뢰경위: ${val(d.contactRoute)}
고객관심사: ${val(d.clientRequest)}
예상작업포인트: ${val(d.keyPoint)}
예상어려움: ${val(d.surprise)}
유사경험참고: ${val(d.tip)}

=== 원고 작성 요청 ===
위 현장 정보를 바탕으로 네이버 블로그 원고를 작성해주세요.
건물유형과 공사내용, 현장 상황을 종합해서 제목을 창의적으로 만들어주세요.`;
}

function escapeHtml(text) {
  return text.replace(/&/g,'&amp;').replace(/</g,'&lt;').replace(/>/g,'&gt;');
}

function toggleAccordion(btn) {
  const content = btn.nextElementSibling;
  content.classList.toggle('open');
  btn.textContent = content.classList.contains('open') ? '📋 프롬프트 내용 접기' : '📋 프롬프트 내용 보기/접기';
}
</script>
</body>
</html>
