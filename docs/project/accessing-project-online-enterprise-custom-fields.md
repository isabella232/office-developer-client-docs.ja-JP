---
title: Project Online エンタープライズ ユーザー設定フィールドへのアクセス
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
ms.assetid: 25509631-fa14-49d8-b594-cfacf5355c38
description: Project Online は、企業がビジネス ニーズを満たすように拡張できる Office 365 サービスの 1 つです。 1 つの拡張領域は、エンタープライズ ユーザー設定フィールド (ECF) です。 ECF は、プロジェクト、リソース、およびタスクに追加できる型指定された値フィールドです。 次の表に、プロジェクト、リソース、およびタスクに関連付けられた ECF のリストと、その ECF のインスタンスに対応する値の例を示します。
localization_priority: Priority
ms.openlocfilehash: 9f754f1446890ae021bf6f7000ffba11e2a2df33
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708306"
---
# <a name="accessing-project-online-enterprise-custom-fields"></a><span data-ttu-id="53ab9-106">Project Online エンタープライズ ユーザー設定フィールドへのアクセス</span><span class="sxs-lookup"><span data-stu-id="53ab9-106">Accessing Project Online enterprise custom fields</span></span>

<span data-ttu-id="53ab9-107">Project Online は、企業がビジネス ニーズを満たすように拡張できる Office 365 サービスの 1 つです。</span><span class="sxs-lookup"><span data-stu-id="53ab9-107">Project Online is an Office 365 service that companies can extend to meet business needs.</span></span> <span data-ttu-id="53ab9-108">1 つの拡張領域は、エンタープライズ ユーザー設定フィールド (ECF) です。</span><span class="sxs-lookup"><span data-stu-id="53ab9-108">One extension area is Enterprise Custom Fields (ECFs).</span></span> <span data-ttu-id="53ab9-109">ECF は、プロジェクト、リソース、およびタスクに追加できる型指定された値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="53ab9-109">ECFs are typed value fields that can be added to projects, resources, and tasks.</span></span> <span data-ttu-id="53ab9-110">次の表に、プロジェクト、リソース、およびタスクに関連付けられた ECF のリストと、その ECF のインスタンスに対応する値の例を示します。</span><span class="sxs-lookup"><span data-stu-id="53ab9-110">The following table lists ECFs that associate with projects, resources, and tasks, and provides an example of a value for an instance of that ECF:</span></span>
  
|<span data-ttu-id="53ab9-111">ECF 名</span><span class="sxs-lookup"><span data-stu-id="53ab9-111">ECF Name</span></span>|<span data-ttu-id="53ab9-112">ECF 型</span><span class="sxs-lookup"><span data-stu-id="53ab9-112">ECF Type</span></span>|<span data-ttu-id="53ab9-113">関連付け</span><span class="sxs-lookup"><span data-stu-id="53ab9-113">Association</span></span>|<span data-ttu-id="53ab9-114">値の例</span><span class="sxs-lookup"><span data-stu-id="53ab9-114">Example Value</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="53ab9-115">妥当性</span><span class="sxs-lookup"><span data-stu-id="53ab9-115">Justification</span></span>  <br/> |<span data-ttu-id="53ab9-116">TEXT</span><span class="sxs-lookup"><span data-stu-id="53ab9-116">TEXT</span></span>  <br/> |<span data-ttu-id="53ab9-117">プロジェクト</span><span class="sxs-lookup"><span data-stu-id="53ab9-117">Project</span></span>  <br/> |<span data-ttu-id="53ab9-118">エンド ユーザーは、人口統計と健康データと共に、健康評価およびより良い健康状態に向けた個別の行動計画を含む結果を記録できます。</span><span class="sxs-lookup"><span data-stu-id="53ab9-118">An end user can record vital statistics and health data, with results that include a health evaluation and an individualized action plan towards better health.</span></span>  <br/> |
|<span data-ttu-id="53ab9-119">リスクの評価</span><span class="sxs-lookup"><span data-stu-id="53ab9-119">Risk Rating</span></span>  <br/> |<span data-ttu-id="53ab9-120">TEXT</span><span class="sxs-lookup"><span data-stu-id="53ab9-120">TEXT</span></span>  <br/> |<span data-ttu-id="53ab9-121">プロジェクト</span><span class="sxs-lookup"><span data-stu-id="53ab9-121">Project</span></span>  <br/> |<span data-ttu-id="53ab9-122">低</span><span class="sxs-lookup"><span data-stu-id="53ab9-122">Low</span></span>  <br/> |
|<span data-ttu-id="53ab9-123">ROI</span><span class="sxs-lookup"><span data-stu-id="53ab9-123">ROI</span></span>  <br/> |<span data-ttu-id="53ab9-124">NUMBER</span><span class="sxs-lookup"><span data-stu-id="53ab9-124">number</span></span>  <br/> |<span data-ttu-id="53ab9-125">プロジェクト</span><span class="sxs-lookup"><span data-stu-id="53ab9-125">Project</span></span>  <br/> |<span data-ttu-id="53ab9-126">2.10</span><span class="sxs-lookup"><span data-stu-id="53ab9-126">"210"</span></span>  <br/> |
|<span data-ttu-id="53ab9-127">総コスト</span><span class="sxs-lookup"><span data-stu-id="53ab9-127">Total Cost</span></span>  <br/> |<span data-ttu-id="53ab9-128">COST</span><span class="sxs-lookup"><span data-stu-id="53ab9-128">Cost</span></span>  <br/> |<span data-ttu-id="53ab9-129">プロジェクト</span><span class="sxs-lookup"><span data-stu-id="53ab9-129">Project</span></span>  <br/> |<span data-ttu-id="53ab9-130">$1,031,514</span><span class="sxs-lookup"><span data-stu-id="53ab9-130">$1,031,514</span></span>  <br/> |
|<span data-ttu-id="53ab9-131">チームの立ち上げ</span><span class="sxs-lookup"><span data-stu-id="53ab9-131">Launch Team</span></span>  <br/> |<span data-ttu-id="53ab9-132">TEXT</span><span class="sxs-lookup"><span data-stu-id="53ab9-132">TEXT</span></span>  <br/> |<span data-ttu-id="53ab9-133">リソース</span><span class="sxs-lookup"><span data-stu-id="53ab9-133">Resources</span></span>  <br/> |<span data-ttu-id="53ab9-134">はい</span><span class="sxs-lookup"><span data-stu-id="53ab9-134">Yes</span></span>  <br/> |
|<span data-ttu-id="53ab9-135">役職</span><span class="sxs-lookup"><span data-stu-id="53ab9-135">Position Role</span></span>  <br/> |<span data-ttu-id="53ab9-136">TEXT</span><span class="sxs-lookup"><span data-stu-id="53ab9-136">TEXT</span></span>  <br/> |<span data-ttu-id="53ab9-137">リソース</span><span class="sxs-lookup"><span data-stu-id="53ab9-137">Resources</span></span>  <br/> |<span data-ttu-id="53ab9-138">テスト担当者</span><span class="sxs-lookup"><span data-stu-id="53ab9-138">Tester</span></span>  <br/> |
|<span data-ttu-id="53ab9-139">フラグの状態</span><span class="sxs-lookup"><span data-stu-id="53ab9-139">Flag Status</span></span>  <br/> |<span data-ttu-id="53ab9-140">FLAG</span><span class="sxs-lookup"><span data-stu-id="53ab9-140">Flag</span></span>  <br/> |<span data-ttu-id="53ab9-141">タスク</span><span class="sxs-lookup"><span data-stu-id="53ab9-141">Task</span></span>  <br/> |<span data-ttu-id="53ab9-142">いいえ</span><span class="sxs-lookup"><span data-stu-id="53ab9-142">No</span></span>  <br/> |
|<span data-ttu-id="53ab9-143">正常性</span><span class="sxs-lookup"><span data-stu-id="53ab9-143">Health</span></span>  <br/> |<span data-ttu-id="53ab9-144">TEXT</span><span class="sxs-lookup"><span data-stu-id="53ab9-144">TEXT</span></span>  <br/> |<span data-ttu-id="53ab9-145">タスク</span><span class="sxs-lookup"><span data-stu-id="53ab9-145">Task</span></span>  <br/> |<span data-ttu-id="53ab9-146">指定なし</span><span class="sxs-lookup"><span data-stu-id="53ab9-146">Not specified</span></span>  <br/> |
   
<span data-ttu-id="53ab9-147">ECF は、プロジェクト、リソース、またはタスクの外部にある Project Web アプリケーション (PWA) インスタンスで定義されます。</span><span class="sxs-lookup"><span data-stu-id="53ab9-147">ECFs are defined at the Project Web Application (PWA) instance, external from any project, resource, or task.</span></span> <span data-ttu-id="53ab9-148">それにもかかわらず、プロジェクト、リソース、またはタスクに関連付けることもできます。</span><span class="sxs-lookup"><span data-stu-id="53ab9-148">Yet, they can become associated with a project, resource, or task.</span></span> <span data-ttu-id="53ab9-149">この記事では、サンプル アプリケーションを使用してユーザー設定フィールドの初歩的な概要を示します。特に、ECF 値の取得について重点的に説明します。</span><span class="sxs-lookup"><span data-stu-id="53ab9-149">This article provides an introductory look at custom fields using a sample application and focuses on retrieving ECF values.</span></span> 
  
<span data-ttu-id="53ab9-150">完全なサンプルは、https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields でダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="53ab9-150">You can download the completed sample at https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields.</span></span>
  
<span data-ttu-id="53ab9-151">さらに、Project Online は、特定のプロジェクト、リソース、またはタスクに固有の読み取り専用エンティティとして、ローカル ユーザー設定フィールドもサポートしています。</span><span class="sxs-lookup"><span data-stu-id="53ab9-151">Additionally, Project Online supports local custom fields as read-only entities specific to the specific project, resource, or task.</span></span> <span data-ttu-id="53ab9-152">ローカル ユーザー設定フィールドの詳細については、サンプル https://github.com/OfficeDev/Project-CSOM-Read-Local-CustomFields\ を参照してください。</span><span class="sxs-lookup"><span data-stu-id="53ab9-152">For more information on local custom fields, see the sample https://github.com/OfficeDev/Project-CSOM-Read-Local-CustomFields\.</span></span>
  
## <a name="background-materials"></a><span data-ttu-id="53ab9-153">背景資料</span><span class="sxs-lookup"><span data-stu-id="53ab9-153">Background materials</span></span>

<span data-ttu-id="53ab9-154">前の記事「[クライアント側オブジェクト モデルを使用した Project Online アプリケーションの開発](developing-a-project-online-application-using-the-client-side-object-model.md)」では、CSOM を使用してアプリケーションを開発する際の背景と初期方針について説明しています。</span><span class="sxs-lookup"><span data-stu-id="53ab9-154">A previous article, [Developing a Project Online application using the client-side object model](developing-a-project-online-application-using-the-client-side-object-model.md), provides background and the initial orientation for developing applications using CSOM.</span></span> <span data-ttu-id="53ab9-155">次の項目については、この記事を参照してください。</span><span class="sxs-lookup"><span data-stu-id="53ab9-155">Refer to this article for the following items:</span></span>
  
- <span data-ttu-id="53ab9-156">Project のスタンドアロン エディションとクラウドベース エディションに関する背景情報</span><span class="sxs-lookup"><span data-stu-id="53ab9-156">Background information about Project, stand-alone and cloud-based editions</span></span> 
    
- <span data-ttu-id="53ab9-157">開発環境 (Visual Studio のエディションとソフトウェア ライブラリ)</span><span class="sxs-lookup"><span data-stu-id="53ab9-157">Development environment (Visual Studio editions and software libraries)</span></span>
    
- <span data-ttu-id="53ab9-158">CSOM ライブラリを使用する .NET アプリケーション用の Visual Studio プロジェクトの設定</span><span class="sxs-lookup"><span data-stu-id="53ab9-158">Visual Studio project setup for a .NET application using the CSOM library</span></span>
    
- <span data-ttu-id="53ab9-159">Project Online サービスへの接続</span><span class="sxs-lookup"><span data-stu-id="53ab9-159">Connecting to the Project Online service</span></span>
    
## <a name="preliminaries-class-level-declarations"></a><span data-ttu-id="53ab9-160">準備 (クラスレベルの宣言)</span><span class="sxs-lookup"><span data-stu-id="53ab9-160">Preliminaries (class-level declarations)</span></span>

<span data-ttu-id="53ab9-161">このアプリケーションのクラスでは、2 つのデータ項目 (プロジェクト コンテキストと pwaECF ディクショナリ) を定義します。</span><span class="sxs-lookup"><span data-stu-id="53ab9-161">The class for this application defines two data items: the project context and the pwaECF dictionary.</span></span>
  
<span data-ttu-id="53ab9-162">プロジェクト コンテキスト オブジェクトは、Project CSOM の一部であり、アプリケーションと PWA インスタンスを接続します。</span><span class="sxs-lookup"><span data-stu-id="53ab9-162">The project context object is part of the Project CSOM, and connects the application and the PWA instance.</span></span> <span data-ttu-id="53ab9-163">サービスに対するすべての要求で、プロジェクト コンテキストを使用します。</span><span class="sxs-lookup"><span data-stu-id="53ab9-163">All requests to the service use the project context.</span></span>
  
```cs
private static ProjectContext projContext = 
     new ProjectContext("https://Contoso216.sharepoint.com/sites/pwa");

```

<span data-ttu-id="53ab9-164">このコンテキストには、アプリケーションでインスタンスを作成するための接続エンドポイントが必要です。</span><span class="sxs-lookup"><span data-stu-id="53ab9-164">The context needs the connection endpoint to create an instance in an application.</span></span> <span data-ttu-id="53ab9-165">この接続エンドポイントは、PWA インスタンスの URL になります。</span><span class="sxs-lookup"><span data-stu-id="53ab9-165">The connection endpoint is the URL of your PWA instance.</span></span> 
  
<span data-ttu-id="53ab9-166">pwaECF ディクショナリには、PWA レベルで定義したプロジェクトの ECF を保存します。</span><span class="sxs-lookup"><span data-stu-id="53ab9-166">The pwaECF dictionary stores the project ECFs defined at the PWA level.</span></span> <span data-ttu-id="53ab9-167">このディクショナリは、キーとして ECF.InternalName を使用し、値として CustomField オブジェクトを使用します。</span><span class="sxs-lookup"><span data-stu-id="53ab9-167">The dictionary uses the ECF.InternalName as the key, and the CustomField object as the value.</span></span> <span data-ttu-id="53ab9-168">ディクショナリのデータは ListPWACustomFields メソッドで設定され、Main メソッドでリファレンスとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="53ab9-168">The dictionary is populated in the ListPWACustomFields method, and then used as a reference in the Main method.</span></span> 
  
```cs
    //Dictionary of ECFs
        static Dictionary<String, CustomField> pwaECF = new Dictionary<string, CustomField>();

```

## <a name="main-method"></a><span data-ttu-id="53ab9-169">Main メソッド</span><span class="sxs-lookup"><span data-stu-id="53ab9-169">Main method</span></span>

<span data-ttu-id="53ab9-170">Main メソッドでは、アプリケーション フローを管理します。</span><span class="sxs-lookup"><span data-stu-id="53ab9-170">The Main method manages the application flow.</span></span> <span data-ttu-id="53ab9-171">Project Online CSOM を使用する他のアプリケーションと同様に、Main でプロジェクト コンテキストを初期化します。</span><span class="sxs-lookup"><span data-stu-id="53ab9-171">As with other applications that use the Project Online CSOM, Main initializes the project context.</span></span> 
  
1. <span data-ttu-id="53ab9-172">Project Online PWA の ECF を取得してリスト表示します。</span><span class="sxs-lookup"><span data-stu-id="53ab9-172">Retrieve and list the ECFs in the Project Online PWA.</span></span>
    
   <span data-ttu-id="53ab9-173">この機能は、ListPWACustomFields メソッドに実装されています。</span><span class="sxs-lookup"><span data-stu-id="53ab9-173">This functionality is implemented in the ListPWACustomFields method.</span></span>
    
2. <span data-ttu-id="53ab9-174">ユーザー設定フィールドと非ユーザー設定フィールドを含むプロジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="53ab9-174">Retrieve projects with custom fields and non-custom fields.</span></span>
    
   <span data-ttu-id="53ab9-175">ECF を含むプロジェクトの取得時には、Project Online へのクエリ要求に次の項目を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="53ab9-175">When retrieving projects with ECFs, the query request to the Project Online service needs to include the following items:</span></span> 
    
   - <span data-ttu-id="53ab9-176">**IncludeCustomFields** &ndash; この項目では、それぞれの発行済みプロジェクトにユーザー設定フィールドをサポートする拡張機能が含まれている PublishedProjects のコレクションを返すようにサービスに要求します。</span><span class="sxs-lookup"><span data-stu-id="53ab9-176">**IncludeCustomFields** &ndash; This item requests the service to return a collection of PublishedProjects where each published project includes an extension that supports custom fields.</span></span> <span data-ttu-id="53ab9-177">この項目が指定されていないと、Project Online はユーザー設定フィールドのデータを含まない PublishedProject オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="53ab9-177">Unless this item is specified, Project Online returns PublishedProject objects that do not include Custom Field data.</span></span>
    
   - <span data-ttu-id="53ab9-178">**IncludeCustomFields.CustomFields** &ndash; この項目では、CustomFields データで PublishedProject オブジェクトのデータを設定するようにサービスに要求します。</span><span class="sxs-lookup"><span data-stu-id="53ab9-178">**IncludeCustomFields.CustomFields** &ndash; This item requests the service to populate the PublishedProject objects with CustomFields data.</span></span>
    
   <span data-ttu-id="53ab9-179">次の要求では、プロジェクトの ID と名前、およびユーザー設定フィールドとユーザー設定フィールド値のオブジェクト拡張機能を指定しています。</span><span class="sxs-lookup"><span data-stu-id="53ab9-179">The following request specifies the project Id and Name, as well as the object extension for custom fields and the custom field values.</span></span>
    
   ```cs
        var projBlk = projContext.LoadQuery(
        projContext.Projects.Include(
            p => p.Id, 
            p => p.Name,
            p => p.IncludeCustomFields,
            p => p.IncludeCustomFields.CustomFields
        ));
    
   ```

3. <span data-ttu-id="53ab9-180">それぞれのプロジェクトを確認します。</span><span class="sxs-lookup"><span data-stu-id="53ab9-180">Examine each project.</span></span>
    
   <span data-ttu-id="53ab9-181">このアプリケーションで使用しているプロジェクトのオブジェクトは、値を取得して表示するために、PublishedProject 型になっています。</span><span class="sxs-lookup"><span data-stu-id="53ab9-181">The project objects used in this application are the PublishedProject type because the values are retrieved and displayed.</span></span> 
    
   <span data-ttu-id="53ab9-182">1 つまたは複数のプロジェクトのデータ値を更新する必要がある場合、更新中のプロジェクトはチェック アウトされ、アプリケーションは値の取得とプロジェクトの更新に DraftProject オブジェクトを使用するようになります。</span><span class="sxs-lookup"><span data-stu-id="53ab9-182">If you need to update data values in one or more projects, the project undergoing the update would be checked out and the application would use a DraftProject object to retrieve the values and update the project.</span></span>
    
4. <span data-ttu-id="53ab9-183">プロジェクトの ECF エントリを割り当てます</span><span class="sxs-lookup"><span data-stu-id="53ab9-183">Accessing the ECF entries for a project</span></span>
    
   <span data-ttu-id="53ab9-184">それぞれの ECF によって、フィールド値がそれ以外の情報と分離されます。</span><span class="sxs-lookup"><span data-stu-id="53ab9-184">Each ECF instance separates the field value from the rest of the ECF information.</span></span> <span data-ttu-id="53ab9-185">フィールド値は、キーと値のペアの一部分として保存されます。</span><span class="sxs-lookup"><span data-stu-id="53ab9-185">The field value is stored as part of a key/value pair.</span></span> <span data-ttu-id="53ab9-186">それ以外の情報は、CustomField オブジェクトに保存されます。</span><span class="sxs-lookup"><span data-stu-id="53ab9-186">The rest of the information is stored in a CustomField object.</span></span>
    
   <span data-ttu-id="53ab9-187">2 つの部分で構成されるプロジェクトの ECF 値にアクセスする方法:</span><span class="sxs-lookup"><span data-stu-id="53ab9-187">Accessing ECF values in a project consists of two parts:</span></span>
    
   - <span data-ttu-id="53ab9-188">CustomFields コレクションを繰り返し処理します</span><span class="sxs-lookup"><span data-stu-id="53ab9-188">Cycling through the CustomFields collection</span></span>
    
   - <span data-ttu-id="53ab9-189">2 つのコンストラクターを使用して適切なエントリにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="53ab9-189">Accessing the proper entry using two constructs.</span></span>
    
   <span data-ttu-id="53ab9-190">それぞれのプロジェクトが、関連付けられた ECF エントリを 2 つの場所 (列挙可能な CustomFields コレクションと、キー/値ペアの一部としてのフィールド値) に保存します。</span><span class="sxs-lookup"><span data-stu-id="53ab9-190">Each project stores associated ECF entries in two places, a CustomFields collection that is enumerable and and the field values as part of key/value pairs.</span></span> <span data-ttu-id="53ab9-191">キー/値ペアでは、internalName がキーになり、フィールド値が値になります。</span><span class="sxs-lookup"><span data-stu-id="53ab9-191">In the key/value pairs, the internalName is the key and the field value is the value.</span></span> <span data-ttu-id="53ab9-192">フィールド値の保持とアクセスには、ディクショナリを使用します。</span><span class="sxs-lookup"><span data-stu-id="53ab9-192">Use a dictionary to hold and access the field values.</span></span> 
    
   <span data-ttu-id="53ab9-193">ECF のプロパティ (フィールド値以外) は、プロジェクトごとに 1 つの CustomField オブジェクトに保存されます。</span><span class="sxs-lookup"><span data-stu-id="53ab9-193">The ECF properties, other than the field values, are stored in CustomField objects, one object per project.</span></span> <span data-ttu-id="53ab9-194">CustomFields コレクションを使用して、それぞれ個別のプロジェクトに関連付けられた ECF にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="53ab9-194">Use a CustomFields collection to access the ECFs associated with an individual project.</span></span> 
    
5. <span data-ttu-id="53ab9-195">それぞれのプロジェクトは、それに関連付けられた ECF をコレクションに保存します。このコレクションの各 ECF エントリは、ECF の内部名であるキーと ECF の値を保持するオブジェクトで構成されています。</span><span class="sxs-lookup"><span data-stu-id="53ab9-195">Each project stores the associated ECFs in a collection where each ECF entry consists of a key--the internal name of the ECF--and an object that holds the value of the ECF.</span></span> <span data-ttu-id="53ab9-196">このコレクションは、それぞれのエントリにアクセスするためのディクショナリに転送します。</span><span class="sxs-lookup"><span data-stu-id="53ab9-196">Transfer the collection to a dictionary to access individual entries.</span></span> <span data-ttu-id="53ab9-197">宣言は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="53ab9-197">The declaration follows.</span></span>
    
   ```cs
    Dictionary<string, object> projDict = pubProj.IncludeCustomFields.FieldValues;
    
   ```

   <span data-ttu-id="53ab9-198">ディクショナリ エントリの値は、ECF のデータ型に相当します。</span><span class="sxs-lookup"><span data-stu-id="53ab9-198">The value in a dictionary entry corresponds to the data type of the ECF.</span></span> <span data-ttu-id="53ab9-199">それぞれの ECF のオブジェクトは、さまざまな型の 1 つにマップします。</span><span class="sxs-lookup"><span data-stu-id="53ab9-199">The object for each ECF maps to one of a variety of types.</span></span> <span data-ttu-id="53ab9-200">ほとんどの ECF は、標準的な変数に適合する単純型を使用します。</span><span class="sxs-lookup"><span data-stu-id="53ab9-200">Most ECFs use simple types that fit into standard variables.</span></span> <span data-ttu-id="53ab9-201">次のフラグメントは、いくつかの型に関連する最小限の処理を示しています。</span><span class="sxs-lookup"><span data-stu-id="53ab9-201">The following fragment shows that minimal processing is involved for several types:</span></span>
    
   ```cs
    switch (cf.FieldType)
    {
        case CustomFieldType.COST:
            decimal costValue = (decimal)oVal;
            Console.WriteLine("\tFieldType:\t{0}\n\tValue:\t{1}", cf.FieldType, 
                costValue.ToString("C"));
            break;
        case CustomFieldType.DATE:
            Console.WriteLine("\tFieldType:\t{0}\n\tValue:\t{1}", cf.FieldType, 
                oVal.ToString());
            break;
        case CustomFieldType.FINISHDATE:
            Console.WriteLine("\tFieldType:\t{0}\n\tValue:\t{1}", cf.FieldType, 
                oVal.ToString());
            break;
        case CustomFieldType.DURATION:
            Console.WriteLine("\tFieldType:\t{0}\n\tValue:\t{1}", cf.FieldType, 
                oVal.ToString());
            break;
        case CustomFieldType.FLAG:
            Console.WriteLine("\tFieldType:\t{0}\n\tValue:\t{1}", cf.FieldType, 
                oVal.ToString());
            break;
        case CustomFieldType.NUMBER:
            Console.WriteLine("\tFieldType:\t{0}\n\tValue:\t{1}", cf.FieldType, 
                oVal.ToString());
            break;
    
   ```

   <span data-ttu-id="53ab9-202">ただし、TEXT 値の参照テーブルには、追加の処理が必要になります。</span><span class="sxs-lookup"><span data-stu-id="53ab9-202">The lookup table of TEXT values, however, requires additional processing.</span></span> <span data-ttu-id="53ab9-203">アプリケーションは、サービスから適切な参照テーブルを取得し、その参照テーブルを調べることで ECF インスタンスを (単一または複数の値と共に) 出力します。</span><span class="sxs-lookup"><span data-stu-id="53ab9-203">The application retrieves the appropriate lookup table from the service, and outputs the ECF instance (with single or multiple values) by traversing the lookup table.</span></span> <span data-ttu-id="53ab9-204">次のコード フラグメントは、単純な値を保持するものと参照テーブルを使用するものを含む TEXT ECF の処理を示しています。</span><span class="sxs-lookup"><span data-stu-id="53ab9-204">The following code fragment shows processing of TEXT ECFs, including those with simple values and those using lookup tables:</span></span> 
    
   ```cs
    case CustomFieldType.TEXT:
        if (!cf.LookupTable.ServerObjectIsNull.HasValue ||
            (cf.LookupTable.ServerObjectIsNull.HasValue && 
            cf.LookupTable.ServerObjectIsNull.Value))
        { //No lookup table
            Console.WriteLine("\tFieldType:\t{0}\n\tText:\t{1}", cf.FieldType, 
                oVal.ToString());
        }
        else
        { //Lookup table
            Console.WriteLine("\tFieldType:\t{0} - using Lookup Table", cf.FieldType);
            String[] entries = (String[])oVal;
            foreach (String entry in entries)
            {
                var luEntry = projContext.LoadQuery(cf.LookupTable.Entries
                    .Where(e => e.InternalName == entry));
                projContext.ExecuteQuery();
                Console.WriteLine("\tLookup Value:\t{0}", luEntry.First().FullValue);  
            }
        }
        break;
    
   ```

   <span data-ttu-id="53ab9-205">このアプリケーションでは、単に値を出力していますが、データの値からより多くの意味を得ることも可能です。</span><span class="sxs-lookup"><span data-stu-id="53ab9-205">This application simply outputs the value(s); however, it is possible to get more meaning from the data value(s).</span></span>
    
## <a name="listpwacustomfields"></a><span data-ttu-id="53ab9-206">ListPWACustomFields</span><span class="sxs-lookup"><span data-stu-id="53ab9-206">ListPWACustomFields</span></span>

<span data-ttu-id="53ab9-207">ListPWACustomFields メソッドでは、プロジェクトに関連付けられた ECF を取得してリスト表示します。</span><span class="sxs-lookup"><span data-stu-id="53ab9-207">The ListPWACustomFields method retrieves and lists the ECFs associated with projects.</span></span> <span data-ttu-id="53ab9-208">このメソッドは、個別のプロジェクトに関連付けできる PWA インスタンスに登録された ECF をリスト表示します。</span><span class="sxs-lookup"><span data-stu-id="53ab9-208">This method lists the ECFs registered on the PWA instance that can be associated with individual projects.</span></span> <span data-ttu-id="53ab9-209">ECF にアクセスするためのエントリ ポイントは、次のクエリ要求に示すように、プロジェクト コンテキストの CustomFields 要素を使用します。</span><span class="sxs-lookup"><span data-stu-id="53ab9-209">The entry point for accessing the ECFs uses the CustomFields element of the project context, as in the following query request:</span></span>
  
```cs
// Project ECFs
    var allECFields = 
            projContext.LoadQuery(projContext.CustomFields.Include(
            qp => qp.InternalName,
            qp => qp.Name
        ));
    projContext.ExecuteQuery();

```

<span data-ttu-id="53ab9-210">このメソッドでは、プロジェクトが特定の ECF を使用しているかどうかを確認していません。</span><span class="sxs-lookup"><span data-stu-id="53ab9-210">The method does not check to see whether a project uses a specific ECF.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="53ab9-211">関連項目</span><span class="sxs-lookup"><span data-stu-id="53ab9-211">See also</span></span>

- [<span data-ttu-id="53ab9-212">Project 開発ポータル</span><span class="sxs-lookup"><span data-stu-id="53ab9-212">Project Development Portal</span></span>](https://developer.microsoft.com/ja-JP/project)
- <span data-ttu-id="53ab9-213">
  [概要: エンタープライズ ユーザー設定フィールドと参照テーブル](https://support.office.com/en-us/article/overview-enterprise-custom-fields-and-lookup-tables-f99db553-0b33-4648-93c0-f6a74637d790?ui=en-us&rs=en-us&ad=us)</span><span class="sxs-lookup"><span data-stu-id="53ab9-213">[Overview: Enterprise custom fields and lookup tables](https://support.office.com/en-us/article/overview-enterprise-custom-fields-and-lookup-tables-f99db553-0b33-4648-93c0-f6a74637d790?ui=en-us&rs=en-us&ad=us)</span></span>
- <span data-ttu-id="53ab9-214">[ローカル ユーザー設定フィールドとエンタープライズ ユーザー設定フィールド](https://msdn.microsoft.com/library/office/ms447495(v=office.14).aspx)</span><span class="sxs-lookup"><span data-stu-id="53ab9-214">[Local and Enterprise Custom Fields](https://msdn.microsoft.com/library/office/ms447495(v=office.14).aspx)</span></span>
- [<span data-ttu-id="53ab9-215">Project Server 2013 でエンタープライズ ユーザー設定フィールドを追加または編集する</span><span class="sxs-lookup"><span data-stu-id="53ab9-215">Add or edit enterprise custom fields in Project Server 2013</span></span>](https://docs.microsoft.com/project/add-or-edit-enterprise-custom-fields-in-project-server)
    

