---
title: ユーザー設定フィールドの更新プログラムを一括して、オンラインのプロジェクトにプロジェクト サイトを作成
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 815131c6-190c-4f29-83bf-c853eee72821
description: お客様のオンライン プロジェクトを最大限に活用し、当社のサービスの拡張性と柔軟性を向上させるために、2 つの方法オンライン プロジェクトのアプリケーションとワークフローで使用できるクライアント側オブジェクト モデルに追加しました。
ms.openlocfilehash: 4f8fee5de5efb69f410b78e9ce93b9dc9bb133f3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804565"
---
# <a name="bulk-update-custom-fields-and-create-project-sites-from-a-workflow-in-project-online"></a><span data-ttu-id="704c1-103">Project Online でユーザー設定フィールドを一括更新し、ワークフローからプロジェクト サイトを作成する</span><span class="sxs-lookup"><span data-stu-id="704c1-103">Bulk update custom fields and create project sites from a workflow in Project Online</span></span>

<span data-ttu-id="704c1-104">お客様のオンライン プロジェクトを最大限に活用し、当社のサービスの拡張性と柔軟性を向上させるために、2 つの方法オンライン プロジェクトのアプリケーションとワークフローで使用できるクライアント側オブジェクト モデルに追加しました。</span><span class="sxs-lookup"><span data-stu-id="704c1-104">To help customers get the most out of Project Online and improve our service extensibility and flexibility, we've added two methods to the client-side object model that you can use in Project Online apps and workflows.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="704c1-105">**UpdateCustomFields**</span><span class="sxs-lookup"><span data-stu-id="704c1-105">**UpdateCustomFields**</span></span> <br/> |<span data-ttu-id="704c1-106">一括では、プロジェクトのユーザー設定フィールドを更新します。</span><span class="sxs-lookup"><span data-stu-id="704c1-106">Bulk updates project custom fields.</span></span> <span data-ttu-id="704c1-107">オンライン プロジェクトのみです。</span><span class="sxs-lookup"><span data-stu-id="704c1-107">For Project Online only.</span></span> <span data-ttu-id="704c1-108">REST API でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="704c1-108">Available only in the REST API.</span></span>  <br/> |
|<span data-ttu-id="704c1-109">**CreateProjectSite**</span><span class="sxs-lookup"><span data-stu-id="704c1-109">**CreateProjectSite**</span></span> <br/> | <span data-ttu-id="704c1-110">プロジェクト サイトを作成します。</span><span class="sxs-lookup"><span data-stu-id="704c1-110">Creates a Project site.</span></span> <span data-ttu-id="704c1-111">オンライン プロジェクトのみです。</span><span class="sxs-lookup"><span data-stu-id="704c1-111">For Project Online only.</span></span> <span data-ttu-id="704c1-112">REST API、マネージ クライアント オブジェクト モデル、および JavaScript クライアント オブジェクト モデルで使用できます。</span><span class="sxs-lookup"><span data-stu-id="704c1-112">Available in the REST API, managed client object model, and JavaScript client object model.</span></span>  <br/> |
   
<span data-ttu-id="704c1-113">高い柔軟性を提供し、これらのメソッドは、保存とワークフロー内でプロジェクトを発行するときに、大幅なパフォーマンス向上も提供します。</span><span class="sxs-lookup"><span data-stu-id="704c1-113">In addition to providing more flexibility, these methods also offer significant performance improvements when saving and publishing projects in a workflow.</span></span> <span data-ttu-id="704c1-114">ここでは、REST API のメソッドを使用する方法について説明し、その一括更新のユーザー設定フィールドおよびプロジェクトのサイトを作成するワークフローは、ワークフローを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="704c1-114">This article describes how to use the methods in the REST API and provides instructions for creating a workflow that bulk updates custom fields and a workflow that creates a Project site.</span></span>
  
> [!NOTE]
> <span data-ttu-id="704c1-115">SharePoint 2013 ワークフローから REST Api を呼び出す方法の詳細については、 [POST メソッドを使用してワークフローからを使用して SharePoint の他のサービス](http://mysharepointinsight.blogspot.com/2013/05/using-sharepoint-rest-services-from.mdl)と[SharePoint ワークフロー デザイナーから SharePoint 2013 の Rest API の呼び出し](https://sergeluca.wordpress.com/2013/04/09/calling-the-sharepoint-2013-rest-api-from-a-sharepoint-designer-workflow/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="704c1-115">To learn more about calling REST APIs from SharePoint 2013 workflows, see [Using SharePoint REST services from workflow with POST method](http://mysharepointinsight.blogspot.com/2013/05/using-sharepoint-rest-services-from.mdl) and [Calling the SharePoint 2013 Rest API from a SharePoint Designer Workflow](https://sergeluca.wordpress.com/2013/04/09/calling-the-sharepoint-2013-rest-api-from-a-sharepoint-designer-workflow/).</span></span> 
  
## <a name="bulk-update-project-custom-fields-from-a-workflow"></a><span data-ttu-id="704c1-116">ワークフローの一括更新プロジェクトのユーザー設定フィールド</span><span class="sxs-lookup"><span data-stu-id="704c1-116">Bulk update project custom fields from a workflow</span></span>
<span data-ttu-id="704c1-117"><a name="BulkUpdateCustomFields"> </a></span><span class="sxs-lookup"><span data-stu-id="704c1-117"></span></span>

<span data-ttu-id="704c1-118">以前は、ワークフローは一度に 1 つのユーザー設定フィールドを更新する可能性がありますだけです。</span><span class="sxs-lookup"><span data-stu-id="704c1-118">Previously, workflows could only update one custom field at a time.</span></span> <span data-ttu-id="704c1-119">1 つのプロジェクト ユーザー設定フィールドを更新する場合は、プロジェクト詳細ページ間でユーザーの移行とに不適切なエンド ユーザー エクスペリエンスを可能性があります。</span><span class="sxs-lookup"><span data-stu-id="704c1-119">Updating project custom fields one at a time can result in a poor end-user experience when users transition between Project Detail Pages.</span></span> <span data-ttu-id="704c1-120">各更新プログラムには、**プロジェクト フィールドの設定**アクションを使用して別のサーバー要求が必要な高レーテンシーの複数のユーザー設定フィールドを更新するには、低帯域幅ネットワークの結果、重要なオーバーヘッドです。</span><span class="sxs-lookup"><span data-stu-id="704c1-120">Each update required a separate server request using the **Set Project Field** action, and updating multiple custom fields on a high-latency, low-bandwidth network resulted in a non-trivial overhead.</span></span> <span data-ttu-id="704c1-121">この問題を解決するには、REST API を一括することがユーザー設定フィールドを更新する**UpdateCustomFields**メソッドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="704c1-121">To resolve this issue, we added the **UpdateCustomFields** method to the REST API that lets you bulk update custom fields.</span></span> <span data-ttu-id="704c1-122">**UpdateCustomFields**を使用するには、名前と、更新するすべてのユーザー設定フィールドの値を格納しているディクショナリを渡します。</span><span class="sxs-lookup"><span data-stu-id="704c1-122">To use **UpdateCustomFields**, you pass in a dictionary that contains the names and values of all the custom fields you want to update.</span></span>
  
<span data-ttu-id="704c1-123">残りの部分メソッドに次の端点にあります。</span><span class="sxs-lookup"><span data-stu-id="704c1-123">The REST method can be found at the following endpoint:</span></span>
  
`https://<site-url>/_api/ProjectServer/Projects('<guid>')/Draft/UpdateCustomFields()`
  
> [!NOTE]
> <span data-ttu-id="704c1-124">交換して、 `<site-url>` 、Project Web App (PWA) サイトの URL の例ではプレース ホルダーと、 `<guid>` 、プロジェクトの UID を持つプレース ホルダー。</span><span class="sxs-lookup"><span data-stu-id="704c1-124">Replace the  `<site-url>` placeholder in the examples with the URL of your Project Web App (PWA) site and the  `<guid>` placeholder with your project UID.</span></span> 
  
<span data-ttu-id="704c1-125">このセクションでは、プロジェクトのユーザー設定フィールドを一括で更新するワークフローを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="704c1-125">This section describes how to create a workflow that bulk updates custom fields for a project.</span></span> <span data-ttu-id="704c1-126">ワークフローは、これらの大まかな手順を次に示します。</span><span class="sxs-lookup"><span data-stu-id="704c1-126">The workflow follows these high-level steps:</span></span>
  
- <span data-ttu-id="704c1-127">プロジェクト チェック アウトを取得するのにを更新するまで待つ</span><span class="sxs-lookup"><span data-stu-id="704c1-127">Wait for the project that you want to update to get checked in</span></span>
    
- <span data-ttu-id="704c1-128">プロジェクト用に、ユーザー設定フィールドのすべての更新を定義するデータ セットを作成します。</span><span class="sxs-lookup"><span data-stu-id="704c1-128">Build a data set that defines all your custom field updates for the project</span></span>
    
- <span data-ttu-id="704c1-129">プロジェクトをチェック アウト</span><span class="sxs-lookup"><span data-stu-id="704c1-129">Check out the project</span></span>
    
- <span data-ttu-id="704c1-130">プロジェクトにユーザー設定フィールドの更新プログラムを適用する**UpdateCustomFields**を呼び出す</span><span class="sxs-lookup"><span data-stu-id="704c1-130">Call **UpdateCustomFields** to apply the custom field updates to the project</span></span> 
    
- <span data-ttu-id="704c1-131">(必要な場合)、ワークフロー履歴リストに関連する情報をログに記録します。</span><span class="sxs-lookup"><span data-stu-id="704c1-131">Log relevant information to the workflow history list (if required)</span></span>
    
- <span data-ttu-id="704c1-132">プロジェクトを発行する</span><span class="sxs-lookup"><span data-stu-id="704c1-132">Publish the project</span></span>
    
- <span data-ttu-id="704c1-133">プロジェクトをチェックインします。</span><span class="sxs-lookup"><span data-stu-id="704c1-133">Check in the project</span></span>
    
<span data-ttu-id="704c1-134">最後に、エンド ・ ツー ・ エンドのワークフローは、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="704c1-134">The final, end-to-end workflow looks like this:</span></span>
  
<span data-ttu-id="704c1-135">![エンド ・ ツー ・ エンドのワークフロー](media/8c0741f9-7f76-409d-8c00-e7a8c3ddb89f.png "エンド ・ ツー ・ エンドのワークフロー")</span><span class="sxs-lookup"><span data-stu-id="704c1-135">![End-to-end workflow](media/8c0741f9-7f76-409d-8c00-e7a8c3ddb89f.png "End-to-end workflow")</span></span>
  
### <a name="to-create-a-workflow-that-bulk-updates-custom-fields"></a><span data-ttu-id="704c1-136">一括でユーザー設定フィールドを更新するワークフローを作成するには</span><span class="sxs-lookup"><span data-stu-id="704c1-136">To create a workflow that bulk updates custom fields</span></span>

1. <span data-ttu-id="704c1-137">省略可能。</span><span class="sxs-lookup"><span data-stu-id="704c1-137">Optional.</span></span> <span data-ttu-id="704c1-138">ワークフロー全体で使用できる変数には、プロジェクトの完全な URL を格納します。</span><span class="sxs-lookup"><span data-stu-id="704c1-138">Store the full URL of your project in a variable that you can use throughout the workflow.</span></span>
    
    <span data-ttu-id="704c1-139">![ストア変数内のプロジェクトの URL](media/a880c5c6-8e7a-44dd-87e9-7e532169d489.png "ストア変数内のプロジェクトの URL")</span><span class="sxs-lookup"><span data-stu-id="704c1-139">![Store the URL of the project in a variable](media/a880c5c6-8e7a-44dd-87e9-7e532169d489.png "Store the URL of the project in a variable")</span></span>
  
2. <span data-ttu-id="704c1-140">**プロジェクト イベントを待機**アクションをワークフローに追加し、**プロジェクトをチェックインするとき**のイベントを選択します。</span><span class="sxs-lookup"><span data-stu-id="704c1-140">Add the **Wait for Project Event** action to the workflow and choose the **When a project is checked in** event.</span></span> 
    
    <span data-ttu-id="704c1-141">![プロジェクトをチェックインするまで待ちます](media/699aa9c7-b3c9-426e-a775-96993a13559c.png "プロジェクトをチェックインするまで待ちます")</span><span class="sxs-lookup"><span data-stu-id="704c1-141">![Wait for the project to be checked in](media/699aa9c7-b3c9-426e-a775-96993a13559c.png "Wait for the project to be checked in")</span></span>
  
3. <span data-ttu-id="704c1-142">**ディクショナリのビルド**アクションを使用して**requestHeader**辞書を作成します。</span><span class="sxs-lookup"><span data-stu-id="704c1-142">Create a **requestHeader** dictionary using the **Build dictionary** action.</span></span> <span data-ttu-id="704c1-143">このワークフローで web サービスを呼び出すすべての同一の要求ヘッダーを使用します。</span><span class="sxs-lookup"><span data-stu-id="704c1-143">You'll use the same request header for all the web service calls in this workflow.</span></span> 
    
    <span data-ttu-id="704c1-144">![RequestHeader ディクショナリを構築します。](media/83b0aa10-9ab7-43dd-800d-a738bb815876.png "RequestHeader ディクショナリを構築します。")</span><span class="sxs-lookup"><span data-stu-id="704c1-144">![Build the requestHeader dictionary](media/83b0aa10-9ab7-43dd-800d-a738bb815876.png "Build the requestHeader dictionary")</span></span>
  
4. <span data-ttu-id="704c1-145">辞書には、次の 2 つの項目を追加します。</span><span class="sxs-lookup"><span data-stu-id="704c1-145">Add the following two items to the dictionary.</span></span>
    
    |<span data-ttu-id="704c1-146">名前</span><span class="sxs-lookup"><span data-stu-id="704c1-146">Name</span></span>|<span data-ttu-id="704c1-147">型</span><span class="sxs-lookup"><span data-stu-id="704c1-147">Type</span></span>|<span data-ttu-id="704c1-148">値</span><span class="sxs-lookup"><span data-stu-id="704c1-148">Value</span></span>|
    |:-----|:-----|:-----|
    |<span data-ttu-id="704c1-149">Accept</span><span class="sxs-lookup"><span data-stu-id="704c1-149">Accept</span></span>  <br/> |<span data-ttu-id="704c1-150">String</span><span class="sxs-lookup"><span data-stu-id="704c1-150">String</span></span>  <br/> |<span data-ttu-id="704c1-151">アプリケーションまたは json です。odata = 詳細</span><span class="sxs-lookup"><span data-stu-id="704c1-151">application/json; odata=verbose</span></span>  <br/> |
    |<span data-ttu-id="704c1-152">Content-Type</span><span class="sxs-lookup"><span data-stu-id="704c1-152">Content-Type</span></span>  <br/> |<span data-ttu-id="704c1-153">String</span><span class="sxs-lookup"><span data-stu-id="704c1-153">String</span></span>  <br/> |<span data-ttu-id="704c1-154">アプリケーションまたは json です。odata = 詳細</span><span class="sxs-lookup"><span data-stu-id="704c1-154">application/json; odata=verbose</span></span>  <br/> |
   
    <span data-ttu-id="704c1-155">![Accept ヘッダーを追加します。](media/2f2e2016-3c49-4cac-b1e7-f2b8118b840c.png "Accept ヘッダーを追加します。")</span><span class="sxs-lookup"><span data-stu-id="704c1-155">![Adding an Accept header](media/2f2e2016-3c49-4cac-b1e7-f2b8118b840c.png "Adding an Accept header")</span></span>
  
5. <span data-ttu-id="704c1-156">**ディクショナリのビルド**アクションを使用して**requestBody**辞書を作成します。</span><span class="sxs-lookup"><span data-stu-id="704c1-156">Create a **requestBody** dictionary using the **Build dictionary** action.</span></span> <span data-ttu-id="704c1-157">このディクショナリでは、適用するすべてのフィールドの更新を格納します。</span><span class="sxs-lookup"><span data-stu-id="704c1-157">This dictionary stores all the field updates that you want to apply.</span></span> 
    
    <span data-ttu-id="704c1-158">各ユーザー設定フィールドの更新プログラムには、4 つの行が必要です: フィールドのメタデータ (1) 型、キー (2)、(3) の値、および (4) の値型です。</span><span class="sxs-lookup"><span data-stu-id="704c1-158">Each custom field update requires four rows: the field's (1) metadata type, (2) key, (3) value, and (4) value type.</span></span>
    
    - <span data-ttu-id="704c1-159">**__metadata/タイプ**フィールドのメタデータのタイプです。</span><span class="sxs-lookup"><span data-stu-id="704c1-159">**__metadata/type** The field's metadata type.</span></span> <span data-ttu-id="704c1-160">このレコードは、常に同じと次の値を使用しています。</span><span class="sxs-lookup"><span data-stu-id="704c1-160">This record is always the same and uses the following values:</span></span> 
    
       - <span data-ttu-id="704c1-161">名: customFieldDictionary (i)/__metadata/タイプ ( **i**は 0 から始まる、ディクショナリ内の各ユーザー設定フィールドのインデックス)</span><span class="sxs-lookup"><span data-stu-id="704c1-161">Name: customFieldDictionary(i)/__metadata/type (where **i** is the index of each custom field in the dictionary, starting with 0)</span></span> 
            
       - <span data-ttu-id="704c1-162">型:String</span><span class="sxs-lookup"><span data-stu-id="704c1-162">Type: String</span></span>
            
       - <span data-ttu-id="704c1-163">値: sp へKeyValue</span><span class="sxs-lookup"><span data-stu-id="704c1-163">Value: SP.KeyValue</span></span>
    
       <span data-ttu-id="704c1-164">![ユーザー設定フィールドの更新プログラムを定義します。](media/a4423493-6603-42ee-ae50-1ef74c5c59bd.png "ユーザー設定フィールドの更新プログラムを定義します。")</span><span class="sxs-lookup"><span data-stu-id="704c1-164">![Defining a custom field update](media/a4423493-6603-42ee-ae50-1ef74c5c59bd.png "Defining a custom field update")</span></span>
  
    - <span data-ttu-id="704c1-165">**キー**形式で、ユーザー設定フィールドの内部名: *Custom_ce23fbf43fa0e411941000155d3c8201*</span><span class="sxs-lookup"><span data-stu-id="704c1-165">**Key** The internal name of the custom field, in the format: *Custom_ce23fbf43fa0e411941000155d3c8201*</span></span> 
    
       <span data-ttu-id="704c1-166">**InternalName**エンドポイントに移動すると、ユーザー設定フィールドの内部名をご覧ください。`https://<site-url>/_api/ProjectServer/CustomFields('<guid>')/InternalName`</span><span class="sxs-lookup"><span data-stu-id="704c1-166">You can find the internal name of a custom field by navigating to it's **InternalName** endpoint: `https://<site-url>/_api/ProjectServer/CustomFields('<guid>')/InternalName`</span></span>
    
       <span data-ttu-id="704c1-167">ユーザー設定フィールドを手動で作成した場合の値をサイトからサイトへと異なります。</span><span class="sxs-lookup"><span data-stu-id="704c1-167">If you created your custom fields manually, the values will differ from site to site.</span></span> <span data-ttu-id="704c1-168">複数のサイト間でワークフローを再利用する場合は、ユーザー設定フィールド Id が正しいことを確認します。</span><span class="sxs-lookup"><span data-stu-id="704c1-168">If you plan to reuse the workflow across multiple sites, make sure the custom field IDs are correct.</span></span>
    
    - <span data-ttu-id="704c1-169">**値**ユーザー設定フィールドに割り当てる値です。</span><span class="sxs-lookup"><span data-stu-id="704c1-169">**Value** The value to assign to the custom field.</span></span> <span data-ttu-id="704c1-170">ルックアップ テーブルにリンクされているユーザー設定フィールド、実際の参照テーブルの値の代わりにルックアップ テーブルのエントリの内部名を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="704c1-170">For custom fields that are linked to lookup tables, you need to use the internal names of the lookup table entries instead of the actual lookup table values.</span></span> 
    
       <span data-ttu-id="704c1-171">次のエンドポイントでは内部参照テーブルのエントリの名前をご覧ください。`https://<site-url>/_api/ProjectServer/CustomFields('<guid>')/LookupEntries('<guid>')/InternalName`</span><span class="sxs-lookup"><span data-stu-id="704c1-171">You can find the internal name of the lookup table entry at the following endpoint: `https://<site-url>/_api/ProjectServer/CustomFields('<guid>')/LookupEntries('<guid>')/InternalName`</span></span>
    
       <span data-ttu-id="704c1-172">ルックアップ テーブル カスタム フィールド セットに複数の値をそのまま使用、使用した場合`;#`に示すように次の例の辞書) の値を連結します。</span><span class="sxs-lookup"><span data-stu-id="704c1-172">If you have a lookup table custom field set up to accept multiple values, use  `;#` to concatenate values (as shown in the example dictionary below).</span></span> 
    
    - <span data-ttu-id="704c1-173">**値型**更新するにはユーザー設定フィールドの型。</span><span class="sxs-lookup"><span data-stu-id="704c1-173">**ValueType** The type of the custom field you are updating.</span></span> 
    
       - <span data-ttu-id="704c1-174">テキスト、期間、フラグ、および LookupTable のフィールドの Edm.String を使用して、</span><span class="sxs-lookup"><span data-stu-id="704c1-174">For Text, Duration, Flag, and LookupTable fields, use Edm.String</span></span>
    
       - <span data-ttu-id="704c1-175">数値フィールドは、「Edm.Int32、Edm.Double、またはその他の OData に受け入れられている数値型の使用」を使用していますください。</span><span class="sxs-lookup"><span data-stu-id="704c1-175">For Number fields, use Edm.Int32, Edm.Double, or any other OData-accepted number type</span></span>
    
       - <span data-ttu-id="704c1-176">日付フィールドでは、Edm.DateTime を使用して、</span><span class="sxs-lookup"><span data-stu-id="704c1-176">For Date fields, use Edm.DateTime</span></span>
    
       <span data-ttu-id="704c1-177">下の辞書の例では、次の 3 つのユーザー設定フィールド用の更新プログラムを定義します。</span><span class="sxs-lookup"><span data-stu-id="704c1-177">The example dictionary below defines updates for three custom fields.</span></span> <span data-ttu-id="704c1-178">複数値ルックアップ テーブルのカスタム フィールドは、最初、2 番目の数値型フィールドでは、日付フィールドには、3 つ目。</span><span class="sxs-lookup"><span data-stu-id="704c1-178">The first is for a multiple value lookup table custom field, the second is for a number field, and the third is for a date field.</span></span> <span data-ttu-id="704c1-179">注方法**customFieldDictionary**インデックスの増分値です。</span><span class="sxs-lookup"><span data-stu-id="704c1-179">Note how the **customFieldDictionary** index increments.</span></span> 
    
       > [!NOTE]
       > <span data-ttu-id="704c1-180">これらの値は、例示目的でのみです。</span><span class="sxs-lookup"><span data-stu-id="704c1-180">These values are for illustration purposes only.</span></span> <span data-ttu-id="704c1-181">使用するキーと値のペアは、PWA のデータによって異なります。</span><span class="sxs-lookup"><span data-stu-id="704c1-181">The key-value pairs you'll use depend on your PWA data.</span></span> 
  
       |<span data-ttu-id="704c1-182">名前</span><span class="sxs-lookup"><span data-stu-id="704c1-182">Name</span></span>|<span data-ttu-id="704c1-183">型</span><span class="sxs-lookup"><span data-stu-id="704c1-183">Type</span></span>|<span data-ttu-id="704c1-184">値</span><span class="sxs-lookup"><span data-stu-id="704c1-184">Value</span></span>|
       |:-----|:-----|:-----|
       |<span data-ttu-id="704c1-185">customFieldDictionary (0)/__metadata/タイプ</span><span class="sxs-lookup"><span data-stu-id="704c1-185">customFieldDictionary(0)/__metadata/type</span></span>  <br/> |<span data-ttu-id="704c1-186">String</span><span class="sxs-lookup"><span data-stu-id="704c1-186">String</span></span>  <br/> |<span data-ttu-id="704c1-187">SP へKeyValue</span><span class="sxs-lookup"><span data-stu-id="704c1-187">SP.KeyValue</span></span>  <br/> |
       |<span data-ttu-id="704c1-188">customFieldDictionary (0)/キー</span><span class="sxs-lookup"><span data-stu-id="704c1-188">customFieldDictionary(0)/Key</span></span>  <br/> |<span data-ttu-id="704c1-189">String</span><span class="sxs-lookup"><span data-stu-id="704c1-189">String</span></span>  <br/> |<span data-ttu-id="704c1-190">カスタム\_ce23fbf43fa0e411941000155d3c8201</span><span class="sxs-lookup"><span data-stu-id="704c1-190">Custom\_ce23fbf43fa0e411941000155d3c8201</span></span>  <br/> |
       |<span data-ttu-id="704c1-191">customFieldDictionary (0)/値</span><span class="sxs-lookup"><span data-stu-id="704c1-191">customFieldDictionary(0)/Value</span></span>  <br/> |<span data-ttu-id="704c1-192">String</span><span class="sxs-lookup"><span data-stu-id="704c1-192">String</span></span>  <br/> |<span data-ttu-id="704c1-193">エントリ\_b9a2fd69279de411940f00155d3c8201; #Entry\_baa2fd69279de411940f00155d3c8201</span><span class="sxs-lookup"><span data-stu-id="704c1-193">Entry\_b9a2fd69279de411940f00155d3c8201;#Entry\_baa2fd69279de411940f00155d3c8201</span></span>  <br/> |
       |<span data-ttu-id="704c1-194">customFieldDictionary (0) または値型</span><span class="sxs-lookup"><span data-stu-id="704c1-194">customFieldDictionary(0)/ValueType</span></span>  <br/> |<span data-ttu-id="704c1-195">String</span><span class="sxs-lookup"><span data-stu-id="704c1-195">String</span></span>  <br/> |<span data-ttu-id="704c1-196">Edm.String</span><span class="sxs-lookup"><span data-stu-id="704c1-196">Edm.String</span></span>  <br/> |
       |<span data-ttu-id="704c1-197">customFieldDictionary (1)/__metadata/タイプ</span><span class="sxs-lookup"><span data-stu-id="704c1-197">customFieldDictionary(1)/__metadata/type</span></span>  <br/> |<span data-ttu-id="704c1-198">String</span><span class="sxs-lookup"><span data-stu-id="704c1-198">String</span></span>  <br/> |<span data-ttu-id="704c1-199">SP へKeyValue</span><span class="sxs-lookup"><span data-stu-id="704c1-199">SP.KeyValue</span></span>  <br/> |
       |<span data-ttu-id="704c1-200">customFieldDictionary (1)/キー</span><span class="sxs-lookup"><span data-stu-id="704c1-200">customFieldDictionary(1)/Key</span></span>  <br/> |<span data-ttu-id="704c1-201">String</span><span class="sxs-lookup"><span data-stu-id="704c1-201">String</span></span>  <br/> |<span data-ttu-id="704c1-202">Custom_c7f114c97098e411940f00155d3c8201</span><span class="sxs-lookup"><span data-stu-id="704c1-202">Custom_c7f114c97098e411940f00155d3c8201</span></span>  <br/> |
       |<span data-ttu-id="704c1-203">customFieldDictionary (1) と値</span><span class="sxs-lookup"><span data-stu-id="704c1-203">customFieldDictionary(1)/Value</span></span>  <br/> |<span data-ttu-id="704c1-204">String</span><span class="sxs-lookup"><span data-stu-id="704c1-204">String</span></span>  <br/> |<span data-ttu-id="704c1-205">90.5</span><span class="sxs-lookup"><span data-stu-id="704c1-205">90.5</span></span>  <br/> |
       |<span data-ttu-id="704c1-206">customFieldDictionary (1) または値型</span><span class="sxs-lookup"><span data-stu-id="704c1-206">customFieldDictionary(1)/ValueType</span></span>  <br/> |<span data-ttu-id="704c1-207">String</span><span class="sxs-lookup"><span data-stu-id="704c1-207">String</span></span>  <br/> |<span data-ttu-id="704c1-208">Edm.Double</span><span class="sxs-lookup"><span data-stu-id="704c1-208">Edm.Double</span></span>  <br/> |
       |<span data-ttu-id="704c1-209">customFieldDictionary (2)/__metadata/タイプ</span><span class="sxs-lookup"><span data-stu-id="704c1-209">customFieldDictionary(2)/__metadata/type</span></span>  <br/> |<span data-ttu-id="704c1-210">String</span><span class="sxs-lookup"><span data-stu-id="704c1-210">String</span></span>  <br/> |<span data-ttu-id="704c1-211">SP へKeyValue</span><span class="sxs-lookup"><span data-stu-id="704c1-211">SP.KeyValue</span></span>  <br/> |
       |<span data-ttu-id="704c1-212">customFieldDictionary (2)/キー</span><span class="sxs-lookup"><span data-stu-id="704c1-212">customFieldDictionary(2)/Key</span></span>  <br/> |<span data-ttu-id="704c1-213">String</span><span class="sxs-lookup"><span data-stu-id="704c1-213">String</span></span>  <br/> |<span data-ttu-id="704c1-214">Custom_c6fb67e0b9a1e411941000155d3c8201</span><span class="sxs-lookup"><span data-stu-id="704c1-214">Custom_c6fb67e0b9a1e411941000155d3c8201</span></span>  <br/> |
       |<span data-ttu-id="704c1-215">customFieldDictionary (2) と値</span><span class="sxs-lookup"><span data-stu-id="704c1-215">customFieldDictionary(2)/Value</span></span>  <br/> |<span data-ttu-id="704c1-216">String</span><span class="sxs-lookup"><span data-stu-id="704c1-216">String</span></span>  <br/> |<span data-ttu-id="704c1-217">2015-04-01T00:00:00.0000000</span><span class="sxs-lookup"><span data-stu-id="704c1-217">2015-04-01T00:00:00.0000000</span></span>  <br/> |
       |<span data-ttu-id="704c1-218">customFieldDictionary (2) または値型</span><span class="sxs-lookup"><span data-stu-id="704c1-218">customFieldDictionary(2)/ValueType</span></span>  <br/> |<span data-ttu-id="704c1-219">String</span><span class="sxs-lookup"><span data-stu-id="704c1-219">String</span></span>  <br/> |<span data-ttu-id="704c1-220">Edm.DateTime</span><span class="sxs-lookup"><span data-stu-id="704c1-220">Edm.DateTime</span></span>  <br/> |
   
       <span data-ttu-id="704c1-221">![辞書の更新プログラムのユーザー設定フィールドを定義します。](media/41a1f18f-a6b2-40ff-904b-437baf962621.png "辞書の更新プログラムのユーザー設定フィールドを定義します。")</span><span class="sxs-lookup"><span data-stu-id="704c1-221">![Dictionary that defines custom field updates](media/41a1f18f-a6b2-40ff-904b-437baf962621.png "Dictionary that defines custom field updates")</span></span>
  
6. <span data-ttu-id="704c1-222">プロジェクトをチェック アウトするには、 **HTTP Web サービスを呼び出す**アクションを追加します。</span><span class="sxs-lookup"><span data-stu-id="704c1-222">Add a **Call HTTP Web Service** action to check the project out.</span></span> 
    
    <span data-ttu-id="704c1-223">![Checkout メソッドを呼び出す](media/8ce56014-0317-419b-afa7-229d05c86885.png "Checkout メソッドを呼び出す")</span><span class="sxs-lookup"><span data-stu-id="704c1-223">![Call the Checkout method](media/8ce56014-0317-419b-afa7-229d05c86885.png "Call the Checkout method")</span></span>
  
7. <span data-ttu-id="704c1-224">Web サービス呼び出しの要求ヘッダーを指定するのプロパティを編集します。</span><span class="sxs-lookup"><span data-stu-id="704c1-224">Edit the properties of the web service call to specify the request header.</span></span> <span data-ttu-id="704c1-225">**プロパティ**] ダイアログ ボックスを開くには、アクションを右クリックして**プロパティ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="704c1-225">To open the **Properties** dialog box, right-click the action and choose **Properties**.</span></span>
    
    <span data-ttu-id="704c1-226">![プロパティを呼び出す web サービスの要求ヘッダーの指定](media/d81e92b1-43df-42ad-9cd0-a693f93b164e.png "プロパティを呼び出す web サービスの要求ヘッダーの指定")</span><span class="sxs-lookup"><span data-stu-id="704c1-226">![Specify the request header in web service call properties](media/d81e92b1-43df-42ad-9cd0-a693f93b164e.png "Specify the request header in web service call properties")</span></span>
  
8. <span data-ttu-id="704c1-227">**UpdateCustomFields**メソッドを呼び出して、 **HTTP Web サービスを呼び出す**アクションを追加します。</span><span class="sxs-lookup"><span data-stu-id="704c1-227">Add a **Call HTTP Web Service** action to call the **UpdateCustomFields** method.</span></span> 
    
    <span data-ttu-id="704c1-228">![HTTP Web サービスを呼び出すアクションを作成します。](media/9a73a201-c035-41b4-8798-506ac48b90f8.png "HTTP Web サービスを呼び出すアクションを作成します。")</span><span class="sxs-lookup"><span data-stu-id="704c1-228">![Create a Call HTTP Web Service action](media/9a73a201-c035-41b4-8798-506ac48b90f8.png "Create a Call HTTP Web Service action")</span></span>
  
    <span data-ttu-id="704c1-229">注、 `/Draft/` 、web サービスの URL のセグメントです。</span><span class="sxs-lookup"><span data-stu-id="704c1-229">Note the  `/Draft/` segment in the web service URL.</span></span> <span data-ttu-id="704c1-230">完全な URL は、次のようになります。`https://<site-url>/_api/ProjectServer/Projects('<guid>')/Draft/UpdateCustomFields()`</span><span class="sxs-lookup"><span data-stu-id="704c1-230">The full URL should look like this: `https://<site-url>/_api/ProjectServer/Projects('<guid>')/Draft/UpdateCustomFields()`</span></span>
    
    <span data-ttu-id="704c1-231">![UpdateCustomFields メソッドを呼び出す](media/03b323f1-8e99-4b18-be18-be505d7cec7e.png "UpdateCustomFields メソッドを呼び出す")</span><span class="sxs-lookup"><span data-stu-id="704c1-231">![Call the UpdateCustomFields method](media/03b323f1-8e99-4b18-be18-be505d7cec7e.png "Call the UpdateCustomFields method")</span></span>
  
9. <span data-ttu-id="704c1-232">作成した辞書を**RequestHeader**と**RequestContent**のパラメーターをバインドする web サービスの呼び出しのプロパティを編集します。</span><span class="sxs-lookup"><span data-stu-id="704c1-232">Edit the properties of the web service call to bind the **RequestHeader** and **RequestContent** parameters to the dictionaries you created.</span></span> <span data-ttu-id="704c1-233">**ResponseContent**を格納する新しい変数を作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="704c1-233">You can also create a new variable to store the **ResponseContent**.</span></span>
    
    <span data-ttu-id="704c1-234">![要求ヘッダーとコンテンツの辞書をバインドします。](media/f96bec92-138e-4eab-b1e7-1ab83d0428a5.png "要求ヘッダーとコンテンツの辞書をバインドします。")</span><span class="sxs-lookup"><span data-stu-id="704c1-234">![Bind the dictionaries to the request header and content](media/f96bec92-138e-4eab-b1e7-1ab83d0428a5.png "Bind the dictionaries to the request header and content")</span></span>
  
10. <span data-ttu-id="704c1-235">省略可能。</span><span class="sxs-lookup"><span data-stu-id="704c1-235">Optional.</span></span> <span data-ttu-id="704c1-236">キュー ジョブの状態を確認し、ワークフローの履歴リストに情報をログに記録する応答のディクショナリから読み込まれます。</span><span class="sxs-lookup"><span data-stu-id="704c1-236">Read from the response dictionary to check the state of the queue job and log the information in the workflow history list.</span></span>
    
    <span data-ttu-id="704c1-237">![ログの設定](media/7d2f4936-61d7-4906-83e8-7478a5935af5.png "ログの設定")</span><span class="sxs-lookup"><span data-stu-id="704c1-237">![Setting up logging](media/7d2f4936-61d7-4906-83e8-7478a5935af5.png "Setting up logging")</span></span>
  
11. <span data-ttu-id="704c1-238">プロジェクトを発行する**発行**エンドポイントに web サービスの呼び出しを追加します。</span><span class="sxs-lookup"><span data-stu-id="704c1-238">Add a web service call to the **Publish** endpoint to publish the project.</span></span> <span data-ttu-id="704c1-239">常に同じ要求ヘッダーを使用します。</span><span class="sxs-lookup"><span data-stu-id="704c1-239">Always use the same request header.</span></span> 
    
    <span data-ttu-id="704c1-240">![Publish メソッドを呼び出す](media/3b661091-ffae-4d7e-a0bb-5b96a6292731.png "Publish メソッドを呼び出す")</span><span class="sxs-lookup"><span data-stu-id="704c1-240">![Call the Publish method](media/3b661091-ffae-4d7e-a0bb-5b96a6292731.png "Call the Publish method")</span></span>
  
    <span data-ttu-id="704c1-241">![発行 web サービスのプロパティを呼び出す](media/6a80a5d3-7e29-4398-993c-f78b3faca8b1.png "発行 web サービスのプロパティを呼び出す")</span><span class="sxs-lookup"><span data-stu-id="704c1-241">![Properties for the Publish web service call](media/6a80a5d3-7e29-4398-993c-f78b3faca8b1.png "Properties for the Publish web service call")</span></span>
  
12. <span data-ttu-id="704c1-242">プロジェクトをチェックインする**チェックイン**のエンドポイントに最終的な web サービス呼び出しを追加します。</span><span class="sxs-lookup"><span data-stu-id="704c1-242">Add a final web service call to the **Checkin** endpoint to check the project in.</span></span> 
    
    <span data-ttu-id="704c1-243">![Checkin メソッドを呼び出す](media/430510cb-0774-4911-af7f-b565b83eba0e.png "Checkin メソッドを呼び出す")</span><span class="sxs-lookup"><span data-stu-id="704c1-243">![Call the Checkin method](media/430510cb-0774-4911-af7f-b565b83eba0e.png "Call the Checkin method")</span></span>
  
    <span data-ttu-id="704c1-244">![チェックイン web サービスのプロパティを呼び出す](media/485f48d6-bbb8-4568-9dc3-aae3218f6bd1.png "チェックイン web サービスのプロパティを呼び出す")</span><span class="sxs-lookup"><span data-stu-id="704c1-244">![Properties for the Checkin web service call](media/485f48d6-bbb8-4568-9dc3-aae3218f6bd1.png "Properties for the Checkin web service call")</span></span>

<span data-ttu-id="704c1-245"><a name="CreateProjectSite"> </a></span><span class="sxs-lookup"><span data-stu-id="704c1-245"></span></span>

## <a name="create-a-project-site-from-a-workflow"></a><span data-ttu-id="704c1-246">ワークフローからのプロジェクト サイトを作成します。</span><span class="sxs-lookup"><span data-stu-id="704c1-246">Create a Project site from a workflow</span></span>

<span data-ttu-id="704c1-247">すべてのプロジェクトは、チーム メンバーが共同作業を行うドキュメントを共有、問題を発生させるに表示され、それぞれ専用の SharePoint サイトを持つことができます。</span><span class="sxs-lookup"><span data-stu-id="704c1-247">Every project can have its own dedicated SharePoint sites where team members can collaborate, share documents, raise issues, and so on.</span></span> <span data-ttu-id="704c1-248">以前は、サイトがのみを作成する自動的に発行または手動で Project Professional でプロジェクト マネージャーまたは管理者は、PWA での設定、またはそれらを無効にでした。</span><span class="sxs-lookup"><span data-stu-id="704c1-248">Previously, sites could only be created automatically on first publish or manually by the project manager in Project Professional or by the administrator in PWA settings, or they could be disabled.</span></span>
  
<span data-ttu-id="704c1-249">プロジェクト サイトを作成する場合に選択することができますので、 **CreateProjectSite**メソッドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="704c1-249">We've added the **CreateProjectSite** method so you can choose when to create project sites.</span></span> <span data-ttu-id="704c1-250">これは、組織ユーザーが最初に発行するのではなく、プロジェクトの提案が、定義済みのワークフローの特定の段階に達すると自動的に自分のサイトを作成する場合に特に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="704c1-250">This is particularly useful for organizations who want to create their sites automatically when a project proposal reaches a specific stage in a pre-defined workflow, rather than on first publish.</span></span> <span data-ttu-id="704c1-251">プロジェクト サイトの作成を大幅に延期すると、プロジェクトの作成のパフォーマンスが向上します。</span><span class="sxs-lookup"><span data-stu-id="704c1-251">Postponing project site creation significantly improves the performance of creating a project.</span></span> 
  
<span data-ttu-id="704c1-252">**前提条件:****PWA の設定**でプロジェクト サイトの作成**を選択するユーザーを許可する**設定を設定する必要があります**CreateProjectSite**を使用する前に > * * 接続されている SharePoint サイト * * >**設定**します。</span><span class="sxs-lookup"><span data-stu-id="704c1-252">**Prerequisite:** Before you can use **CreateProjectSite**, the **Allow users to choose** setting must be set for project site creation in **PWA Settings** > ** Connected SharePoint Sites ** > **Settings**.</span></span>
  
<span data-ttu-id="704c1-253">![の設定「を許可するユーザーを選択する」PWA の設定で](media/6c6c8175-eb10-431d-8056-cea55718fdb4.png "PWA の設定を選択する設定が可能にします。")</span><span class="sxs-lookup"><span data-stu-id="704c1-253">![Setting "Allow users to choose" in PWA settings](media/6c6c8175-eb10-431d-8056-cea55718fdb4.png "Setting Allow users to choose in PWA settings")</span></span>
  
### <a name="to-create-a-workflow-that-creates-a-project-site"></a><span data-ttu-id="704c1-254">プロジェクト サイトを作成するワークフローを作成するには</span><span class="sxs-lookup"><span data-stu-id="704c1-254">To create a workflow that creates a Project site</span></span>

1. <span data-ttu-id="704c1-255">作成または既存のワークフローを編集し、プロジェクト サイトを作成するステップを選択します。</span><span class="sxs-lookup"><span data-stu-id="704c1-255">Create or edit an existing workflow and select the step where you want to create your Project sites.</span></span>
    
2. <span data-ttu-id="704c1-256">**ディクショナリのビルド**アクションを使用して**requestHeader**辞書を作成します。</span><span class="sxs-lookup"><span data-stu-id="704c1-256">Create a **requestHeader** dictionary using the **Build dictionary** action.</span></span> 
    
    <span data-ttu-id="704c1-257">![RequestHeader ディクショナリを構築します。](media/83b0aa10-9ab7-43dd-800d-a738bb815876.png "RequestHeader ディクショナリを構築します。")</span><span class="sxs-lookup"><span data-stu-id="704c1-257">![Build the requestHeader dictionary](media/83b0aa10-9ab7-43dd-800d-a738bb815876.png "Build the requestHeader dictionary")</span></span>
  
3. <span data-ttu-id="704c1-258">辞書には、次の 2 つの項目を追加します。</span><span class="sxs-lookup"><span data-stu-id="704c1-258">Add the following two items to the dictionary.</span></span>
    
    |<span data-ttu-id="704c1-259">名前</span><span class="sxs-lookup"><span data-stu-id="704c1-259">Name</span></span>|<span data-ttu-id="704c1-260">型</span><span class="sxs-lookup"><span data-stu-id="704c1-260">Type</span></span>|<span data-ttu-id="704c1-261">値</span><span class="sxs-lookup"><span data-stu-id="704c1-261">Value</span></span>|
    |:-----|:-----|:-----|
    |<span data-ttu-id="704c1-262">Accept</span><span class="sxs-lookup"><span data-stu-id="704c1-262">Accept</span></span>  <br/> |<span data-ttu-id="704c1-263">String</span><span class="sxs-lookup"><span data-stu-id="704c1-263">String</span></span>  <br/> |<span data-ttu-id="704c1-264">アプリケーションまたは json です。odata = 詳細</span><span class="sxs-lookup"><span data-stu-id="704c1-264">application/json; odata=verbose</span></span>  <br/> |
    |<span data-ttu-id="704c1-265">Content-Type</span><span class="sxs-lookup"><span data-stu-id="704c1-265">Content-Type</span></span>  <br/> |<span data-ttu-id="704c1-266">String</span><span class="sxs-lookup"><span data-stu-id="704c1-266">String</span></span>  <br/> |<span data-ttu-id="704c1-267">アプリケーションまたは json です。odata = 詳細</span><span class="sxs-lookup"><span data-stu-id="704c1-267">application/json; odata=verbose</span></span>  <br/> |
   
    <span data-ttu-id="704c1-268">![Accept ヘッダーを追加します。](media/2f2e2016-3c49-4cac-b1e7-f2b8118b840c.png "Accept ヘッダーを追加します。")</span><span class="sxs-lookup"><span data-stu-id="704c1-268">![Adding an Accept header](media/2f2e2016-3c49-4cac-b1e7-f2b8118b840c.png "Adding an Accept header")</span></span>
  
4. <span data-ttu-id="704c1-269">**HTTP Web サービスを呼び出す**アクションを追加します。</span><span class="sxs-lookup"><span data-stu-id="704c1-269">Add the **Call HTTP Web Service** action.</span></span> <span data-ttu-id="704c1-270">**POST**を使用する要求の種類を変更し、次の形式を使用して URL を設定します。</span><span class="sxs-lookup"><span data-stu-id="704c1-270">Change the request type to use **POST**, and set the URL using the following format:</span></span>
    
    `https://<site-url>/_api/ProjectServer/Projects('<guid>')/CreateProjectSite('New web name')`
    
    <span data-ttu-id="704c1-271">![CreateProjectSite エンドポイントの URI を構築します。](media/42a90a5e-8d1b-4667-a933-785175212847.png "CreateProjectSite エンドポイントの URI を構築します。")</span><span class="sxs-lookup"><span data-stu-id="704c1-271">![Building the CreateProjectSite endpoint URI](media/42a90a5e-8d1b-4667-a933-785175212847.png "Building the CreateProjectSite endpoint URI")</span></span>
  
    <span data-ttu-id="704c1-272">プロジェクト サイトの名前を**CreateProjectSite**メソッドに文字列として渡します。</span><span class="sxs-lookup"><span data-stu-id="704c1-272">Pass the name of the Project site to the **CreateProjectSite** method as a string.</span></span> <span data-ttu-id="704c1-273">サイト名としてプロジェクト名を使用するには、空の文字列を渡します。</span><span class="sxs-lookup"><span data-stu-id="704c1-273">To use the project name as the site name, pass an empty string.</span></span> <span data-ttu-id="704c1-274">作業は、次にプロジェクト サイトを作成するために一意の名前を使用することを確認します。</span><span class="sxs-lookup"><span data-stu-id="704c1-274">Be sure to use unique names so the next project site you create will work.</span></span> 
    
5. <span data-ttu-id="704c1-275">作成した辞書を**RequestHeader**パラメーターにバインドする web サービスの呼び出しのプロパティを編集します。</span><span class="sxs-lookup"><span data-stu-id="704c1-275">Edit the properties of the web service call to bind the **RequestHeader** parameter to the dictionary you created.</span></span> 
    
    <span data-ttu-id="704c1-276">![要求する辞書をバインド](media/61a5a0a8-405f-44eb-b5e7-80b11f7caec3.png "要求する辞書をバインド")</span><span class="sxs-lookup"><span data-stu-id="704c1-276">![Binding the dictionary to the request](media/61a5a0a8-405f-44eb-b5e7-80b11f7caec3.png "Binding the dictionary to the request")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="704c1-277">関連項目</span><span class="sxs-lookup"><span data-stu-id="704c1-277">See also</span></span>

- [<span data-ttu-id="704c1-278">Project のプログラミング タスク</span><span class="sxs-lookup"><span data-stu-id="704c1-278">Project programming tasks</span></span>](project-programming-tasks.md)
- [<span data-ttu-id="704c1-279">Project 2013 のクライアント側オブジェクト モデル (CSOM)</span><span class="sxs-lookup"><span data-stu-id="704c1-279">Client-side object model (CSOM) for Project 2013</span></span>](client-side-object-model-csom-for-project-2013.md)
- [<span data-ttu-id="704c1-280">Microsoft SharePoint 2010 SDK へようこそ</span><span class="sxs-lookup"><span data-stu-id="704c1-280">Workflows in SharePoint 2013</span></span>](http://msdn.microsoft.com/library/e0602371-ae22-44be-8a7e-9e47e9f046d6%28Office.15%29.aspx)
    

