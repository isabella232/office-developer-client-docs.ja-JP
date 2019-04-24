---
title: project Online でユーザー設定フィールドを一括更新し、プロジェクトサイトを作成する
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 815131c6-190c-4f29-83bf-c853eee72821
description: お客様が project online を最大限に活用し、サービスの拡張性と柔軟性を向上させるために、project online のアプリとワークフローで使用できるクライアント側オブジェクトモデルに2つのメソッドを追加しました。
ms.openlocfilehash: 4de42471cd8c2f12a982447ccffc27ec8104fa31
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355401"
---
# <a name="bulk-update-custom-fields-and-create-project-sites-from-a-workflow-in-project-online"></a><span data-ttu-id="ee348-103">Project Online でユーザー設定フィールドを一括更新し、ワークフローからプロジェクト サイトを作成する</span><span class="sxs-lookup"><span data-stu-id="ee348-103">Bulk update custom fields and create project sites from a workflow in Project Online</span></span>

<span data-ttu-id="ee348-104">お客様が project online を最大限に活用し、サービスの拡張性と柔軟性を向上させるために、project online のアプリとワークフローで使用できるクライアント側オブジェクトモデルに2つのメソッドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="ee348-104">To help customers get the most out of Project Online and improve our service extensibility and flexibility, we've added two methods to the client-side object model that you can use in Project Online apps and workflows.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ee348-105">**UpdateCustomFields**</span><span class="sxs-lookup"><span data-stu-id="ee348-105">**UpdateCustomFields**</span></span> <br/> |<span data-ttu-id="ee348-106">プロジェクトユーザー設定フィールドを一括更新します。</span><span class="sxs-lookup"><span data-stu-id="ee348-106">Bulk updates project custom fields.</span></span> <span data-ttu-id="ee348-107">Project Online の場合のみ。</span><span class="sxs-lookup"><span data-stu-id="ee348-107">For Project Online only.</span></span> <span data-ttu-id="ee348-108">REST API でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="ee348-108">Available only in the REST API.</span></span>  <br/> |
|<span data-ttu-id="ee348-109">**CreateProjectSite**</span><span class="sxs-lookup"><span data-stu-id="ee348-109">**CreateProjectSite**</span></span> <br/> | <span data-ttu-id="ee348-110">プロジェクトサイトを作成します。</span><span class="sxs-lookup"><span data-stu-id="ee348-110">Creates a Project site.</span></span> <span data-ttu-id="ee348-111">Project Online の場合のみ。</span><span class="sxs-lookup"><span data-stu-id="ee348-111">For Project Online only.</span></span> <span data-ttu-id="ee348-112">REST API、マネージクライアントオブジェクトモデル、および JavaScript クライアントオブジェクトモデルで使用できます。</span><span class="sxs-lookup"><span data-stu-id="ee348-112">Available in the REST API, managed client object model, and JavaScript client object model.</span></span>  <br/> |
   
<span data-ttu-id="ee348-113">これらの方法では、柔軟性が向上するだけでなく、プロジェクトをワークフローに保存して発行するときのパフォーマンスも大幅に向上しています。</span><span class="sxs-lookup"><span data-stu-id="ee348-113">In addition to providing more flexibility, these methods also offer significant performance improvements when saving and publishing projects in a workflow.</span></span> <span data-ttu-id="ee348-114">この記事では、REST API のメソッドを使用する方法について説明し、ユーザー設定フィールドおよびプロジェクトサイトを作成するワークフローを一括で更新するワークフローを作成するための手順を示します。</span><span class="sxs-lookup"><span data-stu-id="ee348-114">This article describes how to use the methods in the REST API and provides instructions for creating a workflow that bulk updates custom fields and a workflow that creates a Project site.</span></span>
  
> [!NOTE]
> <span data-ttu-id="ee348-115">sharepoint 2013 ワークフローから REST api を呼び出す方法の詳細については、「 [POST メソッドを使用してワークフローから sharepoint rest サービスを使用](https://mysharepointinsight.blogspot.com/2013/05/using-sharepoint-rest-services-from.mdl)する」および「sharepoint [Designer ワークフローから sharepoint 2013 rest api を呼び出す](https://sergeluca.wordpress.com/2013/04/09/calling-the-sharepoint-2013-rest-api-from-a-sharepoint-designer-workflow/)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ee348-115">To learn more about calling REST APIs from SharePoint 2013 workflows, see [Using SharePoint REST services from workflow with POST method](https://mysharepointinsight.blogspot.com/2013/05/using-sharepoint-rest-services-from.mdl) and [Calling the SharePoint 2013 Rest API from a SharePoint Designer Workflow](https://sergeluca.wordpress.com/2013/04/09/calling-the-sharepoint-2013-rest-api-from-a-sharepoint-designer-workflow/).</span></span> 
  
## <a name="bulk-update-project-custom-fields-from-a-workflow"></a><span data-ttu-id="ee348-116">ワークフローからのプロジェクトユーザー設定フィールドの一括更新</span><span class="sxs-lookup"><span data-stu-id="ee348-116">Bulk update project custom fields from a workflow</span></span>
<span data-ttu-id="ee348-117"><a name="BulkUpdateCustomFields"> </a></span><span class="sxs-lookup"><span data-stu-id="ee348-117"></span></span>

<span data-ttu-id="ee348-118">以前は、ワークフローは一度に1つのユーザー設定フィールドしか更新できませんでした。</span><span class="sxs-lookup"><span data-stu-id="ee348-118">Previously, workflows could only update one custom field at a time.</span></span> <span data-ttu-id="ee348-119">一度に1つのプロジェクトユーザー設定フィールドを更新すると、ユーザーがプロジェクト詳細ページ間を移行するときに、エンドユーザーの作業が遅くなる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ee348-119">Updating project custom fields one at a time can result in a poor end-user experience when users transition between Project Detail Pages.</span></span> <span data-ttu-id="ee348-120">各更新プログラムでは、[**プロジェクトフィールドの設定]** アクションを使用して、複数のユーザー設定フィールドを高待機時間の低帯域幅のネットワーク上で更新することによって、単純なオーバーヘッドが発生しました。</span><span class="sxs-lookup"><span data-stu-id="ee348-120">Each update required a separate server request using the **Set Project Field** action, and updating multiple custom fields on a high-latency, low-bandwidth network resulted in a non-trivial overhead.</span></span> <span data-ttu-id="ee348-121">この問題を解決するには、 **UpdateCustomFields**メソッドを REST API に追加して、ユーザー設定フィールドを一括更新できるようにしました。</span><span class="sxs-lookup"><span data-stu-id="ee348-121">To resolve this issue, we added the **UpdateCustomFields** method to the REST API that lets you bulk update custom fields.</span></span> <span data-ttu-id="ee348-122">**UpdateCustomFields**を使用するには、更新するすべてのユーザー設定フィールドの名前と値を含むディクショナリを渡します。</span><span class="sxs-lookup"><span data-stu-id="ee348-122">To use **UpdateCustomFields**, you pass in a dictionary that contains the names and values of all the custom fields you want to update.</span></span>
  
<span data-ttu-id="ee348-123">REST メソッドは、次のエンドポイントにあります。</span><span class="sxs-lookup"><span data-stu-id="ee348-123">The REST method can be found at the following endpoint:</span></span>
  
`https://<site-url>/_api/ProjectServer/Projects('<guid>')/Draft/UpdateCustomFields()`
  
> [!NOTE]
> <span data-ttu-id="ee348-124">例の`<site-url>`プレースホルダーを、project Web App (PWA) サイトの URL、およびプロジェクト UID を含む`<guid>`プレースホルダーに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="ee348-124">Replace the  `<site-url>` placeholder in the examples with the URL of your Project Web App (PWA) site and the  `<guid>` placeholder with your project UID.</span></span> 
  
<span data-ttu-id="ee348-125">このセクションでは、プロジェクトのユーザー設定フィールドを一括更新するワークフローを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="ee348-125">This section describes how to create a workflow that bulk updates custom fields for a project.</span></span> <span data-ttu-id="ee348-126">ワークフローは、次の大まかな手順に従います。</span><span class="sxs-lookup"><span data-stu-id="ee348-126">The workflow follows these high-level steps:</span></span>
  
- <span data-ttu-id="ee348-127">更新するプロジェクトがチェックインされるまで待機する</span><span class="sxs-lookup"><span data-stu-id="ee348-127">Wait for the project that you want to update to get checked in</span></span>
    
- <span data-ttu-id="ee348-128">プロジェクトのすべてのユーザー設定フィールドの更新を定義するデータセットを構築する</span><span class="sxs-lookup"><span data-stu-id="ee348-128">Build a data set that defines all your custom field updates for the project</span></span>
    
- <span data-ttu-id="ee348-129">プロジェクトをチェックアウトする</span><span class="sxs-lookup"><span data-stu-id="ee348-129">Check out the project</span></span>
    
- <span data-ttu-id="ee348-130">**UpdateCustomFields**を呼び出して、ユーザー設定フィールドの更新をプロジェクトに適用します。</span><span class="sxs-lookup"><span data-stu-id="ee348-130">Call **UpdateCustomFields** to apply the custom field updates to the project</span></span> 
    
- <span data-ttu-id="ee348-131">関連情報をワークフロー履歴リストに記録する (必要な場合)</span><span class="sxs-lookup"><span data-stu-id="ee348-131">Log relevant information to the workflow history list (if required)</span></span>
    
- <span data-ttu-id="ee348-132">プロジェクトを発行する</span><span class="sxs-lookup"><span data-stu-id="ee348-132">Publish the project</span></span>
    
- <span data-ttu-id="ee348-133">プロジェクトをチェックインする</span><span class="sxs-lookup"><span data-stu-id="ee348-133">Check in the project</span></span>
    
<span data-ttu-id="ee348-134">最終的なエンドツーエンドのワークフローは、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="ee348-134">The final, end-to-end workflow looks like this:</span></span>
  
<span data-ttu-id="ee348-135">![エンドツーエンドのワークフロー](media/8c0741f9-7f76-409d-8c00-e7a8c3ddb89f.png "エンドツーエンドのワークフロー")</span><span class="sxs-lookup"><span data-stu-id="ee348-135">![End-to-end workflow](media/8c0741f9-7f76-409d-8c00-e7a8c3ddb89f.png "End-to-end workflow")</span></span>
  
### <a name="to-create-a-workflow-that-bulk-updates-custom-fields"></a><span data-ttu-id="ee348-136">ユーザー設定フィールドを一括更新するワークフローを作成するには</span><span class="sxs-lookup"><span data-stu-id="ee348-136">To create a workflow that bulk updates custom fields</span></span>

1. <span data-ttu-id="ee348-137">省略可能です。</span><span class="sxs-lookup"><span data-stu-id="ee348-137">Optional.</span></span> <span data-ttu-id="ee348-138">ワークフロー全体で使用できる変数に、プロジェクトの完全な URL を格納します。</span><span class="sxs-lookup"><span data-stu-id="ee348-138">Store the full URL of your project in a variable that you can use throughout the workflow.</span></span>
    
    <span data-ttu-id="ee348-139">![プロジェクトの URL を変数に格納する](media/a880c5c6-8e7a-44dd-87e9-7e532169d489.png "プロジェクトの URL を変数に格納する")</span><span class="sxs-lookup"><span data-stu-id="ee348-139">![Store the URL of the project in a variable](media/a880c5c6-8e7a-44dd-87e9-7e532169d489.png "Store the URL of the project in a variable")</span></span>
  
2. <span data-ttu-id="ee348-140">[**プロジェクトイベントの待機**] アクションをワークフローに追加し、[**プロジェクトのチェックイン時**] イベントを選択します。</span><span class="sxs-lookup"><span data-stu-id="ee348-140">Add the **Wait for Project Event** action to the workflow and choose the **When a project is checked in** event.</span></span> 
    
    <span data-ttu-id="ee348-141">![プロジェクトがチェックインされるまで待機する](media/699aa9c7-b3c9-426e-a775-96993a13559c.png "プロジェクトがチェックインされるまで待機する")</span><span class="sxs-lookup"><span data-stu-id="ee348-141">![Wait for the project to be checked in](media/699aa9c7-b3c9-426e-a775-96993a13559c.png "Wait for the project to be checked in")</span></span>
  
3. <span data-ttu-id="ee348-142">「Create **dictionary** action」アクションを使用して、 **requestHeader**辞書を作成します。</span><span class="sxs-lookup"><span data-stu-id="ee348-142">Create a **requestHeader** dictionary using the **Build dictionary** action.</span></span> <span data-ttu-id="ee348-143">このワークフローのすべての web サービス呼び出しに対して同じ要求ヘッダーを使用します。</span><span class="sxs-lookup"><span data-stu-id="ee348-143">You'll use the same request header for all the web service calls in this workflow.</span></span> 
    
    <span data-ttu-id="ee348-144">![requestHeader 辞書を作成する](media/83b0aa10-9ab7-43dd-800d-a738bb815876.png "requestHeader 辞書を作成する")</span><span class="sxs-lookup"><span data-stu-id="ee348-144">![Build the requestHeader dictionary](media/83b0aa10-9ab7-43dd-800d-a738bb815876.png "Build the requestHeader dictionary")</span></span>
  
4. <span data-ttu-id="ee348-145">次の2つの項目をディクショナリに追加します。</span><span class="sxs-lookup"><span data-stu-id="ee348-145">Add the following two items to the dictionary.</span></span>
    
    |<span data-ttu-id="ee348-146">名前</span><span class="sxs-lookup"><span data-stu-id="ee348-146">Name</span></span>|<span data-ttu-id="ee348-147">型</span><span class="sxs-lookup"><span data-stu-id="ee348-147">Type</span></span>|<span data-ttu-id="ee348-148">値</span><span class="sxs-lookup"><span data-stu-id="ee348-148">Value</span></span>|
    |:-----|:-----|:-----|
    |<span data-ttu-id="ee348-149">Accept</span><span class="sxs-lookup"><span data-stu-id="ee348-149">Accept</span></span>  <br/> |<span data-ttu-id="ee348-150">String</span><span class="sxs-lookup"><span data-stu-id="ee348-150">String</span></span>  <br/> |<span data-ttu-id="ee348-151">application/json;odata = verbose</span><span class="sxs-lookup"><span data-stu-id="ee348-151">application/json; odata=verbose</span></span>  <br/> |
    |<span data-ttu-id="ee348-152">Content-Type</span><span class="sxs-lookup"><span data-stu-id="ee348-152">Content-Type</span></span>  <br/> |<span data-ttu-id="ee348-153">String</span><span class="sxs-lookup"><span data-stu-id="ee348-153">String</span></span>  <br/> |<span data-ttu-id="ee348-154">application/json;odata = verbose</span><span class="sxs-lookup"><span data-stu-id="ee348-154">application/json; odata=verbose</span></span>  <br/> |
   
    <span data-ttu-id="ee348-155">![Accept ヘッダーの追加](media/2f2e2016-3c49-4cac-b1e7-f2b8118b840c.png "Accept ヘッダーの追加")</span><span class="sxs-lookup"><span data-stu-id="ee348-155">![Adding an Accept header](media/2f2e2016-3c49-4cac-b1e7-f2b8118b840c.png "Adding an Accept header")</span></span>
  
5. <span data-ttu-id="ee348-156">「**辞書を構築**する」アクションを使用して、 **requestbody**辞書を作成します。</span><span class="sxs-lookup"><span data-stu-id="ee348-156">Create a **requestBody** dictionary using the **Build dictionary** action.</span></span> <span data-ttu-id="ee348-157">この辞書には、適用するすべてのフィールドの更新が格納されます。</span><span class="sxs-lookup"><span data-stu-id="ee348-157">This dictionary stores all the field updates that you want to apply.</span></span> 
    
    <span data-ttu-id="ee348-158">各ユーザー設定フィールドの更新では、フィールドの (1) メタデータ型、(2) キー、(3) 値、および (4) 値の型の4つの行が必要です。</span><span class="sxs-lookup"><span data-stu-id="ee348-158">Each custom field update requires four rows: the field's (1) metadata type, (2) key, (3) value, and (4) value type.</span></span>
    
    - <span data-ttu-id="ee348-159">**__ メタデータ/型**フィールドのメタデータ型。</span><span class="sxs-lookup"><span data-stu-id="ee348-159">**__metadata/type** The field's metadata type.</span></span> <span data-ttu-id="ee348-160">このレコードは常に同じであり、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="ee348-160">This record is always the same and uses the following values:</span></span> 
    
       - <span data-ttu-id="ee348-161">Name: customfielddictionary (i)/__ metadata/type (ここで、 **i**は0から始まる辞書内の各ユーザー設定フィールドのインデックス)</span><span class="sxs-lookup"><span data-stu-id="ee348-161">Name: customFieldDictionary(i)/__metadata/type (where **i** is the index of each custom field in the dictionary, starting with 0)</span></span> 
            
       - <span data-ttu-id="ee348-162">型:String</span><span class="sxs-lookup"><span data-stu-id="ee348-162">Type: String</span></span>
            
       - <span data-ttu-id="ee348-163">値: SP。KeyValue</span><span class="sxs-lookup"><span data-stu-id="ee348-163">Value: SP.KeyValue</span></span>
    
       <span data-ttu-id="ee348-164">![ユーザー設定フィールドの更新を定義する](media/a4423493-6603-42ee-ae50-1ef74c5c59bd.png "ユーザー設定フィールドの更新を定義する")</span><span class="sxs-lookup"><span data-stu-id="ee348-164">![Defining a custom field update](media/a4423493-6603-42ee-ae50-1ef74c5c59bd.png "Defining a custom field update")</span></span>
  
    - <span data-ttu-id="ee348-165">**キー**ユーザー設定フィールドの内部名 (形式: *Custom_ce23fbf43fa0e411941000155d3c8201*</span><span class="sxs-lookup"><span data-stu-id="ee348-165">**Key** The internal name of the custom field, in the format: *Custom_ce23fbf43fa0e411941000155d3c8201*</span></span> 
    
       <span data-ttu-id="ee348-166">**InternalName**エンドポイントに移動することで、ユーザー設定フィールドの内部名を検索できます。`https://<site-url>/_api/ProjectServer/CustomFields('<guid>')/InternalName`</span><span class="sxs-lookup"><span data-stu-id="ee348-166">You can find the internal name of a custom field by navigating to it's **InternalName** endpoint: `https://<site-url>/_api/ProjectServer/CustomFields('<guid>')/InternalName`</span></span>
    
       <span data-ttu-id="ee348-167">ユーザー設定フィールドを手動で作成した場合、値はサイトごとに異なります。</span><span class="sxs-lookup"><span data-stu-id="ee348-167">If you created your custom fields manually, the values will differ from site to site.</span></span> <span data-ttu-id="ee348-168">複数のサイト間でワークフローを再利用することを計画している場合は、ユーザー設定フィールド id が正しいことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="ee348-168">If you plan to reuse the workflow across multiple sites, make sure the custom field IDs are correct.</span></span>
    
    - <span data-ttu-id="ee348-169">**値**ユーザー設定フィールドに割り当てる値を指定します。</span><span class="sxs-lookup"><span data-stu-id="ee348-169">**Value** The value to assign to the custom field.</span></span> <span data-ttu-id="ee348-170">参照テーブルにリンクされているユーザー設定フィールドの場合は、実際の参照テーブルの値の代わりに、参照テーブルのエントリの内部名を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ee348-170">For custom fields that are linked to lookup tables, you need to use the internal names of the lookup table entries instead of the actual lookup table values.</span></span> 
    
       <span data-ttu-id="ee348-171">参照テーブルエントリの内部名は、次のエンドポイントで確認できます。`https://<site-url>/_api/ProjectServer/CustomFields('<guid>')/LookupEntries('<guid>')/InternalName`</span><span class="sxs-lookup"><span data-stu-id="ee348-171">You can find the internal name of the lookup table entry at the following endpoint: `https://<site-url>/_api/ProjectServer/CustomFields('<guid>')/LookupEntries('<guid>')/InternalName`</span></span>
    
       <span data-ttu-id="ee348-172">複数の値を受け入れるように参照テーブルのユーザー設定フィールドが設定さ`;#`れている場合は、を使用して値を連結します (下記の辞書例を参照)。</span><span class="sxs-lookup"><span data-stu-id="ee348-172">If you have a lookup table custom field set up to accept multiple values, use  `;#` to concatenate values (as shown in the example dictionary below).</span></span> 
    
    - <span data-ttu-id="ee348-173">**ValueType**更新するユーザー設定フィールドの種類を示します。</span><span class="sxs-lookup"><span data-stu-id="ee348-173">**ValueType** The type of the custom field you are updating.</span></span> 
    
       - <span data-ttu-id="ee348-174">Text、Duration、Flag、および lookuptable フィールドの場合は、Edm を使用します。</span><span class="sxs-lookup"><span data-stu-id="ee348-174">For Text, Duration, Flag, and LookupTable fields, use Edm.String</span></span>
    
       - <span data-ttu-id="ee348-175">数値フィールドの場合は、edm を使用して、またはその他の OData 承認番号の種類を使用します。</span><span class="sxs-lookup"><span data-stu-id="ee348-175">For Number fields, use Edm.Int32, Edm.Double, or any other OData-accepted number type</span></span>
    
       - <span data-ttu-id="ee348-176">日付フィールドについては、Edm を使用します。</span><span class="sxs-lookup"><span data-stu-id="ee348-176">For Date fields, use Edm.DateTime</span></span>
    
       <span data-ttu-id="ee348-177">次の辞書例では、3つのユーザー設定フィールドの更新を定義しています。</span><span class="sxs-lookup"><span data-stu-id="ee348-177">The example dictionary below defines updates for three custom fields.</span></span> <span data-ttu-id="ee348-178">1つ目は、複数値の参照テーブルのユーザー設定フィールドで、2番目は数値フィールドで、3番目は日付フィールド用です。</span><span class="sxs-lookup"><span data-stu-id="ee348-178">The first is for a multiple value lookup table custom field, the second is for a number field, and the third is for a date field.</span></span> <span data-ttu-id="ee348-179">**customfielddictionary**インデックスがどのようにインクリメントされるかに注目してください。</span><span class="sxs-lookup"><span data-stu-id="ee348-179">Note how the **customFieldDictionary** index increments.</span></span> 
    
       > [!NOTE]
       > <span data-ttu-id="ee348-180">これらの値は、説明のみを目的としています。</span><span class="sxs-lookup"><span data-stu-id="ee348-180">These values are for illustration purposes only.</span></span> <span data-ttu-id="ee348-181">使用するキーと値のペアは、PWA のデータによって異なります。</span><span class="sxs-lookup"><span data-stu-id="ee348-181">The key-value pairs you'll use depend on your PWA data.</span></span> 
  
       |<span data-ttu-id="ee348-182">名前</span><span class="sxs-lookup"><span data-stu-id="ee348-182">Name</span></span>|<span data-ttu-id="ee348-183">型</span><span class="sxs-lookup"><span data-stu-id="ee348-183">Type</span></span>|<span data-ttu-id="ee348-184">値</span><span class="sxs-lookup"><span data-stu-id="ee348-184">Value</span></span>|
       |:-----|:-----|:-----|
       |<span data-ttu-id="ee348-185">customfielddictionary (0)/__ metadata/type</span><span class="sxs-lookup"><span data-stu-id="ee348-185">customFieldDictionary(0)/__metadata/type</span></span>  <br/> |<span data-ttu-id="ee348-186">String</span><span class="sxs-lookup"><span data-stu-id="ee348-186">String</span></span>  <br/> |<span data-ttu-id="ee348-187">sp2.KeyValue</span><span class="sxs-lookup"><span data-stu-id="ee348-187">SP.KeyValue</span></span>  <br/> |
       |<span data-ttu-id="ee348-188">customfielddictionary (0)/キー</span><span class="sxs-lookup"><span data-stu-id="ee348-188">customFieldDictionary(0)/Key</span></span>  <br/> |<span data-ttu-id="ee348-189">String</span><span class="sxs-lookup"><span data-stu-id="ee348-189">String</span></span>  <br/> |<span data-ttu-id="ee348-190">カスタム\_ce23fbf43fa0e411941000155d3c8201</span><span class="sxs-lookup"><span data-stu-id="ee348-190">Custom\_ce23fbf43fa0e411941000155d3c8201</span></span>  <br/> |
       |<span data-ttu-id="ee348-191">customfielddictionary (0)/Value</span><span class="sxs-lookup"><span data-stu-id="ee348-191">customFieldDictionary(0)/Value</span></span>  <br/> |<span data-ttu-id="ee348-192">String</span><span class="sxs-lookup"><span data-stu-id="ee348-192">String</span></span>  <br/> |<span data-ttu-id="ee348-193">Entry\_b9a2fd69279de411940f00155d3c8201; #Entry\_baa2fd69279de411940f00155d3c8201</span><span class="sxs-lookup"><span data-stu-id="ee348-193">Entry\_b9a2fd69279de411940f00155d3c8201;#Entry\_baa2fd69279de411940f00155d3c8201</span></span>  <br/> |
       |<span data-ttu-id="ee348-194">customfielddictionary (0)/ValueType</span><span class="sxs-lookup"><span data-stu-id="ee348-194">customFieldDictionary(0)/ValueType</span></span>  <br/> |<span data-ttu-id="ee348-195">String</span><span class="sxs-lookup"><span data-stu-id="ee348-195">String</span></span>  <br/> |<span data-ttu-id="ee348-196">Edm.String</span><span class="sxs-lookup"><span data-stu-id="ee348-196">Edm.String</span></span>  <br/> |
       |<span data-ttu-id="ee348-197">customfielddictionary (1)/__ metadata/type</span><span class="sxs-lookup"><span data-stu-id="ee348-197">customFieldDictionary(1)/__metadata/type</span></span>  <br/> |<span data-ttu-id="ee348-198">String</span><span class="sxs-lookup"><span data-stu-id="ee348-198">String</span></span>  <br/> |<span data-ttu-id="ee348-199">sp2.KeyValue</span><span class="sxs-lookup"><span data-stu-id="ee348-199">SP.KeyValue</span></span>  <br/> |
       |<span data-ttu-id="ee348-200">customfielddictionary (1)/キー</span><span class="sxs-lookup"><span data-stu-id="ee348-200">customFieldDictionary(1)/Key</span></span>  <br/> |<span data-ttu-id="ee348-201">String</span><span class="sxs-lookup"><span data-stu-id="ee348-201">String</span></span>  <br/> |<span data-ttu-id="ee348-202">Custom_c7f114c97098e411940f00155d3c8201</span><span class="sxs-lookup"><span data-stu-id="ee348-202">Custom_c7f114c97098e411940f00155d3c8201</span></span>  <br/> |
       |<span data-ttu-id="ee348-203">customfielddictionary (1)/Value</span><span class="sxs-lookup"><span data-stu-id="ee348-203">customFieldDictionary(1)/Value</span></span>  <br/> |<span data-ttu-id="ee348-204">String</span><span class="sxs-lookup"><span data-stu-id="ee348-204">String</span></span>  <br/> |<span data-ttu-id="ee348-205">90.5</span><span class="sxs-lookup"><span data-stu-id="ee348-205">90.5</span></span>  <br/> |
       |<span data-ttu-id="ee348-206">customfielddictionary (1)/ValueType</span><span class="sxs-lookup"><span data-stu-id="ee348-206">customFieldDictionary(1)/ValueType</span></span>  <br/> |<span data-ttu-id="ee348-207">String</span><span class="sxs-lookup"><span data-stu-id="ee348-207">String</span></span>  <br/> |<span data-ttu-id="ee348-208">Edm.Double</span><span class="sxs-lookup"><span data-stu-id="ee348-208">Edm.Double</span></span>  <br/> |
       |<span data-ttu-id="ee348-209">customfielddictionary (2)/__ metadata/type</span><span class="sxs-lookup"><span data-stu-id="ee348-209">customFieldDictionary(2)/__metadata/type</span></span>  <br/> |<span data-ttu-id="ee348-210">String</span><span class="sxs-lookup"><span data-stu-id="ee348-210">String</span></span>  <br/> |<span data-ttu-id="ee348-211">sp2.KeyValue</span><span class="sxs-lookup"><span data-stu-id="ee348-211">SP.KeyValue</span></span>  <br/> |
       |<span data-ttu-id="ee348-212">customfielddictionary (2)/キー</span><span class="sxs-lookup"><span data-stu-id="ee348-212">customFieldDictionary(2)/Key</span></span>  <br/> |<span data-ttu-id="ee348-213">String</span><span class="sxs-lookup"><span data-stu-id="ee348-213">String</span></span>  <br/> |<span data-ttu-id="ee348-214">Custom_c6fb67e0b9a1e411941000155d3c8201</span><span class="sxs-lookup"><span data-stu-id="ee348-214">Custom_c6fb67e0b9a1e411941000155d3c8201</span></span>  <br/> |
       |<span data-ttu-id="ee348-215">customfielddictionary (2)/Value</span><span class="sxs-lookup"><span data-stu-id="ee348-215">customFieldDictionary(2)/Value</span></span>  <br/> |<span data-ttu-id="ee348-216">String</span><span class="sxs-lookup"><span data-stu-id="ee348-216">String</span></span>  <br/> |<span data-ttu-id="ee348-217">2015-04-01t00:00: 00.0000000</span><span class="sxs-lookup"><span data-stu-id="ee348-217">2015-04-01T00:00:00.0000000</span></span>  <br/> |
       |<span data-ttu-id="ee348-218">customfielddictionary (2)/ValueType</span><span class="sxs-lookup"><span data-stu-id="ee348-218">customFieldDictionary(2)/ValueType</span></span>  <br/> |<span data-ttu-id="ee348-219">String</span><span class="sxs-lookup"><span data-stu-id="ee348-219">String</span></span>  <br/> |<span data-ttu-id="ee348-220">Edm.DateTime</span><span class="sxs-lookup"><span data-stu-id="ee348-220">Edm.DateTime</span></span>  <br/> |
   
       <span data-ttu-id="ee348-221">![ユーザー設定フィールドの更新を定義する辞書](media/41a1f18f-a6b2-40ff-904b-437baf962621.png "ユーザー設定フィールドの更新を定義する辞書")</span><span class="sxs-lookup"><span data-stu-id="ee348-221">![Dictionary that defines custom field updates](media/41a1f18f-a6b2-40ff-904b-437baf962621.png "Dictionary that defines custom field updates")</span></span>
  
6. <span data-ttu-id="ee348-222">[ **HTTP Web サービスの呼び出し**] アクションを追加して、プロジェクトをチェックアウトします。</span><span class="sxs-lookup"><span data-stu-id="ee348-222">Add a **Call HTTP Web Service** action to check the project out.</span></span> 
    
    <span data-ttu-id="ee348-223">![Checkout メソッドを呼び出す](media/8ce56014-0317-419b-afa7-229d05c86885.png "Checkout メソッドを呼び出す")</span><span class="sxs-lookup"><span data-stu-id="ee348-223">![Call the Checkout method](media/8ce56014-0317-419b-afa7-229d05c86885.png "Call the Checkout method")</span></span>
  
7. <span data-ttu-id="ee348-224">web サービス呼び出しのプロパティを編集して、要求ヘッダーを指定します。</span><span class="sxs-lookup"><span data-stu-id="ee348-224">Edit the properties of the web service call to specify the request header.</span></span> <span data-ttu-id="ee348-225">[**プロパティ**] ダイアログボックスを開くには、アクションを右クリックして [**プロパティ**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="ee348-225">To open the **Properties** dialog box, right-click the action and choose **Properties**.</span></span>
    
    <span data-ttu-id="ee348-226">![web サービス呼び出しプロパティで要求ヘッダーを指定する](media/d81e92b1-43df-42ad-9cd0-a693f93b164e.png "web サービス呼び出しプロパティで要求ヘッダーを指定する")</span><span class="sxs-lookup"><span data-stu-id="ee348-226">![Specify the request header in web service call properties](media/d81e92b1-43df-42ad-9cd0-a693f93b164e.png "Specify the request header in web service call properties")</span></span>
  
8. <span data-ttu-id="ee348-227">**UpdateCustomFields**メソッドを呼び出す**HTTP Web サービスの呼び出し**アクションを追加します。</span><span class="sxs-lookup"><span data-stu-id="ee348-227">Add a **Call HTTP Web Service** action to call the **UpdateCustomFields** method.</span></span> 
    
    <span data-ttu-id="ee348-228">![HTTP Web サービスの呼び出しアクションを作成する](media/9a73a201-c035-41b4-8798-506ac48b90f8.png "HTTP Web サービスの呼び出しアクションを作成する")</span><span class="sxs-lookup"><span data-stu-id="ee348-228">![Create a Call HTTP Web Service action](media/9a73a201-c035-41b4-8798-506ac48b90f8.png "Create a Call HTTP Web Service action")</span></span>
  
    <span data-ttu-id="ee348-229">web サービス`/Draft/` URL のセグメントをメモします。</span><span class="sxs-lookup"><span data-stu-id="ee348-229">Note the  `/Draft/` segment in the web service URL.</span></span> <span data-ttu-id="ee348-230">完全な URL は次のようになります。`https://<site-url>/_api/ProjectServer/Projects('<guid>')/Draft/UpdateCustomFields()`</span><span class="sxs-lookup"><span data-stu-id="ee348-230">The full URL should look like this: `https://<site-url>/_api/ProjectServer/Projects('<guid>')/Draft/UpdateCustomFields()`</span></span>
    
    <span data-ttu-id="ee348-231">![UpdateCustomFields メソッドを呼び出す](media/03b323f1-8e99-4b18-be18-be505d7cec7e.png "UpdateCustomFields メソッドを呼び出す")</span><span class="sxs-lookup"><span data-stu-id="ee348-231">![Call the UpdateCustomFields method](media/03b323f1-8e99-4b18-be18-be505d7cec7e.png "Call the UpdateCustomFields method")</span></span>
  
9. <span data-ttu-id="ee348-232">web サービス呼び出しのプロパティを編集して、作成した辞書に**RequestHeader**および**requestcontent**パラメーターをバインドします。</span><span class="sxs-lookup"><span data-stu-id="ee348-232">Edit the properties of the web service call to bind the **RequestHeader** and **RequestContent** parameters to the dictionaries you created.</span></span> <span data-ttu-id="ee348-233">また、新しい変数を作成して、応答可能な**テント**を格納することもできます。</span><span class="sxs-lookup"><span data-stu-id="ee348-233">You can also create a new variable to store the **ResponseContent**.</span></span>
    
    <span data-ttu-id="ee348-234">![要求ヘッダーとコンテンツに辞書をバインドする](media/f96bec92-138e-4eab-b1e7-1ab83d0428a5.png "要求ヘッダーとコンテンツに辞書をバインドする")</span><span class="sxs-lookup"><span data-stu-id="ee348-234">![Bind the dictionaries to the request header and content](media/f96bec92-138e-4eab-b1e7-1ab83d0428a5.png "Bind the dictionaries to the request header and content")</span></span>
  
10. <span data-ttu-id="ee348-235">省略可能です。</span><span class="sxs-lookup"><span data-stu-id="ee348-235">Optional.</span></span> <span data-ttu-id="ee348-236">応答ディクショナリから読み取り、キュージョブの状態を確認し、ワークフロー履歴リストに情報を記録します。</span><span class="sxs-lookup"><span data-stu-id="ee348-236">Read from the response dictionary to check the state of the queue job and log the information in the workflow history list.</span></span>
    
    <span data-ttu-id="ee348-237">![ログの設定](media/7d2f4936-61d7-4906-83e8-7478a5935af5.png "ログの設定")</span><span class="sxs-lookup"><span data-stu-id="ee348-237">![Setting up logging](media/7d2f4936-61d7-4906-83e8-7478a5935af5.png "Setting up logging")</span></span>
  
11. <span data-ttu-id="ee348-238">web サービス呼び出しを**発行**エンドポイントに追加して、プロジェクトを発行します。</span><span class="sxs-lookup"><span data-stu-id="ee348-238">Add a web service call to the **Publish** endpoint to publish the project.</span></span> <span data-ttu-id="ee348-239">常に同じ要求ヘッダーを使用します。</span><span class="sxs-lookup"><span data-stu-id="ee348-239">Always use the same request header.</span></span> 
    
    <span data-ttu-id="ee348-240">![Publish メソッドを呼び出す](media/3b661091-ffae-4d7e-a0bb-5b96a6292731.png "Publish メソッドを呼び出す")</span><span class="sxs-lookup"><span data-stu-id="ee348-240">![Call the Publish method](media/3b661091-ffae-4d7e-a0bb-5b96a6292731.png "Call the Publish method")</span></span>
  
    <span data-ttu-id="ee348-241">![発行 web サービスの呼び出しのプロパティ](media/6a80a5d3-7e29-4398-993c-f78b3faca8b1.png "発行 web サービスの呼び出しのプロパティ")</span><span class="sxs-lookup"><span data-stu-id="ee348-241">![Properties for the Publish web service call](media/6a80a5d3-7e29-4398-993c-f78b3faca8b1.png "Properties for the Publish web service call")</span></span>
  
12. <span data-ttu-id="ee348-242">プロジェクトをチェックインするための、最後の web サービス呼び出しを**Checkin**エンドポイントに追加します。</span><span class="sxs-lookup"><span data-stu-id="ee348-242">Add a final web service call to the **Checkin** endpoint to check the project in.</span></span> 
    
    <span data-ttu-id="ee348-243">![Checkin メソッドを呼び出す](media/430510cb-0774-4911-af7f-b565b83eba0e.png "Checkin メソッドを呼び出す")</span><span class="sxs-lookup"><span data-stu-id="ee348-243">![Call the Checkin method](media/430510cb-0774-4911-af7f-b565b83eba0e.png "Call the Checkin method")</span></span>
  
    <span data-ttu-id="ee348-244">![Checkin web サービス呼び出しのプロパティ](media/485f48d6-bbb8-4568-9dc3-aae3218f6bd1.png "Checkin web サービス呼び出しのプロパティ")</span><span class="sxs-lookup"><span data-stu-id="ee348-244">![Properties for the Checkin web service call](media/485f48d6-bbb8-4568-9dc3-aae3218f6bd1.png "Properties for the Checkin web service call")</span></span>

<span data-ttu-id="ee348-245"><a name="CreateProjectSite"> </a></span><span class="sxs-lookup"><span data-stu-id="ee348-245"></span></span>

## <a name="create-a-project-site-from-a-workflow"></a><span data-ttu-id="ee348-246">ワークフローからプロジェクトサイトを作成する</span><span class="sxs-lookup"><span data-stu-id="ee348-246">Create a Project site from a workflow</span></span>

<span data-ttu-id="ee348-247">各プロジェクトには、チームメンバーが共同作業を行ったり、ドキュメントを共有したり、問題を発生させたりできる、独自の専用の SharePoint サイトを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="ee348-247">Every project can have its own dedicated SharePoint sites where team members can collaborate, share documents, raise issues, and so on.</span></span> <span data-ttu-id="ee348-248">以前は、サイトは、最初に発行するとき、または project Professional のプロジェクトマネージャー、または管理者が PWA 設定で手動で作成することができます。または、無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="ee348-248">Previously, sites could only be created automatically on first publish or manually by the project manager in Project Professional or by the administrator in PWA settings, or they could be disabled.</span></span>
  
<span data-ttu-id="ee348-249">プロジェクトサイトを作成するタイミングを選択できるように、 **createprojectsite**メソッドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="ee348-249">We've added the **CreateProjectSite** method so you can choose when to create project sites.</span></span> <span data-ttu-id="ee348-250">これは、プロジェクト提案が最初の発行時ではなく、定義済みのワークフローの特定のステージに達したときに、サイトを自動的に作成する必要がある組織に特に便利です。</span><span class="sxs-lookup"><span data-stu-id="ee348-250">This is particularly useful for organizations who want to create their sites automatically when a project proposal reaches a specific stage in a pre-defined workflow, rather than on first publish.</span></span> <span data-ttu-id="ee348-251">プロジェクトサイトの作成を延期すると、プロジェクトの作成のパフォーマンスが大幅に向上します。</span><span class="sxs-lookup"><span data-stu-id="ee348-251">Postponing project site creation significantly improves the performance of creating a project.</span></span> 
  
<span data-ttu-id="ee348-252">**前提条件:\*\*\*\*createprojectsite**を使用できるようにするには、「 **PWA**設定 > \* \* 接続された SharePoint サイト \* \* > の**設定**で、 **[ユーザーに選択を許可する]** 設定を [プロジェクトサイトの作成] に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ee348-252">**Prerequisite:** Before you can use **CreateProjectSite**, the **Allow users to choose** setting must be set for project site creation in **PWA Settings** > \*\* Connected SharePoint Sites \*\* > **Settings**.</span></span>
  
<span data-ttu-id="ee348-253">![PWA 設定で [ユーザーに選択を許可する]] を設定する(media/6c6c8175-eb10-431d-8056-cea55718fdb4.png "ユーザーが PWA 設定で選択できるようにする設定")</span><span class="sxs-lookup"><span data-stu-id="ee348-253">![Setting "Allow users to choose" in PWA settings](media/6c6c8175-eb10-431d-8056-cea55718fdb4.png "Setting Allow users to choose in PWA settings")</span></span>
  
### <a name="to-create-a-workflow-that-creates-a-project-site"></a><span data-ttu-id="ee348-254">プロジェクトサイトを作成するワークフローを作成するには</span><span class="sxs-lookup"><span data-stu-id="ee348-254">To create a workflow that creates a Project site</span></span>

1. <span data-ttu-id="ee348-255">既存のワークフローを作成または編集し、プロジェクトサイトを作成する手順を選択します。</span><span class="sxs-lookup"><span data-stu-id="ee348-255">Create or edit an existing workflow and select the step where you want to create your Project sites.</span></span>
    
2. <span data-ttu-id="ee348-256">「Create **dictionary** action」アクションを使用して、 **requestHeader**辞書を作成します。</span><span class="sxs-lookup"><span data-stu-id="ee348-256">Create a **requestHeader** dictionary using the **Build dictionary** action.</span></span> 
    
    <span data-ttu-id="ee348-257">![requestHeader 辞書を作成する](media/83b0aa10-9ab7-43dd-800d-a738bb815876.png "requestHeader 辞書を作成する")</span><span class="sxs-lookup"><span data-stu-id="ee348-257">![Build the requestHeader dictionary](media/83b0aa10-9ab7-43dd-800d-a738bb815876.png "Build the requestHeader dictionary")</span></span>
  
3. <span data-ttu-id="ee348-258">次の2つの項目をディクショナリに追加します。</span><span class="sxs-lookup"><span data-stu-id="ee348-258">Add the following two items to the dictionary.</span></span>
    
    |<span data-ttu-id="ee348-259">名前</span><span class="sxs-lookup"><span data-stu-id="ee348-259">Name</span></span>|<span data-ttu-id="ee348-260">型</span><span class="sxs-lookup"><span data-stu-id="ee348-260">Type</span></span>|<span data-ttu-id="ee348-261">値</span><span class="sxs-lookup"><span data-stu-id="ee348-261">Value</span></span>|
    |:-----|:-----|:-----|
    |<span data-ttu-id="ee348-262">Accept</span><span class="sxs-lookup"><span data-stu-id="ee348-262">Accept</span></span>  <br/> |<span data-ttu-id="ee348-263">String</span><span class="sxs-lookup"><span data-stu-id="ee348-263">String</span></span>  <br/> |<span data-ttu-id="ee348-264">application/json;odata = verbose</span><span class="sxs-lookup"><span data-stu-id="ee348-264">application/json; odata=verbose</span></span>  <br/> |
    |<span data-ttu-id="ee348-265">Content-Type</span><span class="sxs-lookup"><span data-stu-id="ee348-265">Content-Type</span></span>  <br/> |<span data-ttu-id="ee348-266">String</span><span class="sxs-lookup"><span data-stu-id="ee348-266">String</span></span>  <br/> |<span data-ttu-id="ee348-267">application/json;odata = verbose</span><span class="sxs-lookup"><span data-stu-id="ee348-267">application/json; odata=verbose</span></span>  <br/> |
   
    <span data-ttu-id="ee348-268">![Accept ヘッダーの追加](media/2f2e2016-3c49-4cac-b1e7-f2b8118b840c.png "Accept ヘッダーの追加")</span><span class="sxs-lookup"><span data-stu-id="ee348-268">![Adding an Accept header](media/2f2e2016-3c49-4cac-b1e7-f2b8118b840c.png "Adding an Accept header")</span></span>
  
4. <span data-ttu-id="ee348-269">[ **HTTP Web サービスの呼び出し**] アクションを追加します。</span><span class="sxs-lookup"><span data-stu-id="ee348-269">Add the **Call HTTP Web Service** action.</span></span> <span data-ttu-id="ee348-270">**POST**を使用するように要求の種類を変更し、次の形式を使用して URL を設定します。</span><span class="sxs-lookup"><span data-stu-id="ee348-270">Change the request type to use **POST**, and set the URL using the following format:</span></span>
    
    `https://<site-url>/_api/ProjectServer/Projects('<guid>')/CreateProjectSite('New web name')`
    
    <span data-ttu-id="ee348-271">![createprojectsite エンドポイント URI を作成する](media/42a90a5e-8d1b-4667-a933-785175212847.png "createprojectsite エンドポイント URI を作成する")</span><span class="sxs-lookup"><span data-stu-id="ee348-271">![Building the CreateProjectSite endpoint URI](media/42a90a5e-8d1b-4667-a933-785175212847.png "Building the CreateProjectSite endpoint URI")</span></span>
  
    <span data-ttu-id="ee348-272">プロジェクトサイトの名前を文字列として**createprojectsite**メソッドに渡します。</span><span class="sxs-lookup"><span data-stu-id="ee348-272">Pass the name of the Project site to the **CreateProjectSite** method as a string.</span></span> <span data-ttu-id="ee348-273">プロジェクト名をサイト名として使用するには、空の文字列を渡します。</span><span class="sxs-lookup"><span data-stu-id="ee348-273">To use the project name as the site name, pass an empty string.</span></span> <span data-ttu-id="ee348-274">次に作成するプロジェクトサイトが機能するように、一意の名前を使用してください。</span><span class="sxs-lookup"><span data-stu-id="ee348-274">Be sure to use unique names so the next project site you create will work.</span></span> 
    
5. <span data-ttu-id="ee348-275">web サービス呼び出しのプロパティを編集して、作成した辞書に**RequestHeader**パラメーターをバインドします。</span><span class="sxs-lookup"><span data-stu-id="ee348-275">Edit the properties of the web service call to bind the **RequestHeader** parameter to the dictionary you created.</span></span> 
    
    <span data-ttu-id="ee348-276">![要求への辞書のバインド](media/61a5a0a8-405f-44eb-b5e7-80b11f7caec3.png "要求への辞書のバインド")</span><span class="sxs-lookup"><span data-stu-id="ee348-276">![Binding the dictionary to the request](media/61a5a0a8-405f-44eb-b5e7-80b11f7caec3.png "Binding the dictionary to the request")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ee348-277">関連項目</span><span class="sxs-lookup"><span data-stu-id="ee348-277">See also</span></span>

- [<span data-ttu-id="ee348-278">Project のプログラミング タスク</span><span class="sxs-lookup"><span data-stu-id="ee348-278">Project programming tasks</span></span>](project-programming-tasks.md)
- [<span data-ttu-id="ee348-279">Project 2013 のクライアント側オブジェクト モデル (CSOM)</span><span class="sxs-lookup"><span data-stu-id="ee348-279">Client-side object model (CSOM) for Project 2013</span></span>](client-side-object-model-csom-for-project-2013.md)
- [<span data-ttu-id="ee348-280">SharePoint 2013 のワークフロー</span><span class="sxs-lookup"><span data-stu-id="ee348-280">Workflows in SharePoint 2013</span></span>](https://msdn.microsoft.com/library/e0602371-ae22-44be-8a7e-9e47e9f046d6%28Office.15%29.aspx)
    

