
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>야구 입문 가이드</title>

    <style>
        :root {
            --blue: #2563eb;
            --yellow: #facc15;
            --bg: #f4f7fc;
            --text: #1e293b;
            --white: #ffffff;
        }

        * {
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            margin: 0;
            font-family: Arial, "Malgun Gothic", sans-serif;
            background: var(--bg);
            color: var(--text);
            line-height: 1.7;
            word-break: keep-all;
            overflow-wrap: break-word;
        }

        header {
            background: var(--blue);
            color: white;
            padding: 22px 6%;
        }

        .top {
            max-width: 1100px;
            margin: auto;
            display: flex;
            align-items: center;
            justify-content: space-between;
            gap: 15px;
            flex-wrap: wrap;
        }

        .logo {
            font-size: 23px;
            font-weight: bold;
        }

        nav {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
        }

        nav a {
            color: white;
            text-decoration: none;
            padding: 8px 10px;
            border-radius: 8px;
        }

        nav a:hover {
            background: #1d4ed8;
        }

        .hero {
            max-width: 1100px;
            margin: 28px auto;
            padding: 55px 25px;
            background: var(--white);
            border-radius: 20px;
            text-align: center;
            border-bottom: 7px solid var(--yellow);
        }

        .hero h1 {
            font-size: clamp(28px, 5vw, 44px);
            margin: 0 0 12px;
        }

        .hero p {
            color: #64748b;
            margin-bottom: 24px;
        }

        .button {
            display: inline-block;
            background: var(--blue);
            color: white;
            padding: 11px 20px;
            border: none;
            border-radius: 10px;
            font-size: 15px;
            text-decoration: none;
            cursor: pointer;
        }

        .button:hover {
            background: #1d4ed8;
        }

        main {
            max-width: 1100px;
            margin: auto;
            padding: 0 20px;
        }

        section {
            margin: 35px 0;
            scroll-margin-top: 20px;
        }

        h2 {
            font-size: 27px;
            margin-bottom: 8px;
        }

        .description {
            color: #64748b;
            margin-top: 0;
        }

        .grid {
            display: grid;
            grid-template-columns: repeat(3, minmax(0, 1fr));
            gap: 18px;
        }

        .card {
            min-width: 0;
            background: white;
            padding: 22px;
            border-radius: 15px;
            border: 1px solid #e2e8f0;
        }

        .card h3 {
            margin-top: 0;
            color: var(--blue);
        }

        .emoji {
            font-size: 30px;
        }

        .highlight {
            background: #fff7cc;
            padding: 3px 7px;
            border-radius: 5px;
        }

        .search-box {
            display: flex;
            gap: 10px;
            margin: 18px 0;
        }

        input, select {
            min-width: 0;
            padding: 12px;
            border: 1px solid #cbd5e1;
            border-radius: 9px;
            font-size: 16px;
        }

        input {
            flex: 1;
            width: 100%;
        }

        input:focus, select:focus {
            outline: 2px solid var(--blue);
            outline-offset: 2px;
        }

        .result {
            margin-top: 15px;
            padding: 18px;
            background: #eff6ff;
            border-radius: 12px;
            min-height: 55px;
        }

        .table-wrap {
            overflow-x: auto;
            background: white;
            border-radius: 12px;
        }

        table {
            width: 100%;
            border-collapse: collapse;
            text-align: center;
        }

        th, td {
            padding: 13px 10px;
            border-bottom: 1px solid #e2e8f0;
        }

        th {
            background: #dbeafe;
        }

        .quiz-options {
            display: grid;
            gap: 10px;
            margin-top: 15px;
        }

        .quiz-options button {
            padding: 12px;
            background: white;
            border: 1px solid #cbd5e1;
            border-radius: 9px;
            text-align: left;
            cursor: pointer;
            font-size: 15px;
        }

        .quiz-options button:hover {
            border-color: var(--blue);
            background: #eff6ff;
        }

        #quizResult {
            font-weight: bold;
            margin-top: 15px;
        }

        .note {
            color: #64748b;
            font-size: 13px;
        }

        footer {
            text-align: center;
            background: #1e293b;
            color: white;
            padding: 25px 15px;
            margin-top: 50px;
        }

        @media (max-width: 700px) {
            .top {
                flex-direction: column;
                align-items: flex-start;
            }

            nav {
                gap: 3px;
            }

            nav a {
                font-size: 14px;
                padding: 7px;
            }

            .hero {
                margin: 18px 12px;
                padding: 35px 18px;
            }

            main {
                padding: 0 14px;
            }

            .grid {
                grid-template-columns: minmax(0, 1fr);
                gap: 12px;
            }

            h2 {
                font-size: 23px;
            }

            .search-box {
                flex-wrap: wrap;
            }

            .search-box .button {
                width: 100%;
            }

            .card {
                padding: 17px;
            }
        }
    </style>
</head>

<body>

<header>
    <div class="top">
        <div class="logo">⚾ 야구 입문 가이드</div>
        <nav>
            <a href="#rules">기본 규칙</a>
            <a href="#terms">야구 용어</a>
            <a href="#players">선수 검색</a>
            <a href="#schedule">경기 일정</a>
            <a href="#ranking">팀 순위</a>
        </nav>
    </div>
</header>

<div class="hero">
    <h1>야구, 처음이어도 괜찮아! ⚾</h1>
    <p>어려운 규칙부터 선수 기록까지, 야구를 쉽고 재미있게 배워 보세요.</p>
    <a class="button" href="#rules">야구 배우러 가기</a>
</div>

<main>

    <section id="rules">
        <h2>⚾ 야구 기본 규칙</h2>
        <p class="description">이것만 알아도 야구 경기를 훨씬 쉽게 볼 수 있어요.</p>

        <div class="grid">
            <article class="card">
                <div class="emoji">🏃</div>
                <h3>점수 내기</h3>
                <p>타자가 공을 치고 1루, 2루, 3루를 돌아 홈으로 들어오면 1점을 얻어요.</p>
            </article>

            <article class="card">
                <div class="emoji">🎯</div>
                <h3>스트라이크와 볼</h3>
                <p>스트라이크가 3개면 삼진, 볼이 4개면 타자는 볼넷으로 1루에 나가요.</p>
            </article>

            <article class="card">
                <div class="emoji">🔄</div>
                <h3>아웃과 이닝</h3>
                <p>공격 팀이 3아웃을 당하면 공격과 수비가 바뀌어요. 일반적인 경기는 9이닝이에요.</p>
            </article>
        </div>
    </section>

    <section id="terms">
        <h2>📚 알아두면 좋은 야구 용어</h2>
        <p class="description">중계에서 자주 나오는 어려운 단어를 쉽게 알아봐요.</p>

        <div class="grid">
            <article class="card">
                <h3>홈런 (Home Run)</h3>
                <p>타자가 친 공이 담장을 넘어가는 등 정해진 조건을 충족하면 타자와 주자가 득점할 수 있어요.</p>
            </article>

            <article class="card">
                <h3>OPS</h3>
                <p>출루율과 장타율을 더한 기록이에요. 타자가 얼마나 자주 출루하고 장타를 치는지 함께 볼 수 있어요.</p>
            </article>

            <article class="card">
                <h3>WAR</h3>
                <p>선수가 대체 선수보다 팀 승리에 얼마나 기여했는지 추정하는 종합 지표예요. 계산 방식에 따라 값이 달라질 수 있어요.</p>
            </article>

            <article class="card">
                <h3>타율</h3>
                <p>안타 수를 타수로 나눈 기록이에요. 예를 들어 타율 0.300은 타수 10번당 안타 3개 수준이에요.</p>
            </article>

            <article class="card">
                <h3>삼진</h3>
                <p>타자가 스트라이크 아웃을 당해 아웃되는 것이에요.</p>
            </article>

            <article class="card">
                <h3>안타</h3>
                <p>타자가 친 공으로 수비 실책 등의 도움 없이 안전하게 출루한 타격을 말해요.</p>
            </article>
        </div>
    </section>

    <section id="players">
        <h2>🔎 선수 검색</h2>
        <p class="description">선수 이름을 입력하고 검색 버튼을 눌러 보세요.</p>

        <div class="search-box">
            <input id="playerName" type="text"
                placeholder="예: 류현진, 노시환, 김도영"
                aria-label="검색할 선수 이름">
            <button class="button" id="searchButton" type="button">선수 검색</button>
        </div>

        <div class="result" id="playerResult" aria-live="polite">
            검색할 선수 이름을 입력해 주세요.
        </div>
        <p class="note">※ 아래 선수 기록은 기능 시연용 예시이며 실제 시즌 기록이 아닙니다.</p>
    </section>

    <section id="schedule">
        <h2>📅 경기 일정</h2>
        <p class="description">경기 일정이 어떻게 표시되는지 확인할 수 있어요.</p>

        <div class="table-wrap">
            <table>
                <thead>
                    <tr>
                        <th>날짜</th>
                        <th>홈팀</th>
                        <th>원정팀</th>
                        <th>경기장</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td>일정 확인 필요</td>
                        <td>한화 이글스</td>
                        <td>상대 팀</td>
                        <td>경기장 확인 필요</td>
                    </tr>
                    <tr>
                        <td>일정 확인 필요</td>
                        <td>LG 트윈스</td>
                        <td>상대 팀</td>
                        <td>경기장 확인 필요</td>
                    </tr>
                </tbody>
            </table>
        </div>
        <p class="note">※ 예시 화면입니다. 실제 경기 일정은 KBO 공식 홈페이지에서 확인하세요.</p>
    </section>

    <section id="ranking">
        <h2>🏆 팀 순위</h2>
        <p class="description">순위표를 읽는 방법을 알아봐요.</p>

        <div class="table-wrap">
            <table>
                <thead>
                    <tr>
                        <th>순위</th>
                        <th>팀</th>
                        <th>경기</th>
                        <th>승</th>
                        <th>패</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td>예시</td>
                        <td>한화 이글스</td>
                        <td>-</td>
                        <td>-</td>
                        <td>-</td>
                    </tr>
                    <tr>
                        <td>예시</td>
                        <td>LG 트윈스</td>
                        <td>-</td>
                        <td>-</td>
                        <td>-</td>
                    </tr>
                    <tr>
                        <td>예시</td>
                        <td>KIA 타이거즈</td>
                        <td>-</td>
                        <td>-</td>
                        <td>-</td>
                    </tr>
                </tbody>
            </table>
        </div>
        <p class="note">※ 실제 순위가 아닌 예시입니다. 최신 순위는 KBO 공식 기록을 확인하세요.</p>
    </section>

    <section id="quiz">
        <h2>🧠 야구 퀴즈</h2>
        <div class="card">
            <h3>문제: 스트라이크가 3개가 되면 어떻게 될까요?</h3>

            <div class="quiz-options">
                <button type="button" data-answer="wrong">① 타자가 1루로 나간다</button>
                <button type="button" data-answer="correct">② 타자가 삼진 아웃된다</button>
                <button type="button" data-answer="wrong">③ 공격 팀이 1점을 얻는다</button>
            </div>

            <p id="quizResult" aria-live="polite">정답이라고 생각하는 항목을 선택해 보세요!</p>
            <button class="button" id="resetQuiz" type="button">다시 풀기</button>
        </div>
    </section>

</main>

<footer>
    <p>⚾ 야구 입문 가이드</p>
    <p>야구를 처음 접하는 사람들을 위한 안내 사이트</p>
</footer>

<script>
    // 선수 검색에 사용할 예시 데이터
    const players = {
        "류현진": {
            team: "한화 이글스",
            position: "투수",
            description: "프로 선수의 기록을 확인할 때는 평균자책점과 탈삼진 등을 살펴보세요."
        },
        "노시환": {
            team: "한화 이글스",
            position: "내야수",
            description: "타자의 기록을 확인할 때는 타율, 홈런, 타점 등을 살펴보세요."
        },
        "김도영": {
            team: "KIA 타이거즈",
            position: "내야수",
            description: "타자의 기록을 확인할 때는 출루율과 장타율도 함께 살펴보세요."
        }
    };

    const playerInput = document.querySelector("#playerName");
    const searchButton = document.querySelector("#searchButton");
    const playerResult = document.querySelector("#playerResult");

    let searchName = "";

    // 검색 결과를 화면에 표시
    function renderPlayer() {
        if (searchName === "") {
            playerResult.textContent = "선수 이름을 입력해 주세요.";
            return;
        }

        const player = players[searchName];

        if (player) {
            playerResult.textContent =
                searchName + " | 팀: " + player.team +
                " | 포지션: " + player.position +
                " | " + player.description;
        } else {
            playerResult.textContent =
                "등록된 예시 정보가 없습니다. 류현진, 노시환, 김도영 중에서 검색해 보세요.";
        }
    }

    // 검색 버튼 클릭
    searchButton.addEventListener("click", function () {
        searchName = playerInput.value.trim();
        renderPlayer();
    });

    // Enter 키로 검색
    playerInput.addEventListener("keydown", function (event) {
        if (event.key === "Enter") {
            searchName = playerInput.value.trim();
            renderPlayer();
        }
    });

    // 퀴즈 선택 기능
    const quizResult = document.querySelector("#quizResult");
    const quizButtons = document.querySelectorAll(".quiz-options button");
    const resetQuiz = document.querySelector("#resetQuiz");

    quizButtons.forEach(function (button) {
        button.addEventListener("click", function () {
            if (button.dataset.answer === "correct") {
                quizResult.textContent = "정답이에요! 스트라이크 아웃으로 타자가 아웃됩니다.";
            } else {
                quizResult.textContent = "아쉬워요! 스트라이크가 3개면 삼진 아웃이에요.";
            }
        });
    });

    // 퀴즈 초기화
    resetQuiz.addEventListener("click", function () {
        quizResult.textContent = "정답이라고 생각하는 항목을 선택해 보세요!";
    });
</script>

</body>
</html>
