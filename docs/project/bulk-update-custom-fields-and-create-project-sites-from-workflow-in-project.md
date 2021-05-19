---
title: ユーザー設定フィールドを一括更新し、プロジェクト サイトを作成Project Online
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 815131c6-190c-4f29-83bf-c853eee72821
description: Project Online を最大限に利用し、サービスの拡張性と柔軟性を向上させるために、Project Online アプリとワークフローで使用できる 2 つのメソッドをクライアント側オブジェクト モデルに追加しました。
ms.openlocfilehash: 4de42471cd8c2f12a982447ccffc27ec8104fa31
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355401"
---
# <a name="bulk-update-custom-fields-and-create-project-sites-from-a-workflow-in-project-online"></a><span data-ttu-id="db414-103">Project Online でユーザー設定フィールドを一括更新し、ワークフローからプロジェクト サイトを作成する</span><span class="sxs-lookup"><span data-stu-id="db414-103">Bulk update custom fields and create project sites from a workflow in Project Online</span></span>

<span data-ttu-id="db414-104">Project Online を最大限に利用し、サービスの拡張性と柔軟性を向上させるために、Project Online アプリとワークフローで使用できる 2 つのメソッドをクライアント側オブジェクト モデルに追加しました。</span><span class="sxs-lookup"><span data-stu-id="db414-104">To help customers get the most out of Project Online and improve our service extensibility and flexibility, we've added two methods to the client-side object model that you can use in Project Online apps and workflows.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="db414-105">**UpdateCustomFields**</span><span class="sxs-lookup"><span data-stu-id="db414-105">**UpdateCustomFields**</span></span> <br/> |<span data-ttu-id="db414-106">プロジェクトのユーザー設定フィールドを一括更新します。</span><span class="sxs-lookup"><span data-stu-id="db414-106">Bulk updates project custom fields.</span></span> <span data-ttu-id="db414-107">このProject Onlineします。</span><span class="sxs-lookup"><span data-stu-id="db414-107">For Project Online only.</span></span> <span data-ttu-id="db414-108">REST API でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="db414-108">Available only in the REST API.</span></span>  <br/> |
|<span data-ttu-id="db414-109">**CreateProjectSite**</span><span class="sxs-lookup"><span data-stu-id="db414-109">**CreateProjectSite**</span></span> <br/> | <span data-ttu-id="db414-110">サイトをProjectします。</span><span class="sxs-lookup"><span data-stu-id="db414-110">Creates a Project site.</span></span> <span data-ttu-id="db414-111">このProject Onlineします。</span><span class="sxs-lookup"><span data-stu-id="db414-111">For Project Online only.</span></span> <span data-ttu-id="db414-112">REST API、マネージ クライアント オブジェクト モデル、JavaScript クライアント オブジェクト モデルで使用できます。</span><span class="sxs-lookup"><span data-stu-id="db414-112">Available in the REST API, managed client object model, and JavaScript client object model.</span></span>  <br/> |
   
<span data-ttu-id="db414-113">これらのメソッドは、柔軟性の向上に加えて、ワークフローでプロジェクトを保存および発行する際のパフォーマンスも大幅に向上します。</span><span class="sxs-lookup"><span data-stu-id="db414-113">In addition to providing more flexibility, these methods also offer significant performance improvements when saving and publishing projects in a workflow.</span></span> <span data-ttu-id="db414-114">この記事では、REST API でメソッドを使用する方法について説明し、カスタム フィールドを一括更新するワークフローと、カスタム サイトを作成するワークフローを作成するProjectします。</span><span class="sxs-lookup"><span data-stu-id="db414-114">This article describes how to use the methods in the REST API and provides instructions for creating a workflow that bulk updates custom fields and a workflow that creates a Project site.</span></span>
  
> [!NOTE]
> <span data-ttu-id="db414-115">SharePoint 2013 ワークフローから REST API を呼び出す方法の詳細については[、「POST](https://mysharepointinsight.blogspot.com/2013/05/using-sharepoint-rest-services-from.mdl)メソッドを使用してワークフローから SharePoint REST サービスを使用する」および「SharePoint Designer ワークフローから[SharePoint 2013 Rest API](https://sergeluca.wordpress.com/2013/04/09/calling-the-sharepoint-2013-rest-api-from-a-sharepoint-designer-workflow/)を呼び出す」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="db414-115">To learn more about calling REST APIs from SharePoint 2013 workflows, see [Using SharePoint REST services from workflow with POST method](https://mysharepointinsight.blogspot.com/2013/05/using-sharepoint-rest-services-from.mdl) and [Calling the SharePoint 2013 Rest API from a SharePoint Designer Workflow](https://sergeluca.wordpress.com/2013/04/09/calling-the-sharepoint-2013-rest-api-from-a-sharepoint-designer-workflow/).</span></span> 
  
## <a name="bulk-update-project-custom-fields-from-a-workflow"></a><span data-ttu-id="db414-116">ワークフローからプロジェクトのユーザー設定フィールドを一括更新する</span><span class="sxs-lookup"><span data-stu-id="db414-116">Bulk update project custom fields from a workflow</span></span>
<span data-ttu-id="db414-117"><a name="BulkUpdateCustomFields"> </a></span><span class="sxs-lookup"><span data-stu-id="db414-117"><a name="BulkUpdateCustomFields"> </a></span></span>

<span data-ttu-id="db414-118">以前は、ワークフローで更新できるユーザー設定フィールドは一度に 1 つのみです。</span><span class="sxs-lookup"><span data-stu-id="db414-118">Previously, workflows could only update one custom field at a time.</span></span> <span data-ttu-id="db414-119">プロジェクトのユーザー設定フィールドを 1 度に 1 つ更新すると、ユーザーが詳細ページ間で切り替わると、エンド Project低下する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="db414-119">Updating project custom fields one at a time can result in a poor end-user experience when users transition between Project Detail Pages.</span></span> <span data-ttu-id="db414-120">各更新プログラムでは **、[Project フィールド** の設定] アクションを使用して個別のサーバー要求を要求し、高遅延で低帯域幅のネットワークで複数のユーザー設定フィールドを更新すると、簡単ではないオーバーヘッドが発生しました。</span><span class="sxs-lookup"><span data-stu-id="db414-120">Each update required a separate server request using the **Set Project Field** action, and updating multiple custom fields on a high-latency, low-bandwidth network resulted in a non-trivial overhead.</span></span> <span data-ttu-id="db414-121">この問題を解決するために、カスタム フィールドを一括更新できる **UpdateCustomFields** メソッドを REST API に追加しました。</span><span class="sxs-lookup"><span data-stu-id="db414-121">To resolve this issue, we added the **UpdateCustomFields** method to the REST API that lets you bulk update custom fields.</span></span> <span data-ttu-id="db414-122">**UpdateCustomFields** を使用するには、更新するユーザー設定フィールドの名前と値を含む辞書を渡します。</span><span class="sxs-lookup"><span data-stu-id="db414-122">To use **UpdateCustomFields**, you pass in a dictionary that contains the names and values of all the custom fields you want to update.</span></span>
  
<span data-ttu-id="db414-123">REST メソッドは、次のエンドポイントで確認できます。</span><span class="sxs-lookup"><span data-stu-id="db414-123">The REST method can be found at the following endpoint:</span></span>
  
`https://<site-url>/_api/ProjectServer/Projects('<guid>')/Draft/UpdateCustomFields()`
  
> [!NOTE]
> <span data-ttu-id="db414-124">例のプレースホルダーを、プロジェクト UID Project Web App (PWA) サイトの URL に `<site-url>` `<guid>` 置き換えてください。</span><span class="sxs-lookup"><span data-stu-id="db414-124">Replace the  `<site-url>` placeholder in the examples with the URL of your Project Web App (PWA) site and the  `<guid>` placeholder with your project UID.</span></span> 
  
<span data-ttu-id="db414-125">このセクションでは、プロジェクトのユーザー設定フィールドを一括更新するワークフローを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="db414-125">This section describes how to create a workflow that bulk updates custom fields for a project.</span></span> <span data-ttu-id="db414-126">ワークフローは、次の高レベルの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="db414-126">The workflow follows these high-level steps:</span></span>
  
- <span data-ttu-id="db414-127">更新するプロジェクトがチェックインされるのを待つ</span><span class="sxs-lookup"><span data-stu-id="db414-127">Wait for the project that you want to update to get checked in</span></span>
    
- <span data-ttu-id="db414-128">プロジェクトのすべてのユーザー設定フィールド更新を定義するデータ セットを作成する</span><span class="sxs-lookup"><span data-stu-id="db414-128">Build a data set that defines all your custom field updates for the project</span></span>
    
- <span data-ttu-id="db414-129">プロジェクトをチェックアウトする</span><span class="sxs-lookup"><span data-stu-id="db414-129">Check out the project</span></span>
    
- <span data-ttu-id="db414-130">**UpdateCustomFields を呼び** 出して、ユーザー設定フィールドの更新プログラムをプロジェクトに適用する</span><span class="sxs-lookup"><span data-stu-id="db414-130">Call **UpdateCustomFields** to apply the custom field updates to the project</span></span> 
    
- <span data-ttu-id="db414-131">関連情報をワークフロー履歴リストに記録する (必要な場合)</span><span class="sxs-lookup"><span data-stu-id="db414-131">Log relevant information to the workflow history list (if required)</span></span>
    
- <span data-ttu-id="db414-132">プロジェクトを発行する</span><span class="sxs-lookup"><span data-stu-id="db414-132">Publish the project</span></span>
    
- <span data-ttu-id="db414-133">プロジェクトをチェックインする</span><span class="sxs-lookup"><span data-stu-id="db414-133">Check in the project</span></span>
    
<span data-ttu-id="db414-134">最終的なエンドツーエンドのワークフローは次のように表示されます。</span><span class="sxs-lookup"><span data-stu-id="db414-134">The final, end-to-end workflow looks like this:</span></span>
  
<span data-ttu-id="db414-135">![エンドツーエンド ワークフロー エンドツーエンド](media/8c0741f9-7f76-409d-8c00-e7a8c3ddb89f.png "ワークフロー")</span><span class="sxs-lookup"><span data-stu-id="db414-135">![End-to-end workflow](media/8c0741f9-7f76-409d-8c00-e7a8c3ddb89f.png "End-to-end workflow")</span></span>
  
### <a name="to-create-a-workflow-that-bulk-updates-custom-fields"></a><span data-ttu-id="db414-136">ユーザー設定フィールドを一括更新するワークフローを作成するには</span><span class="sxs-lookup"><span data-stu-id="db414-136">To create a workflow that bulk updates custom fields</span></span>

1. <span data-ttu-id="db414-137">オプション。</span><span class="sxs-lookup"><span data-stu-id="db414-137">Optional.</span></span> <span data-ttu-id="db414-138">プロジェクトの完全な URL を、ワークフロー全体で使用できる変数に格納します。</span><span class="sxs-lookup"><span data-stu-id="db414-138">Store the full URL of your project in a variable that you can use throughout the workflow.</span></span>
    
    <span data-ttu-id="db414-139">![プロジェクトの URL を変数に格納](media/a880c5c6-8e7a-44dd-87e9-7e532169d489.png "する プロジェクトの URL を変数に格納する")</span><span class="sxs-lookup"><span data-stu-id="db414-139">![Store the URL of the project in a variable](media/a880c5c6-8e7a-44dd-87e9-7e532169d489.png "Store the URL of the project in a variable")</span></span>
  
2. <span data-ttu-id="db414-140">[イベント **の待機Project]** アクションをワークフローに追加し、[プロジェクトがチェックイン **された場合] イベントを選択** します。</span><span class="sxs-lookup"><span data-stu-id="db414-140">Add the **Wait for Project Event** action to the workflow and choose the **When a project is checked in** event.</span></span> 
    
    <span data-ttu-id="db414-141">![[プロジェクトがチェックインされる]のを待つ] でプロジェクト(media/699aa9c7-b3c9-426e-a775-96993a13559c.png "がチェックインされるのを待つ")</span><span class="sxs-lookup"><span data-stu-id="db414-141">![Wait for the project to be checked in](media/699aa9c7-b3c9-426e-a775-96993a13559c.png "Wait for the project to be checked in")</span></span>
  
3. <span data-ttu-id="db414-142">[辞書の **作成] アクションを** 使用して **requestHeader ディクショナリを作成** します。</span><span class="sxs-lookup"><span data-stu-id="db414-142">Create a **requestHeader** dictionary using the **Build dictionary** action.</span></span> <span data-ttu-id="db414-143">このワークフローのすべての Web サービス呼び出しに同じ要求ヘッダーを使用します。</span><span class="sxs-lookup"><span data-stu-id="db414-143">You'll use the same request header for all the web service calls in this workflow.</span></span> 
    
    <span data-ttu-id="db414-144">![requestHeader ディクショナリのビルド](media/83b0aa10-9ab7-43dd-800d-a738bb815876.png "requestHeader ディクショナリの作成")</span><span class="sxs-lookup"><span data-stu-id="db414-144">![Build the requestHeader dictionary](media/83b0aa10-9ab7-43dd-800d-a738bb815876.png "Build the requestHeader dictionary")</span></span>
  
4. <span data-ttu-id="db414-145">辞書に次の 2 つの項目を追加します。</span><span class="sxs-lookup"><span data-stu-id="db414-145">Add the following two items to the dictionary.</span></span>
    
    |<span data-ttu-id="db414-146">名前</span><span class="sxs-lookup"><span data-stu-id="db414-146">Name</span></span>|<span data-ttu-id="db414-147">型</span><span class="sxs-lookup"><span data-stu-id="db414-147">Type</span></span>|<span data-ttu-id="db414-148">値</span><span class="sxs-lookup"><span data-stu-id="db414-148">Value</span></span>|
    |:-----|:-----|:-----|
    |<span data-ttu-id="db414-149">Accept</span><span class="sxs-lookup"><span data-stu-id="db414-149">Accept</span></span>  <br/> |<span data-ttu-id="db414-150">String</span><span class="sxs-lookup"><span data-stu-id="db414-150">String</span></span>  <br/> |<span data-ttu-id="db414-151">application/json;odata=verbose</span><span class="sxs-lookup"><span data-stu-id="db414-151">application/json; odata=verbose</span></span>  <br/> |
    |<span data-ttu-id="db414-152">Content-Type</span><span class="sxs-lookup"><span data-stu-id="db414-152">Content-Type</span></span>  <br/> |<span data-ttu-id="db414-153">文字列</span><span class="sxs-lookup"><span data-stu-id="db414-153">String</span></span>  <br/> |<span data-ttu-id="db414-154">application/json;odata=verbose</span><span class="sxs-lookup"><span data-stu-id="db414-154">application/json; odata=verbose</span></span>  <br/> |
   
    <span data-ttu-id="db414-155">![Accept ヘッダーの追加](media/2f2e2016-3c49-4cac-b1e7-f2b8118b840c.png "Accept ヘッダーの追加")</span><span class="sxs-lookup"><span data-stu-id="db414-155">![Adding an Accept header](media/2f2e2016-3c49-4cac-b1e7-f2b8118b840c.png "Adding an Accept header")</span></span>
  
5. <span data-ttu-id="db414-156">[辞書の **作成]** アクションを使用して **requestBody ディクショナリを作成** します。</span><span class="sxs-lookup"><span data-stu-id="db414-156">Create a **requestBody** dictionary using the **Build dictionary** action.</span></span> <span data-ttu-id="db414-157">この辞書には、適用するフィールド更新プログラムすべてが格納されます。</span><span class="sxs-lookup"><span data-stu-id="db414-157">This dictionary stores all the field updates that you want to apply.</span></span> 
    
    <span data-ttu-id="db414-158">各ユーザー設定フィールドの更新には、フィールドの (1) メタデータ型、(2) キー、(3) 値、および (4) 値の種類の 4 つの行が必要です。</span><span class="sxs-lookup"><span data-stu-id="db414-158">Each custom field update requires four rows: the field's (1) metadata type, (2) key, (3) value, and (4) value type.</span></span>
    
    - <span data-ttu-id="db414-159">**__metadata/型** フィールドのメタデータ型。</span><span class="sxs-lookup"><span data-stu-id="db414-159">**__metadata/type** The field's metadata type.</span></span> <span data-ttu-id="db414-160">このレコードは常に同じであり、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="db414-160">This record is always the same and uses the following values:</span></span> 
    
       - <span data-ttu-id="db414-161">名前: customFieldDictionary(i)/__metadata/type (ここで **、i** は辞書内の各ユーザー設定フィールドのインデックスで、0 から始まる)</span><span class="sxs-lookup"><span data-stu-id="db414-161">Name: customFieldDictionary(i)/__metadata/type (where **i** is the index of each custom field in the dictionary, starting with 0)</span></span> 
            
       - <span data-ttu-id="db414-162">型:String</span><span class="sxs-lookup"><span data-stu-id="db414-162">Type: String</span></span>
            
       - <span data-ttu-id="db414-163">値: SP。KeyValue</span><span class="sxs-lookup"><span data-stu-id="db414-163">Value: SP.KeyValue</span></span>
    
       <span data-ttu-id="db414-164">![ユーザー設定フィールド更新の定義](media/a4423493-6603-42ee-ae50-1ef74c5c59bd.png "ユーザー設定フィールド更新の定義")</span><span class="sxs-lookup"><span data-stu-id="db414-164">![Defining a custom field update](media/a4423493-6603-42ee-ae50-1ef74c5c59bd.png "Defining a custom field update")</span></span>
  
    - <span data-ttu-id="db414-165">**キー** ユーザー設定フィールドの内部名 (*形式:* Custom_ce23fbf43fa0e411941000155d3c8201</span><span class="sxs-lookup"><span data-stu-id="db414-165">**Key** The internal name of the custom field, in the format: *Custom_ce23fbf43fa0e411941000155d3c8201*</span></span> 
    
       <span data-ttu-id="db414-166">カスタム フィールドの内部名を見つけるには、そのユーザー設定フィールドの **InternalName エンドポイントに移動** します。 `https://<site-url>/_api/ProjectServer/CustomFields('<guid>')/InternalName`</span><span class="sxs-lookup"><span data-stu-id="db414-166">You can find the internal name of a custom field by navigating to it's **InternalName** endpoint: `https://<site-url>/_api/ProjectServer/CustomFields('<guid>')/InternalName`</span></span>
    
       <span data-ttu-id="db414-167">ユーザー設定フィールドを手動で作成した場合、値はサイトごとに異なります。</span><span class="sxs-lookup"><span data-stu-id="db414-167">If you created your custom fields manually, the values will differ from site to site.</span></span> <span data-ttu-id="db414-168">複数のサイトでワークフローを再利用する場合は、ユーザー設定フィールドの ID が正しいか確認してください。</span><span class="sxs-lookup"><span data-stu-id="db414-168">If you plan to reuse the workflow across multiple sites, make sure the custom field IDs are correct.</span></span>
    
    - <span data-ttu-id="db414-169">**値** ユーザー設定フィールドに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="db414-169">**Value** The value to assign to the custom field.</span></span> <span data-ttu-id="db414-170">参照テーブルにリンクされているユーザー設定フィールドの場合は、実際の参照テーブル値ではなく、参照テーブル エントリの内部名を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="db414-170">For custom fields that are linked to lookup tables, you need to use the internal names of the lookup table entries instead of the actual lookup table values.</span></span> 
    
       <span data-ttu-id="db414-171">参照テーブル エントリの内部名は、次のエンドポイントで確認できます。 `https://<site-url>/_api/ProjectServer/CustomFields('<guid>')/LookupEntries('<guid>')/InternalName`</span><span class="sxs-lookup"><span data-stu-id="db414-171">You can find the internal name of the lookup table entry at the following endpoint: `https://<site-url>/_api/ProjectServer/CustomFields('<guid>')/LookupEntries('<guid>')/InternalName`</span></span>
    
       <span data-ttu-id="db414-172">複数の値を受け入れるルックアップ テーブルのユーザー設定フィールドが設定されている場合は、値を連結するために使用します (以下の辞書例に  `;#` 示すように)。</span><span class="sxs-lookup"><span data-stu-id="db414-172">If you have a lookup table custom field set up to accept multiple values, use  `;#` to concatenate values (as shown in the example dictionary below).</span></span> 
    
    - <span data-ttu-id="db414-173">**ValueType** 更新するユーザー設定フィールドの種類。</span><span class="sxs-lookup"><span data-stu-id="db414-173">**ValueType** The type of the custom field you are updating.</span></span> 
    
       - <span data-ttu-id="db414-174">テキスト、期間、フラグ、および LookupTable フィールドの場合は、Edm.String を使用します。</span><span class="sxs-lookup"><span data-stu-id="db414-174">For Text, Duration, Flag, and LookupTable fields, use Edm.String</span></span>
    
       - <span data-ttu-id="db414-175">[数値] フィールドには、Edm.Int32、Edm.Double、または他の OData で受け入れられる数値の種類を使用します。</span><span class="sxs-lookup"><span data-stu-id="db414-175">For Number fields, use Edm.Int32, Edm.Double, or any other OData-accepted number type</span></span>
    
       - <span data-ttu-id="db414-176">[日付] フィールドには、Edm.DateTime を使用します。</span><span class="sxs-lookup"><span data-stu-id="db414-176">For Date fields, use Edm.DateTime</span></span>
    
       <span data-ttu-id="db414-177">次の辞書の例では、3 つのユーザー設定フィールドの更新プログラムを定義します。</span><span class="sxs-lookup"><span data-stu-id="db414-177">The example dictionary below defines updates for three custom fields.</span></span> <span data-ttu-id="db414-178">1 つ目は複数値参照テーブルのユーザー設定フィールド、2 つ目は数値フィールド、3 つ目は日付フィールド用です。</span><span class="sxs-lookup"><span data-stu-id="db414-178">The first is for a multiple value lookup table custom field, the second is for a number field, and the third is for a date field.</span></span> <span data-ttu-id="db414-179">**customFieldDictionary インデックスの** 増分方法に注意してください。</span><span class="sxs-lookup"><span data-stu-id="db414-179">Note how the **customFieldDictionary** index increments.</span></span> 
    
       > [!NOTE]
       > <span data-ttu-id="db414-180">これらの値は、説明のみを目的とします。</span><span class="sxs-lookup"><span data-stu-id="db414-180">These values are for illustration purposes only.</span></span> <span data-ttu-id="db414-181">使用するキーと値の組み合PWAします。</span><span class="sxs-lookup"><span data-stu-id="db414-181">The key-value pairs you'll use depend on your PWA data.</span></span> 
  
       |<span data-ttu-id="db414-182">名前</span><span class="sxs-lookup"><span data-stu-id="db414-182">Name</span></span>|<span data-ttu-id="db414-183">型</span><span class="sxs-lookup"><span data-stu-id="db414-183">Type</span></span>|<span data-ttu-id="db414-184">値</span><span class="sxs-lookup"><span data-stu-id="db414-184">Value</span></span>|
       |:-----|:-----|:-----|
       |<span data-ttu-id="db414-185">customFieldDictionary(0)/__metadata/type</span><span class="sxs-lookup"><span data-stu-id="db414-185">customFieldDictionary(0)/__metadata/type</span></span>  <br/> |<span data-ttu-id="db414-186">String</span><span class="sxs-lookup"><span data-stu-id="db414-186">String</span></span>  <br/> |<span data-ttu-id="db414-187">SP。KeyValue</span><span class="sxs-lookup"><span data-stu-id="db414-187">SP.KeyValue</span></span>  <br/> |
       |<span data-ttu-id="db414-188">customFieldDictionary(0)/Key</span><span class="sxs-lookup"><span data-stu-id="db414-188">customFieldDictionary(0)/Key</span></span>  <br/> |<span data-ttu-id="db414-189">String</span><span class="sxs-lookup"><span data-stu-id="db414-189">String</span></span>  <br/> |<span data-ttu-id="db414-190">カスタム \_ ce23fbf43fa0e411941000155d3c8201</span><span class="sxs-lookup"><span data-stu-id="db414-190">Custom\_ce23fbf43fa0e411941000155d3c8201</span></span>  <br/> |
       |<span data-ttu-id="db414-191">customFieldDictionary(0)/Value</span><span class="sxs-lookup"><span data-stu-id="db414-191">customFieldDictionary(0)/Value</span></span>  <br/> |<span data-ttu-id="db414-192">String</span><span class="sxs-lookup"><span data-stu-id="db414-192">String</span></span>  <br/> |<span data-ttu-id="db414-193">エントリ \_ b9a2fd69279de411940f00155d3c8201;#Entry \_ baa2fd69279de411940f00155d3c8201</span><span class="sxs-lookup"><span data-stu-id="db414-193">Entry\_b9a2fd69279de411940f00155d3c8201;#Entry\_baa2fd69279de411940f00155d3c8201</span></span>  <br/> |
       |<span data-ttu-id="db414-194">customFieldDictionary(0)/ValueType</span><span class="sxs-lookup"><span data-stu-id="db414-194">customFieldDictionary(0)/ValueType</span></span>  <br/> |<span data-ttu-id="db414-195">String</span><span class="sxs-lookup"><span data-stu-id="db414-195">String</span></span>  <br/> |<span data-ttu-id="db414-196">Edm.String</span><span class="sxs-lookup"><span data-stu-id="db414-196">Edm.String</span></span>  <br/> |
       |<span data-ttu-id="db414-197">customFieldDictionary(1)/__metadata/type</span><span class="sxs-lookup"><span data-stu-id="db414-197">customFieldDictionary(1)/__metadata/type</span></span>  <br/> |<span data-ttu-id="db414-198">String</span><span class="sxs-lookup"><span data-stu-id="db414-198">String</span></span>  <br/> |<span data-ttu-id="db414-199">SP。KeyValue</span><span class="sxs-lookup"><span data-stu-id="db414-199">SP.KeyValue</span></span>  <br/> |
       |<span data-ttu-id="db414-200">customFieldDictionary(1)/Key</span><span class="sxs-lookup"><span data-stu-id="db414-200">customFieldDictionary(1)/Key</span></span>  <br/> |<span data-ttu-id="db414-201">String</span><span class="sxs-lookup"><span data-stu-id="db414-201">String</span></span>  <br/> |<span data-ttu-id="db414-202">Custom_c7f114c97098e411940f00155d3c8201</span><span class="sxs-lookup"><span data-stu-id="db414-202">Custom_c7f114c97098e411940f00155d3c8201</span></span>  <br/> |
       |<span data-ttu-id="db414-203">customFieldDictionary(1)/Value</span><span class="sxs-lookup"><span data-stu-id="db414-203">customFieldDictionary(1)/Value</span></span>  <br/> |<span data-ttu-id="db414-204">String</span><span class="sxs-lookup"><span data-stu-id="db414-204">String</span></span>  <br/> |<span data-ttu-id="db414-205">90.5</span><span class="sxs-lookup"><span data-stu-id="db414-205">90.5</span></span>  <br/> |
       |<span data-ttu-id="db414-206">customFieldDictionary(1)/ValueType</span><span class="sxs-lookup"><span data-stu-id="db414-206">customFieldDictionary(1)/ValueType</span></span>  <br/> |<span data-ttu-id="db414-207">String</span><span class="sxs-lookup"><span data-stu-id="db414-207">String</span></span>  <br/> |<span data-ttu-id="db414-208">Edm.Double</span><span class="sxs-lookup"><span data-stu-id="db414-208">Edm.Double</span></span>  <br/> |
       |<span data-ttu-id="db414-209">customFieldDictionary(2)/__metadata/type</span><span class="sxs-lookup"><span data-stu-id="db414-209">customFieldDictionary(2)/__metadata/type</span></span>  <br/> |<span data-ttu-id="db414-210">String</span><span class="sxs-lookup"><span data-stu-id="db414-210">String</span></span>  <br/> |<span data-ttu-id="db414-211">SP。KeyValue</span><span class="sxs-lookup"><span data-stu-id="db414-211">SP.KeyValue</span></span>  <br/> |
       |<span data-ttu-id="db414-212">customFieldDictionary(2)/Key</span><span class="sxs-lookup"><span data-stu-id="db414-212">customFieldDictionary(2)/Key</span></span>  <br/> |<span data-ttu-id="db414-213">String</span><span class="sxs-lookup"><span data-stu-id="db414-213">String</span></span>  <br/> |<span data-ttu-id="db414-214">Custom_c6fb67e0b9a1e411941000155d3c8201</span><span class="sxs-lookup"><span data-stu-id="db414-214">Custom_c6fb67e0b9a1e411941000155d3c8201</span></span>  <br/> |
       |<span data-ttu-id="db414-215">customFieldDictionary(2)/Value</span><span class="sxs-lookup"><span data-stu-id="db414-215">customFieldDictionary(2)/Value</span></span>  <br/> |<span data-ttu-id="db414-216">String</span><span class="sxs-lookup"><span data-stu-id="db414-216">String</span></span>  <br/> |<span data-ttu-id="db414-217">2015-04-01T00:00:00</span><span class="sxs-lookup"><span data-stu-id="db414-217">2015-04-01T00:00:00.0000000</span></span>  <br/> |
       |<span data-ttu-id="db414-218">customFieldDictionary(2)/ValueType</span><span class="sxs-lookup"><span data-stu-id="db414-218">customFieldDictionary(2)/ValueType</span></span>  <br/> |<span data-ttu-id="db414-219">String</span><span class="sxs-lookup"><span data-stu-id="db414-219">String</span></span>  <br/> |<span data-ttu-id="db414-220">Edm.DateTime</span><span class="sxs-lookup"><span data-stu-id="db414-220">Edm.DateTime</span></span>  <br/> |
   
       <span data-ttu-id="db414-221">![ユーザー設定フィールドを定義する辞書は、ユーザー設定](media/41a1f18f-a6b2-40ff-904b-437baf962621.png "フィールドの更新を定義する辞書を更新します。")</span><span class="sxs-lookup"><span data-stu-id="db414-221">![Dictionary that defines custom field updates](media/41a1f18f-a6b2-40ff-904b-437baf962621.png "Dictionary that defines custom field updates")</span></span>
  
6. <span data-ttu-id="db414-222">[HTTP **Web サービスの呼び出し] アクションを** 追加して、プロジェクトをチェックアウトします。</span><span class="sxs-lookup"><span data-stu-id="db414-222">Add a **Call HTTP Web Service** action to check the project out.</span></span> 
    
    <span data-ttu-id="db414-223">![Checkout メソッドを呼び出す](media/8ce56014-0317-419b-afa7-229d05c86885.png "Checkout メソッドを呼び出す")</span><span class="sxs-lookup"><span data-stu-id="db414-223">![Call the Checkout method](media/8ce56014-0317-419b-afa7-229d05c86885.png "Call the Checkout method")</span></span>
  
7. <span data-ttu-id="db414-224">Web サービス呼び出しのプロパティを編集して、要求ヘッダーを指定します。</span><span class="sxs-lookup"><span data-stu-id="db414-224">Edit the properties of the web service call to specify the request header.</span></span> <span data-ttu-id="db414-225">[プロパティ] **ダイアログ ボックスを** 開く場合は、アクションを右クリックし、[プロパティ] を **選択します**。</span><span class="sxs-lookup"><span data-stu-id="db414-225">To open the **Properties** dialog box, right-click the action and choose **Properties**.</span></span>
    
    <span data-ttu-id="db414-226">![Web サービス呼び出しプロパティで要求ヘッダーを指定]する Web サービス呼び出しプロパティ(media/d81e92b1-43df-42ad-9cd0-a693f93b164e.png "で要求ヘッダーを指定する")</span><span class="sxs-lookup"><span data-stu-id="db414-226">![Specify the request header in web service call properties](media/d81e92b1-43df-42ad-9cd0-a693f93b164e.png "Specify the request header in web service call properties")</span></span>
  
8. <span data-ttu-id="db414-227">**UpdateCustomFields** メソッドを呼び出す HTTP Web サービスの呼び出しアクションを追加します。 </span><span class="sxs-lookup"><span data-stu-id="db414-227">Add a **Call HTTP Web Service** action to call the **UpdateCustomFields** method.</span></span> 
    
    <span data-ttu-id="db414-228">![[HTTP Web サービスの呼び出し] アクションを作成](media/9a73a201-c035-41b4-8798-506ac48b90f8.png "する HTTP Web サービスの呼")び出しアクションを作成する</span><span class="sxs-lookup"><span data-stu-id="db414-228">![Create a Call HTTP Web Service action](media/9a73a201-c035-41b4-8798-506ac48b90f8.png "Create a Call HTTP Web Service action")</span></span>
  
    <span data-ttu-id="db414-229">Web サービス  `/Draft/` URL のセグメントに注意してください。</span><span class="sxs-lookup"><span data-stu-id="db414-229">Note the  `/Draft/` segment in the web service URL.</span></span> <span data-ttu-id="db414-230">完全な URL は次のように表示されます。 `https://<site-url>/_api/ProjectServer/Projects('<guid>')/Draft/UpdateCustomFields()`</span><span class="sxs-lookup"><span data-stu-id="db414-230">The full URL should look like this: `https://<site-url>/_api/ProjectServer/Projects('<guid>')/Draft/UpdateCustomFields()`</span></span>
    
    <span data-ttu-id="db414-231">![UpdateCustomFields メソッドを呼び出す](media/03b323f1-8e99-4b18-be18-be505d7cec7e.png "UpdateCustomFields メソッドを呼び出す")</span><span class="sxs-lookup"><span data-stu-id="db414-231">![Call the UpdateCustomFields method](media/03b323f1-8e99-4b18-be18-be505d7cec7e.png "Call the UpdateCustomFields method")</span></span>
  
9. <span data-ttu-id="db414-232">Web サービス呼び出しのプロパティを編集して **、RequestHeader** パラメーターと **RequestContent** パラメーターを作成した辞書にバインドします。</span><span class="sxs-lookup"><span data-stu-id="db414-232">Edit the properties of the web service call to bind the **RequestHeader** and **RequestContent** parameters to the dictionaries you created.</span></span> <span data-ttu-id="db414-233">ResponseContent を格納する新しい **変数を作成できます**。</span><span class="sxs-lookup"><span data-stu-id="db414-233">You can also create a new variable to store the **ResponseContent**.</span></span>
    
    <span data-ttu-id="db414-234">![辞書を要求ヘッダーとコンテンツに]バインドする 辞書を要求(media/f96bec92-138e-4eab-b1e7-1ab83d0428a5.png "ヘッダーとコンテンツにバインドする")</span><span class="sxs-lookup"><span data-stu-id="db414-234">![Bind the dictionaries to the request header and content](media/f96bec92-138e-4eab-b1e7-1ab83d0428a5.png "Bind the dictionaries to the request header and content")</span></span>
  
10. <span data-ttu-id="db414-235">オプション。</span><span class="sxs-lookup"><span data-stu-id="db414-235">Optional.</span></span> <span data-ttu-id="db414-236">応答辞書から読み取り、キュー ジョブの状態を確認し、ワークフロー履歴リストに情報を記録します。</span><span class="sxs-lookup"><span data-stu-id="db414-236">Read from the response dictionary to check the state of the queue job and log the information in the workflow history list.</span></span>
    
    <span data-ttu-id="db414-237">![ログの設定](media/7d2f4936-61d7-4906-83e8-7478a5935af5.png "ログの設定")</span><span class="sxs-lookup"><span data-stu-id="db414-237">![Setting up logging](media/7d2f4936-61d7-4906-83e8-7478a5935af5.png "Setting up logging")</span></span>
  
11. <span data-ttu-id="db414-238">プロジェクトを発行する発行エンドポイントに Web サービス呼 **び** 出しを追加します。</span><span class="sxs-lookup"><span data-stu-id="db414-238">Add a web service call to the **Publish** endpoint to publish the project.</span></span> <span data-ttu-id="db414-239">常に同じ要求ヘッダーを使用します。</span><span class="sxs-lookup"><span data-stu-id="db414-239">Always use the same request header.</span></span> 
    
    <span data-ttu-id="db414-240">![Publish メソッドを呼び出す](media/3b661091-ffae-4d7e-a0bb-5b96a6292731.png "Publish メソッドを呼び出す")</span><span class="sxs-lookup"><span data-stu-id="db414-240">![Call the Publish method](media/3b661091-ffae-4d7e-a0bb-5b96a6292731.png "Call the Publish method")</span></span>
  
    <span data-ttu-id="db414-241">![発行 Web サービス呼び出しのプロパティ](media/6a80a5d3-7e29-4398-993c-f78b3faca8b1.png "Web サービスの発行呼び出しのプロパティ")</span><span class="sxs-lookup"><span data-stu-id="db414-241">![Properties for the Publish web service call](media/6a80a5d3-7e29-4398-993c-f78b3faca8b1.png "Properties for the Publish web service call")</span></span>
  
12. <span data-ttu-id="db414-242">Checkin エンドポイントに最終的な Web サービス呼 **び出しを追加** して、プロジェクトをチェックインします。</span><span class="sxs-lookup"><span data-stu-id="db414-242">Add a final web service call to the **Checkin** endpoint to check the project in.</span></span> 
    
    <span data-ttu-id="db414-243">![Checkin メソッドを呼び出す](media/430510cb-0774-4911-af7f-b565b83eba0e.png "Checkin メソッドを呼び出す")</span><span class="sxs-lookup"><span data-stu-id="db414-243">![Call the Checkin method](media/430510cb-0774-4911-af7f-b565b83eba0e.png "Call the Checkin method")</span></span>
  
    <span data-ttu-id="db414-244">![Checkin Web サービス呼び出し](media/485f48d6-bbb8-4568-9dc3-aae3218f6bd1.png "のプロパティ Checkin Web サービス呼び出しのプロパティ")</span><span class="sxs-lookup"><span data-stu-id="db414-244">![Properties for the Checkin web service call](media/485f48d6-bbb8-4568-9dc3-aae3218f6bd1.png "Properties for the Checkin web service call")</span></span>

<span data-ttu-id="db414-245"><a name="CreateProjectSite"> </a></span><span class="sxs-lookup"><span data-stu-id="db414-245"><a name="CreateProjectSite"> </a></span></span>

## <a name="create-a-project-site-from-a-workflow"></a><span data-ttu-id="db414-246">ワークフローからProjectサイトを作成する</span><span class="sxs-lookup"><span data-stu-id="db414-246">Create a Project site from a workflow</span></span>

<span data-ttu-id="db414-247">すべてのプロジェクトには、チーム メンバーが共同作業、ドキュメントSharePoint問題の発生など、独自の専用のサイトを用意できます。</span><span class="sxs-lookup"><span data-stu-id="db414-247">Every project can have its own dedicated SharePoint sites where team members can collaborate, share documents, raise issues, and so on.</span></span> <span data-ttu-id="db414-248">以前は、Project Professional のプロジェクト マネージャーまたは PWA の設定で管理者が最初に発行または手動でサイトを自動的に作成するか、無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="db414-248">Previously, sites could only be created automatically on first publish or manually by the project manager in Project Professional or by the administrator in PWA settings, or they could be disabled.</span></span>
  
<span data-ttu-id="db414-249">プロジェクト サイトを作成する場合を選択できるよう **、CreateProjectSite** メソッドが追加されました。</span><span class="sxs-lookup"><span data-stu-id="db414-249">We've added the **CreateProjectSite** method so you can choose when to create project sites.</span></span> <span data-ttu-id="db414-250">これは、プロジェクト提案が最初の発行ではなく、事前に定義されたワークフローの特定のステージに達したときにサイトを自動的に作成する組織にとって特に便利です。</span><span class="sxs-lookup"><span data-stu-id="db414-250">This is particularly useful for organizations who want to create their sites automatically when a project proposal reaches a specific stage in a pre-defined workflow, rather than on first publish.</span></span> <span data-ttu-id="db414-251">プロジェクト サイトの作成を延期すると、プロジェクトの作成のパフォーマンスが大幅に向上します。</span><span class="sxs-lookup"><span data-stu-id="db414-251">Postponing project site creation significantly improves the performance of creating a project.</span></span> 
  
<span data-ttu-id="db414-252">**前提条件:\*\*\*\*CreateProjectSite** を使用する前に **、PWA 設定**> \*\* Connected SharePoint Sites \*\* > 設定 でプロジェクト サイトの作成に対して [ユーザーに選択を許可する] 設定を設定する **必要があります**。</span><span class="sxs-lookup"><span data-stu-id="db414-252">**Prerequisite:** Before you can use **CreateProjectSite**, the **Allow users to choose** setting must be set for project site creation in **PWA Settings** > \*\* Connected SharePoint Sites \*\* > **Settings**.</span></span>
  
<span data-ttu-id="db414-253">![[ユーザーの選択を許可する]]PWA設定(media/6c6c8175-eb10-431d-8056-cea55718fdb4.png "設定 設定")でユーザーが選択PWAする</span><span class="sxs-lookup"><span data-stu-id="db414-253">![Setting "Allow users to choose" in PWA settings](media/6c6c8175-eb10-431d-8056-cea55718fdb4.png "Setting Allow users to choose in PWA settings")</span></span>
  
### <a name="to-create-a-workflow-that-creates-a-project-site"></a><span data-ttu-id="db414-254">サイトを作成するワークフローをProjectするには</span><span class="sxs-lookup"><span data-stu-id="db414-254">To create a workflow that creates a Project site</span></span>

1. <span data-ttu-id="db414-255">既存のワークフローを作成または編集し、サイトを作成する手順をProjectします。</span><span class="sxs-lookup"><span data-stu-id="db414-255">Create or edit an existing workflow and select the step where you want to create your Project sites.</span></span>
    
2. <span data-ttu-id="db414-256">[辞書の **作成] アクションを** 使用して **requestHeader ディクショナリを作成** します。</span><span class="sxs-lookup"><span data-stu-id="db414-256">Create a **requestHeader** dictionary using the **Build dictionary** action.</span></span> 
    
    <span data-ttu-id="db414-257">![requestHeader ディクショナリのビルド](media/83b0aa10-9ab7-43dd-800d-a738bb815876.png "requestHeader ディクショナリの作成")</span><span class="sxs-lookup"><span data-stu-id="db414-257">![Build the requestHeader dictionary](media/83b0aa10-9ab7-43dd-800d-a738bb815876.png "Build the requestHeader dictionary")</span></span>
  
3. <span data-ttu-id="db414-258">辞書に次の 2 つの項目を追加します。</span><span class="sxs-lookup"><span data-stu-id="db414-258">Add the following two items to the dictionary.</span></span>
    
    |<span data-ttu-id="db414-259">名前</span><span class="sxs-lookup"><span data-stu-id="db414-259">Name</span></span>|<span data-ttu-id="db414-260">型</span><span class="sxs-lookup"><span data-stu-id="db414-260">Type</span></span>|<span data-ttu-id="db414-261">値</span><span class="sxs-lookup"><span data-stu-id="db414-261">Value</span></span>|
    |:-----|:-----|:-----|
    |<span data-ttu-id="db414-262">Accept</span><span class="sxs-lookup"><span data-stu-id="db414-262">Accept</span></span>  <br/> |<span data-ttu-id="db414-263">String</span><span class="sxs-lookup"><span data-stu-id="db414-263">String</span></span>  <br/> |<span data-ttu-id="db414-264">application/json;odata=verbose</span><span class="sxs-lookup"><span data-stu-id="db414-264">application/json; odata=verbose</span></span>  <br/> |
    |<span data-ttu-id="db414-265">Content-Type</span><span class="sxs-lookup"><span data-stu-id="db414-265">Content-Type</span></span>  <br/> |<span data-ttu-id="db414-266">文字列</span><span class="sxs-lookup"><span data-stu-id="db414-266">String</span></span>  <br/> |<span data-ttu-id="db414-267">application/json;odata=verbose</span><span class="sxs-lookup"><span data-stu-id="db414-267">application/json; odata=verbose</span></span>  <br/> |
   
    <span data-ttu-id="db414-268">![Accept ヘッダーの追加](media/2f2e2016-3c49-4cac-b1e7-f2b8118b840c.png "Accept ヘッダーの追加")</span><span class="sxs-lookup"><span data-stu-id="db414-268">![Adding an Accept header](media/2f2e2016-3c49-4cac-b1e7-f2b8118b840c.png "Adding an Accept header")</span></span>
  
4. <span data-ttu-id="db414-269">[HTTP **Web サービスの呼び出し] アクションを追加** します。</span><span class="sxs-lookup"><span data-stu-id="db414-269">Add the **Call HTTP Web Service** action.</span></span> <span data-ttu-id="db414-270">POST を使用する要求 **の種類を** 変更し、次の形式で URL を設定します。</span><span class="sxs-lookup"><span data-stu-id="db414-270">Change the request type to use **POST**, and set the URL using the following format:</span></span>
    
    `https://<site-url>/_api/ProjectServer/Projects('<guid>')/CreateProjectSite('New web name')`
    
    <span data-ttu-id="db414-271">![CreateProjectSite エンドポイント URI のビルド](media/42a90a5e-8d1b-4667-a933-785175212847.png "CreateProjectSite エンドポイント URI の作成")</span><span class="sxs-lookup"><span data-stu-id="db414-271">![Building the CreateProjectSite endpoint URI](media/42a90a5e-8d1b-4667-a933-785175212847.png "Building the CreateProjectSite endpoint URI")</span></span>
  
    <span data-ttu-id="db414-272">サイトの名前を文字列Project **CreateProjectSite** メソッドに渡します。</span><span class="sxs-lookup"><span data-stu-id="db414-272">Pass the name of the Project site to the **CreateProjectSite** method as a string.</span></span> <span data-ttu-id="db414-273">プロジェクト名をサイト名として使用するには、空の文字列を渡します。</span><span class="sxs-lookup"><span data-stu-id="db414-273">To use the project name as the site name, pass an empty string.</span></span> <span data-ttu-id="db414-274">作成する次のプロジェクト サイトが機能するには、必ず一意の名前を使用してください。</span><span class="sxs-lookup"><span data-stu-id="db414-274">Be sure to use unique names so the next project site you create will work.</span></span> 
    
5. <span data-ttu-id="db414-275">Web サービス呼び出しのプロパティを編集して **、RequestHeader** パラメーターを作成した辞書にバインドします。</span><span class="sxs-lookup"><span data-stu-id="db414-275">Edit the properties of the web service call to bind the **RequestHeader** parameter to the dictionary you created.</span></span> 
    
    <span data-ttu-id="db414-276">![ディクショナリを要求にバインド](media/61a5a0a8-405f-44eb-b5e7-80b11f7caec3.png "する ディクショナリを要求にバインドする")</span><span class="sxs-lookup"><span data-stu-id="db414-276">![Binding the dictionary to the request](media/61a5a0a8-405f-44eb-b5e7-80b11f7caec3.png "Binding the dictionary to the request")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="db414-277">関連項目</span><span class="sxs-lookup"><span data-stu-id="db414-277">See also</span></span>

- [<span data-ttu-id="db414-278">Project のプログラミング タスク</span><span class="sxs-lookup"><span data-stu-id="db414-278">Project programming tasks</span></span>](project-programming-tasks.md)
- [<span data-ttu-id="db414-279">Project 2013 のクライアント側オブジェクト モデル (CSOM)</span><span class="sxs-lookup"><span data-stu-id="db414-279">Client-side object model (CSOM) for Project 2013</span></span>](client-side-object-model-csom-for-project-2013.md)
- [<span data-ttu-id="db414-280">SharePoint 2013 のワークフロー</span><span class="sxs-lookup"><span data-stu-id="db414-280">Workflows in SharePoint 2013</span></span>](https://msdn.microsoft.com/library/e0602371-ae22-44be-8a7e-9e47e9f046d6%28Office.15%29.aspx)
    

