---
title: Project Online の基本
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5b48958e-6dab-4121-871f-fb15f58f1b24
description: アプリケーション開発者は、スタンドアロンアプリケーションまたはプロジェクトアドインを使用して、project Online サイト (SharePoint ホスト型) をカスタマイズできます。プロジェクトに関与する必要のあるニーズに対処することから、次のような PMO サポート機能まで、さまざまなアプリケーションが存在する可能性があります。
ms.openlocfilehash: 00f79b05b886bfd2c54c118245e22f10bb5451bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344409"
---
# <a name="from-0-to-60-with-project-online"></a>Project Online の基本

アプリケーション開発者は、スタンドアロンアプリケーションまたはプロジェクトアドインを使用して、project Online サイト (SharePoint ホスト型) をカスタマイズできます。プロジェクトに関与する必要のあるニーズに対処することから、次のような PMO サポート機能まで、さまざまなアプリケーションが存在する可能性があります。
  
- 作業者の合理化されたタイムカードデータ入力
- 監修者への効率的なタイムカードの承認
- プロジェクトに必要な許可 (調達および状態) を監視する
- アクティブなプロジェクトの状態/正常性チェック
- 問題レポート
- 変更管理の状態レポート
    
Project Online には、次のシナリオに対応するための API サポートが含まれています。
  
- プロジェクト (SharePoint) ホスト型アドインの場合:
    
  - SharePoint Online でホストされているコード (JavaScript、HTML、CSS)
  - ブラウザーにダウンロードされ、SharePoint Online に対して実行されるアセット。  
  - JavaScript のビジネスロジック   
  - Project Online または SharePoint に格納されているデータにアクセスする (ただし、に制限されることはありません)。  
  - Custom fields  
  - リスト
    
- プロジェクト (SharePoint) プロバイダー向けのホスト型アドインの場合:
    
  - Project Online サイト外のサイトに存在するコード 
  - 外部サイト。以下のことができます (ただし、制限はありません)。  
  - 別の SharePoint サイト  
  - 任意のプラットフォーム上に構築された Web App/サービス  
  - 外部サイトにビジネスロジックが含まれている  
  - ブラウザーが project online から外部サイトにリダイレクトされ、access トークンが project online にリダイレクトされます。  
  - 外部サイトは、SharePoint および Project Online を呼び出すことができます。
    
- 外部/スタンドアロンアドインの場合:
    
  - ユーザーがデバイス上でアプリケーションを実行する
  - アプリケーションは、Project Online api を直接認証して呼び出します。
    

|アプリケーションの種類|API 実装|ターゲット環境|アプリケーションの例|
|:-----|:-----|:-----|:-----|
|ホストされるプロジェクト  <br/> |jsom (Java Script オブジェクトモデル)  <br/> REST  <br/> |ブラウザー  <br/> |タイムカードエントリ  <br/> タイムカードの承認  <br/> プロジェクトの進捗状況  <br/> 問題レポート  <br/> |
|ホストされているプロジェクトプロバイダー  <br/> |csom クライアントライブラリ  <br/> |Azure web サイト/アプリ  <br/> Windows 以外の環境 (ランプ等)  <br/> |外部タイムシートの検証  <br/> プロジェクトインポーター  <br/> |
|外部/スタンドアロン  <br/> |REST  <br/> CSOM  <br/> |REST-任意のプラットフォーム  <br/> csom-任意の .net サポートされるプラットフォーム  <br/> |タイムカードエントリ  <br/> 新しいサイトへのプロジェクトの移行  <br/> 管理の状態を変更します。  <br/> |
   
## <a name="what-does-it-take-to-start-developing-applications-for-project-online"></a>Project Online 用のアプリケーションの開発を開始するには、何が必要ですか?

project online アプリケーションの開発に必要な一般的なアイテムは、project online アカウントおよびテストデータ--プロジェクトとプロジェクト関連の情報で、割り当て、タスク、リソース、およびユーザー設定フィールドを含みます。 開発環境も必要ですが、開発環境の仕様はアプリケーションの種類とアプリケーションに必要な API インターフェイスによって異なります。 次のいくつかのセクションでは、3つの API インターフェイスの開発ニーズについて説明します。
  
参照ドキュメントでは、3つすべてのインターフェイスに共通のオブジェクトモデルと、オブジェクトモデルコンポーネント間の関係を示すエンティティマップについて説明しています。
  
## <a name="project-hosted-add-in-development-environment"></a>プロジェクトでホストされるアドインの開発環境

ホストされるアドインは、サーバー上に存在し、ランタイムの実行のためにブラウザーにダウンロードされるアドインです。 ホストされたアドインは、jsom または REST インターフェイスを使用して、JavaScript で記述できます。 Project Online では、ランタイムの実行のための jsom ライブラリへの参照が提供されています。 開発が Windows プラットフォームで実行されている場合、必要なリソースは次のとおりです。
  
- visual studio 2015 (推奨) または visual studio 2013
    
- Office 開発ツール (Visual Studio)
    
- JavaScript 言語
    
サンプルhttps://github.com/OfficeDev/Project-JSOM-Copy-Work-Packagesアプリケーションを参照してください。 
  
簡単な手順でサンプルをダウンロードして実行することができます。
  
1. サンプルアプリケーションをダウンロードして開く
    
2. [プロパティ] ウィンドウで SiteURL を更新する
    
   project online は、アドインのアプリケーションスコープとユーザー権限の両方を調べて、project online ホスト上の情報へのアクセスを管理します。 どちらか一方または両方の設定で明示的にアクセスが拒否されている場合、Project Online は情報へのアクセスを拒否します。 それ以外の場合は、アクセスが許可されます。
    
3. サイトで[サイドローディング](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins)を有効にします。  
    
4. プロジェクトをビルドします。
    
5. プロジェクトを実行します。
    
## <a name="project-provider-hosted-add-in-development-environment"></a>プロジェクトプロバイダー向けのホスト型アドインの開発環境

プロバイダーホスト型アドインは、どの web プラットフォームにも記述され、常駐するアプリケーションです。 これらのユーザーは、REST (または csom for Microsoft プラットフォーム) API を使用して接続し、データ操作を実行できます。 REST インターフェイスをサポートするすべての言語と環境を開発に使用できます。 
  
この種類のアプリケーションの Windows 開発環境の例には、次の項目が含まれています。
  
-  visual studio 2015 (推奨) または visual studio 2013 
    
- Microsoft Office 開発ツール (visual studio 2015 Professional および Enterprise edition で提供されています)
    
- .net Framework 4.0 またはそれ以降
    
- [sharepointonline csom パッケージ](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM)(csom 呼び出しの場合) 
    
- プログラミング言語 (C# など) 
    
作業https://github.com/OfficeDev/Project-Add-in-REST-BasicDataOperations用サンプルスクリプトにアクセスします。 
  
サンプルは、いくつかの手順で実行できます。
  
1. サンプルアプリケーションをダウンロードして開く
    
2. [プロパティ] ウィンドウで SiteURL を更新する
    
   project online は、アドインのアプリケーションスコープとユーザー権限の両方を調べて、project online ホスト上の情報へのアクセスを管理します。 どちらか一方または両方の設定で明示的にアクセスが拒否されている場合、Project Online は情報へのアクセスを拒否します。 それ以外の場合は、アクセスが許可されます。
    
3. サイトで[サイドローディング](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins)を有効にします。 
    
4. プロジェクトをビルドします。
    
5. プロジェクトを実行します。
    
## <a name="externalstandalone-application-development-environment"></a>外部/スタンドアロンアプリケーション開発環境

スタンドアロンアプリケーションは、クライアント側オブジェクトモデル (csom) を使用して project online を呼び出し、project online と通信して、サーバー上に存在する情報を作成、取得、更新、および削除することができます。 これは、ユーザーアクセスレベルによって実行されるスタンドアロンクライアントアプリケーションです。 
  
この種類のアプリケーションの Windows 開発環境の例には、次の項目が含まれています。
  
- visual studio 2015 (推奨) または visual studio 2013 
    
- Microsoft Office 開発ツール (visual studio 2015 Professional および Enterprise edition で提供されています)
    
- .net Framework 4.0 またはそれ以降
    
- [sharepointonline csom パッケージ](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM)(csom 呼び出しの場合) 
    
- プログラミング言語 (C# など) 
    
サンプルhttps://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFieldsアプリケーションを参照してください。 
  
サンプルは、いくつかの手順で実行できます。
  
1. サンプルアプリケーションをダウンロードする
    
2. プロジェクトオンラインサイト (サイト名、ユーザーアカウント、パスワード) にアクセスするための、いくつかの変更を行います。
    
   ユーザーがすべてのプロジェクトにアクセスできることを確認します。 Project Online では、ユーザー権限を使用して、データストア内の情報へのアクセスを管理します。
    
3. nuget コンソールで次のように入力して、[ツール] メニューから利用できる nuget パッケージマネージャーコンソールを使用して、SharePoint アセンブリを参照に追加します。 
    
   `Install-Package Microsoft.SharePointOnline.CSOM`

4. プロジェクトをビルドします。
    
5. プロジェクトを実行します。
    
## <a name="next-steps"></a>次のステップ

各サンプルアプリケーションには、個々のプロジェクト API を使用した作業の概要を説明する記事があります。 この記事は、エンティティの関係、クエリシステムの情報、およびユーザー設定フィールドへのアクセスについて説明するいくつかの記事と共に、次のリストに表示されます。 
  
- [クライアント側オブジェクトモデルを使用した Project Online アプリケーションの開発](developing-a-project-online-application-using-the-client-side-object-model.md)
    
- [JavaScript オブジェクトモデル (jsom) を使用して Project Online アドインを開発する](developing-a-project-online-add-in-using-the-javascript-object-model-jsom.md)
    
- [Project Online エンタープライズ ユーザー設定フィールドへのアクセス](accessing-project-online-enterprise-custom-fields.md)
    
## <a name="see-also"></a>関連項目

Project Online および CSOM を使用したアプリケーション開発に関するドキュメントとサンプルについては、[Project 開発ポータル](https://developer.microsoft.com/en-us/project)をご覧ください。
    

