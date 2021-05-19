---
title: PSI が行うこと、行わないこと
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: eac6be6a-9a20-4bc0-8da2-b2fd93aab04f
description: Project サーバー インターフェイス (PSI) は、サーバー 2013 のオンプレミス インストールで多くのサーバー側プロセスを自動化Projectできます。 ただし、いくつかの関数では、複数の関数を使用する必要Microsoft Project Professional 2013。
ms.openlocfilehash: b93c3535ca6693a84d11370de17bc18375f168ab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346530"
---
# <a name="what-the-psi-does-and-does-not-do"></a><span data-ttu-id="29d98-104">PSI のすること、しないこと</span><span class="sxs-lookup"><span data-stu-id="29d98-104">What the PSI does and does not do</span></span>

<span data-ttu-id="29d98-105">Project サーバー インターフェイス (PSI) は、サーバー 2013 のオンプレミス インストールで多くのサーバー側プロセスを自動化Projectできます。</span><span class="sxs-lookup"><span data-stu-id="29d98-105">The Project Server Interface (PSI) can help to automate many server-side processes in on-premises installations of Project Server 2013.</span></span> <span data-ttu-id="29d98-106">ただし、いくつかの関数では、複数の関数を使用する必要Microsoft Project Professional 2013。</span><span class="sxs-lookup"><span data-stu-id="29d98-106">But, several functions require the use of Microsoft Project Professional 2013.</span></span>
  
|||
|:-----|:-----|
|||
   
<span data-ttu-id="29d98-107">PSI は、すべての機能にサーバー ベースの代替手段を提供するのではなく、Project Professional 2013 の機能を補完Project Professionalされています。</span><span class="sxs-lookup"><span data-stu-id="29d98-107">The PSI is designed to complement the capabilities of Project Professional 2013, rather than provide a server-based alternative for all Project Professional functions.</span></span> <span data-ttu-id="29d98-108">サード パーティの開発者は、PSI を使用して、Project Web App およびプロジェクト ワークスペースのオンプレミス インストール用の Web パーツ の作成、オンプレミスの Project Server データを操作するカスタム Windows アプリケーションと Web アプリケーションの作成、プロジェクト ポートフォリオ管理のワークフロー ロジックの開発、ローカルの完全信頼イベント ハンドラーの開発、Project Server と他のアプリケーションの統合を支援できます。</span><span class="sxs-lookup"><span data-stu-id="29d98-108">Third-party developers can use the PSI to help create Web Parts for on-premises installations of Project Web App and project workspaces, create custom Windows applications and web applications that interact with on-premises Project Server data, develop workflow logic for project portfolio management, develop local full-trust event handlers, and integrate Project Server with other applications.</span></span> <span data-ttu-id="29d98-109">PSI は、Office ストア、モバイル デバイス、またはタブレット用のアプリの開発には使用できません。このためには、クライアント側オブジェクト モデル (CSOM) を使用できます。</span><span class="sxs-lookup"><span data-stu-id="29d98-109">The PSI cannot be used for development of apps for the Office Store, mobile devices, or tablets; for that, you can use the client-side object model (CSOM).</span></span>
  
> [!NOTE]
> <span data-ttu-id="29d98-110">PSI は、CSOM が提供するよりも、Project Server 2013 に対してより包括的なプログラムインターフェイスを提供します。</span><span class="sxs-lookup"><span data-stu-id="29d98-110">The PSI provides a more comprehensive programmatic interface for Project Server 2013 than the CSOM provides.</span></span> <span data-ttu-id="29d98-111">ただし、CSOM に必要な機能がない場合を除き、新規アプリケーションの開発には CSOM を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="29d98-111">But, unless the CSOM does not provide the functionality that you require, we recommend that you use the CSOM to develop new applications.</span></span> <span data-ttu-id="29d98-112">詳細については、「[What the CSOM does and does not do](what-the-csom-does-and-does-not-do.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="29d98-112">For more information, see [What the CSOM does and does not do](what-the-csom-does-and-does-not-do.md).</span></span> 
  
## <a name="usage-scenarios-for-the-psi"></a><span data-ttu-id="29d98-113">PSI の使用シナリオ</span><span class="sxs-lookup"><span data-stu-id="29d98-113">Usage scenarios for the PSI</span></span>
<span data-ttu-id="29d98-114"><a name="pj14_WhatPSIDoes_UsageScenarios"> </a></span><span class="sxs-lookup"><span data-stu-id="29d98-114"><a name="pj14_WhatPSIDoes_UsageScenarios"> </a></span></span>

<span data-ttu-id="29d98-115">以下に、PSI がサーバー側のプロジェクトおよび計算のためにサポートするアプリケーションの例をいくつか示します。</span><span class="sxs-lookup"><span data-stu-id="29d98-115">Following are examples of some applications that the PSI supports for server-side projects and calculations:</span></span>
  
- <span data-ttu-id="29d98-116">**サーバー内のエンティティ** の作成または管理をProjectするProject Professional 2013 と Project Web App は、プロジェクト、エンタープライズ リソース、ユーザー設定フィールドなどのエンティティの管理と作成を処理するように設計されていますが、多くの場合、カスタム アプリケーションは一括ジョブや繰り返しジョブで時間を節約できます。</span><span class="sxs-lookup"><span data-stu-id="29d98-116">**Automate the creation or management of entities in Project Server** Although Project Professional 2013 and Project Web App together are designed to handle management and creation of entities such as projects, enterprise resources, and custom fields, there are often cases where a custom application can save time with bulk or repetitive jobs.</span></span> <span data-ttu-id="29d98-117">PSI は、OLAP キューブ、プロジェクト ポートフォリオ分析、ビジネス ドライバー、通知、オブジェクト リンク プロバイダー、セキュリティ、SharePoint との相互運用性など、CSOM では不可能な、いくつかの種類のジョブの自動化を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="29d98-117">The PSI can automate several kinds of jobs that the CSOM does not do, for example, with OLAP cubes, project portfolio analyses, business drivers, notifications, object link providers, security, and SharePoint interoperability.</span></span> 
    
- <span data-ttu-id="29d98-118">**データベースの発行済みテーブルまたはアーカイブ テーブルのデータをProjectする** 下書き、発行済み、およびアーカイブ テーブルへの直接データベース アクセスはサポートされていないので、PSI を使用して、レポート テーブルまたはビューで使用できないデータを読み取りできます。</span><span class="sxs-lookup"><span data-stu-id="29d98-118">**Get data in the published or archive tables of the Project database** Because direct database access to the draft, published, and archive tables is not supported, you can use the PSI to read data that is not available in the reporting tables or views.</span></span> <span data-ttu-id="29d98-119">たとえば、アーカイブ テーブルに格納されているプロジェクトのバージョン、日付、変更に関する情報を取得し、Web パーツの JS Grid コントロールに情報を設定します。</span><span class="sxs-lookup"><span data-stu-id="29d98-119">For example, get information about project versions, dates, and changes that are stored in the archive tables, and then populate a JS Grid control in a web part with the information.</span></span> 
    
- <span data-ttu-id="29d98-120">**状態とタイムシートのデータを検証する** ローカルのプレイベント ハンドラーの PSI を使用して、ユーザーが入力した割り当て状態またはタイムシート データを検証してから、データをユーザーに保存Project Web App。</span><span class="sxs-lookup"><span data-stu-id="29d98-120">**Validate statusing and timesheet data** Use the PSI in local pre-event handlers to validate assignment status or timesheet data that users enter, before the data is saved in Project Web App.</span></span> 
    
- <span data-ttu-id="29d98-p107">**保守プロジェクト** リソース計画と共に使用するプレースホルダー プロジェクトを作成します。リソースに対する保守作業または基本業務用の時間を確保または予約します。通常、保守プロジェクトはタスクを持っていません。</span><span class="sxs-lookup"><span data-stu-id="29d98-p107">**Maintenance projects** Create placeholder projects to use with resource plans. Reserve or book time against resources for maintenance work or base business. Maintenance projects generally do not have tasks.</span></span> 
    
- <span data-ttu-id="29d98-124">**財務プロジェクトの作成** 財務システムとの統合用にタイムシートを使用して、時間取得のためのプロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="29d98-124">**Create financial projects** Create projects for time capture through the timesheet for integration with a financial system.</span></span> <span data-ttu-id="29d98-125">財務システムのコスト ブレークダウン ストラクチャを反映した、財務コードの階層を作成します。</span><span class="sxs-lookup"><span data-stu-id="29d98-125">Create a hierarchy of financial codes that reflect the cost breakdown structure of the financial system.</span></span> <span data-ttu-id="29d98-126">財務プロジェクトには、スケジュールや実績の更新は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="29d98-126">Financial projects do not require scheduling or status updates.</span></span> 
    
- <span data-ttu-id="29d98-127">**会計システムとの統合** 財務システムと課金システムに入力し、予算を比較する目的のために、プロジェクトに関連するリソース コストと経費を取得します。</span><span class="sxs-lookup"><span data-stu-id="29d98-127">**Integrate with accounting systems** Capture the resource costs and expenses associated with projects to feed financial and billing systems and for budget comparison purposes.</span></span> <span data-ttu-id="29d98-128">システム間のタスク、リソース、および割り当てを同期します。</span><span class="sxs-lookup"><span data-stu-id="29d98-128">Synchronize tasks, resources, and assignments between the systems.</span></span> <span data-ttu-id="29d98-129">あるシステムのタイムシート データを取得して、他のタイムシート データに入力します (使用するタイムシートは、組織または個別のプロジェクトのニーズによって決まります)。</span><span class="sxs-lookup"><span data-stu-id="29d98-129">Capture timesheet data in one system to feed the other (which timesheet is used depends on the needs of the organization or of individual projects).</span></span> 
    
- <span data-ttu-id="29d98-130">**チーム メンバーの更新の自動化** アクティブに管理されていないプロジェクトについて、プロジェクト チーム メンバーからの進捗およびその他の変更に関してサーバー上で自動的にプロジェクトが更新されるようにします。</span><span class="sxs-lookup"><span data-stu-id="29d98-130">**Automate updates from team members** For projects that are not actively managed, automatically update projects on the server with progress and other changes from project team members.</span></span> <span data-ttu-id="29d98-131">プロジェクト管理者が結果を見直したり、計画を調整したりしなくても、プロジェクトを更新したり、再発行したりできます。</span><span class="sxs-lookup"><span data-stu-id="29d98-131">Projects can be updated and republished without a project manager reviewing the results or making adjustments to the plan.</span></span> 
    
- <span data-ttu-id="29d98-132">**ローカルProjectイベント ハンドラーの** サーバー データの評価ProjectCreating プレイベントのローカル イベント ハンドラーは **、PSI** Project Server データを使用して、イベントをキャンセルするかどうかを判断できます。</span><span class="sxs-lookup"><span data-stu-id="29d98-132">**Evaluate Project Server data in local full-trust event handlers** A local event handler for the **ProjectCreating** pre-event can use Project Server data from the PSI to help determine whether to cancel an event.</span></span> <span data-ttu-id="29d98-133">たとえば、プロジェクトを作成する前に、既存のプロジェクトとプロジェクトの提案を比較することができます。</span><span class="sxs-lookup"><span data-stu-id="29d98-133">For example, before creating a project, compare the project proposal with existing projects.</span></span> 
    
- <span data-ttu-id="29d98-134">**需要管理用のカスタム ワークフロー アクティビティを作成する** ローカルの完全信頼ワークフロー アクティビティの PSI を使用して、エンタープライズ プロジェクト テンプレートに基づいてプロジェクト提案を変更および更新します。</span><span class="sxs-lookup"><span data-stu-id="29d98-134">**Create custom workflow activities for demand management** Use the PSI in local, full-trust workflow activities to modify and update project proposals based on enterprise project templates.</span></span> <span data-ttu-id="29d98-135">プロジェクト ユーザー設定フィールドを使用して開始および承認プロセスに必要な情報でプロジェクトにタグを付けます。</span><span class="sxs-lookup"><span data-stu-id="29d98-135">Use project custom fields to tag the project with information needed for the initiation and approval process.</span></span> <span data-ttu-id="29d98-136">主要なマイルストーンまたは成果物のプロジェクト フェーズを識別するタスクを追加します。</span><span class="sxs-lookup"><span data-stu-id="29d98-136">Add tasks to identify project phases for key milestones or deliverables.</span></span> <span data-ttu-id="29d98-137">承認された提案は、ワークフローによって Project Professional で管理される完全なプロジェクトに変更することができます。</span><span class="sxs-lookup"><span data-stu-id="29d98-137">When project proposals are approved, a workflow can change the proposals into full-scale projects that are managed with Project Professional.</span></span> 
    
- <span data-ttu-id="29d98-138">**PSI 拡張機能を作成する** (**非推奨)。**</span><span class="sxs-lookup"><span data-stu-id="29d98-138">**Create PSI extensions** (**Deprecated.**</span></span> <span data-ttu-id="29d98-139">拡張機能は Server 2013 Project非推奨であり、今後のリリースではサポートされません)。PSI は、カスタム サービスを使用して、WINDOWS (WCF) インターフェイスを使用して拡張できます。</span><span class="sxs-lookup"><span data-stu-id="29d98-139">Extensions are deprecated in Project Server 2013, and will not be supported in future releases.) The PSI can be extended with custom services by using the Windows Communication Foundation (WCF) interface.</span></span> <span data-ttu-id="29d98-140">PSI 拡張機能は Project Server コンピューターで実行でき、組み込みの PSI サービスで使用するのと同じセキュリティ インフラストラクチャを使用できます。</span><span class="sxs-lookup"><span data-stu-id="29d98-140">PSI extensions run on the Project Server computer, and can use the same security infrastructure that the built-in PSI services use.</span></span> <span data-ttu-id="29d98-141">拡張機能では、レポート テーブルのクエリ、別のデータベース テーブルの使用、帯域幅を節約するための PSI 呼び出しの統合、サードパーティ アプリケーションやその他のサーバー側コンポーネントとの統合を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="29d98-141">Extensions can query the reporting tables, use separate database tables, consolidate PSI calls to save bandwidth, and integrate with third-party applications and other server-side components.</span></span> <span data-ttu-id="29d98-142">詳細については、「[PSI 拡張機能の開発](https://msdn.microsoft.com/library/1b484623-94fb-47c9-84c1-3e68a9133042%28Office.15%29.aspx)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="29d98-142">For more information, see [Developing PSI Extensions](https://msdn.microsoft.com/library/1b484623-94fb-47c9-84c1-3e68a9133042%28Office.15%29.aspx).</span></span>
    
- <span data-ttu-id="29d98-143">**ローカルの完全信頼アプリケーションで偽装を使用する** PSI の WCF インターフェイスへの呼び出しは偽装できます。そのため、アプリケーションは偽装されたユーザーのセキュリティアクセス許可を前提とします。</span><span class="sxs-lookup"><span data-stu-id="29d98-143">**Use impersonation in local, full-trust applications** Calls to the WCF interface of the PSI can be impersonated, so that an application assumes the security permissions of the impersonated user.</span></span> <span data-ttu-id="29d98-144">偽装は限定的かつ慎重に使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="29d98-144">Impersonation should be used sparingly and carefully.</span></span> <span data-ttu-id="29d98-145">他のユーザーの状態情報の読み取りと更新には、偽装は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="29d98-145">Reading and updating status information for other users does not require impersonation.</span></span> <span data-ttu-id="29d98-146">偽装を必要とする新しいアプリケーションでは、PSI ではなく CSOM および OAuth プロトコルを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="29d98-146">New applications that require impersonation should use the CSOM and the OAuth protocol instead of the PSI.</span></span> <span data-ttu-id="29d98-147">PSI での偽装の詳細については、「Use [Impersonation with WCF」を参照してください](https://msdn.microsoft.com/library/e3597901-2f02-44a2-8076-d32aae540b38%28Office.15%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="29d98-147">For more information about impersonation with the PSI, see [Use Impersonation with WCF](https://msdn.microsoft.com/library/e3597901-2f02-44a2-8076-d32aae540b38%28Office.15%29.aspx).</span></span>
    
> [!NOTE]
> <span data-ttu-id="29d98-148">場合によっては、PSI は CSOM とクライアント アプリケーションで使用Project Online。</span><span class="sxs-lookup"><span data-stu-id="29d98-148">In some cases, the PSI can be used in client applications with the CSOM and Project Online.</span></span> <span data-ttu-id="29d98-149">ASMX ベースの PSI Web サービスを使用する場合、アプリケーションには、CSOM で [Microsoft.ProjectServer.Client.ProjectContext](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.aspx) オブジェクトを認証するメソッドと **、System.Web.Services.Protocols.SoapHttpClientProtocol** クライアント オブジェクトを認証するメソッドが含まれる必要があります。</span><span class="sxs-lookup"><span data-stu-id="29d98-149">If you use an ASMX-based PSI web service, the application must include a method to authenticate the [Microsoft.ProjectServer.Client.ProjectContext](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.aspx) object in the CSOM and a method to authenticate the **System.Web.Services.Protocols.SoapHttpClientProtocol** client object.</span></span> <span data-ttu-id="29d98-150">SharePoint CSOM で Web サービスを使用する例については、「[クレーム ベース認証を使用した SharePoint Online でのリモート認証](https://msdn.microsoft.com/library/49067f7a-3020-478f-ba97-4b7ce3ea9b87%28Office.15%29.aspx)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="29d98-150">For an example that uses a web service with the SharePoint CSOM, see [Remote Authentication in SharePoint Online Using Claims-Based Authentication](https://msdn.microsoft.com/library/49067f7a-3020-478f-ba97-4b7ce3ea9b87%28Office.15%29.aspx).</span></span> <span data-ttu-id="29d98-151">>アプリ レベルのアクセス許可が制限されたため、パブリック ストアでの配布用に設計されたアプリでは PSI をOfficeできません。</span><span class="sxs-lookup"><span data-stu-id="29d98-151">> Because of constrained app-level permissions, the PSI cannot be used in apps that are designed for distribution in the public Office Store.</span></span> <span data-ttu-id="29d98-152">その場合は、CSOM のみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="29d98-152">In that case, you can use only the CSOM.</span></span> 
  
## <a name="what-the-psi-does-not-do"></a><span data-ttu-id="29d98-153">PSI が行わないこと</span><span class="sxs-lookup"><span data-stu-id="29d98-153">What the PSI does not do</span></span>
<span data-ttu-id="29d98-154"><a name="pj14_WhatPSIDoes_DoesNotDo"> </a></span><span class="sxs-lookup"><span data-stu-id="29d98-154"><a name="pj14_WhatPSIDoes_DoesNotDo"> </a></span></span>

<span data-ttu-id="29d98-p116">PSI が行えることはたくさんありますが、PSI が行えないこともあります。以下に、PSI では行えず、CSOM では行えることを 2 つ示します。</span><span class="sxs-lookup"><span data-stu-id="29d98-p116">Although there are many things the PSI can do, there are some things the PSI does not do. Following are two things the PSI cannot do, but the CSOM can do.</span></span>
  
### <a name="project-online-and-remote-event-receivers"></a><span data-ttu-id="29d98-157">Project Onlineリモート イベント レシーバー</span><span class="sxs-lookup"><span data-stu-id="29d98-157">Project Online and remote event receivers</span></span>

<span data-ttu-id="29d98-158">PSI の主な制限は、次のProject Online。</span><span class="sxs-lookup"><span data-stu-id="29d98-158">The primary limitation of the PSI is with Project Online.</span></span> <span data-ttu-id="29d98-159">PSI を使用するアプリケーションには、Project Server の社内インストールに対する完全信頼アクセス権が必要です。</span><span class="sxs-lookup"><span data-stu-id="29d98-159">Applications that use the PSI require full-trust access to an on-premises installation of Project Server.</span></span> <span data-ttu-id="29d98-160">たとえば、PSI はリモート イベント レシーバーでは使用できません。イベント レシーバーは、イベント レシーバーがサービスとしてインストールMicrosoft Azure。</span><span class="sxs-lookup"><span data-stu-id="29d98-160">For example, the PSI cannot be used in remote event receivers, where the event receiver is installed as a service on Microsoft Azure.</span></span>
  
### <a name="workflows-and-claims-authentication"></a><span data-ttu-id="29d98-161">ワークフローおよびクレーム認証</span><span class="sxs-lookup"><span data-stu-id="29d98-161">Workflows and claims authentication</span></span>

<span data-ttu-id="29d98-162">ワークフロー Foundation バージョン 4 (WF4) Windowsを使用するワークフロー定義では、PSI が直接サポートしないクレーム認証が必要です。</span><span class="sxs-lookup"><span data-stu-id="29d98-162">A workflow definition that uses Windows Workflow Foundation version 4 (WF4) requires claims authentication, which the PSI does not directly support.</span></span> <span data-ttu-id="29d98-163">つまり、PSI を使用して、WF4 ワークフロー定義を持つエンタープライズ プロジェクトタイプ (EPT) を持つ Project Server 2013 でプロジェクトを作成することはできません。</span><span class="sxs-lookup"><span data-stu-id="29d98-163">This means you cannot use the PSI to create a project in Project Server 2013 that has an enterprise project type (EPT) with a WF4 workflow definition.</span></span>
  
<span data-ttu-id="29d98-164">PSI を使用して、ワークフローがない EPT または従来の WF3.5 定義 (Project Server 2010 のワークフロー バージョン) を使用してプロジェクトを作成できます。</span><span class="sxs-lookup"><span data-stu-id="29d98-164">You can use the PSI to create projects with EPTs that either have no workflow or use a legacy WF3.5 definition (the workflow version in Project Server 2010).</span></span> <span data-ttu-id="29d98-165">WF4 定義を持つ EPT でプロジェクトを作成するには、CSOM を使用します。</span><span class="sxs-lookup"><span data-stu-id="29d98-165">To create a project with an EPT that has a WF4 definition, use the CSOM.</span></span>
  
 <span data-ttu-id="29d98-166">**Project Professional を必要とするアクション:**</span><span class="sxs-lookup"><span data-stu-id="29d98-166">**Actions that require Project Professional:**</span></span>
  
<span data-ttu-id="29d98-167">次のリストは、PSI と CSOM のどちらでも行うことのできない処理を示しています。</span><span class="sxs-lookup"><span data-stu-id="29d98-167">The following list are things that neither the PSI nor the CSOM can do.</span></span>
  
#### <a name="local-data"></a><span data-ttu-id="29d98-168">ローカル データ</span><span class="sxs-lookup"><span data-stu-id="29d98-168">Local data</span></span>

- <span data-ttu-id="29d98-p120">ローカル プロジェクト (.mpp ファイル) でのデータの操作。たとえば、コスト単価表またはローカル リソースの利用可能時間の定義。</span><span class="sxs-lookup"><span data-stu-id="29d98-p120">Manipulating data in local projects (.mpp files). For example, defining cost rate tables or availability contours for local resources.</span></span> 
    
- <span data-ttu-id="29d98-171">ローカル基本カレンダーまたはリソース カレンダー (カレンダーの例外を含む) の定義または編集。</span><span class="sxs-lookup"><span data-stu-id="29d98-171">Defining or editing local base calendars or resource calendars, including calendar exceptions.</span></span>
    
- <span data-ttu-id="29d98-p121">ローカル ユーザー設定フィールドの定義 (PSI で、タスク、リソース、および割り当てのローカル ユーザー設定フィールドの値を編集することは可能です)。</span><span class="sxs-lookup"><span data-stu-id="29d98-p121">Defining local custom fields. (The PSI does support editing local custom field values on tasks, resources, and assignments.)</span></span>
    
#### <a name="enterprise-data"></a><span data-ttu-id="29d98-174">エンタープライズ データ</span><span class="sxs-lookup"><span data-stu-id="29d98-174">Enterprise data</span></span>

- <span data-ttu-id="29d98-175">エンタープライズ グローバル テンプレートのチェック アウトまたは編集。</span><span class="sxs-lookup"><span data-stu-id="29d98-175">Checking out or editing the enterprise global template.</span></span> <span data-ttu-id="29d98-176">Project Server 2013 のエンタープライズ グローバル データは、Project データベース内のバイナリ データ テーブルのセットであり、Office Project Server 2007 以前のバージョンのプロジェクト テンプレートではありません。</span><span class="sxs-lookup"><span data-stu-id="29d98-176">The enterprise global data in Project Server 2013 is a set of binary data tables in the Project database, not a project template as in Office Project Server 2007 and earlier versions.</span></span>
    
- <span data-ttu-id="29d98-177">エンタープライズ カレンダーの定義または編集。</span><span class="sxs-lookup"><span data-stu-id="29d98-177">Defining or editing enterprise calendars.</span></span> <span data-ttu-id="29d98-178">[Calendar メソッドは](https://msdn.microsoft.com/library/WebSvcCalendar.Calendar.aspx)、予定表の例外のみを管理します。</span><span class="sxs-lookup"><span data-stu-id="29d98-178">The [Calendar](https://msdn.microsoft.com/library/WebSvcCalendar.Calendar.aspx) methods manage only calendar exceptions.</span></span> 
    
#### <a name="master-projects-and-cross-project-links"></a><span data-ttu-id="29d98-179">マスター プロジェクトおよびプロジェクト間のリンク</span><span class="sxs-lookup"><span data-stu-id="29d98-179">Master projects and cross-project links</span></span>

- <span data-ttu-id="29d98-180">マスター プロジェクトの作成とサブプロジェクトの挿入。</span><span class="sxs-lookup"><span data-stu-id="29d98-180">Creating master projects and inserting subprojects.</span></span>
    
- <span data-ttu-id="29d98-181">マスター プロジェクト全体にわたるクリティカル パスのスケジューリング。</span><span class="sxs-lookup"><span data-stu-id="29d98-181">Scheduling a critical path across a master project.</span></span> 
    
- <span data-ttu-id="29d98-182">プロジェクト間のリンクの作成。</span><span class="sxs-lookup"><span data-stu-id="29d98-182">Creating cross-project links.</span></span>
    
#### <a name="resources"></a><span data-ttu-id="29d98-183">リソース</span><span class="sxs-lookup"><span data-stu-id="29d98-183">Resources</span></span>

- <span data-ttu-id="29d98-184">リソースの平準化の要求または実行。</span><span class="sxs-lookup"><span data-stu-id="29d98-184">Requesting or performing resource leveling.</span></span>
    
- <span data-ttu-id="29d98-p124">割り当て上のリソースの変更 (PSI を使用して割り当てを削除し、新しい割り当てを作成することは可能です)。</span><span class="sxs-lookup"><span data-stu-id="29d98-p124">Changing the resource on an assignment. (You can use the PSI to delete the assignment and create a new one.)</span></span>
    
- <span data-ttu-id="29d98-187">認められた実際の作業 (実績) を持つリソースの削除または置換。</span><span class="sxs-lookup"><span data-stu-id="29d98-187">Deleting or replacing a resource that has actual work accepted (actuals).</span></span>
    
- <span data-ttu-id="29d98-188">時間単価型、数量単価型、およびコスト型の間でのリソースの種類の変更。</span><span class="sxs-lookup"><span data-stu-id="29d98-188">Changing a resource type between work, material, and cost.</span></span>
    
- <span data-ttu-id="29d98-189">リソース カレンダーの作成または編集。</span><span class="sxs-lookup"><span data-stu-id="29d98-189">Creating or editing resource calendars.</span></span>
    
- <span data-ttu-id="29d98-p125">タスクにリソースを追加する場合、PSI は Project Professional のように作業を自動的に再配布しません。割り当てで作業の配布を選択して明示的に設定するのは、開発者の役割です。</span><span class="sxs-lookup"><span data-stu-id="29d98-p125">When adding a resource to a task, the PSI does not automatically redistribute work the way Project Professional does. It is up to the developer to choose and explicitly set the work distribution on the assignments.</span></span>
    
#### <a name="cost-resources"></a><span data-ttu-id="29d98-192">Cost resources</span><span class="sxs-lookup"><span data-stu-id="29d98-192">Cost resources</span></span>

- <span data-ttu-id="29d98-193">コスト リソースと割り当ての編集、作成、または削除は、Project[使用します](https://msdn.microsoft.com/library/WebSvcProject.Project.aspx)。</span><span class="sxs-lookup"><span data-stu-id="29d98-193">Editing, creating, or deleting cost resources and assignments using the [Project](https://msdn.microsoft.com/library/WebSvcProject.Project.aspx) methods.</span></span> <span data-ttu-id="29d98-194">Resource [メソッドは](https://msdn.microsoft.com/library/WebSvcResource.Resource.aspx) コスト リソースを作成できますが、編集することはできません。</span><span class="sxs-lookup"><span data-stu-id="29d98-194">The [Resource](https://msdn.microsoft.com/library/WebSvcResource.Resource.aspx) methods can create cost resources but cannot edit them.</span></span> 
    
#### <a name="work-contours"></a><span data-ttu-id="29d98-195">作業配分</span><span class="sxs-lookup"><span data-stu-id="29d98-195">Work contours</span></span>

- <span data-ttu-id="29d98-196">タイムスケール データの編集。</span><span class="sxs-lookup"><span data-stu-id="29d98-196">Editing timephased data.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="29d98-197">[Statusing Web サービスの UpdateStatus](https://msdn.microsoft.com/library/WebSvcStatusing.Statusing.UpdateStatus.aspx)メソッドは、プロジェクト マネージャーが割り当てデータを更新して発行した後、割り当て時のタイムスケール実績を編集できます。 </span><span class="sxs-lookup"><span data-stu-id="29d98-197">The [UpdateStatus](https://msdn.microsoft.com/library/WebSvcStatusing.Statusing.UpdateStatus.aspx) method in the **Statusing** Web service can edit timephased actuals on assignments after the project manager updates and publishes the assignment data.</span></span> 
  
- <span data-ttu-id="29d98-198">割り当ての配分型 (均等型、増加型、減少型など) の設定または変更。</span><span class="sxs-lookup"><span data-stu-id="29d98-198">Setting or changing the assignment contour type (such as flat, back-loaded, or front-loaded).</span></span>
    
#### <a name="baselines-and-earned-value"></a><span data-ttu-id="29d98-199">基準計画および達成額</span><span class="sxs-lookup"><span data-stu-id="29d98-199">Baselines and earned value</span></span>

- <span data-ttu-id="29d98-200">基準計画の保存または基準計画データの編集。</span><span class="sxs-lookup"><span data-stu-id="29d98-200">Saving a baseline or editing baseline data.</span></span> 
    
- <span data-ttu-id="29d98-201">進捗日の設定。</span><span class="sxs-lookup"><span data-stu-id="29d98-201">Setting a progress date.</span></span>
    
- <span data-ttu-id="29d98-202">差異および達成額の計算。</span><span class="sxs-lookup"><span data-stu-id="29d98-202">Calculating variance and earned value.</span></span> 
    
#### <a name="interactive-scheduling"></a><span data-ttu-id="29d98-203">対話型スケジューリング</span><span class="sxs-lookup"><span data-stu-id="29d98-203">Interactive scheduling</span></span>

- <span data-ttu-id="29d98-p127">対話型スケジューリングのサポート (Project Server は対話を非同期に処理するため、対話型スケジューリングは Project Professional を使用して行う必要があります)。</span><span class="sxs-lookup"><span data-stu-id="29d98-p127">Supporting interactive scheduling. (Because Project Server handles interactions asynchronously, interactive scheduling should be done with Project Professional.)</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="29d98-206">プログラムによる動作の変更を避けるため、Project Server 2010 から転送される PSI メソッドは、Project Server 2013 でも同様に動作します。</span><span class="sxs-lookup"><span data-stu-id="29d98-206">To avoid changing programmatic behavior, the PSI methods that are brought forward from Project Server 2010 act the same way in Project Server 2013.</span></span> <span data-ttu-id="29d98-207">たとえば [、QueueUpdateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject.aspx) には引き続き同じ制限があり、以前のサーバー側スケジューリング エンジンを使用します。</span><span class="sxs-lookup"><span data-stu-id="29d98-207">For example, [QueueUpdateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject.aspx) still has the same limitations and uses the older server-side scheduling engine.</span></span> <span data-ttu-id="29d98-208">新しい[QueueUpdateProject2](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject2.aspx)メソッドは、これらの制限の多くを削除し、Project Server 2013 サーバー側の新しいスケジューリング エンジン (Project Professional 2013 と同じスケジュール エンジン) を使用します。</span><span class="sxs-lookup"><span data-stu-id="29d98-208">The new [QueueUpdateProject2](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject2.aspx) method removes many of those limitations and uses the new Project Server 2013 server-side scheduling engine, which is the same scheduling engine that is in Project Professional 2013.</span></span> 
  
#### <a name="wbs"></a><span data-ttu-id="29d98-209">WBS</span><span class="sxs-lookup"><span data-stu-id="29d98-209">WBS</span></span>

- <span data-ttu-id="29d98-210">Work Breakdown Structure (WBS) コード マスクの定義。</span><span class="sxs-lookup"><span data-stu-id="29d98-210">Defining a work breakdown structure (WBS) code mask.</span></span> 
    
#### <a name="tasks"></a><span data-ttu-id="29d98-211">タスク</span><span class="sxs-lookup"><span data-stu-id="29d98-211">Tasks</span></span>

- <span data-ttu-id="29d98-212">タスクの種類 (作業時間固定、期間固定、または単位数固定) の変更。</span><span class="sxs-lookup"><span data-stu-id="29d98-212">Changing the task type (fixed work, duration, or units).</span></span>
    
- <span data-ttu-id="29d98-213">タスクが残存作業優先であるかどうかの変更。</span><span class="sxs-lookup"><span data-stu-id="29d98-213">Changing whether a task is effort-driven.</span></span>
    
- <span data-ttu-id="29d98-214">タスクの固定コスト計上の時期の変更。</span><span class="sxs-lookup"><span data-stu-id="29d98-214">Changing task fixed-cost accrual.</span></span>
    
- <span data-ttu-id="29d98-215">[プロパティ] フィールドの [TASK_NOTES](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_NOTES.aspx) 変更します。</span><span class="sxs-lookup"><span data-stu-id="29d98-215">Changing the content of the [TASK_NOTES](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_NOTES.aspx) field.</span></span> <span data-ttu-id="29d98-216">PSI は、.rtf バイナリ データであるタスク メモのテキスト部分のみを読み取ることができます。</span><span class="sxs-lookup"><span data-stu-id="29d98-216">The PSI can read only the text part of the task notes, which are .rtf binary data.</span></span> <span data-ttu-id="29d98-217">ただし、テキスト データである割り当 [てメモ (ASSN_NOTES)](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.AssignmentRow.ASSN_NOTES.aspx) を編集できます。</span><span class="sxs-lookup"><span data-stu-id="29d98-217">But, you can edit assignment notes ( [ASSN_NOTES](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.AssignmentRow.ASSN_NOTES.aspx) ), which are text data.</span></span> <span data-ttu-id="29d98-218">レポート データベースは、タスク メモまたは割り当てメモを含みません。</span><span class="sxs-lookup"><span data-stu-id="29d98-218">The Reporting database does not include task or assignment notes.</span></span> 
    
- <span data-ttu-id="29d98-219">定期タスクの作成または編集。</span><span class="sxs-lookup"><span data-stu-id="29d98-219">Creating or editing recurring tasks.</span></span>
    
- <span data-ttu-id="29d98-220">既存のタスクでのタスク カレンダーの割り当てまたは変更。</span><span class="sxs-lookup"><span data-stu-id="29d98-220">Assigning or changing the task calendar on existing tasks.</span></span>
    
- <span data-ttu-id="29d98-221">タスク カレンダーを使用した新しいタスクの作成。</span><span class="sxs-lookup"><span data-stu-id="29d98-221">Creating a new task with a task calendar.</span></span>
    
- <span data-ttu-id="29d98-222">[タスク] フィールドの [値TASK_IGNORES_RES_CAL](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_IGNORES_RES_CAL.aspx) 変更します (タスクはリソースカレンダーを無視します)。</span><span class="sxs-lookup"><span data-stu-id="29d98-222">Changing the value of the [TASK_IGNORES_RES_CAL](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_IGNORES_RES_CAL.aspx) field (task ignores resource calendar).</span></span> 
    
- <span data-ttu-id="29d98-223">同じ呼び出しで追加の変更が行われた場合は [、QueueUpdateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject.aspx) を使用してタスクのアクティブな状態を変更します。</span><span class="sxs-lookup"><span data-stu-id="29d98-223">Changing the active status of a task by using [QueueUpdateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject.aspx) , if additional changes are made in the same call.</span></span> <span data-ttu-id="29d98-224">詳細については、「サーバーのプログラミング」*の「Project* のスケジュール設定 [」セクションProject参照してください](project-server-programmability.md)。</span><span class="sxs-lookup"><span data-stu-id="29d98-224">For more information, see the  *Project Scheduling on the Server*  section in [Project Server programmability](project-server-programmability.md).</span></span>
    
#### <a name="summary-tasks"></a><span data-ttu-id="29d98-225">サマリー タスク</span><span class="sxs-lookup"><span data-stu-id="29d98-225">Summary tasks</span></span>

- <span data-ttu-id="29d98-226">サマリー タスクでの割り当ての作成または変更。</span><span class="sxs-lookup"><span data-stu-id="29d98-226">Creating or changing assignments on summary tasks.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="29d98-227">Project Professional またはその他の方法を使用してサマリー タスク上で割り当てを作成しないことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="29d98-227">We recommend that you do not make assignments on summary tasks using Project Professional or any other way.</span></span> <span data-ttu-id="29d98-228">詳細については、「サーバーのプログラミング」*の「Project* のスケジュール設定 [」セクションProject参照してください](project-server-programmability.md)。</span><span class="sxs-lookup"><span data-stu-id="29d98-228">For more information, see the  *Project Scheduling on the Server*  section in [Project Server programmability](project-server-programmability.md).</span></span> 
  
- <span data-ttu-id="29d98-p132">通常サブタスクから重ね合わされるサマリー タスク フィールドの編集。サーバー側プロジェクトは、サマリー タスクに情報を設定してサブタスクにプッシュする代わりに、常にサマリー情報を重ね合わせます。サマリー タスクでは、以下のフィールドのみを編集できます。</span><span class="sxs-lookup"><span data-stu-id="29d98-p132">Editing summary task fields that are normally rolled up from the subtask. Server-side projects always roll up summary information, instead of setting information on the summary task and pushing it down to the subtasks. You can edit only the following fields on summary tasks:</span></span>
    
  - <span data-ttu-id="29d98-232">タスクの依存関係</span><span class="sxs-lookup"><span data-stu-id="29d98-232">Task dependencies</span></span>
    
  - <span data-ttu-id="29d98-233">式ではないユーザー設定フィールド</span><span class="sxs-lookup"><span data-stu-id="29d98-233">Non-formula custom fields</span></span>
    
  - [<span data-ttu-id="29d98-234">TASK_NAME</span><span class="sxs-lookup"><span data-stu-id="29d98-234">TASK_NAME</span></span>](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_NAME.aspx)
    
  - [<span data-ttu-id="29d98-235">TASK_OUTLINE_LEVEL</span><span class="sxs-lookup"><span data-stu-id="29d98-235">TASK_OUTLINE_LEVEL</span></span>](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_OUTLINE_LEVEL.aspx)
    
  - [<span data-ttu-id="29d98-236">TASK_IS_MARKED</span><span class="sxs-lookup"><span data-stu-id="29d98-236">TASK_IS_MARKED</span></span>](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_IS_MARKED.aspx)
    
  - [<span data-ttu-id="29d98-237">TASK_CONSTRAINT_TYPE</span><span class="sxs-lookup"><span data-stu-id="29d98-237">TASK_CONSTRAINT_TYPE</span></span>](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_CONSTRAINT_TYPE.aspx)
    
  - [<span data-ttu-id="29d98-238">TASK_CONSTRAINT_DATE</span><span class="sxs-lookup"><span data-stu-id="29d98-238">TASK_CONSTRAINT_DATE</span></span>](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_CONSTRAINT_DATE.aspx)
    
  - [<span data-ttu-id="29d98-239">TASK_PRIORITY</span><span class="sxs-lookup"><span data-stu-id="29d98-239">TASK_PRIORITY</span></span>](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_PRIORITY.aspx)
    
  - [<span data-ttu-id="29d98-240">TASK_DEADLINE</span><span class="sxs-lookup"><span data-stu-id="29d98-240">TASK_DEADLINE</span></span>](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_DEADLINE.aspx)
    
  - [<span data-ttu-id="29d98-241">TASK_FIXED_COST</span><span class="sxs-lookup"><span data-stu-id="29d98-241">TASK_FIXED_COST</span></span>](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_FIXED_COST.aspx)
    
  - <span data-ttu-id="29d98-242">[TASK_FIXED_COST_ACCRUAL](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_FIXED_COST_ACCRUAL.aspx) (タスクの作成時にのみ値を設定する)</span><span class="sxs-lookup"><span data-stu-id="29d98-242">[TASK_FIXED_COST_ACCRUAL](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_FIXED_COST_ACCRUAL.aspx) (set the value only when creating the task)</span></span> 
    
  - [<span data-ttu-id="29d98-243">TASK_WBS</span><span class="sxs-lookup"><span data-stu-id="29d98-243">TASK_WBS</span></span>](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_WBS.aspx)
    
<span data-ttu-id="29d98-p133">プロジェクトのサマリー タスクについては、PSI の制限は、Project Professional に対するものと同じです。PSI は、予算割り当てを編集できます。これには、コスト型予算も含まれます。</span><span class="sxs-lookup"><span data-stu-id="29d98-p133">For the project summary task, the PSI limitations are the same as for Project Professional. The PSI can edit budget assignments—including cost budgets.</span></span>
  
#### <a name="project-level-calculation-options"></a><span data-ttu-id="29d98-246">プロジェクト レベルの計算オプション</span><span class="sxs-lookup"><span data-stu-id="29d98-246">Project-level calculation options</span></span>

- <span data-ttu-id="29d98-p134">Schedule From Start (SFS) と Schedule From Finish (SFF) の間でのプロジェクトの種類の変更 (PSI はプロジェクトを SFS または SFF として作成できますが、いったん作成したプロジェクトは、Project Professional でのみ変更できます)。</span><span class="sxs-lookup"><span data-stu-id="29d98-p134">Changing a project type between Schedule From Start (SFS) and Schedule From Finish (SFF). (The PSI can create a project as either SFS or SFF, but once created it can be changed only in Project Professional.)</span></span>
    
- <span data-ttu-id="29d98-249">プロジェクトの作成後にプロジェクトの基本カレンダー[(CAL_UID)](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.CAL_UID.aspx) を変更します。</span><span class="sxs-lookup"><span data-stu-id="29d98-249">Changing the project base calendar ([CAL_UID](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.CAL_UID.aspx) ) after project creation.</span></span> 
    
- <span data-ttu-id="29d98-p135">計算のオプションの変更。プロジェクトの作成時に、PSI を使用して以下の計算オプションを設定できますが、これらのオプションを変更するには Project Professional が必要です (Backstage ビューで、[**オプション**] を選択し、[**Project のオプション**] ダイアログ ボックスの [**スケジュール**] タブを選択します)。</span><span class="sxs-lookup"><span data-stu-id="29d98-p135">Changing options for calculations. You can use the PSI to set the following calculation options when the project is created, but changing the options requires Project Professional. (In Backstage view, choose **Options**, and then choose the **Schedule** tab in the **Project Options** dialog box.)</span></span> 
    
  - [<span data-ttu-id="29d98-253">PROJ_OPT_CALC_ACT_COSTS</span><span class="sxs-lookup"><span data-stu-id="29d98-253">PROJ_OPT_CALC_ACT_COSTS</span></span>](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_CALC_ACT_COSTS.aspx)
    
  - [<span data-ttu-id="29d98-254">PROJ_OPT_CRITICAL_SLACK_LIMIT</span><span class="sxs-lookup"><span data-stu-id="29d98-254">PROJ_OPT_CRITICAL_SLACK_LIMIT</span></span>](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_CRITICAL_SLACK_LIMIT.aspx)
    
  - [<span data-ttu-id="29d98-255">PROJ_OPT_HONOR_CONSTRAINTS</span><span class="sxs-lookup"><span data-stu-id="29d98-255">PROJ_OPT_HONOR_CONSTRAINTS</span></span>](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_HONOR_CONSTRAINTS.aspx)
    
  - [<span data-ttu-id="29d98-256">PROJ_OPT_MOVE_ACTUAL_IF_LATER</span><span class="sxs-lookup"><span data-stu-id="29d98-256">PROJ_OPT_MOVE_ACTUAL_IF_LATER</span></span>](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_MOVE_ACTUAL_IF_LATER.aspx)
    
  - [<span data-ttu-id="29d98-257">PROJ_OPT_MOVE_ACTUAL_TO_STATUS</span><span class="sxs-lookup"><span data-stu-id="29d98-257">PROJ_OPT_MOVE_ACTUAL_TO_STATUS</span></span>](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_MOVE_ACTUAL_TO_STATUS.aspx)
    
  - [<span data-ttu-id="29d98-258">PROJ_OPT_MOVE_REMAINING_IF_EARLIER</span><span class="sxs-lookup"><span data-stu-id="29d98-258">PROJ_OPT_MOVE_REMAINING_IF_EARLIER</span></span>](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_MOVE_REMAINING_IF_EARLIER.aspx)
    
  - [<span data-ttu-id="29d98-259">PROJ_OPT_MOVE_REMAINING_TO_STATUS</span><span class="sxs-lookup"><span data-stu-id="29d98-259">PROJ_OPT_MOVE_REMAINING_TO_STATUS</span></span>](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_MOVE_REMAINING_TO_STATUS.aspx)
    
  - [<span data-ttu-id="29d98-260">PROJ_OPT_MULT_CRITICAL_PATHS</span><span class="sxs-lookup"><span data-stu-id="29d98-260">PROJ_OPT_MULT_CRITICAL_PATHS</span></span>](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_MULT_CRITICAL_PATHS.aspx)
    
  - [<span data-ttu-id="29d98-261">PROJ_OPT_SPLIT_IN_PROGRESS</span><span class="sxs-lookup"><span data-stu-id="29d98-261">PROJ_OPT_SPLIT_IN_PROGRESS</span></span>](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_SPLIT_IN_PROGRESS.aspx)
    
  - [<span data-ttu-id="29d98-262">PROJ_OPT_SPREAD_ACT_COSTS</span><span class="sxs-lookup"><span data-stu-id="29d98-262">PROJ_OPT_SPREAD_ACT_COSTS</span></span>](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_SPREAD_ACT_COSTS.aspx)
    
  - [<span data-ttu-id="29d98-263">PROJ_OPT_SPREAD_PCT_COMP</span><span class="sxs-lookup"><span data-stu-id="29d98-263">PROJ_OPT_SPREAD_PCT_COMP</span></span>](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_SPREAD_PCT_COMP.aspx)
    
  - [<span data-ttu-id="29d98-264">PROJ_OPT_TASK_UPDATES_RES</span><span class="sxs-lookup"><span data-stu-id="29d98-264">PROJ_OPT_TASK_UPDATES_RES</span></span>](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_TASK_UPDATES_RES.aspx)
    
## <a name="see-also"></a><span data-ttu-id="29d98-265">関連項目</span><span class="sxs-lookup"><span data-stu-id="29d98-265">See also</span></span>

- [<span data-ttu-id="29d98-266">CSOM ができること、できないこと</span><span class="sxs-lookup"><span data-stu-id="29d98-266">What the CSOM does and does not do</span></span>](what-the-csom-does-and-does-not-do.md)  
- [<span data-ttu-id="29d98-267">Project Server プログラミング</span><span class="sxs-lookup"><span data-stu-id="29d98-267">Project Server programmability</span></span>](project-server-programmability.md)   
- [<span data-ttu-id="29d98-268">クレーム ベース認証を使用した SharePoint Online でのリモート認証</span><span class="sxs-lookup"><span data-stu-id="29d98-268">Remote Authentication in SharePoint Online Using Claims-Based Authentication</span></span>](https://msdn.microsoft.com/library/49067f7a-3020-478f-ba97-4b7ce3ea9b87%28Office.15%29.aspx)  
- [<span data-ttu-id="29d98-269">Office アドイン</span><span class="sxs-lookup"><span data-stu-id="29d98-269">Office Add-ins</span></span>](https://docs.microsoft.com/office/dev/add-ins/overview/office-add-ins) 
    

