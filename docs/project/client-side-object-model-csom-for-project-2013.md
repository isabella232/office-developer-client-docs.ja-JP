---
title: Project 2013 のクライアント側オブジェクト モデル (CSOM)
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
ms.assetid: 716325eb-b092-4934-921f-84129d0a1f5f
description: Project Server 2013 のクライアント側オブジェクト モデル (CSOM) は、一般的なサーバー機能を実装しています。 Project Server CSOM には、Microsoft .NET CSOM、Microsoft Silverlight CSOM、Windows Phone 8 CSOM、および JavaScript オブジェクト モデル (JSOM) が含まれます。 さらに、この CSOM には REST インターフェイスを有効にする OData サービスも含まれています。 この REST インターフェイスは、主に iOS や Android などの Windows 以外のプラットフォームでアプリを開発するためのものです。
localization_priority: Priority
ms.openlocfilehash: b722e316f5cb2054eb6522297c5c5ef3e75f9fa4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355203"
---
# <a name="client-side-object-model-csom-for-project-2013"></a>Project 2013 のクライアント側オブジェクト モデル (CSOM)

Project Server 2013 のクライアント側オブジェクト モデル (CSOM) は、一般的なサーバー機能を実装しています。 Project Server CSOM には、Microsoft .NET CSOM、Microsoft Silverlight CSOM、Windows Phone 8 CSOM、および JavaScript オブジェクト モデル (JSOM) が含まれます。 さらに、この CSOM には REST インターフェイスを有効にする OData サービスも含まれています。 この REST インターフェイスは、主に iOS や Android などの Windows 以外のプラットフォームでアプリを開発するためのものです。
  
> [!NOTE]
> Project Online 用のソリューションには CSOM を使用する必要があります。 ただし、オンプレミスのアプリには CSOM と Project Server Interface (PSI) のどちらかを使用できます。 使用する予定の機能が CSOM に含まれている場合、新しいアプリには CSOM を使用することをお勧めします。 
  
CSOM の拡張機能 **ProjectContext** オブジェクトは、サーバー コンテンツと機能へのエントリ ポイントを提供します。 .NET CSOM、Silverlight CSOM、および Windows Phone CSOM は、[Microsoft.ProjectServer.Client.ProjectContext](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.aspx) オブジェクトを使用し、JSOM は **PS.ProjectContext** オブジェクトを使用します。 **ProjectContext** のプロパティは、現在の Project Web App サイト コレクションに含まれる主要な Project Server オブジェクトへの直接アクセスを提供します。 CSOM アセンブリと JavaScript ファイルの場所に関する詳細については、[Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx) を参照してください。 
  
 **アプリとセキュリティ モデル** アプリは、Project Server 2013 および Project Online の CRUD (作成、読み取り、更新、削除) 操作に CSOM を使用する必要があります。 Project アプリは、SharePoint 2013 のアプリ専用の認証モデルを使用しません。 Project Server アプリには、どのユーザーの代わりにコマンドを実行するかを指定する特定のアクセス許可要求のスコープが必要です。 
  
 **REST クエリ** CSOM OData サービスの REST クエリはメタデータを利用することなく作成できます。 一部のサード パーティ製のツールでは、CSOM 対応の .NET アセンブリを使用して、その他のデバイス用アプリを開発できます。 たとえば、「iOS または Android 対応のクロスプラットフォーム .NET 開発ツール」についてインターネットを検索してください。 
  
> [!NOTE]
> **ProjectData** レポート サービスの `$metadata` オプションは有効ですが (`https://ServerName/pwaName/_api/ProjectData/$metadata`)、CSOM の **ProjectServer** サービスの `$metadata` オプションは、リリース済みバージョンの Project Server 2013 では削除されています。 REST エンドポイントとして利用可能な CSOM のオブジェクトとメンバーを調べるには、「[Project Server 2013 の JavaScript ライブラリおよび REST リファレンス](javascript-library-and-rest-reference-for-project-server-2013.md)」を参照してください。 
  
CSOM で利用可能なエンティティを REST インターフェイスで確認する場合は、`https://ServerName/pwaName/_api/ProjectServer` クエリを使用できます。 REST クエリの場合、**ProjectServer** エンティティは、Microsoft.ProjectServer.Client.dll マネージ アセンブリの [ProjectContext](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.aspx) オブジェクトと JSOM の [PS.ProjectContext](https://msdn.microsoft.com/library/a490b675-a845-ee94-3877-b99ada9bf2b0%28Office.15%29.aspx) オブジェクトのプロパティを忠実に再現しています。 たとえば、Project Web App のプロジェクト、指定したプロジェクトの割り当て、および指定したリソースの指定した割り当てのタスク名に関する情報は、ブラウザーで次に示すクエリ (それぞれのクエリは同じ `https://ServerName/pwaName/_api` URL プレフィックスを使用) を使用することで CSOM から取得できます。 **Project.Id**、**EnterpriseResource.Id**、および **Assignment.Id** の GUID はサンプルの値です。
  
```HTML
/ProjectServer/Projects
/ProjectServer/Projects('263fc8d7-427c-e111-92fc-00155d3ba208')/Assignments
/ProjectServer/EnterpriseResources('28eeb2b5-fe74-4efc-aa35-6a64514d1526')/Assignments('a2eafeb5-437c-e111-92fc-00155d3ba208')/Task?$select=Name
```

**ProjectData** サービスの OData インターフェイス (レポート用の読み取り専用インターフェイス) とは異なり、**ProjectServer** サービスで REST クエリを使用すると CRUD 操作を実行できます。 Project Server CSOM に対する REST クエリは、主に Windows デスクトップ以外のプラットフォーム (Windows RT、iOS、Android など) に向けて設計されています。 Windows デスクトップおよびサーバー プラットフォーム (Windows 7、Windows 8、および Windows Server 2008 R2) の場合は、CSOM マネージ アセンブリを使用できます。 Web アプリの場合は、JavaScript 用の PS.js を使用できます。 REST クエリを使用した CRUD 操作の実行に関する詳細については、SharePoint 2013 SDK のトピック「[SharePoint REST 要求で OData クエリ操作を使用する](https://msdn.microsoft.com/library/d4b5c277-ed50-420c-8a9b-860342284b72%28Office.15%29.aspx)」を参照してください。 **ProjectData** サービスの使用に関する詳細については、「[Project レポート データの OData フィードを照会する](https://msdn.microsoft.com/library/office/jj163048.aspx)」を参照してください。
  
表 1 に、Project Server のオブジェクトを表す **ProjectContext** のプロパティを示します。 これらのオブジェクトを使用することで、Project Server 2013 のその他のエンティティ (割り当てやタスクなど) を取得できます。 
  
**表 1. CSOM と JSOM の Project Server オブジェクトにアクセスするための ProjectContext のプロパティ**

|**CSOM (.NET、Silverlight、および Windows Phone)**|**JSOM**|
|:-----|:-----|
|[CustomFields](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.CustomFields.aspx) <br/> |customFields  <br/> |
|[EnterpriseProjectTypes](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.EnterpriseProjectTypes.aspx) <br/> |enterpriseProjectTypes  <br/> |
|[EnterpriseResources](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.EnterpriseResources.aspx) <br/> |enterpriseResources  <br/> |
|[EntityTypes](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.EntityTypes.aspx) <br/> |entityTypes  <br/> |
|[EventHandlers](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.EventHandlers.aspx) <br/> |eventHandlers  <br/> |
|[Events](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.Events.aspx) <br/> |events  <br/> |
|[LookupTables](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.LookupTables.aspx) <br/> |lookupTables  <br/> |
|[Phases](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.Phases.aspx) <br/> |phases  <br/> |
|[Projects](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.Projects.aspx) <br/> |projects  <br/> |
|[Stages](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.Stages.aspx) <br/> |stages  <br/> |
|[WorkflowActivities](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.WorkflowActivities.aspx) <br/> |workflowActivities  <br/> |
|[WorkflowDesigner](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.WorkflowDesigner.aspx) <br/> |workflowDesigner  <br/> |
   
## <a name="in-this-section"></a>このセクションの内容

「[Project Server CSOM と .NET の使用を開始する](getting-started-with-the-project-server-csom-and-net.md)」には、Project Server CSOM と .NET の概要情報、単純な .NET CSOM 拡張機能を Visual Studio 2012 で作成する手順、およびサポート コードのサンプルが含まれています。 
  
「[Project Server 2013 JavaScript オブジェクト モデルの概要](getting-started-with-the-project-server-2013-javascript-object-model.md)」には、Project Server JSOM の概要情報、単純な JSOM 拡張機能を Visual Studio 2012 で作成する手順、およびサポートされているコード サンプルが含まれています。 
  
CSOM の使用方法を示す次の記事も確認してください。
  
- [Project Online でユーザー設定フィールドを一括更新し、ワークフローからプロジェクト サイトを作成する](bulk-update-custom-fields-and-create-project-sites-from-workflow-in-project.md)
    
- [JavaScript オブジェクト モデルを使用してプロジェクトを操作する](create-retrieve-update-delete-projects-using-project-server-javascript.md)
    
> [!NOTE]
> CSOM を使用した .NET Framework 4 開発には Visual Studio 2010 を使用することもできます。 
  
## <a name="reference"></a>リファレンス

[Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx)
  
## <a name="see-also"></a>関連項目



[Project Server 2013 のアーキテクチャ](project-server-2013-architecture.md)


[SharePoint 2013 の適切な API セットを選択する](https://msdn.microsoft.com/library/f36645da-77c5-47f1-a2ca-13d4b62b320d%28Office.15%29.aspx)

