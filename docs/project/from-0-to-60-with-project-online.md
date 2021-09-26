---
title: Project Online の基本
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 5b48958e-6dab-4121-871f-fb15f58f1b24
description: アプリケーション開発者は、スタンドアロン アプリケーションProject OnlineアドインをSharePointして、Project サイト (ホストされている) をカスタマイズできます。プロジェクトに関わるユーザーのニーズへの対応から、次のような PMO サポート機能まで、さまざまなアプリケーションが利用できます。
ms.openlocfilehash: 3ea7c451022c3c7b55d1ce788b002df6bb8bb591
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59619240"
---
# <a name="from-0-to-60-with-project-online"></a>Project Online の基本

アプリケーション開発者は、スタンドアロン アプリケーションProject OnlineアドインをSharePointして、Project サイト (ホストされている) をカスタマイズできます。プロジェクトに関わるユーザーのニーズへの対応から、次のような PMO サポート機能まで、さまざまなアプリケーションが利用できます。
  
- ワーカーのタイムカード データエントリの合理化
- 監督者の効率的なタイムカード承認
- プロジェクトに必要な許可 (調達と状態) の監視
- アクティブなプロジェクトの状態/正常性チェック
- 問題レポート
- [管理状態の変更] レポート
    
Project Onlineのシナリオに対応する API サポートが含まれています。
  
- ホストProject (SharePoint) の場合:
    
  - オンラインでホストされているコード (JavaScript、HTML、CSS) SharePointします。
  - ブラウザーにダウンロードされ、オンラインに対して実行SharePoint。  
  - JavaScript にあるビジネス ロジック   
  - 次に示すデータなど、Project OnlineまたはSharePointに格納されているデータにアクセスします (ただし、これらに限定されません)。  
  - カスタム フィールド  
  - リスト
    
- プロバイダーホストProject (SharePoint) アドインの場合:
    
  - サイトの外部サイトに存在するコードProject Onlineします。 
  - 外部サイトは、次の場合があります (ただし、これらに限定されない)。  
  - 別のSharePoint サイト  
  - 任意のプラットフォーム上に構築された Web App/Service  
  - 外部サイトにはビジネス ロジックが含まれています  
  - ブラウザーは、アクセス トークンを使用Project Online外部サイトから外部サイトにリダイレクトProject Online  
  - 外部サイトは、ユーザーとユーザーのSharePointをProject Online
    
- 外部アドインまたはスタンドアロン アドインの場合:
    
  - ユーザーがデバイス上でアプリケーションを実行する
  - アプリケーションが API を直接認証Project Online呼び出す
    

|アプリケーションの種類|API の実装|ターゲット環境|アプリケーションの例|
|:-----|:-----|:-----|:-----|
|Projectホスト  <br/> |JSOM (Java スクリプト オブジェクト モデル)  <br/> REST  <br/> |ブラウザー  <br/> |タイムカードエントリ  <br/> タイムカードの承認  <br/> プロジェクトの進捗状況  <br/> 問題レポート  <br/> |
|Projectプロバイダーホスト型  <br/> |CSOM クライアント ライブラリ  <br/> |Azure Web サイト/アプリ  <br/> 非Windows環境 (LAMP など)  <br/> |外部タイムシート検証機能  <br/> ProjectImporter  <br/> |
|外部/スタンドアロン  <br/> |REST  <br/> CSOM  <br/> |REST - 任意のプラットフォーム  <br/> CSOM - 任意の .NET でサポートされるプラットフォーム  <br/> |タイムカードエントリ  <br/> 新しいサイトへのプロジェクトの移行  <br/> [管理状態の変更] をクリックします。  <br/> |
   
## <a name="what-does-it-take-to-start-developing-applications-for-project-online"></a>アプリケーションの開発を開始するには何が必要Project Online?

Project Online アプリケーションの開発に必要な一般的な項目は、Project Online アカウントとテスト データです。割り当て、タスク、リソース、およびユーザー設定フィールドを含むプロジェクトとプロジェクト関連の情報です。 開発環境も必要ですが、開発環境の詳細は、アプリケーションの種類とアプリケーションに必要な API インターフェイスによって異なります。 次のいくつかのセクションでは、3 つの API インターフェイスの開発ニーズについて説明します。
  
リファレンス ドキュメントでは、3 つのインターフェイスすべてで一般的なオブジェクト モデルと、オブジェクト モデル コンポーネント間の関係を示すエンティティ マップについて説明します。
  
## <a name="project-hosted-add-in-development-environment"></a>Projectホスト型アドインの開発環境

ホスト型アドインは、サーバー上に存在し、実行時に実行するためにブラウザーにダウンロードされるアドインです。 ホストされたアドインは、JSOM または REST インターフェイスを使用し、JavaScript で記述されます。 Project Online実行時に JSOM ライブラリへの参照を提供します。 開発が新しいプラットフォーム上Windows、必要なリソースは次のとおりです。
  
- Visual Studio 2015 (優先) または Visual Studio 2013
    
- Office開発ツールのVisual Studio
    
- JavaScript 言語
    
サンプル https://github.com/OfficeDev/Project-JSOM-Copy-Work-Packages アプリケーションを参照してください。 
  
サンプルは、次の簡単な手順でダウンロードして実行できます。
  
1. サンプル アプリケーションをダウンロードして開く
    
2. [プロパティ] ウィンドウで SiteURL を更新する
    
   Project Online、アドインのアプリケーション スコープと、アドイン ホスト上の情報へのアクセスを管理するユーザーアクセス許可の両方をProject Onlineします。 どちらかまたは両方の設定でアクセスが明示的に拒否された場合、Project Onlineへのアクセスを拒否する必要があります。 それ以外の場合は、アクセスが許可されます。
    
3. サイト [でサイドローディング](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) を有効にする。  
    
4. プロジェクトをビルドします。
    
5. プロジェクトを実行します。
    
## <a name="project-provider-hosted-add-in-development-environment"></a>Projectホスト型アドインの開発環境

プロバイダーホスト型アドインは、任意の Web プラットフォームで作成および常駐するアプリケーションです。 REST (または Microsoft プラットフォーム用 CSOM) API を使用して、データ操作を接続して実行できます。 REST インターフェイスをサポートする言語と環境は、開発に使用できます。 
  
この種類のアプリケーションWindows環境の例には、次の項目があります。
  
-  Visual Studio 2015 (優先) または Visual Studio 2013 
    
- Microsoft Office開発ツール for Visual Studio (Visual Studio 2015 Professional および Enterpriseエディション)
    
- .NET Framework 4.0 以降
    
- [SharePointOnline CSOM パッケージ](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (CSOM 呼び出しの場合) 
    
- プログラミング言語 (C など)# 
    
作業 https://github.com/OfficeDev/Project-Add-in-REST-BasicDataOperations サンプル スクリプトについては、次のページをご覧ください。 
  
このサンプルは、いくつかの手順で実行できます。
  
1. サンプル アプリケーションをダウンロードして開く
    
2. [プロパティ] ウィンドウで SiteURL を更新する
    
   Project Online、アドインのアプリケーション スコープと、アドイン ホスト上の情報へのアクセスを管理するユーザーアクセス許可の両方をProject Onlineします。 どちらかまたは両方の設定でアクセスが明示的に拒否された場合、Project Onlineへのアクセスを拒否する必要があります。 それ以外の場合は、アクセスが許可されます。
    
3. サイト [でサイドローディング](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) を有効にする。 
    
4. プロジェクトをビルドします。
    
5. プロジェクトを実行します。
    
## <a name="externalstandalone-application-development-environment"></a>外部/スタンドアロン アプリケーションの開発環境

スタンドアロン アプリケーションは、クライアント側オブジェクト モデル (CSOM) または REST を使用して Project Online を呼び出して、Project Online と通信して、サーバーに存在する情報を作成、取得、更新、および削除できます。 これは、実行するユーザー アクセス レベルに依存するスタンドアロン クライアント アプリケーションです。 
  
この種類のアプリケーションWindows環境の例には、次の項目があります。
  
- Visual Studio 2015 (優先) または Visual Studio 2013 
    
- Microsoft Office開発ツール for Visual Studio (Visual Studio 2015 Professional および Enterpriseエディション)
    
- .NET Framework 4.0 以降
    
- [SharePointOnline CSOM パッケージ](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (CSOM 呼び出しの場合) 
    
- プログラミング言語 (C など)# 
    
サンプル https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields アプリケーションを参照してください。 
  
このサンプルは、いくつかの手順で実行できます。
  
1. サンプル アプリケーションのダウンロード
    
2. サイト名、ユーザー アカウント、およびパスワードProject Onlineアクセスするために、いくつかの変更を加えます。
    
   ユーザーがすべてのプロジェクトにアクセスできます。 Project Onlineアクセス許可を使用して、データ ストア内の情報へのアクセスを管理します。
    
3. Nuget コンソールSharePointを使用して、パッケージ マネージャー アセンブリを参照に追加します。Nuget コンソールで次のように入力して、[ツール] メニューから使用できます。 
    
   `Install-Package Microsoft.SharePointOnline.CSOM`

4. プロジェクトをビルドします。
    
5. プロジェクトを実行します。
    
## <a name="next-steps"></a>次の手順

各サンプル アプリケーションには、API を使用して個々のアプリケーションを操作するProjectがあります。 記事は、エンティティの関係、クエリ システムに関する情報、およびユーザー設定フィールドへのアクセスについて説明する記事と共に、次の一覧に表示されます。 
  
- [クライアント側Project Onlineモデルを使用したアプリケーションの開発](developing-a-project-online-application-using-the-client-side-object-model.md)
    
- [JavaScript オブジェクト Project Online (JSOM) を使用したアドインの開発](developing-a-project-online-add-in-using-the-javascript-object-model-jsom.md)
    
- [Project Online エンタープライズ ユーザー設定フィールドへのアクセス](accessing-project-online-enterprise-custom-fields.md)
    
## <a name="see-also"></a>関連項目

Project Online および CSOM を使用したアプリケーション開発に関するドキュメントとサンプルについては、[Project 開発ポータル](https://developer.microsoft.com/en-us/project)をご覧ください。
    

