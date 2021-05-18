---
title: Project 用の作業ウィンドウ アドイン
manager: soliver
ms.date: 09/10/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 44712b7c-aead-433d-8c0e-76407264166c
description: Project Standard 2013 および 2013 Project Professionalは、両方ともアドインの作業ウィンドウOfficeをサポートします。作業ウィンドウ アドインを使用すると、プロジェクト内のプロジェクト、タスク、リソース、およびビュー データを他の Office 2013 クライアント アプリケーション、SharePoint アプリケーション、Web パーツ、その他の Web ページ、および外部データと統合できます。
ms.openlocfilehash: 26942cab1d1b127872a230a46fbc6242ab27b754
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330017"
---
# <a name="task-pane-add-ins-for-project"></a>Project 用の作業ウィンドウ アドイン

Project Standard 2013 および 2013 Project Professionalは、両方ともアドインの作業ウィンドウOfficeをサポートします。作業ウィンドウ アドインを使用すると、プロジェクト内のプロジェクト、タスク、リソース、およびビュー データを他の Office 2013 クライアント アプリケーション、SharePoint アプリケーション、Web パーツ、その他の Web ページ、および外部データと統合できます。
  
Officeアドインは、2013 年の複数のクライアント アプリケーションでサポートOffice機能拡張モデルです。 完全なアドイン プラットフォームには、コンテキスト、コンテンツ、作業ウィンドウ アドインの種類が含まれます。 Outlook 2013 では、メール アドインがサポートされています。これは、アイテム内のコンテンツに関連する電子メール メッセージまたは予定表の予定アイテム内に Web ページを表示できます。 Word 2013 および Excel 2013 ではコンテンツ アドインがサポートされ、Web ページをドキュメントに埋め込みコンテンツとして表示できます。 Word 2013、Excel 2013、Project Professional 2013 は作業ウィンドウ アドインをサポートしています。作業ウィンドウ内の Web ページを表示して、コンテンツがプロジェクト内のコンテキスト情報に関連付けできます。
  
たとえば、Projectアドインは、アクティブなプロジェクトのデータを要約し、選択したタスクまたはリソースに関する追加のデータを表示できます。 アドイン内の関連データは、SharePoint リスト、Project Server データベース内のレポート テーブル、Web サービス、または別のエンタープライズ アプリケーションなどの外部ソースから取得できます。 作業ウィンドウ アドインは、HTML 5、JavaScript、JQuery、その他の JavaScript ライブラリを使用して開発できます。 作業ウィンドウ アドインは、ユーザー、Silverlight、または Flash コンポーネントActiveX直接サポートされません。 Office アドインは **IFrame** 要素を使用して、ASP.NET と .NET Framework 4.5 ライブラリを使用するサーバー側 Web アプリケーションにアクセスすることができますが、そのようなソリューションは推奨またはサポートされていません。 アドインは、データをローカルに保存したり、外部の場所にデータを書き込む場合に開発できます。 
  
> [!NOTE]
> 作業ウィンドウ Projectアドインは、OAuth 認証を使用して、Project Onlineからデータにアクセスできます。 Project Professional 2013 では、Project Server 2013 のオンプレミス インストールとオンプレミスまたはオンライン SharePoint 2013 の両方にアクセスする作業ウィンドウ アドインを開発できます。 たとえば、「タスク ウィンドウ アドイン[を Projectに接続する](https://blogs.msdn.com/b/project_programmability/archive/2012/11/02/connecting-a-project-task-pane-app-to-pwa.aspx)」を参照PWA「Project」を参照してください。 > Project Standard 2013 では、Project Server データまたは SharePoint サーバーと同期されるタスク リストとの直接統合はProjectされません。 
  
Office 2013 のアドインの詳細については、「OfficeアドインSharePoint[を参照してください](https://msdn.microsoft.com/library/office/fp161507%28v=office.15%29)。 
  
## <a name="developing-task-pane-add-ins"></a>作業ウィンドウ アドインの開発

アドインのOfficeおよびSharePointの開発者向けドキュメントには、包括的な記事と参照が含まれています。 Project Professional 2013 および他の Office クライアント アプリケーション用のアドインの開発の概要、および JavaScript リファレンスと XML マニフェストリファレンスについては[、「Office](https://msdn.microsoft.com/library/office/apps/jj220060%28v=office.15%29)アドイン」を参照してください。
  
Project 2013 SDK のダウンロードには、**タスク**、リソース、ビューの GUID を取得する方法、アクティブなプロジェクトのプロパティを取得する方法、およびタスク、リソース、またはビューの選択変更イベント ハンドラーを設定する方法を示す Project OM Test サンプル アドインが含まれています。 SDK とサンプルを展開し、Project2013SDK.msiファイルにインストールする場合は、サブディレクトリと  `\Samples\Apps\Copy_to_AppSource_FileShare` サブディレクトリを  `\Samples\Apps\Copy_to_AppManifests_FileShare` 参照してください。 この JSOMCall.htmサンプルでは、ダウンロードに含まれる office.js ファイルと project-15.js ファイルの JavaScript 関数を使用します。 対応するデバッグ ファイル (office.debug.js および project-15.debug.js) を使用すると、これらの関数を検証できます。 
  
2013 **HelloProject_OData** 2013 のサンプル アドインProject Professional 2012 年に開発Visual Studioしました。 アドインは **ProjectData** サービスの REST クエリを使用して、プロジェクト コストなどの情報のレポート データを取得し、現在のプロジェクトと Project Web App のすべてのプロジェクトの平均値を比較します。 
  
## <a name="see-also"></a>関連項目
<a name="bk_addresources"> </a>

- [Project 用の作業ウィンドウ アドイン](https://msdn.microsoft.com/library/office/apps/fp161143%28v=office.15%29)
    
- [作業ウィンドウ Projectアドインをユーザーに接続PWA](https://blogs.msdn.com/b/project_programmability/archive/2012/11/02/connecting-a-project-task-pane-app-to-pwa.aspx)
    
- [Project 2013 SDK のダウンロード](https://www.microsoft.com/en-us/download/details.aspx?id=30435%20)
    
- [Office アドインと SharePoint アドイン](https://msdn.microsoft.com/library/office/fp161507%28v=office.15%29)
    
- [Office アドイン](https://msdn.microsoft.com/library/office/apps/jj220060%28v=office.15%29)
    

