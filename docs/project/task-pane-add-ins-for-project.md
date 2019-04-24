---
title: Project 用の作業ウィンドウ アドイン
manager: soliver
ms.date: 09/10/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 44712b7c-aead-433d-8c0e-76407264166c
description: project Standard 2013 および project Professional 2013 はどちらも作業ウィンドウ Office アドインをサポートしています。作業ウィンドウアドインを使用すると、プロジェクト、タスク、リソース、およびデータの表示を、他の Office 2013 クライアントアプリケーション、SharePoint アプリケーション、Web パーツ、その他の web ページ、外部データと統合できます。
ms.openlocfilehash: 26942cab1d1b127872a230a46fbc6242ab27b754
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330017"
---
# <a name="task-pane-add-ins-for-project"></a>Project 用の作業ウィンドウ アドイン

project Standard 2013 および project Professional 2013 はどちらも作業ウィンドウ Office アドインをサポートしています。作業ウィンドウアドインを使用すると、プロジェクト、タスク、リソース、およびデータの表示を、他の Office 2013 クライアントアプリケーション、SharePoint アプリケーション、Web パーツ、その他の web ページ、外部データと統合できます。
  
office アドインは、いくつかの office 2013 クライアントアプリケーションでサポートされている拡張モデルです。 完全なアドインプラットフォームには、コンテキスト、コンテンツ、および作業ウィンドウアドインの種類が含まれています。 Outlook 2013 ではメールアドインがサポートされており、電子メールメッセージ内の web ページ、またはアイテムのコンテンツに関連する予定表アイテムの予定表を表示することができます。 Word 2013 および Excel 2013 はコンテンツアドインをサポートします。これにより、web ページがドキュメントに埋め込まれたコンテンツとして表示されます。 Word 2013、Excel 2013、および Project Professional 2013 サポート作業ウィンドウアドイン。これは、コンテンツがプロジェクト内のコンテキスト情報に関連している作業ウィンドウで web ページを表示することができます。
  
たとえば、プロジェクトアドインでは、作業中のプロジェクトのデータを要約し、選択したタスクまたはリソースに関する追加データを表示できます。 アドイン内の関連データは、SharePoint リスト、Project Server データベースのレポートテーブル、web サービス、またはその他のエンタープライズアプリケーションなどの外部ソースから取得できます。 作業ウィンドウアドインは、HTML 5、javascript、JQuery およびその他の javascript ライブラリを使用して開発できます。 作業ウィンドウアドインは、ActiveX、Silverlight、Flash のコンポーネントを直接サポートしていません。 Office アドインは、 **IFrame**要素を使用して、ASP.NET と .net Framework 4.5 ライブラリを使用するサーバー側の web アプリケーションにアクセスできますが、この種類のソリューションは推奨またはサポートされていません。 アドインは、データをローカルに保存するため、または外部の場所にデータを書き込むために開発できます。 
  
> [!NOTE]
> 作業ウィンドウプロジェクトアドインは、OAuth 認証を使用して project Online のデータにアクセスできます。 project Professional 2013 を使用すると、project Server 2013 とオンプレミスまたはオンラインの SharePoint 2013 の両方のオンプレミスインストールにアクセスする作業ウィンドウアドインを開発できます。 たとえば、「project の[作業ウィンドウアドインを PWA に接続する](https://blogs.msdn.com/b/project_programmability/archive/2012/11/02/connecting-a-project-task-pane-app-to-pwa.aspx)Programmibility」を参照してください。 > project Standard 2013 では、project server データまたは project server と同期されている SharePoint タスクリストとの直接統合をサポートしていません。 
  
office 2013 用アドインの詳細については、「 [office アドイン」および「SharePoint アドイン](https://msdn.microsoft.com/library/office/fp161507%28v=office.15%29)」を参照してください。 
  
## <a name="developing-task-pane-add-ins"></a>作業ウィンドウアドインの開発

Office アドインおよび SharePoint アドインの開発者向けドキュメントには、包括的な記事と参考情報が含まれています。 Project Professional 2013 およびその他の Office 2013 クライアントアプリケーション用のアドインの開発の概要と、JavaScript リファレンスおよび XML マニフェストリファレンスについては、「 [Office アドイン](https://msdn.microsoft.com/library/office/apps/jj220060%28v=office.15%29)」を参照してください。
  
project 2013 SDK のダウンロードには、タスク、リソース、およびビューの GUID を取得する方法、アクティブなプロジェクトのプロパティを取得する方法、およびタスク、リソース、またはビューの選択変更イベントハンドラーを設定する方法を示す**project OM Test**サンプルアドインが含まれています。 Project2013SDK ファイルで SDK とサンプルを抽出してインストールする場合は、 `\Samples\Apps\Copy_to_AppSource_FileShare`サブディレクトリと`\Samples\Apps\Copy_to_AppManifests_FileShare`サブディレクトリを参照してください。 jsomcall.html サンプルでは、ダウンロードに含まれている、office .js ファイルおよび project-15.debug.js 内ファイルの JavaScript 関数を使用します。 対応するデバッグ ファイル (office.debug.js および project-15.debug.js) を使用すると、これらの関数を検証できます。 
  
Project Professional 2013 用の**HelloProject_OData**サンプルアドインは、Visual Studio 2012 を使用して開発されました。 このアドインは、 **projectdata**サービスの REST クエリを使用して、プロジェクトのコストやその他の情報に関するレポートデータを取得し、現在のプロジェクトを project Web App のすべてのプロジェクトの平均値と比較します。 
  
## <a name="see-also"></a>関連項目
<a name="bk_addresources"> </a>

- [Project 用の作業ウィンドウ アドイン](https://msdn.microsoft.com/library/office/apps/fp161143%28v=office.15%29)
    
- [プロジェクトの作業ウィンドウアドインを PWA に接続する](https://blogs.msdn.com/b/project_programmability/archive/2012/11/02/connecting-a-project-task-pane-app-to-pwa.aspx)
    
- [Project 2013 SDK のダウンロード](https://www.microsoft.com/en-us/download/details.aspx?id=30435%20)
    
- [Office アドインと SharePoint アドイン](https://msdn.microsoft.com/library/office/fp161507%28v=office.15%29)
    
- [Office アドイン](https://msdn.microsoft.com/library/office/apps/jj220060%28v=office.15%29)
    

