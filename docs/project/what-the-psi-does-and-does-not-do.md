---
title: PSI が行うこと、行わないこと
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: eac6be6a-9a20-4bc0-8da2-b2fd93aab04f
description: プロジェクト Server インターフェイス (PSI) は、Project Server 2013 のオンプレミスのインストール環境で多くのサーバー側プロセスを自動化するのに役立ちます。 ですが、いくつかの関数は、Microsoft Project Professional 2013 の使用を要求します。
ms.openlocfilehash: e926e970c5e8dd382370fbe4d7c34c4136502cbf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588112"
---
# <a name="what-the-psi-does-and-does-not-do"></a><span data-ttu-id="ba30e-104">PSI のすること、しないこと</span><span class="sxs-lookup"><span data-stu-id="ba30e-104">What the PSI does and does not do</span></span>

<span data-ttu-id="ba30e-105">プロジェクト Server インターフェイス (PSI) は、Project Server 2013 のオンプレミスのインストール環境で多くのサーバー側プロセスを自動化するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="ba30e-105">The Project Server Interface (PSI) can help to automate many server-side processes in on-premises installations of Project Server 2013.</span></span> <span data-ttu-id="ba30e-106">ですが、いくつかの関数は、Microsoft Project Professional 2013 の使用を要求します。</span><span class="sxs-lookup"><span data-stu-id="ba30e-106">But, several functions require the use of Microsoft Project Professional 2013.</span></span>
  
|||
|:-----|:-----|
|||
   
<span data-ttu-id="ba30e-107">PSI は、Project Professional のすべての機能は、サーバ ・ ベースの代替を提供するのではなく、プロジェクトの評価のための機能を補完するよう設計されています。</span><span class="sxs-lookup"><span data-stu-id="ba30e-107">The PSI is designed to complement the capabilities of Project Professional 2013, rather than provide a server-based alternative for all Project Professional functions.</span></span> <span data-ttu-id="ba30e-108">サード パーティの開発者は、PSI を使用して、設置の Project Web App の [プロジェクト ワークスペースの Web パーツを作成、カスタムの Windows アプリケーションとオンプレミスの Project Server のデータと対話する、ワークフローを開発する web アプリケーションの作成を支援するにはプロジェクト ポートフォリオ管理のためのロジックでは、ローカルの完全信頼のイベント ハンドラーを開発し、Project Server を他のアプリケーションに統合します。</span><span class="sxs-lookup"><span data-stu-id="ba30e-108">Third-party developers can use the PSI to help create Web Parts for on-premises installations of Project Web App and project workspaces, create custom Windows applications and web applications that interact with on-premises Project Server data, develop workflow logic for project portfolio management, develop local full-trust event handlers, and integrate Project Server with other applications.</span></span> <span data-ttu-id="ba30e-109">Office ストア、モバイル デバイス、またはタブレットのためのアプリケーションを開発するため、PSI を使用することはできません。そのため、クライアント側オブジェクト モデル (CSOM) を使用できます。</span><span class="sxs-lookup"><span data-stu-id="ba30e-109">The PSI cannot be used for development of apps for the Office Store, mobile devices, or tablets; for that, you can use the client-side object model (CSOM).</span></span>
  
> [!NOTE]
> <span data-ttu-id="ba30e-110">PSI より包括的なプログラム インターフェイスを提供 Project Server 2013 は、CSOM で提供されます。</span><span class="sxs-lookup"><span data-stu-id="ba30e-110">The PSI provides a more comprehensive programmatic interface for Project Server 2013 than the CSOM provides.</span></span> <span data-ttu-id="ba30e-111">新しいアプリケーションを開発するのには、CSOM を使用することをお勧め、CSOM から、必要な機能が提供されない限り、します。</span><span class="sxs-lookup"><span data-stu-id="ba30e-111">But, unless the CSOM does not provide the functionality that you require, we recommend that you use the CSOM to develop new applications.</span></span> <span data-ttu-id="ba30e-112">詳細については、[どのような CSOM しサポートしない](what-the-csom-does-and-does-not-do.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ba30e-112">For more information, see [What the CSOM does and does not do](what-the-csom-does-and-does-not-do.md).</span></span> 
  
## <a name="usage-scenarios-for-the-psi"></a><span data-ttu-id="ba30e-113">PSI の使用シナリオ</span><span class="sxs-lookup"><span data-stu-id="ba30e-113">Usage scenarios for the PSI</span></span>
<span data-ttu-id="ba30e-114"><a name="pj14_WhatPSIDoes_UsageScenarios"> </a></span><span class="sxs-lookup"><span data-stu-id="ba30e-114"></span></span>

<span data-ttu-id="ba30e-115">以下に、PSI がサーバー側のプロジェクトおよび計算のためにサポートするアプリケーションの例をいくつか示します。</span><span class="sxs-lookup"><span data-stu-id="ba30e-115">Following are examples of some applications that the PSI supports for server-side projects and calculations:</span></span>
  
- <span data-ttu-id="ba30e-116">**自動化、作成、または Project Server 内のエンティティの管理**カスタム アプリケーションが一括で時間を保存する場所の場合、多くの場合は、評価のためのプロジェクトと Project Web App には、管理し、プロジェクト、エンタープライズ リソース ユーザー設定フィールドなどのエンティティの作成を処理するために、または反復的なジョブです。</span><span class="sxs-lookup"><span data-stu-id="ba30e-116">**Automate the creation or management of entities in Project Server** Although Project Professional 2013 and Project Web App together are designed to handle management and creation of entities such as projects, enterprise resources, and custom fields, there are often cases where a custom application can save time with bulk or repetitive jobs.</span></span> <span data-ttu-id="ba30e-117">PSI には、CSOM が実行できないジョブのたとえば、OLAP キューブ、プロジェクト ポートフォリオ分析、ビジネス ドライバー、通知、オブジェクト リンク プロバイダー、セキュリティ、および SharePoint の相互運用性を持ついくつかの種類を自動化できます。</span><span class="sxs-lookup"><span data-stu-id="ba30e-117">The PSI can automate several kinds of jobs that the CSOM does not do, for example, with OLAP cubes, project portfolio analyses, business drivers, notifications, object link providers, security, and SharePoint interoperability.</span></span> 
    
- <span data-ttu-id="ba30e-118">**プロジェクト データベースのアーカイブ テーブルまたは、パブリッシュされたデータを取得します。** テーブルはサポートされていないため、データベースに直接、公開、下書きにアクセスし、アーカイブがレポートのテーブルまたはビューで使用できないデータを読み取る PSI を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="ba30e-118">**Get data in the published or archive tables of the Project database** Because direct database access to the draft, published, and archive tables is not supported, you can use the PSI to read data that is not available in the reporting tables or views.</span></span> <span data-ttu-id="ba30e-119">たとえば、プロジェクトのバージョン、日付、およびアーカイブ テーブルに格納されている変更に関する情報を取得し、情報を持つ web パーツ内の JS グリッド コントロールを作成し、します。</span><span class="sxs-lookup"><span data-stu-id="ba30e-119">For example, get information about project versions, dates, and changes that are stored in the archive tables, and then populate a JS Grid control in a web part with the information.</span></span> 
    
- <span data-ttu-id="ba30e-120">**状態管理とタイムシートのデータを検証します。** ローカルの前のイベント ハンドラーで PSI を使用すると、Project Web App でデータが保存される前に、ユーザーが入力した割り当ての状態] または [タイムシート データを検証します。</span><span class="sxs-lookup"><span data-stu-id="ba30e-120">**Validate statusing and timesheet data** Use the PSI in local pre-event handlers to validate assignment status or timesheet data that users enter, before the data is saved in Project Web App.</span></span> 
    
- <span data-ttu-id="ba30e-121">**メンテナンス プロジェクト**プロジェクトのリソース計画で使用するプレース ホルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="ba30e-121">**Maintenance projects** Create placeholder projects to use with resource plans.</span></span> <span data-ttu-id="ba30e-122">予約または本時間リソースに対する保守作業または基本業務です。</span><span class="sxs-lookup"><span data-stu-id="ba30e-122">Reserve or book time against resources for maintenance work or base business.</span></span> <span data-ttu-id="ba30e-123">通常、保守プロジェクトにはタスクはありません。</span><span class="sxs-lookup"><span data-stu-id="ba30e-123">Maintenance projects generally do not have tasks.</span></span> 
    
- <span data-ttu-id="ba30e-124">**財務プロジェクトの作成**財務システムとの統合のためにタイムシートをタイム キャプチャ用のプロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="ba30e-124">**Create financial projects** Create projects for time capture through the timesheet for integration with a financial system.</span></span> <span data-ttu-id="ba30e-125">財務システムのコストの内訳構造を反映した、財務コードの階層を作成します。</span><span class="sxs-lookup"><span data-stu-id="ba30e-125">Create a hierarchy of financial codes that reflect the cost breakdown structure of the financial system.</span></span> <span data-ttu-id="ba30e-126">財務プロジェクトでは、スケジュール設定やステータスの更新は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="ba30e-126">Financial projects do not require scheduling or status updates.</span></span> 
    
- <span data-ttu-id="ba30e-127">**会計システムとの統合**リソースのコストおよび関連する財務および請求システムをフィードするプロジェクトと予算の比較のための経費をキャプチャします。</span><span class="sxs-lookup"><span data-stu-id="ba30e-127">**Integrate with accounting systems** Capture the resource costs and expenses associated with projects to feed financial and billing systems and for budget comparison purposes.</span></span> <span data-ttu-id="ba30e-128">タスク、リソース、およびシステム間での割り当てを同期します。</span><span class="sxs-lookup"><span data-stu-id="ba30e-128">Synchronize tasks, resources, and assignments between the systems.</span></span> <span data-ttu-id="ba30e-129">他のフィードを 1 つのシステムでタイムシート データをキャプチャ (組織または個々 のプロジェクトのニーズに依存するタイムシートが表示されます)。</span><span class="sxs-lookup"><span data-stu-id="ba30e-129">Capture timesheet data in one system to feed the other (which timesheet is used depends on the needs of the organization or of individual projects).</span></span> 
    
- <span data-ttu-id="ba30e-130">**チーム メンバーから更新を自動化**積極的に管理されていないプロジェクトでは、進行状況とプロジェクト チームのメンバーからの他の変更をサーバー上のプロジェクトを自動的に更新します。</span><span class="sxs-lookup"><span data-stu-id="ba30e-130">**Automate updates from team members** For projects that are not actively managed, automatically update projects on the server with progress and other changes from project team members.</span></span> <span data-ttu-id="ba30e-131">プロジェクトを更新し、プロジェクト管理者は、結果を確認するか、計画を調整することがなく再公開できます。</span><span class="sxs-lookup"><span data-stu-id="ba30e-131">Projects can be updated and republished without a project manager reviewing the results or making adjustments to the plan.</span></span> 
    
- <span data-ttu-id="ba30e-132">**ローカルの完全信頼のイベント ハンドラーでデータを Project Server の評価**プレ イベントの**ProjectCreating**のローカル イベント ハンドラーは、イベントをキャンセルするのにかどうかを判断するために PSI から Project Server データを使用できます。</span><span class="sxs-lookup"><span data-stu-id="ba30e-132">**Evaluate Project Server data in local full-trust event handlers** A local event handler for the **ProjectCreating** pre-event can use Project Server data from the PSI to help determine whether to cancel an event.</span></span> <span data-ttu-id="ba30e-133">たとえば、プロジェクトを作成する前に既存のプロジェクトとプロジェクトの提案を比較します。</span><span class="sxs-lookup"><span data-stu-id="ba30e-133">For example, before creating a project, compare the project proposal with existing projects.</span></span> 
    
- <span data-ttu-id="ba30e-134">**需要管理のユーザー定義ワークフロー活動を作成します。** 変更およびエンタープライズ プロジェクト テンプレートに基づいてプロジェクト提案書を更新する、ローカルの完全信頼ワークフロー アクティビティで、PSI を使用します。</span><span class="sxs-lookup"><span data-stu-id="ba30e-134">**Create custom workflow activities for demand management** Use the PSI in local, full-trust workflow activities to modify and update project proposals based on enterprise project templates.</span></span> <span data-ttu-id="ba30e-135">開始および承認プロセスに必要な情報をプロジェクトにタグ付けするのにには、プロジェクトのユーザー設定フィールドを使用します。</span><span class="sxs-lookup"><span data-stu-id="ba30e-135">Use project custom fields to tag the project with information needed for the initiation and approval process.</span></span> <span data-ttu-id="ba30e-136">主なマイルス トーンまたは成果物のプロジェクト フェーズを識別するタスクを追加します。</span><span class="sxs-lookup"><span data-stu-id="ba30e-136">Add tasks to identify project phases for key milestones or deliverables.</span></span> <span data-ttu-id="ba30e-137">プロジェクトの提案が承認されると、ワークフローは、Project Professional で管理されている本格的なプロジェクトの提案を変更できます。</span><span class="sxs-lookup"><span data-stu-id="ba30e-137">When project proposals are approved, a workflow can change the proposals into full-scale projects that are managed with Project Professional.</span></span> 
    
- <span data-ttu-id="ba30e-138">**作成の PSI 拡張機能**(**は使用されなくなりました**。</span><span class="sxs-lookup"><span data-stu-id="ba30e-138">**Create PSI extensions** (**Deprecated.**</span></span> <span data-ttu-id="ba30e-139">拡張機能で Project Server 2013 では、推奨されていませんし、将来のリリースではサポートされません。)Windows Communication Foundation (WCF) インターフェイスを使用してカスタム サービスを使用して、PSI を拡張できます。</span><span class="sxs-lookup"><span data-stu-id="ba30e-139">Extensions are deprecated in Project Server 2013, and will not be supported in future releases.) The PSI can be extended with custom services by using the Windows Communication Foundation (WCF) interface.</span></span> <span data-ttu-id="ba30e-140">PSI 拡張機能は、Project Server コンピューター上で実行し、組み込みの PSI サービスを使用するのと同じセキュリティ インフラストラクチャを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="ba30e-140">PSI extensions run on the Project Server computer, and can use the same security infrastructure that the built-in PSI services use.</span></span> <span data-ttu-id="ba30e-141">拡張機能はレポート テーブルのクエリを実行、別のデータベース テーブルを使用して、帯域幅を保存し、サードパーティ製のアプリケーションおよびその他のサーバー側コンポーネントとの統合の PSI 呼び出しを統合します。</span><span class="sxs-lookup"><span data-stu-id="ba30e-141">Extensions can query the reporting tables, use separate database tables, consolidate PSI calls to save bandwidth, and integrate with third-party applications and other server-side components.</span></span> <span data-ttu-id="ba30e-142">詳細については、 [PSI 拡張機能の開発](http://msdn.microsoft.com/library/1b484623-94fb-47c9-84c1-3e68a9133042%28Office.15%29.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ba30e-142">For more information, see [Developing PSI Extensions](http://msdn.microsoft.com/library/1b484623-94fb-47c9-84c1-3e68a9133042%28Office.15%29.aspx).</span></span>
    
- <span data-ttu-id="ba30e-143">**ローカルの完全信頼アプリケーションで偽装を使用**PSI の WCF インターフェイスを呼び出すことができますふりをする、できるように、アプリケーションには、偽装ユーザーのセキュリティ アクセス許可が前提としています。</span><span class="sxs-lookup"><span data-stu-id="ba30e-143">**Use impersonation in local, full-trust applications** Calls to the WCF interface of the PSI can be impersonated, so that an application assumes the security permissions of the impersonated user.</span></span> <span data-ttu-id="ba30e-144">注意して慎重に、偽装を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ba30e-144">Impersonation should be used sparingly and carefully.</span></span> <span data-ttu-id="ba30e-145">読み取りと他のユーザーの状態に関する情報を更新するには、偽装は不要です。</span><span class="sxs-lookup"><span data-stu-id="ba30e-145">Reading and updating status information for other users does not require impersonation.</span></span> <span data-ttu-id="ba30e-146">偽装を必要とする新しいアプリケーションでは、PSI ではなく、CSOM および OAuth プロトコルを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ba30e-146">New applications that require impersonation should use the CSOM and the OAuth protocol instead of the PSI.</span></span> <span data-ttu-id="ba30e-147">PSI の偽装の詳細については、 [WCF を使用して偽装](http://msdn.microsoft.com/library/e3597901-2f02-44a2-8076-d32aae540b38%28Office.15%29.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ba30e-147">For more information about impersonation with the PSI, see [Use Impersonation with WCF](http://msdn.microsoft.com/library/e3597901-2f02-44a2-8076-d32aae540b38%28Office.15%29.aspx).</span></span>
    
> [!NOTE]
> <span data-ttu-id="ba30e-148">いくつかの場合では、CSOM とオンライン プロジェクトでのクライアント アプリケーションで PSI を使用できます。</span><span class="sxs-lookup"><span data-stu-id="ba30e-148">In some cases, the PSI can be used in client applications with the CSOM and Project Online.</span></span> <span data-ttu-id="ba30e-149">アプリケーションが、CSOM で[Microsoft.ProjectServer.Client.ProjectContext](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.aspx)オブジェクトを認証する方法と、**を認証するためのメソッドを含める必要があります PSI の ASMX ベース web サービスを使用する場合System.Web.Services.Protocols.SoapHttpClientProtocol**クライアント オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="ba30e-149">If you use an ASMX-based PSI web service, the application must include a method to authenticate the [Microsoft.ProjectServer.Client.ProjectContext](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.aspx) object in the CSOM and a method to authenticate the **System.Web.Services.Protocols.SoapHttpClientProtocol** client object.</span></span> <span data-ttu-id="ba30e-150">SharePoint CSOM で web サービスを使用する例では、 [SharePoint Online Using Claims-Based 認証でリモートの認証](http://msdn.microsoft.com/library/49067f7a-3020-478f-ba97-4b7ce3ea9b87%28Office.15%29.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ba30e-150">For an example that uses a web service with the SharePoint CSOM, see [Remote Authentication in SharePoint Online Using Claims-Based Authentication](http://msdn.microsoft.com/library/49067f7a-3020-478f-ba97-4b7ce3ea9b87%28Office.15%29.aspx).</span></span> <span data-ttu-id="ba30e-151">> 制約のあるアプリケーション ・ レベルのアクセス権があるためは Office のパブリック ストアでの配布の PSI に設計されたアプリケーションで使用できません。</span><span class="sxs-lookup"><span data-stu-id="ba30e-151">> Because of constrained app-level permissions, the PSI cannot be used in apps that are designed for distribution in the public Office Store.</span></span> <span data-ttu-id="ba30e-152">その場合は、CSOM のみを使用できます。</span><span class="sxs-lookup"><span data-stu-id="ba30e-152">In that case, you can use only the CSOM.</span></span> 
  
## <a name="what-the-psi-does-not-do"></a><span data-ttu-id="ba30e-153">PSI が行わないこと</span><span class="sxs-lookup"><span data-stu-id="ba30e-153">What the PSI does not do</span></span>
<span data-ttu-id="ba30e-154"><a name="pj14_WhatPSIDoes_DoesNotDo"> </a></span><span class="sxs-lookup"><span data-stu-id="ba30e-154"></span></span>

<span data-ttu-id="ba30e-p116">PSI が行えることはたくさんありますが、PSI が行えないこともあります。以下に、PSI では行えず、CSOM では行えることを 2 つ示します。</span><span class="sxs-lookup"><span data-stu-id="ba30e-p116">Although there are many things the PSI can do, there are some things the PSI does not do. Following are two things the PSI cannot do, but the CSOM can do.</span></span>
  
### <a name="project-online-and-remote-event-receivers"></a><span data-ttu-id="ba30e-157">オンラインおよびリモート イベント レシーバーをプロジェクトします。</span><span class="sxs-lookup"><span data-stu-id="ba30e-157">Project Online and remote event receivers</span></span>

<span data-ttu-id="ba30e-158">プロジェクトをオンラインでは、PSI の主な制限です。</span><span class="sxs-lookup"><span data-stu-id="ba30e-158">The primary limitation of the PSI is with Project Online.</span></span> <span data-ttu-id="ba30e-159">PSI を使用するアプリケーションでは、プロジェクトのサーバーの設置型インストールに完全信頼のアクセスが必要です。</span><span class="sxs-lookup"><span data-stu-id="ba30e-159">Applications that use the PSI require full-trust access to an on-premises installation of Project Server.</span></span> <span data-ttu-id="ba30e-160">たとえば、PSI では使用できませんリモート イベント レシーバーでは、イベント レシーバーが Microsoft Azure にサービスとしてインストールされています。</span><span class="sxs-lookup"><span data-stu-id="ba30e-160">For example, the PSI cannot be used in remote event receivers, where the event receiver is installed as a service on Microsoft Azure.</span></span>
  
### <a name="workflows-and-claims-authentication"></a><span data-ttu-id="ba30e-161">ワークフローおよびクレーム認証</span><span class="sxs-lookup"><span data-stu-id="ba30e-161">Workflows and claims authentication</span></span>

<span data-ttu-id="ba30e-162">4 (WF4) する必要がありますクレーム認証では、PSI を直接サポートしていない Windows Workflow Foundation のバージョンを使用するためのワークフロー定義。</span><span class="sxs-lookup"><span data-stu-id="ba30e-162">A workflow definition that uses Windows Workflow Foundation version 4 (WF4) requires claims authentication, which the PSI does not directly support.</span></span> <span data-ttu-id="ba30e-163">つまり、WF4 のワークフロー定義を使用してエンタープライズ プロジェクトの種類 (EPT) を持つ Project Server 2013 でプロジェクトを作成するのには、PSI を使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="ba30e-163">This means you cannot use the PSI to create a project in Project Server 2013 that has an enterprise project type (EPT) with a WF4 workflow definition.</span></span>
  
<span data-ttu-id="ba30e-164">EPTs ワークフローがないとしているか、従来の WF3.5 定義 (Project Server 2010 のワークフローのバージョン) を使用するとプロジェクトを作成するのには、PSI を使用できます。</span><span class="sxs-lookup"><span data-stu-id="ba30e-164">You can use the PSI to create projects with EPTs that either have no workflow or use a legacy WF3.5 definition (the workflow version in Project Server 2010).</span></span> <span data-ttu-id="ba30e-165">WF4 定義を持つ、EPT でプロジェクトを作成するには、CSOM を使用します。</span><span class="sxs-lookup"><span data-stu-id="ba30e-165">To create a project with an EPT that has a WF4 definition, use the CSOM.</span></span>
  
 <span data-ttu-id="ba30e-166">**Project Professional を必要とするアクション:**</span><span class="sxs-lookup"><span data-stu-id="ba30e-166">**Actions that require Project Professional:**</span></span>
  
<span data-ttu-id="ba30e-167">次のリストは、PSI と CSOM のどちらでも行うことのできない処理を示しています。</span><span class="sxs-lookup"><span data-stu-id="ba30e-167">The following list are things that neither the PSI nor the CSOM can do.</span></span>
  
#### <a name="local-data"></a><span data-ttu-id="ba30e-168">ローカル データ</span><span class="sxs-lookup"><span data-stu-id="ba30e-168">Local data</span></span>

- <span data-ttu-id="ba30e-p120">ローカル プロジェクト (.mpp ファイル) でのデータの操作。たとえば、コスト単価表またはローカル リソースの利用可能時間の定義。</span><span class="sxs-lookup"><span data-stu-id="ba30e-p120">Manipulating data in local projects (.mpp files). For example, defining cost rate tables or availability contours for local resources.</span></span> 
    
- <span data-ttu-id="ba30e-171">ローカル基本カレンダーまたはリソース カレンダー (カレンダーの例外を含む) の定義または編集。</span><span class="sxs-lookup"><span data-stu-id="ba30e-171">Defining or editing local base calendars or resource calendars, including calendar exceptions.</span></span>
    
- <span data-ttu-id="ba30e-p121">ローカル ユーザー設定フィールドの定義 (PSI で、タスク、リソース、および割り当てのローカル ユーザー設定フィールドの値を編集することは可能です)。</span><span class="sxs-lookup"><span data-stu-id="ba30e-p121">Defining local custom fields. (The PSI does support editing local custom field values on tasks, resources, and assignments.)</span></span>
    
#### <a name="enterprise-data"></a><span data-ttu-id="ba30e-174">エンタープライズ データ</span><span class="sxs-lookup"><span data-stu-id="ba30e-174">Enterprise data</span></span>

- <span data-ttu-id="ba30e-175">チェック アウトするか、エンタープライズ グローバル テンプレートを編集します。</span><span class="sxs-lookup"><span data-stu-id="ba30e-175">Checking out or editing the enterprise global template.</span></span> <span data-ttu-id="ba30e-176">エンタープライズのグローバル データを Project Server 2013 では、Office Project Server 2007 と以前のバージョンのようにプロジェクト テンプレートではなく、プロジェクト データベース内のバイナリ データのテーブルのセットです。</span><span class="sxs-lookup"><span data-stu-id="ba30e-176">The enterprise global data in Project Server 2013 is a set of binary data tables in the Project database, not a project template as in Office Project Server 2007 and earlier versions.</span></span>
    
- <span data-ttu-id="ba30e-177">定義またはエンタープライズ カレンダーを編集します。</span><span class="sxs-lookup"><span data-stu-id="ba30e-177">Defining or editing enterprise calendars.</span></span> <span data-ttu-id="ba30e-178">[Calendar](https://msdn.microsoft.com/library/WebSvcCalendar.Calendar.aspx)のメソッドは、カレンダーの例外のみを管理します。</span><span class="sxs-lookup"><span data-stu-id="ba30e-178">The [Calendar](https://msdn.microsoft.com/library/WebSvcCalendar.Calendar.aspx) methods manage only calendar exceptions.</span></span> 
    
#### <a name="master-projects-and-cross-project-links"></a><span data-ttu-id="ba30e-179">マスター プロジェクトおよびプロジェクト間のリンク</span><span class="sxs-lookup"><span data-stu-id="ba30e-179">Master projects and cross-project links</span></span>

- <span data-ttu-id="ba30e-180">マスター プロジェクトの作成とサブプロジェクトの挿入。</span><span class="sxs-lookup"><span data-stu-id="ba30e-180">Creating master projects and inserting subprojects.</span></span>
    
- <span data-ttu-id="ba30e-181">マスター プロジェクト全体にわたるクリティカル パスのスケジューリング。</span><span class="sxs-lookup"><span data-stu-id="ba30e-181">Scheduling a critical path across a master project.</span></span> 
    
- <span data-ttu-id="ba30e-182">プロジェクト間のリンクの作成。</span><span class="sxs-lookup"><span data-stu-id="ba30e-182">Creating cross-project links.</span></span>
    
#### <a name="resources"></a><span data-ttu-id="ba30e-183">リソース</span><span class="sxs-lookup"><span data-stu-id="ba30e-183">Resources</span></span>

- <span data-ttu-id="ba30e-184">リソースの平準化の要求または実行。</span><span class="sxs-lookup"><span data-stu-id="ba30e-184">Requesting or performing resource leveling.</span></span>
    
- <span data-ttu-id="ba30e-p124">割り当て上のリソースの変更 (PSI を使用して割り当てを削除し、新しい割り当てを作成することは可能です)。</span><span class="sxs-lookup"><span data-stu-id="ba30e-p124">Changing the resource on an assignment. (You can use the PSI to delete the assignment and create a new one.)</span></span>
    
- <span data-ttu-id="ba30e-187">認められた実際の作業 (実績) を持つリソースの削除または置換。</span><span class="sxs-lookup"><span data-stu-id="ba30e-187">Deleting or replacing a resource that has actual work accepted (actuals).</span></span>
    
- <span data-ttu-id="ba30e-188">時間単価型、数量単価型、およびコスト型の間でのリソースの種類の変更。</span><span class="sxs-lookup"><span data-stu-id="ba30e-188">Changing a resource type between work, material, and cost.</span></span>
    
- <span data-ttu-id="ba30e-189">リソース カレンダーの作成または編集。</span><span class="sxs-lookup"><span data-stu-id="ba30e-189">Creating or editing resource calendars.</span></span>
    
- <span data-ttu-id="ba30e-p125">タスクにリソースを追加する場合、PSI は Project Professional のように作業を自動的に再配布しません。割り当てで作業の配布を選択して明示的に設定するのは、開発者の役割です。</span><span class="sxs-lookup"><span data-stu-id="ba30e-p125">When adding a resource to a task, the PSI does not automatically redistribute work the way Project Professional does. It is up to the developer to choose and explicitly set the work distribution on the assignments.</span></span>
    
#### <a name="cost-resources"></a><span data-ttu-id="ba30e-192">コスト型リソース</span><span class="sxs-lookup"><span data-stu-id="ba30e-192">Cost resources</span></span>

- <span data-ttu-id="ba30e-193">編集、作成、またはコスト単価型リソースと[プロジェクト](https://msdn.microsoft.com/library/WebSvcProject.Project.aspx)のメソッドを使用して、割り当てを削除します。</span><span class="sxs-lookup"><span data-stu-id="ba30e-193">Editing, creating, or deleting cost resources and assignments using the [Project](https://msdn.microsoft.com/library/WebSvcProject.Project.aspx) methods.</span></span> <span data-ttu-id="ba30e-194">[リソース](https://msdn.microsoft.com/library/WebSvcResource.Resource.aspx)の方法は、コスト単価型リソースを作成できますが、編集はできません。</span><span class="sxs-lookup"><span data-stu-id="ba30e-194">The [Resource](https://msdn.microsoft.com/library/WebSvcResource.Resource.aspx) methods can create cost resources but cannot edit them.</span></span> 
    
#### <a name="work-contours"></a><span data-ttu-id="ba30e-195">作業配分</span><span class="sxs-lookup"><span data-stu-id="ba30e-195">Work contours</span></span>

- <span data-ttu-id="ba30e-196">タイムスケール データの編集。</span><span class="sxs-lookup"><span data-stu-id="ba30e-196">Editing timephased data.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="ba30e-197">[UpdateStatus](https://msdn.microsoft.com/library/WebSvcStatusing.Statusing.UpdateStatus.aspx) **状態管理**Web サービスのメソッドは、プロジェクト マネージャーが更新され、割り当てのデータを公開した後、割り当てのタイム スケール領域の実績作業時間を編集できます。</span><span class="sxs-lookup"><span data-stu-id="ba30e-197">The [UpdateStatus](https://msdn.microsoft.com/library/WebSvcStatusing.Statusing.UpdateStatus.aspx) method in the **Statusing** Web service can edit timephased actuals on assignments after the project manager updates and publishes the assignment data.</span></span> 
  
- <span data-ttu-id="ba30e-198">割り当ての配分型 (均等型、増加型、減少型など) の設定または変更。</span><span class="sxs-lookup"><span data-stu-id="ba30e-198">Setting or changing the assignment contour type (such as flat, back-loaded, or front-loaded).</span></span>
    
#### <a name="baselines-and-earned-value"></a><span data-ttu-id="ba30e-199">基準計画および達成額</span><span class="sxs-lookup"><span data-stu-id="ba30e-199">Baselines and earned value</span></span>

- <span data-ttu-id="ba30e-200">基準計画の保存または基準計画データの編集。</span><span class="sxs-lookup"><span data-stu-id="ba30e-200">Saving a baseline or editing baseline data.</span></span> 
    
- <span data-ttu-id="ba30e-201">進捗日の設定。</span><span class="sxs-lookup"><span data-stu-id="ba30e-201">Setting a progress date.</span></span>
    
- <span data-ttu-id="ba30e-202">差異および達成額の計算。</span><span class="sxs-lookup"><span data-stu-id="ba30e-202">Calculating variance and earned value.</span></span> 
    
#### <a name="interactive-scheduling"></a><span data-ttu-id="ba30e-203">対話型スケジューリング</span><span class="sxs-lookup"><span data-stu-id="ba30e-203">Interactive scheduling</span></span>

- <span data-ttu-id="ba30e-p127">対話型スケジューリングのサポート (Project Server は対話を非同期に処理するため、対話型スケジューリングは Project Professional を使用して行う必要があります)。</span><span class="sxs-lookup"><span data-stu-id="ba30e-p127">Supporting interactive scheduling. (Because Project Server handles interactions asynchronously, interactive scheduling should be done with Project Professional.)</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="ba30e-206">プログラムの動作を変更することを避けるためには、Project Server 2010 から前方に置かれる PSI メソッドの動作は Project Server 2013 でも同じ方法です。</span><span class="sxs-lookup"><span data-stu-id="ba30e-206">To avoid changing programmatic behavior, the PSI methods that are brought forward from Project Server 2010 act the same way in Project Server 2013.</span></span> <span data-ttu-id="ba30e-207">やなどの[QueueUpdateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject.aspx)も同じ制限があります古いサーバー側のスケジュール エンジンを使用します。</span><span class="sxs-lookup"><span data-stu-id="ba30e-207">For example, [QueueUpdateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject.aspx) still has the same limitations and uses the older server-side scheduling engine.</span></span> <span data-ttu-id="ba30e-208">新しい[QueueUpdateProject2](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject2.aspx)メソッドでは、これらの制限の多くを削除し、エンジンを使用して新しい Project Server 2013 のサーバー側スケジューリング、評価のためのプロジェクトに含まれるものと同じスケジュール エンジンであります。</span><span class="sxs-lookup"><span data-stu-id="ba30e-208">The new [QueueUpdateProject2](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject2.aspx) method removes many of those limitations and uses the new Project Server 2013 server-side scheduling engine, which is the same scheduling engine that is in Project Professional 2013.</span></span> 
  
#### <a name="wbs"></a><span data-ttu-id="ba30e-209">WBS</span><span class="sxs-lookup"><span data-stu-id="ba30e-209">WBS</span></span>

- <span data-ttu-id="ba30e-210">Work Breakdown Structure (WBS) コード マスクの定義。</span><span class="sxs-lookup"><span data-stu-id="ba30e-210">Defining a work breakdown structure (WBS) code mask.</span></span> 
    
#### <a name="tasks"></a><span data-ttu-id="ba30e-211">タスク</span><span class="sxs-lookup"><span data-stu-id="ba30e-211">Tasks</span></span>

- <span data-ttu-id="ba30e-212">タスクの種類 (作業時間固定、期間固定、または単位数固定) の変更。</span><span class="sxs-lookup"><span data-stu-id="ba30e-212">Changing the task type (fixed work, duration, or units).</span></span>
    
- <span data-ttu-id="ba30e-213">タスクが残存作業優先であるかどうかの変更。</span><span class="sxs-lookup"><span data-stu-id="ba30e-213">Changing whether a task is effort-driven.</span></span>
    
- <span data-ttu-id="ba30e-214">タスクの固定コスト計上の時期の変更。</span><span class="sxs-lookup"><span data-stu-id="ba30e-214">Changing task fixed-cost accrual.</span></span>
    
- <span data-ttu-id="ba30e-215">[TASK_NOTES](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_NOTES.aspx)フィールドの内容を変更します。</span><span class="sxs-lookup"><span data-stu-id="ba30e-215">Changing the content of the [TASK_NOTES](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_NOTES.aspx) field.</span></span> <span data-ttu-id="ba30e-216">PSI には、.rtf バイナリ データであるタスク メモのテキストの部分のみを読み取ることができます。</span><span class="sxs-lookup"><span data-stu-id="ba30e-216">The PSI can read only the text part of the task notes, which are .rtf binary data.</span></span> <span data-ttu-id="ba30e-217">しかし、割り当てメモ ( [ASSN_NOTES](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.AssignmentRow.ASSN_NOTES.aspx) ) は、テキスト データを編集することができます。</span><span class="sxs-lookup"><span data-stu-id="ba30e-217">But, you can edit assignment notes ( [ASSN_NOTES](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.AssignmentRow.ASSN_NOTES.aspx) ), which are text data.</span></span> <span data-ttu-id="ba30e-218">レポート データベースは、タスクまたは割り当てのメモには含まれません。</span><span class="sxs-lookup"><span data-stu-id="ba30e-218">The Reporting database does not include task or assignment notes.</span></span> 
    
- <span data-ttu-id="ba30e-219">定期タスクの作成または編集。</span><span class="sxs-lookup"><span data-stu-id="ba30e-219">Creating or editing recurring tasks.</span></span>
    
- <span data-ttu-id="ba30e-220">既存のタスクでのタスク カレンダーの割り当てまたは変更。</span><span class="sxs-lookup"><span data-stu-id="ba30e-220">Assigning or changing the task calendar on existing tasks.</span></span>
    
- <span data-ttu-id="ba30e-221">タスク カレンダーを使用した新しいタスクの作成。</span><span class="sxs-lookup"><span data-stu-id="ba30e-221">Creating a new task with a task calendar.</span></span>
    
- <span data-ttu-id="ba30e-222">[TASK_IGNORES_RES_CAL](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_IGNORES_RES_CAL.aspx)フィールドの値を変更する (タスクは、リソース カレンダーを無視します)。</span><span class="sxs-lookup"><span data-stu-id="ba30e-222">Changing the value of the [TASK_IGNORES_RES_CAL](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_IGNORES_RES_CAL.aspx) field (task ignores resource calendar).</span></span> 
    
- <span data-ttu-id="ba30e-223">同じ呼び出しで追加の変更を加える場合は、 [QueueUpdateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject.aspx)を使用して、タスクの現在のステータスを変更します。</span><span class="sxs-lookup"><span data-stu-id="ba30e-223">Changing the active status of a task by using [QueueUpdateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject.aspx) , if additional changes are made in the same call.</span></span> <span data-ttu-id="ba30e-224">詳細については、 [Project Server プログラミング](project-server-programmability.md)する*サーバー上でプロジェクトのスケジュール設定*」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ba30e-224">For more information, see the  *Project Scheduling on the Server*  section in [Project Server programmability](project-server-programmability.md).</span></span>
    
#### <a name="summary-tasks"></a><span data-ttu-id="ba30e-225">サマリー タスク</span><span class="sxs-lookup"><span data-stu-id="ba30e-225">Summary tasks</span></span>

- <span data-ttu-id="ba30e-226">サマリー タスクでの割り当ての作成または変更。</span><span class="sxs-lookup"><span data-stu-id="ba30e-226">Creating or changing assignments on summary tasks.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="ba30e-227">Project Professional またはその他の方法を使用して、サマリー タスクの割り当てを行わないことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="ba30e-227">We recommend that you do not make assignments on summary tasks using Project Professional or any other way.</span></span> <span data-ttu-id="ba30e-228">詳細については、 [Project Server プログラミング](project-server-programmability.md)する*サーバー上でプロジェクトのスケジュール設定*」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ba30e-228">For more information, see the  *Project Scheduling on the Server*  section in [Project Server programmability](project-server-programmability.md).</span></span> 
  
- <span data-ttu-id="ba30e-p132">通常サブタスクから重ね合わされるサマリー タスク フィールドの編集。サーバー側プロジェクトは、サマリー タスクに情報を設定してサブタスクにプッシュする代わりに、常にサマリー情報を重ね合わせます。サマリー タスクでは、以下のフィールドのみを編集できます。</span><span class="sxs-lookup"><span data-stu-id="ba30e-p132">Editing summary task fields that are normally rolled up from the subtask. Server-side projects always roll up summary information, instead of setting information on the summary task and pushing it down to the subtasks. You can edit only the following fields on summary tasks:</span></span>
    
  - <span data-ttu-id="ba30e-232">タスクの依存関係</span><span class="sxs-lookup"><span data-stu-id="ba30e-232">Task dependencies</span></span>
    
  - <span data-ttu-id="ba30e-233">式ではないユーザー設定フィールド</span><span class="sxs-lookup"><span data-stu-id="ba30e-233">Non-formula custom fields</span></span>
    
  - [<span data-ttu-id="ba30e-234">TASK_NAME</span><span class="sxs-lookup"><span data-stu-id="ba30e-234">TASK_NAME</span></span>](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_NAME.aspx)
    
  - [<span data-ttu-id="ba30e-235">TASK_OUTLINE_LEVEL</span><span class="sxs-lookup"><span data-stu-id="ba30e-235">TASK_OUTLINE_LEVEL</span></span>](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_OUTLINE_LEVEL.aspx)
    
  - [<span data-ttu-id="ba30e-236">TASK_IS_MARKED</span><span class="sxs-lookup"><span data-stu-id="ba30e-236">TASK_IS_MARKED</span></span>](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_IS_MARKED.aspx)
    
  - [<span data-ttu-id="ba30e-237">TASK_CONSTRAINT_TYPE</span><span class="sxs-lookup"><span data-stu-id="ba30e-237">TASK_CONSTRAINT_TYPE</span></span>](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_CONSTRAINT_TYPE.aspx)
    
  - [<span data-ttu-id="ba30e-238">TASK_CONSTRAINT_DATE</span><span class="sxs-lookup"><span data-stu-id="ba30e-238">TASK_CONSTRAINT_DATE</span></span>](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_CONSTRAINT_DATE.aspx)
    
  - [<span data-ttu-id="ba30e-239">TASK_PRIORITY</span><span class="sxs-lookup"><span data-stu-id="ba30e-239">TASK_PRIORITY</span></span>](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_PRIORITY.aspx)
    
  - [<span data-ttu-id="ba30e-240">TASK_DEADLINE</span><span class="sxs-lookup"><span data-stu-id="ba30e-240">TASK_DEADLINE</span></span>](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_DEADLINE.aspx)
    
  - [<span data-ttu-id="ba30e-241">TASK_FIXED_COST</span><span class="sxs-lookup"><span data-stu-id="ba30e-241">TASK_FIXED_COST</span></span>](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_FIXED_COST.aspx)
    
  - <span data-ttu-id="ba30e-242">[TASK_FIXED_COST_ACCRUAL](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_FIXED_COST_ACCRUAL.aspx)(タスクを作成する場合にのみ値を設定)</span><span class="sxs-lookup"><span data-stu-id="ba30e-242">[TASK_FIXED_COST_ACCRUAL](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_FIXED_COST_ACCRUAL.aspx) (set the value only when creating the task)</span></span> 
    
  - [<span data-ttu-id="ba30e-243">TASK_WBS</span><span class="sxs-lookup"><span data-stu-id="ba30e-243">TASK_WBS</span></span>](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_WBS.aspx)
    
<span data-ttu-id="ba30e-p133">プロジェクトのサマリー タスクについては、PSI の制限は、Project Professional に対するものと同じです。PSI は、予算割り当てを編集できます。これには、コスト型予算も含まれます。</span><span class="sxs-lookup"><span data-stu-id="ba30e-p133">For the project summary task, the PSI limitations are the same as for Project Professional. The PSI can edit budget assignments—including cost budgets.</span></span>
  
#### <a name="project-level-calculation-options"></a><span data-ttu-id="ba30e-246">プロジェクト レベルの計算オプション</span><span class="sxs-lookup"><span data-stu-id="ba30e-246">Project-level calculation options</span></span>

- <span data-ttu-id="ba30e-p134">Schedule From Start (SFS) と Schedule From Finish (SFF) の間でのプロジェクトの種類の変更 (PSI はプロジェクトを SFS または SFF として作成できますが、いったん作成したプロジェクトは、Project Professional でのみ変更できます)。</span><span class="sxs-lookup"><span data-stu-id="ba30e-p134">Changing a project type between Schedule From Start (SFS) and Schedule From Finish (SFF). (The PSI can create a project as either SFS or SFF, but once created it can be changed only in Project Professional.)</span></span>
    
- <span data-ttu-id="ba30e-249">プロジェクトの作成後、プロジェクトの基本カレンダー ([CAL_UID](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.CAL_UID.aspx) ) を変更します。</span><span class="sxs-lookup"><span data-stu-id="ba30e-249">Changing the project base calendar ([CAL_UID](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.CAL_UID.aspx) ) after project creation.</span></span> 
    
- <span data-ttu-id="ba30e-p135">計算のオプションの変更。プロジェクトの作成時に、PSI を使用して以下の計算オプションを設定できますが、これらのオプションを変更するには Project Professional が必要です (Backstage ビューで、[**オプション**] を選択し、[**Project のオプション**] ダイアログ ボックスの [**スケジュール**] タブを選択します)。</span><span class="sxs-lookup"><span data-stu-id="ba30e-p135">Changing options for calculations. You can use the PSI to set the following calculation options when the project is created, but changing the options requires Project Professional. (In Backstage view, choose **Options**, and then choose the **Schedule** tab in the **Project Options** dialog box.)</span></span> 
    
  - [<span data-ttu-id="ba30e-253">PROJ_OPT_CALC_ACT_COSTS</span><span class="sxs-lookup"><span data-stu-id="ba30e-253">PROJ_OPT_CALC_ACT_COSTS</span></span>](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_CALC_ACT_COSTS.aspx)
    
  - [<span data-ttu-id="ba30e-254">PROJ_OPT_CRITICAL_SLACK_LIMIT</span><span class="sxs-lookup"><span data-stu-id="ba30e-254">PROJ_OPT_CRITICAL_SLACK_LIMIT</span></span>](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_CRITICAL_SLACK_LIMIT.aspx)
    
  - [<span data-ttu-id="ba30e-255">PROJ_OPT_HONOR_CONSTRAINTS</span><span class="sxs-lookup"><span data-stu-id="ba30e-255">PROJ_OPT_HONOR_CONSTRAINTS</span></span>](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_HONOR_CONSTRAINTS.aspx)
    
  - [<span data-ttu-id="ba30e-256">PROJ_OPT_MOVE_ACTUAL_IF_LATER</span><span class="sxs-lookup"><span data-stu-id="ba30e-256">PROJ_OPT_MOVE_ACTUAL_IF_LATER</span></span>](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_MOVE_ACTUAL_IF_LATER.aspx)
    
  - [<span data-ttu-id="ba30e-257">PROJ_OPT_MOVE_ACTUAL_TO_STATUS</span><span class="sxs-lookup"><span data-stu-id="ba30e-257">PROJ_OPT_MOVE_ACTUAL_TO_STATUS</span></span>](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_MOVE_ACTUAL_TO_STATUS.aspx)
    
  - [<span data-ttu-id="ba30e-258">PROJ_OPT_MOVE_REMAINING_IF_EARLIER</span><span class="sxs-lookup"><span data-stu-id="ba30e-258">PROJ_OPT_MOVE_REMAINING_IF_EARLIER</span></span>](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_MOVE_REMAINING_IF_EARLIER.aspx)
    
  - [<span data-ttu-id="ba30e-259">PROJ_OPT_MOVE_REMAINING_TO_STATUS</span><span class="sxs-lookup"><span data-stu-id="ba30e-259">PROJ_OPT_MOVE_REMAINING_TO_STATUS</span></span>](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_MOVE_REMAINING_TO_STATUS.aspx)
    
  - [<span data-ttu-id="ba30e-260">PROJ_OPT_MULT_CRITICAL_PATHS</span><span class="sxs-lookup"><span data-stu-id="ba30e-260">PROJ_OPT_MULT_CRITICAL_PATHS</span></span>](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_MULT_CRITICAL_PATHS.aspx)
    
  - [<span data-ttu-id="ba30e-261">PROJ_OPT_SPLIT_IN_PROGRESS</span><span class="sxs-lookup"><span data-stu-id="ba30e-261">PROJ_OPT_SPLIT_IN_PROGRESS</span></span>](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_SPLIT_IN_PROGRESS.aspx)
    
  - [<span data-ttu-id="ba30e-262">PROJ_OPT_SPREAD_ACT_COSTS</span><span class="sxs-lookup"><span data-stu-id="ba30e-262">PROJ_OPT_SPREAD_ACT_COSTS</span></span>](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_SPREAD_ACT_COSTS.aspx)
    
  - [<span data-ttu-id="ba30e-263">PROJ_OPT_SPREAD_PCT_COMP</span><span class="sxs-lookup"><span data-stu-id="ba30e-263">PROJ_OPT_SPREAD_PCT_COMP</span></span>](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_SPREAD_PCT_COMP.aspx)
    
  - [<span data-ttu-id="ba30e-264">PROJ_OPT_TASK_UPDATES_RES</span><span class="sxs-lookup"><span data-stu-id="ba30e-264">PROJ_OPT_TASK_UPDATES_RES</span></span>](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_TASK_UPDATES_RES.aspx)
    
## <a name="see-also"></a><span data-ttu-id="ba30e-265">関連項目</span><span class="sxs-lookup"><span data-stu-id="ba30e-265">See also</span></span>

- [<span data-ttu-id="ba30e-266">CSOM のすること、しないこと</span><span class="sxs-lookup"><span data-stu-id="ba30e-266">What the CSOM does and does not do</span></span>](what-the-csom-does-and-does-not-do.md)  
- [<span data-ttu-id="ba30e-267">Project Server プログラミング</span><span class="sxs-lookup"><span data-stu-id="ba30e-267">Project Server programmability</span></span>](project-server-programmability.md)   
- [<span data-ttu-id="ba30e-268">クレーム ベース認証を使用した SharePoint Online でのリモート認証</span><span class="sxs-lookup"><span data-stu-id="ba30e-268">Remote Authentication in SharePoint Online Using Claims-Based Authentication</span></span>](http://msdn.microsoft.com/library/49067f7a-3020-478f-ba97-4b7ce3ea9b87%28Office.15%29.aspx)  
- [<span data-ttu-id="ba30e-269">Office 用アプリの作成</span><span class="sxs-lookup"><span data-stu-id="ba30e-269">Office Add-ins</span></span>](https://docs.microsoft.com/office/dev/add-ins/overview/office-add-ins) 
    

