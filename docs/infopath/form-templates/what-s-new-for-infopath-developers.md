---
title: InfoPath 開発者向けの新機能
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- what's new [infopath 2007],developer features [InfoPath 2007],InfoPath 2007, what's new,new features [InfoPath 2007]
localization_priority: Normal
ms.assetid: d0ad3111-bd41-4f35-8a34-62c17f20fc19
description: InfoPath を使用すると、Microsoft SharePoint Server プラットフォームで充実したフォーム ベースのアプリケーションを簡単に構築できます。Microsoft SharePoint Server 2013 および InfoPath Forms Services と連携する Microsoft InfoPath 2013 には、開発者向けのさまざまな機能が用意されています。SharePoint Server 2013 で利用できる InfoPath Forms Services により、InfoPath フォーム テンプレートを SharePoint Server に展開できるため、InfoPath リッチ クライアントをインストールしていないユーザーは Web ブラウザーで InfoPath フォームを開いて入力できます。
ms.openlocfilehash: a11c6b4018e60a470197ecd7ffdf3b79a13658b9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799223"
---
# <a name="whats-new-for-infopath-developers"></a>InfoPath 開発者向けの新機能

InfoPath を使用すると、Microsoft SharePoint Server プラットフォームで充実したフォーム ベースのアプリケーションを簡単に構築できます。Microsoft SharePoint Server 2013 および InfoPath Forms Services と連携する Microsoft InfoPath 2013 には、開発者向けのさまざまな機能が用意されています。SharePoint Server 2013 で利用できる InfoPath Forms Services により、InfoPath フォーム テンプレートを SharePoint Server に展開できるため、InfoPath リッチ クライアントをインストールしていないユーザーは Web ブラウザーで InfoPath フォームを開いて入力できます。
  
InfoPath 2013 を使用して作成されたフォーム テンプレートでは、 **Microsoft.Office.InfoPath** 名前空間のクラスとメンバーに対して記述されたビジネス ロジックが引き続きサポートされます。このビジネス ロジックは、InfoPath Filler で開いたフォームでも、Web ブラウザーで開いたフォームでも同様に動作します。このマネージ オブジェクト モデルに対して記述されたビジネス ロジックを使用し、InfoPath Designer のデザイン チェック機能を利用することで、単一のフォーム テンプレートを作成し、適切に構成された SharePoint Server 2013 のドキュメント ライブラリに展開できます。展開したフォーム テンプレートは InfoPath Filler と Web ブラウザーの両方で動作します。 
  
## <a name="new-features-and-improvements"></a>新機能と強化された機能

以下のセクションでは、InfoPath の開発者にとって役立つ次の新機能と強化された機能について簡単に説明します。
  
- コードを作成および編集する新しい方法
    
- SharePoint サンドボックス ソリューション
    
- 1 クリックでのフォームの発行
    
- SharePoint リスト フォームの拡張
    
- InfoPath フォーム Web パーツを使用したポータル ページ上でのフォームのホスト
    
- さらに豊富になった Web フォーム
    
- 標準に準拠したブラウザー フォーム
    
- デジタル署名による情報のセキュリティと整合性の強化
    
- 新しいコントロール
    
## <a name="new-way-to-write-and-edit-code"></a>コードを作成および編集する新しい方法

InfoPath 2013 では、InfoPath 2010 と統合されていた Microsoft Visual Studio Tools for Applications IDE が削除されました。InfoPath 2013 でフォーム コードを作成または編集するには、[Microsoft Visual Studio Tools for Applications 2012](http://www.microsoft.com/en-us/download/details.aspx?id=38807) アドオンがインストールされた Visual Studio 2012 が必要となります。プログラミング作業自体は基本的に変わっていませんが、InfoPath フォームのマネージ コードを作成する際に Visual Studio での開発経験を最大限に活用できるようになりました。 
  
以下のセクションでは、InfoPath 2010 と SharePoint Server 2010 で初めて追加され、InfoPath 2013 と SharePoint Server 2013 を使用する開発者にとって付加価値となる機能について説明します。
  
## <a name="sharepoint-server-sandboxed-solutions"></a>SharePoint Server サンドボックス ソリューション

InfoPath では、コードを含むフォームをこれまでよりも簡単に SharePoint Server 2013 に展開できます。Office InfoPath 2007 では、コードを含むフォームはすべて SharePoint ファーム管理者が承認し、アップロードする必要がありました。SharePoint Server 2013 では、セキュリティで保護されたソリューションがサポートされているため、サイト コレクションの管理権限を持つフォーム作成者は、コードを含むほとんどのフォームを SharePoint サイトに直接発行できるようになりました。サーバーのリソース クォータ設定により、リソースが過剰に使用されることはなくなります。サイト コレクション管理者が引き続き管理権を持ち、ソリューションの信頼性について判断します。ファーム管理者が関与する必要はありません。InfoPath フォーム テンプレートをセキュリティで保護されたソリューションとして発行する方法の詳細については、「[コードを含むフォームを発行する](publishing-forms-with-code.md)」を参照してください。
  
## <a name="publish-forms-with-one-click"></a>1 クリックでのフォームの発行

InfoPath では、これまでよりも簡単にフォームの更新を発行できます。フォーム テンプレートを初めて発行した後、いくつかのダイアログ ボックスを順にクリックしていくのではなく、新しい [ **クイック発行**] ボタンを 1 回クリックするだけで作業を完了できます。このボタンは、[ **クイック アクセス ツール バー**] と新しい Microsoft Office Backstage ([ **ファイル**] タブをクリックして表示) に用意されています。 
  
## <a name="enhance-sharepoint-list-forms"></a>SharePoint リスト フォームの強化

InfoPath を使用して、SharePoint リスト内のアイテムの作成、編集、および表示に使用するフォームを拡張し強化できるようになりました。リストを開き、[ **リスト ツール**] の [ **リスト**] タブをクリックして、[ **フォームのユーザー設定**] をクリックすることで、すぐに利用できる既定の SharePoint リスト フォームに似た InfoPath フォームを自動生成できます。InfoPath で、レイアウトの変更、追加のビューの作成、ルールやデータ検証の追加などを行うことで、このフォームをカスタマイズし、強化できます。リスト フォームの変更作業が終了したら、InfoPath の新しい 1 クリック発行機能を使用して SharePoint に発行できます。
  
## <a name="host-forms-on-portal-pages-using-the-infopath-form-web-part"></a>InfoPath フォーム Web パーツを使用したポータル ページ上でのフォームのホスト

SharePoint Server 2013 では、新しい **InfoPath フォーム Web パーツ**を使用して、これまでよりも簡単に Web ページ上でフォームをホストできます。 Microsoft Office SharePoint Server 2007 では、ユーザーが Visual Studio でコードを記述しなければ、InfoPath フォームを Web ページでホストすることはできません。 現在、コードを 1 行も作成せずに、**InfoPath フォーム Web パーツ**を使用して SharePoint リストやフォーム ライブラリに発行する任意の InfoPath ブラウザー フォームをホストできるようになっています。それには、**InfoPath フォーム Web パーツ**を Web パーツのページに追加して、そのパーツで発行済みフォームを指せばよいだけです。 また、InfoPath フォーム Web パーツをページ上の他の Web パーツに接続して、データを送受信することもできます。 **InfoPath フォーム Web パーツ**の使用方法の詳細については、SharePoint 2010 SDK の「[InfoPath フォーム Web パーツの使用](http://msdn.microsoft.com/library/bb87e126-1a07-45aa-af36-b294df3a2576%28Office.15%29.aspx)」を参照してください。 
  
## <a name="richer-web-forms"></a>さらに豊富になった Web フォーム

クライアント フォームとブラウザー フォームの機能の差が少なくなり、すべてのユーザーのフォーム入力操作について一貫性が高まります。ブラウザー フォームで次のコントロールや機能がサポートされるようになりました。
  
- 箇条書き、段落番号、および標準リスト
    
- 複数選択リスト ボックス
    
- コンボ ボックス
    
- ピクチャ ボタン
    
- ハイパーリンク機能
    
- 選択肢グループおよびセクション 
    
- 日付と時刻コントロール
    
- ユーザー/グループの選択
    
- フィルター機能
    
## <a name="standards-compliant-browser-forms"></a>標準に準拠したブラウザー フォーム

InfoPath ブラウザー フォームは WCAG 2.0 (Web Content Accessibility Guidelines 2.0) の AA に準拠するようになったため、フォーム作成者は障碍のあるユーザーが利用できるフォームを作成できます。
  
## <a name="provide-enhanced-information-security-and-integrity-with-digital-signatures"></a>デジタル署名による情報のセキュリティと整合性の強化

InfoPath は、CNG (Cryptography Next Generation) のデジタル署名されたコンテンツをサポートしています。フォームに含まれる情報の整合性を確保するために、InfoPath クライアントと SharePoint Server 2013 には、フォーム全体またはフォームの各セクションに対する単一署名、連署、副署の各シナリオの実現に必要なコントロールが用意されています。フォームへの署名は、Internet Explorer で ActiveX 署名欄コントロールを使用して実行できます。署名済みフォームは、SharePoint Server 2013 でサポートされているどのブラウザーでも表示できます。
  
## <a name="new-controls"></a>新しいコントロール

InfoPath では、フォームに追加できるコントロールがより豊富になっています。いくつかの新しいコントロールについて以下に簡単に説明します。
  
- **ピクチャ ボタン** - 従来の灰色の四角形に代わって、フォームで任意の画像をボタンとして使用できます。 
    
- **ハイパーリンク** - ユーザーはフォームへの入力時に独自のハイパーリンクを入力できます。 
    
- **ユーザー/グループの選択** - ユーザーはフォームへの入力時にアカウント名およびグループの確認や問い合わせを実行できます。 
    
- **エンティティの選択** - ユーザーはフォームへの入力時に、SharePoint Server 2013 を実行しているサーバー上の外部リストから値を選択できます。 
    
- **署名欄** - ユーザーはフォームへのデジタル署名時に署名欄または印鑑イメージを使用できます。 
    
## <a name="see-also"></a>関連項目



[コードを含む InfoPath フォーム テンプレートを開発する](developing-infopath-form-templates-with-code.md)
  
[InfoPath 2003 オブジェクト モデルを使用してフォーム テンプレートを開発する](developing-form-templates-using-the-infopath-2003-object-model.md)

