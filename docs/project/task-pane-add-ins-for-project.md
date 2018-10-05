---
title: Project 用の作業ウィンドウ アドイン
manager: soliver
ms.date: 09/10/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 44712b7c-aead-433d-8c0e-76407264166c
description: 標準 2013 のプロジェクトおよびプロジェクト評価のための両方は Office アドイン] 作業ウィンドウをサポートします。プロジェクト、タスク、リソースを統合する作業ウィンドウ - アドインを使用し、他の Office 2013 のクライアント アプリケーション、SharePoint アプリケーション、Web パーツ、その他の web ページ、および外部のデータを持つプロジェクトのデータを表示できます。
ms.openlocfilehash: 26942cab1d1b127872a230a46fbc6242ab27b754
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396016"
---
# <a name="task-pane-add-ins-for-project"></a>Project 用の作業ウィンドウ アドイン

標準 2013 のプロジェクトおよびプロジェクト評価のための両方は Office アドイン] 作業ウィンドウをサポートします。プロジェクト、タスク、リソースを統合する作業ウィンドウ - アドインを使用し、他の Office 2013 のクライアント アプリケーション、SharePoint アプリケーション、Web パーツ、その他の web ページ、および外部のデータを持つプロジェクトのデータを表示できます。
  
Office アドインは、いくつかの Office 2013 のクライアント アプリケーションでサポートされている機能拡張モデルです。 完全に追加のプラットフォームでは、コンテキスト、コンテンツが含まれています、作業ウィンドウの種類を追加で。 Outlook 2013 では、メール アドイン、電子メール メッセージ内の web ページを表示することができます、またはアイテムのコンテンツに関連付けられているカレンダーの予定アイテムをサポートします。 Word 2013 および Excel 2013 は、コンテンツのアドイン、文書内の埋め込みコンテンツとして web ページを表示することをサポートします。 Word 2013、2013 年 Excel および評価のためのプロジェクトは、作業ウィンドウのアドイン プロジェクト内でのコンテキストの情報をコンテンツに関係している作業ウィンドウで web ページを表示することができますをサポートします。
  
などのプロジェクトを追加で作業中のプロジェクトのデータを集計でき、選択したタスクまたはリソースに関する追加データを表示できます。 アドインに関連するデータは、Project Server データベース、web サービス、または他のエンタープライズ アプリケーション内のテーブルのレポートを作成、SharePoint リストなどの外部ソースから取得できます。 5 を HTML、JavaScript、JQuery と他の JavaScript ライブラリで、作業ウィンドウ アドインを開発できます。 作業ウィンドウ アドインを直接サポートしていませんか、ActiveX、Silverlight では、Flash コンポーネント。 Office アドイン可能性がありますを使用して**IFrame**要素 ASP.NET および.NET Framework 4.5 のライブラリを使用するサーバー側の web アプリケーションにアクセスするのには、その種のソリューションは推奨もサポートします。 ローカルでデータを保存したり、外部の場所にデータを書き込むには、アドインを開発できます。 
  
> [!NOTE]
> プロジェクトの [アドイン] 作業ウィンドウは OAuth 認証を使用して、オンラインのプロジェクトからデータにアクセスできます。 評価のためのプロジェクトでは、作業ウィンドウ アドインを Project Server 2013 と設置型またはオンラインの SharePoint 2013 の両方の設置型インストールにアクセスを開発できます。 などを参照してください[プロジェクトの作業ウィンドウを接続する追加の PWA に](https://blogs.msdn.com/b/project_programmability/archive/2012/11/02/connecting-a-project-task-pane-app-to-pwa.aspx)プロジェクトの Programmibility のブログです。 > プロジェクトの標準的な 2013 は、Project Server のデータ、または Project Server と同期している SharePoint タスク リストと直接統合をサポートしていません。 
  
Office 2013 用のアドインの詳細については、 [Office および SharePoint アドイン](https://msdn.microsoft.com/library/office/fp161507%28v=office.15%29)を参照してください。 
  
## <a name="developing-task-pane-add-ins"></a>作業ウィンドウ - アドインを開発

Office および SharePoint アドインの開発者向けドキュメントには、包括的な記事と参照が含まれています。 評価のためのプロジェクトおよびその他の Office 2013 のクライアント アプリケーションと、JavaScript 参照および XML マニフェストの参照アドインの開発の概要については、 [Office アドイン](https://msdn.microsoft.com/library/office/apps/jj220060%28v=office.15%29)を参照してください。
  
Project 2013 SDK ダウンロードには、**プロジェクト オブジェクト モデルのテスト**サンプルを追加で、タスク、リソース、およびビューの GUID を取得する方法、作業中のプロジェクトのプロパティを取得する方法と、タスク、リソース、または選択変更イベント ハンドラーを表示する方法を示していますが含まれています。 抽出 Project2013SDK.msi ファイルで、SDK およびサンプルをインストールするを参照してください、`\Samples\Apps\Copy_to_AppSource_FileShare`サブディレクトリ、および`\Samples\Apps\Copy_to_AppManifests_FileShare`サブディレクトリです。 JSOMCall.html サンプルでは、ダウンロードに含まれている office.js ファイルとプロジェクトの 15.js ファイル、JavaScript 関数を使用します。 これらの関数は、対応するデバッグ ファイル (office.debug.js と project-15.debug.js) を使用して検証できます。 
  
**HelloProject_OData**サンプル アドインの評価のためのプロジェクトには、Visual Studio 2012 で開発されました。 アドインの**ProjectData**サービスの残りのクエリを使用して、プロジェクトのコストのデータおよびその他の情報のレポートを取得して、現在のプロジェクトを Project Web App のすべてのプロジェクトの平均値とを比較します。 
  
## <a name="see-also"></a>関連項目
<a name="bk_addresources"> </a>

- [Project 用の作業ウィンドウ アドイン](https://msdn.microsoft.com/library/office/apps/fp161143%28v=office.15%29)
    
- [PWA にプロジェクトの作業ウィンドウを追加で接続します。](https://blogs.msdn.com/b/project_programmability/archive/2012/11/02/connecting-a-project-task-pane-app-to-pwa.aspx)
    
- [Project 2013 SDK のダウンロード](https://www.microsoft.com/en-us/download/details.aspx?id=30435%20)
    
- [Office アドインと SharePoint アドイン](https://msdn.microsoft.com/library/office/fp161507%28v=office.15%29)
    
- [Office 用アプリの作成](https://msdn.microsoft.com/library/office/apps/jj220060%28v=office.15%29)
    

