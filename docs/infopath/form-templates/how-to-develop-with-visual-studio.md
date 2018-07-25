---
title: Visual Studio で開発する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e39d633d-d8fb-4e2f-a396-6cb50beb8c3e
description: Visual Studio 2012 で開発したマネージ コードを使用して InfoPath フォームを拡張することによって、フォームの機能を大幅に強化できます。フォームを拡張したら、コードを含むフォームを SharePoint Server 2013 のフォーム ライブラリに発行できます。
ms.openlocfilehash: d6a2cfa1847b4b59b6978b8f4a0775aedf07a72d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799133"
---
# <a name="develop-with-visual-studio"></a>Visual Studio で開発する

Visual Studio 2012 で開発したマネージ コードを使用して InfoPath フォームを拡張することによって、フォームの機能を大幅に強化できます。フォームを拡張したら、コードを含むフォームを SharePoint Server 2013 のフォーム ライブラリに発行できます。
  
マネージ コードを含む InfoPath フォームのプログラミングと展開は、次の 3 つの大まかな手順で始めることができます。
  
1. Visual Studio 2012 を [Microsoft Visual Studio Tools for Applications 2012](http://www.microsoft.com/en-us/download/details.aspx?id=38807) アドオンと共にインストールします。 
    
2. プログラミング言語を設定し、Visual Studio 2012 コード エディターでコードを記述してデバッグします。
    
3. フォームのデザインとコードの開発が完了したら、フォーム テンプレートを SharePoint Server 2013 に発行できます。
    
次の理由から、SharePoint Server 2013 と互換性のあるフォームを作成することを検討してください。
  
- InfoPath Forms Services を実行している SharePoint Server 2013 にフォームを展開すると、ブラウザーでフォームに入力できます。これにより、InfoPath をインストールしていないユーザーもフォームを開いて使用できるようになります。
    
- デザインするフォームのバージョンを 1 つに限定できます。Microsoft SharePoint Server と互換性のあるフォームは InfoPath Filler とも互換性がありますが、InfoPath Filler としか互換性のないフォームをブラウザーで開くことはできません。
    
フォームを SharePoint に発行する方法としては、SharePoint のセキュリティで保護されたソリューションと管理者が展開するソリューションの 2 つがあります。それぞれの発行方法と、現在のシナリオに最適な方法を判断する際の推奨事項の詳細については、「[コードを含むフォームを発行する](publishing-forms-with-code.md)」を参照してください。セキュリティで保護されたソリューションの例については、「[サンドボックス ソリューションのサンプル](sample-sandboxed-solutions.md)」を参照してください。
  
## <a name="developing-with-visual-studio"></a>Visual Studio での開発

Visual Studio 2012 と Microsoft Visual Studio Tools for Applications 2012 アドオンをインストールしたら、InfoPath マネージ コード ソリューションの開発をいつでも開始できます。
  
### <a name="choosing-a-programming-language"></a>プログラミング言語の選択

InfoPath では、Visual Basic と C# の 2 種類の言語で 4 つのバージョンの InfoPath オブジェクト モデルを使用することによって、プログラミングのためのオプションを提供しています。4 つのバージョンのオブジェクト モデルは、InfoPath 2013、InfoPath、Office InfoPath 2007、および Microsoft InfoPath 2003 と互換性があります。
  
### <a name="to-specify-the-programming-language-and-object-model"></a>プログラミング言語とオブジェクト モデルを指定するには

1. InfoPath デザイン モードでフォーム テンプレート プロジェクトを開いた状態で、[ **開発**] タブの [ **言語**] をクリックします。 
    
2. [ **フォームのオプション**] ダイアログ ボックスの [ **プログラミング**] カテゴリで、[ **フォーム テンプレートのコード言語**] ボックスの一覧から使用する言語を選択します。[ **ターゲット バージョン**] ボックスの一覧からオブジェクト モデルのバージョンを選択します。InfoPath 2013 としか互換性のない **ターゲット バージョン** オプションには、" **InfoPath**" という名前の後にバージョンを表す年が付いていません。 
    
    > [!NOTE]
    > すべての種類のフォーム テンプレートがコードをサポートしているわけではありません。たとえば、 **SharePoint リスト** フォーム テンプレートと **テンプレート パーツ**は、フォーム コードをサポートしていません。コードをサポートしていないフォーム テンプレートをデザインする場合、[ **開発**] タブは使用できません。また、4 つのバージョンのオブジェクト モデルをすべてサポートしているのは一部のフォーム テンプレートに限られます。たとえば、 **空白のフォーム (InfoPath Filler)** テンプレートは、4 つのバージョンのオブジェクト モデルをすべてサポートしており、各バージョンでは InfoPath Filler とのみ互換性があるフォーム テンプレートが作成されます。しかし、 **空白のフォーム** テンプレートは InfoPath 2013 と InfoPath だけをサポートしており、InfoPath Filler とブラウザーの両方と互換性があるフォーム テンプレートが作成されます。 
  
    既定のプログラミング言語を設定できます。その場合、InfoPath フォーム デザイナーは選択した言語とオブジェクト モデル バージョンで常に起動するようになります。
    
### <a name="to-set-the-default-programming-language"></a>既定のプログラミング言語を設定するには

1. [ **ファイル**] タブをクリックし、[ **オプション**] をクリックします。
    
2. [ **InfoPath オプション**] ダイアログ ボックスの [ **基本設定**] セクションで、[ **その他のオプション**] をクリックします。
    
3. [ **オプション**] ダイアログ ボックスの [ **デザイン**] タブの [ **プログラミング用の既定値**] セクションで、既定のプログラミング言語を選択します。 
    
### <a name="writing-code"></a>コードの作成

これで、InfoPath 2013 と Visual Studio 2012 を使用して開発作業を開始できます。 
  
### <a name="to-start-the-visual-studio-code-editor"></a>Visual Studio コード エディターを起動するには

1. InfoPath デザイン モードでフォーム テンプレートを開きます。
    
2. [ **開発**] タブの [ **コード エディター**] をクリックします。 
    
> [!TIP]
> [ **開発**] タブのコマンド、ショートカット メニュー、およびその他のユーザー インターフェイスを使用して、コード エディターを起動し、フォームのイベント ハンドラーやコントロール イベントを自動的に追加することもできます。 詳細については、「[イベント ハンドラーを追加する](how-to-add-an-event-handler.md)」を参照してください
  

