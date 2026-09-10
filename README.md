*[Read in English](README.en.md)*

# 詮釋權宣言 / interpretive-sovereignty

這不只是一個工具，是一份藝術行動與宣言。

在AI技術得以無需同意就擷取、模仿、販售原住民族的圖騰、祭儀、歌謠與神話的此刻，詮釋權——誰有資格說出這個故事——正從文化的主人手中悄悄轉移到訓練資料的擁有者手中。

完整的立場、控訴與宣告，請讀 **[MANIFESTO.md](MANIFESTO.md)**。

這份 repository 把宣言變成一個真正能運作的 [Claude Code](https://claude.com/claude-code) skill：`interpretive-sovereignty`。它在 Claude 生成涉及原住民族傳統文化元素（圖像、敘事、音樂舞蹈描述、程式碼或設計中的文化素材）的內容前，要求使用者提供社群同意佐證；沒有佐證，就拒絕生成，並說明如何取得授權。

參考依據：台灣《[原住民族傳統智慧創作保護條例](https://law.moj.gov.tw/LawClass/LawAll.aspx?pcode=D0130021)》、[CARE Principles for Indigenous Data Governance](https://www.un.org/digital-emerging-technologies/sites/www.un.org.techenvoy/files/GDC-submission_WAMPUM_Lab_and_the_Collaboratory_for_Indigenous.pdf)、[Local Contexts TK Labels](https://localcontexts.org/labels/traditional-knowledge-labels/)。

## 加入這份宣告：安裝方式

**方法一：複製到個人設定（全域適用所有專案）**

```bash
git clone https://github.com/<your-username>/<repo-name>.git
cp -r <repo-name>/.claude/skills/interpretive-sovereignty ~/.claude/skills/
```

**方法二：加到單一專案**

```bash
cp -r <repo-name>/.claude/skills/interpretive-sovereignty <your-project>/.claude/skills/
```

安裝後 Claude Code 會自動讀取 `SKILL.md` 的 `description`，在相關情境下自動觸發，不需要手動呼叫。

## 這個 skill 實際上會做什麼

1. 偵測請求是否涉及特定原住民族的傳統文化表達（圖騰、祭儀、神話、歌舞、服飾等）
2. 未附上同意佐證（部落/協會授權文件、原民會核准字號、Local Contexts TK Label 編號等）→ 直接拒絕生成，並以宣言的立場說明為何拒絕、如何取得授權
3. 已附上佐證 → 生成內容，但註明「依使用者聲明已取得授權」

詳細判斷邏輯見 [SKILL.md](.claude/skills/interpretive-sovereignty/SKILL.md)，法律與框架依據見 [reference.md](.claude/skills/interpretive-sovereignty/reference.md)。

## 誠實的限制

這是**行為指引**，不是技術鎖。Claude 無法驗證使用者提供的佐證是否真實，也無法阻止使用者移除或繞過這份 skill。一份宣言的力量不在於它能強制誰，而在於它讓「未經同意不得生成」成為使用者自己選擇遵守的預設立場。商業用途或大規模發布，仍應直接洽詢相關部落、原住民族委員會或 Local Contexts 取得正式授權——這份工具不構成法律合規保證。

## 加入這份行動

在擴充或修改判斷邏輯之前，建議實際與原住民族相關組織（部落、族群文化發展協會、原住民族委員會）討論用詞與判斷標準是否恰當，避免在缺乏社群參與的情況下由外部單方面訂定規則。歡迎透過 Issue / PR 加入你的聲音，或直接分享給任何一個你認為需要看到這份宣言的人。

## License

本 repository 的程式碼與文件採用 [MIT License](LICENSE) 授權；但這不代表 skill 所保護的原住民族傳統文化內容本身的權利歸屬——那些內容的權利仍屬於相關原住民族社群所有。
