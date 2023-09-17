# Communicative Agents for Software Development

<p align="center">   <img src='./misc/logo1.png' width=600> </p>

<p align="center">
    【<a href="README.md">English</a> | Chinese | <a href="README-Japanese.md">Japanese</a> | <a href="README-Korean.md">Korean </a>】
</p>

## 📖 概述

- **ChatDev** 是一家**虛擬軟件公司**，通過各種不同角色的**智能體**
  運營，包括執行官、技術官、程序員、測試員等。這些智能體形成了一個多智能體組織結構，其使命是“通過編程改變數字世界”。 ChatDev內的智能體通過參加專業的功能研討會來
  **協作**，包括設計、編碼、測試和文檔編寫等任務。
- ChatDev的主要目標是提供一個基於大型語言模型（LLM）的**易於使用**、**高度可定制**並且**可擴展**的框架，它是研究群體智能的理想場景。

## 📰 新聞

- **2023年9月1日：Art模式現已可用！您可以使用智能體生成軟件中使用的圖像，嘗試 `python3 run.py --config "Art"`。 **
  請參見此處的[示例](/WareHouse/gomokugameArtExample_THUNLP_20230831122822)。
- 2023年8月28日：系統已公開提供使用。
- 2023年8月17日：V1.0.0版本已準備好發布。
- 2023年7月30日：用戶可以自定義ChatChain、Phase和Role設置。此外，現在支持在線Log模式和重放模式。
- 2023年7月16日：與該項目相關的[預印本論文](https://arxiv.org/abs/2307.07924)已發表。
- 2023年6月30日：發布了`ChatDev`倉庫的初始版本。

## ❓ ChatDev能做什麼？

![intro](misc/intro.png)

https://github.com/OpenBMB/ChatDev/assets/11889052/80d01d2f-677b-4399-ad8b-f7af9bb62b72

## ⚡️ 快速開始

要開始使用，按照以下步驟操作：

1. **克隆GitHub存儲庫：** 首先，使用以下命令克隆存儲庫：

   ```
   git clone https://github.com/OpenBMB/ChatDev.git
   ```

2. **設置Python環境：** 確保您具有3.9或更高版本的Python環境。您可以使用以下命令創建並激活環境，可以將`ChatDev_conda_env`
   替換為您喜歡的環境名稱：

   ```
   conda create -n ChatDev_conda_env python=3.9 -y
   conda activate ChatDev_conda_env
   ```

3. **安裝依賴項：** 進入`ChatDev`目錄並運行以下命令來安裝必要的依賴項：

   ```
   cd ChatDev
   pip3 install -r requirements.txt
   ```

4. **設置OpenAI API密鑰：** 將您的OpenAI API密鑰導出為環境變量。將`"your_OpenAI_API_key"`
   替換為您的實際API密鑰。請注意，此環境變量是特定於會話的，因此如果打開新的終端會話，您需要重新設置它。
   在Unix/Linux系統上：

   ```
   export OPENAI_API_KEY="your_OpenAI_API_key"
   ```

   在Windows系統上：

   ```
   $env:OPENAI_API_KEY="your_OpenAI_API_key"
   ```

5. **構建您的軟件：** 使用以下命令啟動生成您的軟件，將`[description_of_your_idea]`替換為您的想法描述，將`[project_name]`
   替換為您想要的項目名稱：
   在Unix/Linux系統上：
   
   ```
   python3 run.py --task "[description_of_your_idea]" --name "[project_name]"
   ```
   
   在Windows系統上：
   
   ```
   python run.py --task "[description_of_your_idea]" --name "[project_name]"
   ```
6. **運行您的軟件：** 生成後，您可以在`WareHouse`
   目錄下的特定項目文件夾中找到您的軟件，例如`project_name_DefaultOrganization_timestamp`。在該目錄中運行以下命令來運行您的軟件：
   在Unix/Linux系統上：
   
   ```
   cd WareHouse/project_name_DefaultOrganization_timestamp
   python3 main.py
   ```
   
   在Windows系統上：
   
   ```
   cd WareHouse/project_name_DefaultOrganization_timestamp
   python main.py
   ```
   
## ✨️ 進階技能

有關更詳細的信息，請參閱我們的[Wiki](wiki.md)，您可以在其中找到：

- 所有命令運行參數的介紹。
- 一個簡單的設置本地Web演示的指南，其中包括增強可視化日誌、重放演示和簡單的ChatChain可視化工具。
- ChatDev框架的概述。
- ChatChain配置中的所有高級參數的全面介紹。
- 自定義ChatDev的指南，包括：
    - ChatChain：設計您自己的軟件開發流程（或任何其他流程），例如`DemandAnalysis -> Coding -> Testing -> Manual`。
    - Phase：在ChatChain內部設計您自己的Phase，比如`DemandAnalysis`。
    - Role：定義您公司內的各種智能體，例如“首席執行官”。

## 🤗 分享您的軟件！

**代碼：** 我們對您參與我們的開源項目表示熱情歡迎。如果您遇到任何問題，請不要猶豫報告它們。如果您準備與我們分享您的工作，隨時創建pull
request！您的貢獻非常寶貴。如果您需要幫助，請聯繫我們！

**公司：** 創建自己定制的“ChatDev公司”非常簡單。此個性化設置涉及三個簡單的配置JSON文件。請查看`CompanyConfig/Default`
目錄中提供的示例。有關自定義的詳細說明，請參閱我們的[Wiki](wiki.md)。

**軟件：** 每當您使用ChatDev開發軟件時，都會生成一個包含所有必要信息的相應文件夾。與我們分享您的工作就像創建一個pull
request一樣簡單。這是一個示例：執行命令`python3 run.py --task "design a 2048 game" --name "2048" --org "THUNLP" --config "Default"`
。這將創建一個軟件包並生成一個名為`/WareHouse/2048_THUNLP_timestamp`的文件夾。其中包括：

- 所有與2048遊戲軟件相關的文件和文檔
- 負責此軟件的公司的配置文件，包括`CompanyConfig/Default`中的三個JSON配置文件
- 描述軟件構建過程的詳細日誌，可用於重播（`timestamp.log`）
- 用於創建此軟件的初始提示（`2048.prompt`）

**參觀社區製造分享的[軟件](Contribution.md)!**

### 軟件分享者

<a href="https://github.com/qianc62"><img src="https://avatars.githubusercontent.com/u/48988402?v=4" alt="Contributor" style="width:5 %; border-radius: 50%;"/></a>
<a href="https://github.com/thinkwee"><img src="https://avatars.githubusercontent.com/u/11889052?v=4" alt="Contributor" style="width:5 %; border-radius: 50%;"/></a>
<a href="https://github.com/NA-Wen"><img src="https://avatars.githubusercontent.com/u/92134380?v=4" alt="Contributor" style="width :5%; border-radius: 50%;"/></a>
<a href="https://github.com/lijiahao2022"><img src="https://avatars.githubusercontent.com/u/111221887?v=4" alt="Contributor" style="width:5 %; border-radius: 50%;"/></a>
<a href="https://github.com/GeekyWizKid"><img src="https://avatars.githubusercontent.com/u/133981481?v=4" alt="Contributor" style="width:5 %; border-radius: 50%;"/></a>

## 📑 引用

```
@misc{qian2023communicative,
      title={Communicative Agents for Software Development}, 
      author={Chen Qian and Xin Cong and Wei Liu and Cheng Yang and Weize Chen and Yusheng Su and Yufan Dang and Jiahao Li and Juyuan Xu and Dahai Li and Zhiyuan Liu and Maosong Sun},
      year={2023},
      eprint={2307.07924},
      archivePrefix={arXiv},
      primaryClass={cs.SE}
}
```

## ⚖️ 許可證

- ChatDev的使用僅限於研究目的。
- 源代碼採用Apache 2.0許可證授權。
- 數據集採用CC BY NC 4.0許可證授權，僅允許非商業用途。請注意，使用這些數據集訓練的任何模型不應用於研究以外的其他目的。

## 星標歷史

[![Star History Chart](https://api.star-history.com/svg?repos=openbmb/chatdev&type=Date)](https://star-history.com/#openbmb/chatdev&Date)

## 聯繫方式

如果您有任何問題、反饋意見或想要聯繫我們，歡迎隨時通過電子郵件與我們聯繫： [chatdev.openbmb@outlook.com](mailto:chatdev.openbmb@outlook.com)
