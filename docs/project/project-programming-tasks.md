---
title: Project のプログラミング タスク
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: ac5544e7-ff7a-4af5-ac1b-33a49bc6be0d
description: このセクションには、JavaScript ライブラリをクライアント側オブジェクトモデル (csom) で使用する方法、および project Server 2013 および project Online の他のプログラミングタスクを実行する方法を示す、方法に関する記事が含まれています。 プログラミングタスクの例としては、SharePoint でホストされる Project Server アプリの作成、需要管理のためのワークフローの作成などがあります。Project Server アプリケーションを Windows Communication Foundation (WCF) を使用してプログラミングする。Project Web App のリボンをカスタマイズするProject Server Web パーツの作成。Project Server イベントハンドラとリモートイベントレシーバーを作成するまたは、ユーザー設定フィールドを一括更新し、project Online 用のプロジェクトサイトを作成します。
ms.openlocfilehash: 385b9fa53c2c7faf2a218816bf4d3f0499b9ecd1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301499"
---
# <a name="project-programming-tasks"></a><span data-ttu-id="9f79d-104">Project のプログラミング タスク</span><span class="sxs-lookup"><span data-stu-id="9f79d-104">Project programming tasks</span></span>

<span data-ttu-id="9f79d-105">このセクションには、JavaScript ライブラリをクライアント側オブジェクトモデル (csom) で使用する方法を示すいくつかの操作方法に関する記事と、project Server 2013 および project Online の他のプログラミングタスクを実行する方法が記載されています。</span><span class="sxs-lookup"><span data-stu-id="9f79d-105">This section includes some "how-to" articles that show how to use the JavaScript library for the client-side object model (CSOM), and perform other programming tasks for Project Server 2013 and Project Online.</span></span> <span data-ttu-id="9f79d-106">プログラミングタスクの例としては、SharePoint でホストされる Project Server アプリの作成、需要管理のためのワークフローの作成などがあります。Project Server アプリケーションを Windows Communication Foundation (WCF) を使用してプログラミングする。Project Web App のリボンをカスタマイズするProject Server Web パーツの作成。Project Server イベントハンドラとリモートイベントレシーバーを作成するまたは、ユーザー設定フィールドを一括更新し、project Online 用のプロジェクトサイトを作成します。</span><span class="sxs-lookup"><span data-stu-id="9f79d-106">Examples of programming tasks include creating a SharePoint-hosted Project Server app, creating workflows for demand management; programming Project Server applications with the Windows Communication Foundation (WCF); customizing the Project Web App ribbon; creating Project Server Web Parts; creating Project Server event handlers and remote event receivers; and bulk updating custom fields and creating project sites for Project Online.</span></span>
  
> [!NOTE]
> <span data-ttu-id="9f79d-107">js grid コントロールを使用したプログラミングの詳細については、「SharePoint 2010 開発者用リファレンス」の「 [js grid control](https://msdn.microsoft.com/library/ee535898%28office.14%29.aspx) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9f79d-107">For information about programming with the JS Grid control, see [JS Grid Control](https://msdn.microsoft.com/library/ee535898%28office.14%29.aspx) in the SharePoint 2010 developer reference.</span></span> <span data-ttu-id="9f79d-108">マネージ コード リファレンスについては、「[Microsoft.SharePoint.JSGrid Namespace](https://msdn.microsoft.com/library/microsoft.sharepoint.jsgrid%28Office.15%29.aspx)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9f79d-108">For the managed code reference, see [Microsoft.SharePoint.JSGrid Namespace](https://msdn.microsoft.com/library/microsoft.sharepoint.jsgrid%28Office.15%29.aspx).</span></span> <span data-ttu-id="9f79d-109">JS Grid コントロール web コントロールの場合は、「 [JSGrid class](https://msdn.microsoft.com/library/microsoft.sharepoint.webcontrols.jsgrid%28Office.15%29.aspx)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9f79d-109">For the JS Grid control web controls, see [JSGrid class](https://msdn.microsoft.com/library/microsoft.sharepoint.webcontrols.jsgrid%28Office.15%29.aspx).</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="9f79d-110">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="9f79d-110">In this section</span></span>

[<span data-ttu-id="9f79d-111">Project Server ワークフロー開発の作業開始</span><span class="sxs-lookup"><span data-stu-id="9f79d-111">Getting started developing Project Server workflows</span></span>](getting-started-developing-project-server-workflows.md)
  
[<span data-ttu-id="9f79d-112">Project Online でユーザー設定フィールドを一括更新し、ワークフローからプロジェクト サイトを作成する</span><span class="sxs-lookup"><span data-stu-id="9f79d-112">Bulk update custom fields and create project sites from a workflow in Project Online</span></span>](bulk-update-custom-fields-and-create-project-sites-from-workflow-in-project.md)
  
[<span data-ttu-id="9f79d-113">Project Server JavaScript オブジェクトモデルを使用してプロジェクトを作成、取得、更新、削除する</span><span class="sxs-lookup"><span data-stu-id="9f79d-113">Create, retrieve, update, and delete projects by using the Project Server JavaScript object model</span></span>](create-retrieve-update-delete-projects-using-project-server-javascript.md)
  
<span data-ttu-id="9f79d-114">[SharePoint ホスト型 project Server アドインを作成](create-a-sharepoint-hosted-project-server-add-in.md)する: project Web App のリボンを変更する方法のセクションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="9f79d-114">[Create a SharePoint-hosted Project Server add-in](create-a-sharepoint-hosted-project-server-add-in.md) : includes a section on how to modify the Project Web App ribbon</span></span> 
  
## <a name="reference"></a><span data-ttu-id="9f79d-115">リファレンス</span><span class="sxs-lookup"><span data-stu-id="9f79d-115">Reference</span></span>

[<span data-ttu-id="9f79d-116">プロジェクト PSI リファレンスの概要</span><span class="sxs-lookup"><span data-stu-id="9f79d-116">Project PSI reference overview</span></span>](project-psi-reference-overview.md)
  
## <a name="see-also"></a><span data-ttu-id="9f79d-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="9f79d-117">See also</span></span>



[<span data-ttu-id="9f79d-118">Project 2013 のクライアント側オブジェクト モデル (CSOM)</span><span class="sxs-lookup"><span data-stu-id="9f79d-118">Client-side object model (CSOM) for Project 2013</span></span>](client-side-object-model-csom-for-project-2013.md)

