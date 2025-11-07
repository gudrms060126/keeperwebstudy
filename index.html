<!doctype html>
<html lang="ko">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Train Note</title>
  <style>
    :root{
      --bg:#f7f8fc;--card:#fff;--text:#101828;--muted:#667085;
      --accent:#2563eb;--accent-weak:rgba(37,99,235,.12);
      --border:#e5e7eb;--radius:14px;--shadow:0 8px 24px rgba(16,24,40,.08);
    }
    *{box-sizing:border-box}
    html,body{height:100%}
    body{margin:0;background:var(--bg);color:var(--text);
      font-family:Inter,Pretendard,-apple-system,"Segoe UI",Roboto,"Noto Sans KR",sans-serif}
    .container{max-width:980px;margin:28px auto;padding:0 20px}
    header{text-align:center;margin-bottom:20px}
    h1{margin:0;font-size:1.6rem}
    .muted{color:var(--muted);font-size:.95rem}
    .layout{display:grid;grid-template-columns:1fr;gap:14px}
    .card{background:var(--card);border:1px solid var(--border);border-radius:var(--radius);
      box-shadow:var(--shadow);padding:16px}
    .card h3{margin:4px 0 8px 0}
    .chips{display:flex;gap:8px;flex-wrap:wrap}
    .chip{padding:8px 12px;border-radius:999px;border:1px solid var(--border);
      background:#fff;cursor:pointer;user-select:none}
    .chip.active{background:var(--accent-weak);border-color:var(--accent);color:var(--accent);font-weight:600}
    .grid{display:grid;gap:12px}
    .cols-2{grid-template-columns:1fr 1fr}
    @media(max-width:700px){.cols-2{grid-template-columns:1fr}}
    label.small{display:block;font-size:.9rem;color:var(--muted);margin-bottom:6px}
    input,textarea,select{width:100%;padding:10px 12px;border:1px solid var(--border);
      border-radius:10px;background:#fff;font:inherit;color:inherit}
    textarea{min-height:80px;resize:vertical}
    .btn{padding:10px 14px;border-radius:10px;border:1px solid var(--border);
      background:var(--accent);color:#fff;cursor:pointer;font-weight:600}
    .entry{border-top:1px dashed var(--border);padding:10px 0}
    .entry:first-child{border-top:0}
    .date-block{border:1px solid var(--border);border-radius:12px;padding:12px;margin:10px 0;background:#fff}
    .date-title{font-weight:700;margin-bottom:6px}
    .subhead{font-weight:600;margin-top:6px}
    .row{display:flex;gap:10px;align-items:center;flex-wrap:wrap}
    footer{margin-top:20px;text-align:center;color:var(--muted);font-size:.9rem}
  </style>
</head>
<body>
  <div class="container">
    <header>
      <h1>Train Note</h1>
      <div class="muted">오늘의 운동과 식단을 간단하게 기록하세요.</div>
    </header>

    <main class="layout">
      <!-- 운동 부위 -->
      <section class="card">
        <h3>운동 부위 선택</h3>
        <p class="muted">오늘은 어디를 운동했나요? (중복 선택 가능)</p>
        <div class="chips" id="bodyChips"></div>
      </section>

      <!-- 운동 기록 -->
      <section class="card">
        <h3>운동 기록 추가</h3>
        <div class="grid cols-2">
          <div>
            <label class="small">날짜</label>
            <input type="date" id="exerciseDate">
          </div>
          <div>
            <label class="small">운동 이름</label>
            <input id="exerciseName" placeholder="예: 스쿼트, 벤치프레스">
          </div>
        </div>
        <div style="margin-top:10px">
          <label class="small">메모</label>
          <textarea id="exerciseMemo" placeholder="예: 3세트 × 10회, 80kg"></textarea>
        </div>
        <div style="text-align:right;margin-top:10px">
          <button class="btn" id="addExercise">운동 추가</button>
        </div>
      </section>

      <section class="card">
        <h3>운동 로그</h3>
        <div id="exerciseList" class="muted">아직 기록이 없습니다.</div>
      </section>

      <!-- 식단 기록 -->
      <section class="card">
        <h3>식단 기록 추가</h3>
        <div class="grid cols-2">
          <div>
            <label class="small">날짜</label>
            <input type="date" id="dietDate">
          </div>
          <div>
            <label class="small">식사 유형</label>
            <select id="mealType">
              <option value="아침">아침</option>
              <option value="점심">점심</option>
              <option value="저녁">저녁</option>
              <option value="간식">간식</option>
            </select>
          </div>
        </div>
        <div style="margin-top:10px">
          <label class="small">메뉴 / 칼로리 메모</label>
          <textarea id="dietMemo" placeholder="예: 닭가슴살 150g, 샐러드 350kcal"></textarea>
        </div>
        <div style="text-align:right;margin-top:10px">
          <button class="btn" id="addDiet">식단 추가</button>
        </div>
      </section>

      <section class="card">
        <h3>식단 로그</h3>
        <div id="dietList" class="muted">아직 기록이 없습니다.</div>
      </section>

      <!-- 전체 로그 (월별 필터 + 날짜별 묶음) -->
      <section class="card">
        <h3>전체 로그</h3>
        <div class="row" style="margin-bottom:10px">
          <label for="monthFilter" class="small" style="margin:0">월 선택</label>
          <input type="month" id="monthFilter" />
          <button class="btn" id="applyMonth">보기</button>
          <div class="muted" id="monthHint"></div>
        </div>
        <div id="combinedList" class="muted">아직 기록이 없습니다.</div>
      </section>
    </main>

    <footer>새로고침 시 데이터는 사라짐</footer>
  </div>

  <script>
    const BODY_PARTS = ['등','가슴','하체','어깨','팔','복근','유산소','전신'];
    const bodyChips = document.getElementById('bodyChips');
    const exerciseDate = document.getElementById('exerciseDate');
    const exerciseName = document.getElementById('exerciseName');
    const exerciseMemo = document.getElementById('exerciseMemo');
    const addExercise = document.getElementById('addExercise');
    const exerciseList = document.getElementById('exerciseList');
    const dietDate = document.getElementById('dietDate');
    const mealType = document.getElementById('mealType');
    const dietMemo = document.getElementById('dietMemo');
    const addDiet = document.getElementById('addDiet');
    const dietList = document.getElementById('dietList');
    const combinedList = document.getElementById('combinedList');
    const monthFilter = document.getElementById('monthFilter');
    const applyMonth = document.getElementById('applyMonth');
    const monthHint = document.getElementById('monthHint');

    const today = new Date().toISOString().slice(0,10);
    const thisMonth = new Date().toISOString().slice(0,7); // YYYY-MM
    exerciseDate.value = today;
    dietDate.value = today;
    monthFilter.value = thisMonth;
    monthHint.textContent = '선택된 월의 기록만 보여줍니다.';

    for(let i=0;i<BODY_PARTS.length;i++){
      const b=document.createElement('button');
      b.type='button';
      b.className='chip';
      b.textContent=BODY_PARTS[i];
      b.addEventListener('click',()=>b.classList.toggle('active'));
      bodyChips.appendChild(b);
    }

    const state={exercises:[],diets:[]};

    function renderExerciseList(){
      if(state.exercises.length===0){exerciseList.textContent='아직 기록이 없습니다.';return;}
      exerciseList.innerHTML='';
      for(let e of state.exercises){
        const div=document.createElement('div');
        div.className='entry';
        div.innerHTML='<strong>'+e.name+'</strong><div class="meta">'+e.date+' · '+(e.parts.length?e.parts.join(', '):'부위 미지정')+'</div>'+(e.memo?'<div>'+e.memo+'</div>':'');
        exerciseList.appendChild(div);
      }
    }
    function renderDietList(){
      if(state.diets.length===0){dietList.textContent='아직 기록이 없습니다.';return;}
      dietList.innerHTML='';
      for(let d of state.diets){
        const div=document.createElement('div');
        div.className='entry';
        div.innerHTML='<strong>['+d.meal+']</strong> '+d.date+(d.memo?'<div>'+d.memo+'</div>':'');
        dietList.appendChild(div);
      }
    }

    // 월별 필터를 적용해 날짜별로 운동+식단 묶어 출력
    function renderCombined(){
      const month = monthFilter.value; // 'YYYY-MM'
      const byDate = {}; // { 'YYYY-MM-DD': {exercises:[], diets:[]} }

      for(let e of state.exercises){
        if(!e.date.startsWith(month)) continue;
        if(!byDate[e.date]) byDate[e.date] = {exercises:[], diets:[]};
        byDate[e.date].exercises.push(e);
      }
      for(let d of state.diets){
        if(!d.date.startsWith(month)) continue;
        if(!byDate[d.date]) byDate[d.date] = {exercises:[], diets:[]};
        byDate[d.date].diets.push(d);
      }

      const dates = Object.keys(byDate).sort((a,b)=> b.localeCompare(a)); // 최신 날짜 우선
      if(dates.length===0){combinedList.textContent='선택한 월에는 기록이 없습니다.';return;}

      combinedList.innerHTML='';
      for(let dt of dates){
        const block = document.createElement('div');
        block.className = 'date-block';

        const title = document.createElement('div');
        title.className = 'date-title';
        title.textContent = dt;
        block.appendChild(title);

        const data = byDate[dt];

        if(data.exercises.length){
          const sh = document.createElement('div');
          sh.className = 'subhead';
          sh.textContent = '운동';
          block.appendChild(sh);

          for(let e of data.exercises){
            const row = document.createElement('div');
            row.className='entry';
            row.innerHTML =
              '<strong>'+e.name+'</strong>' +
              '<div class="meta">'+ (e.parts.length? e.parts.join(', ') : '부위 미지정') +'</div>' +
              (e.memo ? '<div style="margin-top:6px">'+ e.memo.replaceAll('<','&lt;').replaceAll('>','&gt;').replaceAll('\\n','<br>') +'</div>' : '');
            block.appendChild(row);
          }
        }

        if(data.diets.length){
          const sh2 = document.createElement('div');
          sh2.className = 'subhead';
          sh2.textContent = '식단';
          block.appendChild(sh2);

          for(let d of data.diets){
            const row = document.createElement('div');
            row.className='entry';
            row.innerHTML =
              '<strong>['+d.meal+']</strong>' +
              (d.memo ? '<div style="margin-top:6px">'+ d.memo.replaceAll('<','&lt;').replaceAll('>','&gt;').replaceAll('\\n','<br>') +'</div>' : '');
            block.appendChild(row);
          }
        }

        combinedList.appendChild(block);
      }
    }

    addExercise.addEventListener('click',()=>{
      const date=exerciseDate.value||today;
      const name=(exerciseName.value||'').trim();
      const memo=(exerciseMemo.value||'').trim();
      if(!name){alert('운동 이름을 입력하세요.');return;}
      const parts=Array.from(document.querySelectorAll('.chip.active')).map(x=>x.textContent);
      state.exercises.push({date,name,memo,parts});
      renderExerciseList();
      exerciseName.value='';exerciseMemo.value='';
      renderCombined(); // 월별+날짜별 묶음 갱신
    });

    addDiet.addEventListener('click',()=>{
      const date=dietDate.value||today;
      const meal=mealType.value;
      const memo=(dietMemo.value||'').trim();
      if(!memo){alert('식단 내용을 입력하세요.');return;}
      state.diets.push({date,meal,memo});
      renderDietList();
      dietMemo.value='';
      renderCombined(); // 월별+날짜별 묶음 갱신
    });

    applyMonth.addEventListener('click', renderCombined);
    monthFilter.addEventListener('change', renderCombined);

    // 초기 렌더
    renderCombined();
  </script>
</body>
</html>
