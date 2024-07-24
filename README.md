<html lang="ja">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SDGs Matching</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #bde6bf;
        }

        header {
            background-color: #4cafaf;
            color: white;
            text-align: center;
            padding: 1em 0;
        }

        main {
            padding: 1em;
        }

        h2 {
            color: #333;
        }

        .goal-buttons {
            display: flex;
            flex-wrap: wrap;
            gap: 1em;
        }

        .goal-buttons img {
            width: 100px;
            height: 100px;
            cursor: pointer;
        }

        #companies {
            margin-top: 1em;
        }

        .company {
            background-color: white;
            padding: 1em;
            margin-bottom: 1em;
            border-radius: 5px;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
        }
    </style>
</head>
<body>
    <header>
        <h1>SDGs Matching</h1>
    </header>

    <main>
        <section id="sdgs-goals">
            <h2>SDGsの目標</h2>
            <div class="goal-buttons">
                <img src="CommunityManagers/Images/image1.png" alt="目標1: 貧困をなくそう" onclick="showCompanies(1)">
                <img src="CommunityManagers/Images/image2.png" alt="目標2: 飢餓をゼロに" onclick="showCompanies(2)">
                <img src="CommunityManagers/Images/image3.jpg" alt="目標3: すべての人に健康と福祉を" onclick="showCompanies(3)">
                <img src="CommunityManagers/Images/image4.png" alt="目標4: 質の高い教育をみんなに" onclick="showCompanies(4)">
                <img src="CommunityManagers/Images/image5.png" alt="目標5: ジェンダー平等を実現しよう" onclick="showCompanies(5)">
                <img src="CommunityManagers/Images/image6.png" alt="目標6: 安全な水とトイレを世界中に" onclick="showCompanies(6)">
                <img src="CommunityManagers/Images/image7.png" alt="目標7: エネルギーをみんなにそしてクリーンに" onclick="showCompanies(7)">
                <img src="CommunityManagers/Images/image8.png" alt="目標8: 働きがいも経済成長も" onclick="showCompanies(8)">
                <img src="CommunityManagers/Images/image9.png" alt="目標9: 産業と技術革新の基盤をつくろう" onclick="showCompanies(9)">
                <img src="CommunityManagers/Images/image10.jpg" alt="目標10: 人や国の不平等をなくそう" onclick="showCompanies(10)">
                <img src="CommunityManagers/Images/image11.jpg" alt="目標11: 住み続けられるまちづくりを" onclick="showCompanies(11)">
                <img src="CommunityManagers/Images/image12.png" alt="目標12: つくる責任つかう責任" onclick="showCompanies(12)">
                <img src="CommunityManagers/Images/image13.jpg" alt="目標13: 気候変動に具体的な対策を" onclick="showCompanies(13)">
                <img src="CommunityManagers/Images/image14.jpg" alt="目標14: 海の豊かさを守ろう" onclick="showCompanies(14)">
                <img src="CommunityManagers/Images/image15.jpg" alt="目標15: 陸の豊かさも守ろう" onclick="showCompanies(15)">
                <img src="CommunityManagers/Images/image16.png" alt="目標16: 平和と公正をすべての人に" onclick="showCompanies(16)">
                <img src="CommunityManagers/Images/image17.png" alt="目標17: パートナーシップで目標を達成しよう" onclick="showCompanies(17)">
            </div>
        </section>

        <section id="companies-list">
            <h2>関連する企業</h2>
            <div id="companies"></div>
        </section>
    </main>

    <script>
        const companiesData = {
            1: [
                { name: "Company A", description: "貧困対策に取り組む企業" },
                { name: "Company B", description: "貧困地域への支援を行う企業" }
            ],
            2: [
                { name: "Company C", description: "食糧支援を行う企業" },
                { name: "Company D", description: "農業支援を行う企業" }
            ],
            3: [
                { name: "Company E", description: "医療支援を行う企業" },
                { name: "Company F", description: "健康促進活動を行う企業" }
            ],
            4: [
                { name: "Company G", description: "教育支援を行う企業" },
                { name: "Company H", description: "教育機会を提供する企業" }
            ],
            5: [
                { name: "Company I", description: "ジェンダー平等を推進する企業" },
                { name: "Company J", description: "女性の権利を擁護する企業" }
            ],
            // 他の目標に関連する企業もここに追加
        };

        function showCompanies(goalNumber) {
            const companiesList = document.getElementById('companies');
            companiesList.innerHTML = '';

            const companies = companiesData[goalNumber] || [];
            companies.forEach(company => {
                const companyElement = document.createElement('div');
                companyElement.className = 'company';
                companyElement.innerHTML = `<h3>${company.name}</h3><p>${company.description}</p>`;
                companiesList.appendChild(companyElement);
            });
        }
    </script>
</body>
</html>
