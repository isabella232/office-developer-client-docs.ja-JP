---
title: プロジェクトのプログラミング タスク
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: ac5544e7-ff7a-4af5-ac1b-33a49bc6be0d
description: このセクションには、何らかの方法で-toarticles クライアント側オブジェクト モデル (CSOM)、JavaScript ライブラリを使用し、Project Server 2013 とオンライン プロジェクトの他のプログラミング タスクを実行する方法を示しているにはが含まれています。 プログラミング タスクの例には、Project Server の SharePoint によってホストされるアプリケーションは、需要管理のワークフローを作成する作成が含まれます。プログラミング プロジェクトのサーバー アプリケーションで、Windows Communication Foundation (WCF)。は Project Web App のリボンをカスタマイズします。作成プロジェクト サーバー Web パーツです。Project Server イベント ハンドラーとリモート イベントの受信機を作成します。一括はユーザー設定フィールドを更新し、オンラインのプロジェクトのプロジェクト サイトを作成します。
ms.openlocfilehash: 79ff301b825b4eea073d5d1896e27be9e0090ba6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804681"
---
# <a name="project-programming-tasks"></a><span data-ttu-id="27049-104">プロジェクトのプログラミング タスク</span><span class="sxs-lookup"><span data-stu-id="27049-104">Project programming tasks</span></span>

<span data-ttu-id="27049-105">このセクションには、クライアント側オブジェクト モデル (CSOM)、JavaScript ライブラリを使用し、Project Server 2013 とオンライン プロジェクトの他のプログラミング タスクを実行する方法を示すいくつかの操作方法の記事が含まれています。</span><span class="sxs-lookup"><span data-stu-id="27049-105">This section includes some "how-to" articles that show how to use the JavaScript library for the client-side object model (CSOM), and perform other programming tasks for Project Server 2013 and Project Online.</span></span> <span data-ttu-id="27049-106">プログラミング タスクの例には、Project Server の SharePoint によってホストされるアプリケーションは、需要管理のワークフローを作成する作成が含まれます。プログラミング プロジェクトのサーバー アプリケーションで、Windows Communication Foundation (WCF)。は Project Web App のリボンをカスタマイズします。作成プロジェクト サーバー Web パーツです。Project Server イベント ハンドラーとリモート イベントの受信機を作成します。一括はユーザー設定フィールドを更新し、オンラインのプロジェクトのプロジェクト サイトを作成します。</span><span class="sxs-lookup"><span data-stu-id="27049-106">Examples of programming tasks include creating a SharePoint-hosted Project Server app, creating workflows for demand management; programming Project Server applications with the Windows Communication Foundation (WCF); customizing the Project Web App ribbon; creating Project Server Web Parts; creating Project Server event handlers and remote event receivers; and bulk updating custom fields and creating project sites for Project Online.</span></span>
  
> [!NOTE]
> <span data-ttu-id="27049-107">JS グリッド コントロールを使用するプログラミングについては、SharePoint 2010 開発者用リファレンスの[JS グリッド コントロール](http://msdn.microsoft.com/en-us/library/ee535898%28office.14%29.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="27049-107">For information about programming with the JS Grid control, see [JS Grid Control](http://msdn.microsoft.com/en-us/library/ee535898%28office.14%29.aspx) in the SharePoint 2010 developer reference.</span></span> <span data-ttu-id="27049-108">マネージ コードの参照は、 [Microsoft.SharePoint.JSGrid の Namespace](http://msdn.microsoft.com/en-us/library/microsoft.sharepoint.jsgrid%28Office.15%29.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="27049-108">For the managed code reference, see [Microsoft.SharePoint.JSGrid Namespace](http://msdn.microsoft.com/en-us/library/microsoft.sharepoint.jsgrid%28Office.15%29.aspx).</span></span> <span data-ttu-id="27049-109">JS グリッド コントロールの web コントロールは、 [JSGrid クラス](http://msdn.microsoft.com/en-us/library/microsoft.sharepoint.webcontrols.jsgrid%28Office.15%29.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="27049-109">For the JS Grid control web controls, see [JSGrid class](http://msdn.microsoft.com/en-us/library/microsoft.sharepoint.webcontrols.jsgrid%28Office.15%29.aspx).</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="27049-110">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="27049-110">In this section</span></span>

[<span data-ttu-id="27049-111">開発 Project Server ワークフローの開始を取得します。</span><span class="sxs-lookup"><span data-stu-id="27049-111">Getting started developing Project Server workflows</span></span>](getting-started-developing-project-server-workflows.md)
  
[<span data-ttu-id="27049-112">ユーザー設定フィールドの更新プログラムを一括して、ワークフロー プロジェクトをオンラインでのプロジェクト サイトを作成</span><span class="sxs-lookup"><span data-stu-id="27049-112">Bulk update custom fields and create project sites from a workflow in Project Online</span></span>](bulk-update-custom-fields-and-create-project-sites-from-workflow-in-project.md)
  
[<span data-ttu-id="27049-113">作成、取得、更新、およびプロジェクトのサーバーの JavaScript オブジェクト モデルを使用してプロジェクトを削除します。</span><span class="sxs-lookup"><span data-stu-id="27049-113">Create, retrieve, update, and delete projects by using the Project Server JavaScript object model</span></span>](create-retrieve-update-delete-projects-using-project-server-javascript.md)
  
<span data-ttu-id="27049-114">[プロジェクト SharePoint でホストされているサーバーを作成するアドイン](create-a-sharepoint-hosted-project-server-add-in.md): Project Web App のリボンを変更する方法に関するセクションが含まれています</span><span class="sxs-lookup"><span data-stu-id="27049-114">[Create a SharePoint-hosted Project Server add-in](create-a-sharepoint-hosted-project-server-add-in.md) : includes a section on how to modify the Project Web App ribbon</span></span> 
  
## <a name="reference"></a><span data-ttu-id="27049-115">リファレンス</span><span class="sxs-lookup"><span data-stu-id="27049-115">Reference</span></span>

[<span data-ttu-id="27049-116">プロジェクト PSI リファレンスの概要</span><span class="sxs-lookup"><span data-stu-id="27049-116">Project PSI reference overview</span></span>](project-psi-reference-overview.md)
  
## <a name="see-also"></a><span data-ttu-id="27049-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="27049-117">See also</span></span>



[<span data-ttu-id="27049-118">Project 2013 のクライアント側オブジェクト モデル (CSOM)</span><span class="sxs-lookup"><span data-stu-id="27049-118">Client-side object model (CSOM) for Project 2013</span></span>](client-side-object-model-csom-for-project-2013.md)

