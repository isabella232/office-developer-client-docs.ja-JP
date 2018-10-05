---
title: Project 2013 のクライアント側オブジェクト モデル (CSOM)
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 716325eb-b092-4934-921f-84129d0a1f5f
description: Project Server 2013 のクライアント側オブジェクト モデル (CSOM) は、一般的なサーバーの機能を実装します。 プロジェクトのサーバー CSOM には、Microsoft .NET CSOM、Microsoft Silverlight の CSOM、Windows Phone 8 CSOM では、JavaScript オブジェクト モデル (JSOM) が含まれています。 さらに、CSOM には、REST インターフェイスを有効にする OData サービスが含まれています。 REST インターフェイスは、iOS および Android などの Windows 以外のプラットフォームでアプリケーションの開発を主に対象としています。
ms.openlocfilehash: 8be603fbee35f228dea0fa6b6be087b8e09c30e5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394448"
---
# <a name="client-side-object-model-csom-for-project-2013"></a>Project 2013 のクライアント側オブジェクト モデル (CSOM)

Project Server 2013 のクライアント側オブジェクト モデル (CSOM) は、一般的なサーバーの機能を実装します。 プロジェクトのサーバー CSOM には、Microsoft .NET CSOM、Microsoft Silverlight の CSOM、Windows Phone 8 CSOM では、JavaScript オブジェクト モデル (JSOM) が含まれています。 さらに、CSOM には、REST インターフェイスを有効にする OData サービスが含まれています。 REST インターフェイスは、iOS および Android などの Windows 以外のプラットフォームでアプリケーションの開発を主に対象としています。
  
> [!NOTE]
> オンライン プロジェクトのソリューションには、CSOM を使用しなければなりません。 ただし、オンプレミス アプリケーションでは、CSOM またはプロジェクト Server インターフェイス (PSI) のいずれかを使用できます。 CSOM には、使用する機能が含まれている場合は、新しいアプリケーションには、CSOM を使用することをお勧めします。 
  
CSOM の拡張機能では、 **ProjectContext**オブジェクトは、サーバーのコンテンツと機能へのエントリ ポイントを提供します。 .NET CSOM、Silverlight CSOM、および Windows Phone の CSOM を使用して、 [Microsoft.ProjectServer.Client.ProjectContext](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.aspx)オブジェクト、および、JSOM を使用して、 **PS.ProjectContext**オブジェクトです。 **ProjectContext**プロパティでは、現在の Project Web App サイト コレクション内の中核となる Project Server オブジェクトへの直接アクセスを提供します。 CSOM アセンブリおよび JavaScript ファイルの場所については、 [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx)を参照してください。 
  
 **アプリケーションとセキュリティ モデル**CRUD のアプリケーションが、CSOM を使用する必要があります (作成、読み取り、更新、削除) Project Server 2013 とオンライン プロジェクトを操作します。 プロジェクトのアプリケーションでは、アプリケーション専用の認証モデルを SharePoint 2013 で使用することがないです。 Project Server アプリケーションには、コマンドの実行対象を指定する特定のアクセス許可要求のスコープが必要です。 
  
 **クエリの残りの部分**メタデータを消費することがなく、CSOM の OData サービスの残りのクエリを作成できます。 いくつかのサード ・ パーティ製ツールは、他のデバイス用のアプリケーションを開発するのには、CSOM の .NET アセンブリを使用して有効にします。 たとえば、プラットフォーム間で .NET 開発ツールの iOS や Android」をインターネットで検索します。 
  
> [!NOTE]
> ですが、 `$metadata` **ProjectData**サービスが有効なレポート作成ののためのオプション ( `https://ServerName/pwaName/_api/ProjectData/$metadata`)、`$metadata`オプションを使用しない、CSOM の**ProjectServer**サービスは、Project Server 2013 のリリース バージョンで削除されています。 CSOM オブジェクトと他のエンドポイントとして使用可能なメンバーを参照してください[JavaScript ライブラリおよび Project Server 2013 の残りの部分参照](javascript-library-and-rest-reference-for-project-server-2013.md)。 
  
REST インターフェイスで CSOM で使用可能なエンティティを表示するには、使用することができます、`https://ServerName/pwaName/_api/ProjectServer`クエリします。 クエリの残りの部分、 **ProjectServer**エンティティより忠実に再現、 [ProjectContext](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.aspx)でオブジェクトのプロパティ Microsoft.ProjectServer.Client.dll はマネージ アセンブリと[PS.ProjectContext](https://msdn.microsoft.com/library/a490b675-a845-ee94-3877-b99ada9bf2b0%28Office.15%29.aspx) 、JSOM 内のオブジェクト。 次のクエリを使用してプロジェクトを Project Web App を指定したプロジェクトと、指定したリソースに指定した割り当てのタスク名の割り当てでは、CSOM から情報を取得するのにはお使いのブラウザーを使用するたとえば、(各クエリを使用して、同じ`https://ServerName/pwaName/_api`の URL 接頭辞)。 Guid は、 **Project.Id**、 **EnterpriseResource.Id**、および**Assignment.Id**のサンプル値です。
  
```HTML
/ProjectServer/Projects
/ProjectServer/Projects('263fc8d7-427c-e111-92fc-00155d3ba208')/Assignments
/ProjectServer/EnterpriseResources('28eeb2b5-fe74-4efc-aa35-6a64514d1526')/Assignments('a2eafeb5-437c-e111-92fc-00155d3ba208')/Task?$select=Name
```

**ProjectData**サービスには、読み取り専用のレポートでは、OData インターフェイスとは異なり、 **ProjectServer**サービスと他のクエリを使用して CRUD 操作を行うことができます。 プロジェクトのサーバー CSOM の残りのクエリは、Windows RT、iOS、Android など、Windows のデスクトップ以外のプラットフォーム用では主に設計されています。 Windows デスクトップおよびサーバー プラットフォーム、Windows 7、Windows 8 では、Windows Server 2008 R2 などの CSOM のマネージ アセンブリを使用できます。 Web アプリケーションでは、JavaScript の PS.js を使用できます。 残りのクエリを使用して CRUD 操作を行う方法の詳細については、SharePoint 2013 SDK に[SharePoint の他の要求のクエリ操作を使用して OData](https://msdn.microsoft.com/library/d4b5c277-ed50-420c-8a9b-860342284b72%28Office.15%29.aspx)を参照してください。 **ProjectData**サービスを使用する方法の詳細については、[プロジェクトのレポート データのフィードの OData をクエリを実行する](https://msdn.microsoft.com/library/office/jj163048.aspx)を参照してください。
  
表 1 は、Project Server のオブジェクトを表す**ProjectContext**のプロパティを一覧表示します。 割り当てやタスクなど、他の Project Server 2013 のエンティティを取得するためにこれらのオブジェクトを使用できます。 
  
**表 1. CSOM と JSOM の Project Server オブジェクトにアクセスするための ProjectContext プロパティ**

|**CSOM (.NET、Silverlight、Windows Phone)**|**JSOM**|
|:-----|:-----|
|[CustomFields](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.CustomFields.aspx) <br/> |名  <br/> |
|[EnterpriseProjectTypes](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.EnterpriseProjectTypes.aspx) <br/> |enterpriseProjectTypes  <br/> |
|[EnterpriseResources](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.EnterpriseResources.aspx) <br/> |enterpriseResources  <br/> |
|[Entitytype](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.EntityTypes.aspx) <br/> |Entitytype  <br/> |
|[EventHandlers](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.EventHandlers.aspx) <br/> |eventHandlers  <br/> |
|[イベント](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.Events.aspx) <br/> |events  <br/> |
|[参照テーブル](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.LookupTables.aspx) <br/> |lookupTables  <br/> |
|[フェーズ](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.Phases.aspx) <br/> |phases  <br/> |
|[Projects](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.Projects.aspx) <br/> |projects  <br/> |
|[ステージ](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.Stages.aspx) <br/> |stages  <br/> |
|[WorkflowActivities](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.WorkflowActivities.aspx) <br/> |workflowActivities  <br/> |
|[WorkflowDesigner](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.WorkflowDesigner.aspx) <br/> |workflowDesigner  <br/> |
   
## <a name="in-this-section"></a>このセクションの内容

[プロジェクト サーバー CSOM および .NET の概要](getting-started-with-the-project-server-csom-and-net.md)は、概要については、プロジェクトのサーバーの CSOM と .NET では、Visual Studio 2012 の、およびサポートのコード例で、単純な .NET CSOM の拡張機能を作成する方法についてを提供します。 
  
[Project Server 2013 の JavaScript オブジェクト モデルを使うにあたって](getting-started-with-the-project-server-2013-javascript-object-model.md)は、プロジェクト サーバー JSOM で、Visual Studio 2012 の、およびサポートのコード例で、単純な JSOM の拡張機能を作成する方法についての概要情報を提供します。 
  
CSOM の使用方法を示す次の記事も確認してください。
  
- [Project Online でユーザー設定フィールドを一括更新し、ワークフローからプロジェクト サイトを作成する](bulk-update-custom-fields-and-create-project-sites-from-workflow-in-project.md)
    
- [JavaScript オブジェクト モデルを使用してプロジェクトを操作する](create-retrieve-update-delete-projects-using-project-server-javascript.md)
    
> [!NOTE]
> CSOM を使用して.NET Framework 4 の開発に Visual Studio 2010 を使用することもできます。 
  
## <a name="reference"></a>リファレンス

[Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx)
  
## <a name="see-also"></a>関連項目



[Project Server 2013 のアーキテクチャ](project-server-2013-architecture.md)


[SharePoint 2013 での適切な API セットの選択](https://msdn.microsoft.com/library/f36645da-77c5-47f1-a2ca-13d4b62b320d%28Office.15%29.aspx)

