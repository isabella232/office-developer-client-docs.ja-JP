---
title: Access で Web アプリを作成してカスタマイズする
manager: kelbow
ms.date: 08/18/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 628745f4-82e9-4838-9726-6f3e506a654f
ms.openlocfilehash: d837a83ea8773018033a27ec894375a22c15c8a3
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391123"
---
# <a name="create-and-customize-a-web-app-in-access"></a><span data-ttu-id="b8219-102">Access で Web アプリを作成してカスタマイズする</span><span class="sxs-lookup"><span data-stu-id="b8219-102">Create and customize a web app in Access</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b8219-p101">現在 Microsoft では、SharePoint での Access Web アプリの作成や使用は推奨していません。代替策として、[Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) を使用して、Web およびモバイル デバイス用の、コーディングが不要なビジネス ソリューションを構築することを検討してください。</span><span class="sxs-lookup"><span data-stu-id="b8219-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
<span data-ttu-id="b8219-p102">Access 2013を特徴付けるものとして、新しいアプリケーション モデルがあります。これにより、領域の専門家は Web ベース アプリケーションをすばやく作成できます。Access に含まれる一連のテンプレートを使用してアプリケーションの作成にすぐに着手できます。</span><span class="sxs-lookup"><span data-stu-id="b8219-p102">Access 2013 features a new application model that enables subject matter experts to quickly create web-based applications. Included with Access are a set of templates that you can use to jump start creating your application.</span></span>

<span data-ttu-id="b8219-107"><a name="ac15_CreateAndCustomizeWebApp_Prerequisites"> </a></span><span class="sxs-lookup"><span data-stu-id="b8219-107"></span></span>

## <a name="prerequisites-for-building-an-app-with-access-2013"></a><span data-ttu-id="b8219-108">Access 2013 でアプリを構築するための前提条件</span><span class="sxs-lookup"><span data-stu-id="b8219-108">Prerequisites for building an app with Access 2013</span></span>

<span data-ttu-id="b8219-109">この例の手順に従うには、以下のものが必要です。</span><span class="sxs-lookup"><span data-stu-id="b8219-109">To follow the steps in this example, you need the following:</span></span>
  
- <span data-ttu-id="b8219-110">Access</span><span class="sxs-lookup"><span data-stu-id="b8219-110">Access</span></span>
    
- <span data-ttu-id="b8219-111">SharePoint 開発環境</span><span class="sxs-lookup"><span data-stu-id="b8219-111">A SharePoint development environment</span></span>
    
<span data-ttu-id="b8219-112">SharePoint 開発環境の設定に関する詳細については、 [SharePoint の全般的な開発環境のセットアップ](https://docs.microsoft.com/sharepoint/dev/general-development/set-up-a-general-development-environment-for-sharepoint)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b8219-112">For more information about setting up your SharePoint development environment, see [Set up a general development environment for SharePoint](https://docs.microsoft.com/sharepoint/dev/general-development/set-up-a-general-development-environment-for-sharepoint).</span></span> 
  
<span data-ttu-id="b8219-113">Access と SharePoint の入手方法の詳細については、「[ダウンロード](https://msdn.microsoft.com/office/apps/fp123627)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b8219-113">For more information about obtaining Access and SharePoint, see [Downloads](https://msdn.microsoft.com/office/apps/fp123627).</span></span>

<span data-ttu-id="b8219-114"><a name="ac15_CreateAndCustomizeWebApp_CreateTheApp"> </a></span><span class="sxs-lookup"><span data-stu-id="b8219-114"></span></span>

## <a name="create-the-app"></a><span data-ttu-id="b8219-115">アプリを作成する</span><span class="sxs-lookup"><span data-stu-id="b8219-115">Create the app</span></span>

<span data-ttu-id="b8219-p103">たとえば、ビジネスの問題を追跡する Access アプリを作成するとします。テーブルとビューの作成をゼロから始める前に、ニーズを満たすスキーマ テンプレートがないかどうかを探す必要があります。</span><span class="sxs-lookup"><span data-stu-id="b8219-p103">Suppose you want to create an Access app that tracks issues for your business. Before you start creating the tables and view from scratch, you should search for a schema template that meets your needs.</span></span>
  
### <a name="to-create-the-issue-tracking-app"></a><span data-ttu-id="b8219-118">問題追跡アプリを作成するには</span><span class="sxs-lookup"><span data-stu-id="b8219-118">To create the issue tracking app</span></span>

1. <span data-ttu-id="b8219-119">Access を開いて、[ **カスタム Web アプリ**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b8219-119">Open Access and choose **Custom web app**.</span></span>
    
2. <span data-ttu-id="b8219-p104">アプリの名前と、Web 上のアプリの場所を入力します。[ **場所**] リストから場所を選択し、[ **作成**] を選択することもできます。</span><span class="sxs-lookup"><span data-stu-id="b8219-p104">Enter a name and the web location for your app. You can also choose a location from the **Locations** list and choose **Create**.</span></span>
    
3. <span data-ttu-id="b8219-122">[ **検索するデータを指定してください。**] ボックスに「 **問題** 」と入力し、Enter キーを押します。</span><span class="sxs-lookup"><span data-stu-id="b8219-122">Type **Issues** into the **What would you like to track?** box and then press ENTER.</span></span> 
    
   <span data-ttu-id="b8219-123">問題を追跡するのに役立つ場合があるテンプレートのリストが図 1 に示されています。</span><span class="sxs-lookup"><span data-stu-id="b8219-123">A list of templates that might be useful for tracking issues is displayed in Figure 1.</span></span>
    
   <span data-ttu-id="b8219-124">**図 1。問題に関する検索に一致するテンプレート**</span><span class="sxs-lookup"><span data-stu-id="b8219-124">**Figure 1. Templates that match the search for issues**</span></span>

   <span data-ttu-id="b8219-125">![問題の検索に一致するテンプレート](media/odc_Access15_CreateAndCustomizeWebApp_Figure01.JPG "問題の検索に一致するテンプレート")</span><span class="sxs-lookup"><span data-stu-id="b8219-125">![Templates that match the search for issues](media/odc_Access15_CreateAndCustomizeWebApp_Figure01.JPG "Templates that match the search for issues")</span></span>
  
4. <span data-ttu-id="b8219-126">[ **問題**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b8219-126">Choose **Issues**.</span></span>
    
<span data-ttu-id="b8219-127">Access は、一連のテーブルとビューを作成します。</span><span class="sxs-lookup"><span data-stu-id="b8219-127">Access creates a set of tables and views.</span></span>
  
## <a name="explore-the-app"></a><span data-ttu-id="b8219-128">アプリを探索する</span><span class="sxs-lookup"><span data-stu-id="b8219-128">Explore the app</span></span>
<span data-ttu-id="b8219-129"><a name="ac15_CreateAndCustomizeWebApp_ExploreTheApp"> </a></span><span class="sxs-lookup"><span data-stu-id="b8219-129"></span></span>

<span data-ttu-id="b8219-130">スキーマとビューがニーズを満たしているかどうかを確認するには、それらを調べる必要があります。</span><span class="sxs-lookup"><span data-stu-id="b8219-130">To understand whether the schema and views meet your needs, you should examine them.</span></span>
  
<span data-ttu-id="b8219-p105">[問題] スキーマを選択することで作成されたテーブルがタイル ウィンドウに表示されます。[問題]、[顧客]、および [従業員] テーブルがこのアプリの中心です。[問題] テーブルには各問題の情報が格納されます。各問題は、顧客に代わって従業員によって開かれ、従業員に割り当てられます。[関連の問題] と [問題に対するコメント] テーブルは、アプリの中でサポートの役割を果たします。[関連の問題] テーブルを使用して、問題同士をリンクできます。[問題に対するコメント] テーブルには、1 つの問題に関する複数のコメントが格納されます。</span><span class="sxs-lookup"><span data-stu-id="b8219-p105">The tables created by selecting the Issues schema are displayed in the Tile Pane. The Issues, Customer, and Employees tables are the main focus of the app. The Issues table stores information about each issue. Each issue is opened by and assigned to an employee on behalf of a customer. The Related Issues and Issue Comments tables play a supporting role in the app. The Related Issues table enables you to link one issue to another. The Issue Comments table stores multiple comments for a single issue.</span></span>
  
<span data-ttu-id="b8219-p106">Access デスクトップ (.accdb) データベースでは、テーブル間のリレーションシップが [ **リレーションシップ**] ウィンドウで管理されます。Access 2013 アプリでは、 **Lookup** データ型に設定されたフィールドを使用して、リレーションシップを管理します。[ **問題**] タイルを右クリックし、[ **テーブルの編集**] を選択して、[問題] テーブルのリレーションシップを調べてみましょう。</span><span class="sxs-lookup"><span data-stu-id="b8219-p106">In an Access desktop (.accdb) database, the relationships between tables are managed in the **Relationships** window. Access 2013 apps manage relationships by using fields set to the **Lookup** data type. Let's examine the relationships for the Issues table by right-clicking the **Issues** tile and selecting **Edit Table**.</span></span>
  
<span data-ttu-id="b8219-p107">[ **顧客** ] フィールドは [ **顧客** ] テーブルに関連付けられています。リレーションシップを調べるには、[ **顧客** ] フィールドを選択し、[ **ルックアップ**] を選択します。図 2 のように、 **ルックアップ ウィザード**が表示されます。</span><span class="sxs-lookup"><span data-stu-id="b8219-p107">The **Customer** field is related to the **Customers** table. To examine the relationship, select the **Customer** field and then select **Modify Lookups**. The **Lookup Wizard** is displayed, as shown in Figure 2.</span></span> 
  
<span data-ttu-id="b8219-144">**図 2。[顧客] テーブルへのリレーションシップを表示するルックアップ ウィザード**</span><span class="sxs-lookup"><span data-stu-id="b8219-144">**Figure 2. Lookup Wizard displaying the relationship to the Customers table**</span></span>

<span data-ttu-id="b8219-145">![ルックアップ ウィザードがリレーションシップを表示します。](media/odc_Access15_CreateAndCustomizeWebApp_Figure02.jpg "ルックアップ ウィザードがリレーションシップを表示します。")</span><span class="sxs-lookup"><span data-stu-id="b8219-145">![Lookup Wizard displaying the relationship](media/odc_Access15_CreateAndCustomizeWebApp_Figure02.jpg "Lookup Wizard displaying the relationship")</span></span>
  
<span data-ttu-id="b8219-146">[ルックアップ ウィザード] ダイアログ ボックスでは、[ **顧客** ] フィールドが [ **顧客** ] テーブルにリンクされており、[ **名前を名姓の順で表示** ] フィールドが [ **顧客** ] テーブルから返されることが示されています。</span><span class="sxs-lookup"><span data-stu-id="b8219-146">The Lookup Wizard dialog box shows that the **Customer** field is linked to the **Customers** table and to return the **Display Name First Last** field from the **Customers** table.</span></span> 
  
<span data-ttu-id="b8219-p108">[ **開始者** ]、[ **担当者** ]、および [ **変更者** ] フィールドは、[ **従業員** ] テーブルに関連します。他のいくつかのフィールドも **Lookup** データ型に設定されています。この場合は、Lookup データ型を使用して、フィールド内で許容される特定の値が指定されています。</span><span class="sxs-lookup"><span data-stu-id="b8219-p108">The **Opened By**, **Assigned To**, and **Changed By** fields are related to the **Employees** table. Several other fields are also set to the **Lookup** data type. In these cases, the Lookup data type is used to specify the specific values to allow for in the field.</span></span> 
  
<span data-ttu-id="b8219-p109">[ **問題** ] テーブルを閉じて、タイル ウィンドウを調べます。図 3 のように、上の 3 つのタイル ([ **問題** ]、[ **顧客** ]、および [ **従業員** ] テーブル用のタイル) は、下の 2 つのタイル ([ **関連の問題** ] および [ **問題に対するコメント** ] テーブル用のタイル) と異なって表示されています。</span><span class="sxs-lookup"><span data-stu-id="b8219-p109">Close the **Issues** table and examine the Tile Pane. The top three tiles, for the **Issues**, **Customers**, and **Employees** tables, are displayed differently than the bottom two tiles for the **Related Issues** and **Issue Comments** table, as shown in Figure 3.</span></span> 
  
<span data-ttu-id="b8219-152">**図 3。[問題] スキーマのタイル ウィンドウ**</span><span class="sxs-lookup"><span data-stu-id="b8219-152">**Figure 3. Tile Pane for the Issues schema**</span></span>

<span data-ttu-id="b8219-153">![問題のスキーマのウィンドウを並べて表示](media/odc_Access15_CreateAndCustomizeWebApp_Figure03.jpg "問題のスキーマのウィンドウを並べて表示")</span><span class="sxs-lookup"><span data-stu-id="b8219-153">![Tile Pane for the Issues schema](media/odc_Access15_CreateAndCustomizeWebApp_Figure03.jpg "Tile Pane for the Issues schema")</span></span>
  
<span data-ttu-id="b8219-154">[ **関連の問題** ] と [ **問題に対するコメント** ] テーブルは、Web ブラウザー上で非表示とするために淡色表示になっています。</span><span class="sxs-lookup"><span data-stu-id="b8219-154">The **Related Issues** and **Issue Comments** tables are dimmed because they are to be hidden from the user in the web browser.</span></span> 
  
<span data-ttu-id="b8219-p110">このアプリを使用していくつかの問題を追跡してみましょう。これを行うには、[ **アプリの起動**] をクリックし、Web ブラウザーでアプリを開きます。</span><span class="sxs-lookup"><span data-stu-id="b8219-p110">Let's use the app to track some issues. To do this, click **Launch App** to open the app in your web browser.</span></span> 
  
<span data-ttu-id="b8219-p111">アプリは、[問題] テーブルの [ **問題リスト** ] ビューを開きます。問題を開く前に、いくつかの顧客と従業員を追加することをお勧めします。[ **顧客** ] タイルをクリックし、顧客の追加を開始します。</span><span class="sxs-lookup"><span data-stu-id="b8219-p111">The app opens the **Issues List** view of the Issues table. Before adding an issue, it would be a good idea to add some customers and employees. Click the **Customers** tile to start adding customers.</span></span> 
  
<span data-ttu-id="b8219-160">図 4 に示されているように、ビュー セレクターを使用して、[ **顧客** ] テーブルで使用可能な 3 つのビューのうちの 1 つを選択します。[ **リスト**]、[ **データシート**]、[ **グループ**] とラベル付けされているビューです。</span><span class="sxs-lookup"><span data-stu-id="b8219-160">Use the View Selector to choose one of three views available for the **Customers** table, labeled **List**, **Datasheet**, and **Groups** as shown in Figure 4.</span></span> 
  
<span data-ttu-id="b8219-161">**図 4。ビュー セレクター**</span><span class="sxs-lookup"><span data-stu-id="b8219-161">**Figure 4. View Selector**</span></span>

<span data-ttu-id="b8219-162">![ビュー セレクター](media/odc_Access15_CreateAndCustomizeWebApp_Figure04.jpg "ビュー セレクター")</span><span class="sxs-lookup"><span data-stu-id="b8219-162">![View Selector](media/odc_Access15_CreateAndCustomizeWebApp_Figure04.jpg "View Selector")</span></span>
  
<span data-ttu-id="b8219-p112">[ **リスト**] を選択すると、[詳細を一覧表示] ビューである [ **顧客リスト** ] ビューが起動されます。[詳細を一覧表示] は、テーブルを作成するときに Access によって自動的に生成されるビューの 1 つです。[詳細を一覧表示] ビューを区別する主な機能は、ビューの左側に表示されるリスト ウィンドウです。リスト ウィンドウを使用して、ビューに含まれるレコードのフィルター処理とナビゲーションを行います。Access デスクトップ データベースで、検索可能なリスト ビューを実装するには、ユーザー設定コードを記述する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b8219-p112">Choosing **List** activates the **Customers List** view, which is a List Details view. List Details is one of the views Access automatically generates when you create a table. The main feature that distinguishes a List Details view is the list pane that appears on the left side of the view. The list pane is used to filter and navigate the records contained in the view. In an Access desktop database, implementing a searchable list view would require writing custom code.</span></span> 
  
<span data-ttu-id="b8219-p113">[ **データシート**] を選択すると、[ **顧客データシート** ] ビューが開きます。[データシート] は、テーブルを作成するときに Access によって自動的に生成される別の種類のビューです。[データシート] ビューは、データをスプレッドシートのような方法で簡単に入力、並べ替え、フィルター処理ができるユーザーにとって便利なビューです。</span><span class="sxs-lookup"><span data-stu-id="b8219-p113">Choosing **Datasheet** opens the **Customers Datasheet** view. Datasheet is the other kind of view Access automatically generates when you create a table. Datasheet views are useful for those who find it easier to enter, sort, and filter data in a spreadsheet-like manner.</span></span> 
  
<span data-ttu-id="b8219-p114">[グループ] を選択すると、[概要] ビューが開きます。[概要] ビューを使用して、フィールドに基づいてレコードをグループ化できます。また、オプションで、合計や平均を計算することもできます。</span><span class="sxs-lookup"><span data-stu-id="b8219-p114">Choosing Groups opens a Summary view. Summary views can be used to group records based on a field and optionally calculate a sum or average.</span></span>
  
<span data-ttu-id="b8219-p115">顧客を追加する場合は、操作バーを使用して、レコードの追加、レコードの編集、レコードの保存、レコードの削除、編集の取り消しを行います。操作バーはカスタマイズ可能なツールバーであり、図 5 のように、各ビューの上部に表示されます。</span><span class="sxs-lookup"><span data-stu-id="b8219-p115">As you're adding customers, use the Action Bar to add records, edit records, save records, delete records, and cancel edits. The Action Bar is a customizable toolbar that appears at the top of each view, as shown in Figure 5.</span></span>
  
<span data-ttu-id="b8219-175">**図 5。操作バー**</span><span class="sxs-lookup"><span data-stu-id="b8219-175">**Figure 5. Action Bar**</span></span>

<span data-ttu-id="b8219-176">![アクション バー](media/odc_Access15_CreateAndCustomizeWebApp_Figure05.jpg "アクション バー")</span><span class="sxs-lookup"><span data-stu-id="b8219-176">![Action Bar](media/odc_Access15_CreateAndCustomizeWebApp_Figure05.jpg "Action Bar")</span></span>
  
<span data-ttu-id="b8219-p116">顧客と従業員の追加が終了した後、[問題リスト] ビューを開いて、問題の追加を開始します。顧客の名前を [顧客] ボックスに入力すると、図 6 のように、1 つ以上の顧客名が表示されます。</span><span class="sxs-lookup"><span data-stu-id="b8219-p116">Once you've added some customers and employees open the Issues List view and start adding an issue. As you type the name of a customer into the into the Customer box, one or more of the customer names will appear, as shown in Figure 6.</span></span>
  
<span data-ttu-id="b8219-179">**図 6。オートコンプリート コントロール**</span><span class="sxs-lookup"><span data-stu-id="b8219-179">**Figure 6. AutoComplete control**</span></span>

<span data-ttu-id="b8219-180">![オートコンプリートのコントロール](media/odc_Access15_CreateAndCustomizeWebApp_Figure06.jpg "オートコンプリートのコントロール")</span><span class="sxs-lookup"><span data-stu-id="b8219-180">![AutoComplete control](media/odc_Access15_CreateAndCustomizeWebApp_Figure06.jpg "AutoComplete control")</span></span>
  
<span data-ttu-id="b8219-p117">[顧客] ボックスは、オートコンプリート コントロールです。オートコンプリート コントロールでは、ボックスに入力されている内容に一致するレコードのリストが表示されます。これにより、データ入力の正確性が確保されます。</span><span class="sxs-lookup"><span data-stu-id="b8219-p117">The Customer box is an AutoComplete control. The AutoComplete control displays a list of records that match what you're typing into the box. This helps ensure the accuracy of data entry.</span></span>
  
## <a name="customize-the-app"></a><span data-ttu-id="b8219-184">アプリをカスタマイズする</span><span class="sxs-lookup"><span data-stu-id="b8219-184">Customize the app</span></span>
<span data-ttu-id="b8219-185"><a name="ac15_CreateAndCustomizeWebApp_CustomizeTheApp"> </a></span><span class="sxs-lookup"><span data-stu-id="b8219-185"></span></span>

<span data-ttu-id="b8219-p118">ここまで、アプリについて紹介してきましたが、[問題リスト] ビューに顧客の連絡先情報が含まれていません。ここで、問題を作成するときに顧客の勤務先電話番号を [問題] テーブルに追加するように、アプリをカスタマイズしてみましょう。</span><span class="sxs-lookup"><span data-stu-id="b8219-p118">Now that you've taken a tour of the app, you notice that the Issues List view doesn't contain contact information for the customer. Let's customize the app to add the customer's work phone to the Issues table as the issue is being created.</span></span>
  
### <a name="to-add-a-field-to-the-issues-table"></a><span data-ttu-id="b8219-188">[問題] テーブルにフィールドを追加するには</span><span class="sxs-lookup"><span data-stu-id="b8219-188">To add a field to the Issues table</span></span>

1. <span data-ttu-id="b8219-189">Access でアプリを開きます。</span><span class="sxs-lookup"><span data-stu-id="b8219-189">Open the app in Access.</span></span>
    
2. <span data-ttu-id="b8219-190">[ **問題**] タイル、[ **設定/アクション**] アイコン、[ **テーブルの編集**] の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="b8219-190">Choose the **Issues** tile, choose the **Settings/Action** icon, and then choose **Edit Table**.</span></span>
    
3. <span data-ttu-id="b8219-191">[ **フィールド名**] 列の最初の空白セルに「 **連絡先番号** 」と入力します。</span><span class="sxs-lookup"><span data-stu-id="b8219-191">Enter **Contact Number** in the first blank cell in the **Field Name** column.</span></span> 
    
4. <span data-ttu-id="b8219-192">[ **データ型**] 列で [ **短いテキスト**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b8219-192">Choose **Short Text** in the **Data Type** column.</span></span> 
    
5. <span data-ttu-id="b8219-193">[ **上書き保存**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b8219-193">Choose **Save**.</span></span>
    
6. <span data-ttu-id="b8219-194">[問題] テーブルを閉じます。</span><span class="sxs-lookup"><span data-stu-id="b8219-194">Close the Issues table.</span></span>
    
<span data-ttu-id="b8219-195">電話番号を格納するフィールドが作成されました。ここで、連絡先情報を参照するためのデータ マクロを作成しましょう。</span><span class="sxs-lookup"><span data-stu-id="b8219-195">Now that we have field in which to store the phone number, let's create a data macro to look up the contact information.</span></span>
  
### <a name="to-create-the-data-macro-to-look-up-contact-information"></a><span data-ttu-id="b8219-196">連絡先情報を参照するためのデータ マクロを作成するには</span><span class="sxs-lookup"><span data-stu-id="b8219-196">To create the data macro to look up contact information</span></span>

1. <span data-ttu-id="b8219-197">[ **作成**] グループで、[ **詳細設定**]、[ **データ マクロ**] の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="b8219-197">In the **Create** group, choose **Advanced**, and then choose **Data Macro**.</span></span>
    
2. <span data-ttu-id="b8219-198">[ **パラメーターの作成**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b8219-198">Choose **Create Parameter**.</span></span>
    
3. <span data-ttu-id="b8219-p119">[ **名前**] ボックスに「 **CustID** 」と入力します。[ **型**] ドロップダウンで、[ **数値 (浮動小数点)**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b8219-p119">In the **Name** box, enter **CustID**. In the **Type** dropdown, choose **Number (Floating Decimal).**</span></span>
    
4. <span data-ttu-id="b8219-201">[ **新しいアクションの追加**] ドロップダウンから [ **レコードの参照** ] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b8219-201">From the **Add New Action** dropdown, choose **LookupRecord**.</span></span> 
    
5. <span data-ttu-id="b8219-202">[ **参照するレコードが含まれるテーブル/クエリ**] ドロップダウンで、[ **顧客** ] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b8219-202">In the **Look Up A Record In** dropdown, choose **Customers**.</span></span> 
    
6. <span data-ttu-id="b8219-203">[ **条件式**] ボックスに「 **[顧客].[ID]=[CustID]** 」と入力します。</span><span class="sxs-lookup"><span data-stu-id="b8219-203">In the **Where Condition** box, enter **[Customers].[ID]=[CustID]**.</span></span> 
    
7. <span data-ttu-id="b8219-204">[ **新しいアクションの追加**] ドロップダウンから [ **戻り変数の設定** ] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b8219-204">Choose **SetReturnVar** from the **Add New Action** dropdown.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="b8219-p120">[!メモ] 2 つの [ **新しいアクションの追加**] ドロップダウンが表示されます。1 つは [ **レコードの参照** ] ブロックの内側にあり、もう 1 つは [ **レコードの参照** ] ブロックの外側にあります。図 7 に示されているように、[ **レコードの参照** ] ブロックの内側にある [ **新しいアクションの追加**] ドロップダウンを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b8219-p120">You'll see two **Add New Action** dropdowns, one within the **LookupRecord** block, and another outside the **LookupRecord** block. You should choose the **Add New Action** dropdown within the **LookupRecord** block, as shown in Figure 7.</span></span> 
  
   <span data-ttu-id="b8219-207">**図 7。[新しいアクションの追加] ドロップダウン**</span><span class="sxs-lookup"><span data-stu-id="b8219-207">**Figure 7. Add New Action dropdown**</span></span>

   <span data-ttu-id="b8219-208">![新しいアクションの追加のドロップダウン リスト](media/odc_Access15_CreateAndCustomizeWebApp_Figure07.jpg "新しいアクションの追加のドロップダウン リスト")</span><span class="sxs-lookup"><span data-stu-id="b8219-208">![Add New Action dropdown](media/odc_Access15_CreateAndCustomizeWebApp_Figure07.jpg "Add New Action dropdown")</span></span>
  
8. <span data-ttu-id="b8219-209">[ **名前**] ボックスに「 **連絡先電話番号** 」と入力します。</span><span class="sxs-lookup"><span data-stu-id="b8219-209">In the **Name** box, enter **ContactPhone**.</span></span> 
    
9. <span data-ttu-id="b8219-210">[ **式**] ボックスに「 **[顧客].[勤務先電話番号]** 」と入力します。</span><span class="sxs-lookup"><span data-stu-id="b8219-210">In the **Expression** box, enter **[Customers].[Work Phone]**.</span></span> 
    
10. <span data-ttu-id="b8219-p121">[ **上書き保存**] を選択します。[ **マクロ名**] ボックスに「 **GetContactPhone** 」と入力し、[ **OK**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b8219-p121">Choose **Save**. Enter **GetContactPhone** in the **Macro Name** box and then choose **OK**.</span></span>
    
    <span data-ttu-id="b8219-213">マクロは、図 8 のようになります。</span><span class="sxs-lookup"><span data-stu-id="b8219-213">The macro should resemble the macro shown in Figure 8.</span></span>
    
    <span data-ttu-id="b8219-214">**図 8。GetContactPhone データ マクロ**</span><span class="sxs-lookup"><span data-stu-id="b8219-214">**Figure 8. GetContactPhone data macro**</span></span>

    <span data-ttu-id="b8219-215">![GetContactPhone データ マクロ](media/odc_Access15_CreateAndCustomizeWebApp_Figure08.jpg "GetContactPhone データ マクロ")</span><span class="sxs-lookup"><span data-stu-id="b8219-215">![GetContactPhone data macro](media/odc_Access15_CreateAndCustomizeWebApp_Figure08.jpg "GetContactPhone data macro")</span></span>
  
11. <span data-ttu-id="b8219-216">マクロのデザイン ビューを閉じます。</span><span class="sxs-lookup"><span data-stu-id="b8219-216">Close macro Design View.</span></span>
    
<span data-ttu-id="b8219-217">これで、[ **連絡先番号** ] フィールドを [問題リスト] フォームに追加する準備ができました。</span><span class="sxs-lookup"><span data-stu-id="b8219-217">Now we're ready to add the **Contact Number** field to the Issues List form.</span></span> 
  
### <a name="to-add-the-contact-number-field-to-the-issues-list-form"></a><span data-ttu-id="b8219-218">[連絡先番号] フィールドを [問題リスト] フォームに追加するには</span><span class="sxs-lookup"><span data-stu-id="b8219-218">To add the Contact Number field to the Issues List form</span></span>

1. <span data-ttu-id="b8219-p122">[ **問題** ] テーブルを選択します。これにより、[問題リスト] フォームが選択されます。</span><span class="sxs-lookup"><span data-stu-id="b8219-p122">Choose the **Issues** table. This chooses the Issues list form.</span></span> 
    
2. <span data-ttu-id="b8219-221">ビュー セレクターで [ **リスト** ] を選択し、[ **設定/アクション**] アイコン、[ **編集**] の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="b8219-221">In the View selector, choose **List**, choose the **Settings/Action** icon, and then choose **Edit**.</span></span>
    
3. <span data-ttu-id="b8219-222">[ **フィールド リスト**] ウィンドウからフォーム上の連絡先番号の表示場所まで [ **連絡先番号** ] フィールドをドラッグします。</span><span class="sxs-lookup"><span data-stu-id="b8219-222">Drag the **Contact Number** field form the **Field List** pane to the location on the form where you want the contact number to be displayed.</span></span> 
    
4. <span data-ttu-id="b8219-223">[ **連絡先番号**] テキスト ボックスを選択し、[ **データ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b8219-223">Choose the **Contact Number** text box, and then click **Data**.</span></span> 
    
5. <span data-ttu-id="b8219-224">[ **コントロール名**] ボックスに「 **CustomerContact** 」と入力し、[ **データ**] ポップアップを閉じます。</span><span class="sxs-lookup"><span data-stu-id="b8219-224">In the **Control Name** box, enter **CustomerContact** and then close the **Data** popup.</span></span> 
    
6. <span data-ttu-id="b8219-225">[ **上書き保存**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b8219-225">Choose **Save**.</span></span>
    
<span data-ttu-id="b8219-p123">ここで、[ **勤務先電話番号** ] フィールドを [ **顧客** ] テーブルから [ **問題** ] テーブルの [ **連絡先電話番号** ] フィールドにコピーするユーザー インターフェイス (UI) マクロを記述する必要があります。マクロの記述場所として、 **CustomerAutocomplete** コントロールの **更新後処理** イベントが適しています。</span><span class="sxs-lookup"><span data-stu-id="b8219-p123">Now we should write a user interface (UI) macro that copies the **Work Phone** field from the **Customers** table into the **Contact Phone** field of the **Issues** table. The **After Update** event of the **CustomerAutocomplete** control is a good location for the macro.</span></span> 
  
### <a name="to-create-the-afterupdate-macro"></a><span data-ttu-id="b8219-228">AfterUpdate マクロを作成するには</span><span class="sxs-lookup"><span data-stu-id="b8219-228">To create the AfterUpdate macro</span></span>

1. <span data-ttu-id="b8219-229">[ **CustomerAutocomplete** ] コントロール、[ **アクション**] ボタン、[ **更新後処理**] の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="b8219-229">Choose the **CustomerAutocomplete** control, choose the **Actions** button, and then choose **After Update**.</span></span> 
    
    <span data-ttu-id="b8219-230">マクロのデザイン ビューに空白のマクロが開かれます。</span><span class="sxs-lookup"><span data-stu-id="b8219-230">A blank macro is opened in macro Design View.</span></span>
    
2. <span data-ttu-id="b8219-231">[ **新しいアクションの追加**] ドロップダウンから [ **データマクロの実行** ] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b8219-231">From the **Add New Action** dropdown, choose **RunDataMacro**.</span></span> 
    
3. <span data-ttu-id="b8219-232">[ **マクロ名**] ドロップダウンで、[ **GetContactPhone** ] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b8219-232">In the **Macro Name** dropdown, choose **GetContactPhone**.</span></span> 
    
4. <span data-ttu-id="b8219-233">[ **CustID**] ボックスに「 **[CustomerAutocomplete]** 」と入力します。</span><span class="sxs-lookup"><span data-stu-id="b8219-233">In the **CustID** box, enter **[CustomerAutocomplete]**.</span></span> 
    
5. <span data-ttu-id="b8219-234">[ **ローカル変数の設定**] ボックスに「 **電話番号** 」と入力します。</span><span class="sxs-lookup"><span data-stu-id="b8219-234">In the **SetLocalVar** box, enter **Phone**.</span></span> 
    
    <span data-ttu-id="b8219-235">以前に作成された GetContactPhone データ マクロを選択した場合、Access によってパラメーター名が自動的に設定され、マクロの変数が返されます。</span><span class="sxs-lookup"><span data-stu-id="b8219-235">When you chose the GetContactPhone data macro that was created earlier, Access automatically filled in the parameter name and return variable for the macro.</span></span>
    
    <span data-ttu-id="b8219-236">顧客の電話番号は、"電話番号" という名前の変数に格納されます。</span><span class="sxs-lookup"><span data-stu-id="b8219-236">The phone number for the customer is stored in a variable named Phone.</span></span>
    
6. <span data-ttu-id="b8219-237">[ **新しいアクションの追加**] ドロップダウンから [ **プロパティの設定** ] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b8219-237">From the **Add New Action** dropdown, choose **SetProperty**.</span></span> 
    
7. <span data-ttu-id="b8219-238">[ **コントロール名**] ボックスに「 **CustomerContact** 」と入力します。</span><span class="sxs-lookup"><span data-stu-id="b8219-238">In the **Control Name** box, enter **CustomerContact**.</span></span> 
    
8. <span data-ttu-id="b8219-239">[ **プロパティ**] ドロップダウンで、[ **値** ] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b8219-239">In the **Property** dropdown, choose **Value**.</span></span> 
    
9. <span data-ttu-id="b8219-240">[ **値**] ボックスに「 **=[Phone]** 」と入力します。</span><span class="sxs-lookup"><span data-stu-id="b8219-240">In the **Value** box, enter **=[Phone]**.</span></span> 
    
10. <span data-ttu-id="b8219-241">[ **上書き保存**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b8219-241">Choose **Save**.</span></span>
    
    <span data-ttu-id="b8219-242">マクロは、図 9 のようになります。</span><span class="sxs-lookup"><span data-stu-id="b8219-242">The macro should resemble the macro shown in Figure 9.</span></span>
    
    <span data-ttu-id="b8219-243">**図 9。更新後処理マクロ**</span><span class="sxs-lookup"><span data-stu-id="b8219-243">**Figure 9. After Update macro**</span></span>

    <span data-ttu-id="b8219-244">![更新後のマクロ](media/odc_Access15_CreateAndCustomizeWebApp_Figure09.jpg "更新後のマクロ")</span><span class="sxs-lookup"><span data-stu-id="b8219-244">![After Update macro](media/odc_Access15_CreateAndCustomizeWebApp_Figure09.jpg "After Update macro")</span></span>
  
11. <span data-ttu-id="b8219-245">マクロのデザイン ビューを閉じます。</span><span class="sxs-lookup"><span data-stu-id="b8219-245">Close macro Design View.</span></span>
    
12. <span data-ttu-id="b8219-p124">[問題リスト] ビューを閉じます。変更内容の保存を求めるプロンプトが表示された場合、[ **はい**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b8219-p124">Close the Issues List view. Choose **Yes** when you are prompted to save your changes.</span></span> 
    
<span data-ttu-id="b8219-248">カスタマイズをテストする準備ができました。</span><span class="sxs-lookup"><span data-stu-id="b8219-248">Now we're ready to text the customization.</span></span> <span data-ttu-id="b8219-249">[ **アプリの起動**] をクリックして、Web ブラウザーでアプリを開いて、新しい問題を追加します。</span><span class="sxs-lookup"><span data-stu-id="b8219-249">Click **Launch App** to open the app in your web browser and then add a new issue.</span></span> <span data-ttu-id="b8219-250">**連絡先番号**] ボックスは、図 10 に示すように、顧客名を入力した後に自動的を更新します。</span><span class="sxs-lookup"><span data-stu-id="b8219-250">The **Contact Number** box updates automatically after the customer name is entered,  as shown in Figure 10.</span></span> 
  
<span data-ttu-id="b8219-251">**図 10。電話番号が更新された [問題] ビュー**</span><span class="sxs-lookup"><span data-stu-id="b8219-251">**Figure 10. Issues view updated with phone number**</span></span>

<span data-ttu-id="b8219-252">![電話番号を使用して更新の問題の表示](media/odc_Access15_CreateAndCustomizeWebApp_Figure10.jpg "電話番号を使用して更新の問題の表示")</span><span class="sxs-lookup"><span data-stu-id="b8219-252">![Issues view updated with phone number](media/odc_Access15_CreateAndCustomizeWebApp_Figure10.jpg "Issues view updated with phone number")</span></span>
  
## <a name="conclusion"></a><span data-ttu-id="b8219-253">終わりに</span><span class="sxs-lookup"><span data-stu-id="b8219-253">Conclusion</span></span>

<span data-ttu-id="b8219-p126">Access Web アプリの作成にすぐに着手するには、 に含まれるスキーマ テンプレートの 1 つを使用することをお勧めします。自動的に作成されるビューには、Access デーストップ データベースへの実装にユーザー設定コードが必要とされる高度な機能が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b8219-p126">Using one of the schema templates included with is a good way to jump start the creation of an Access web app. The views that are automatically created for you contain advanced functionally that requires custom code to implement in a Access desktop database.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b8219-256">関連項目</span><span class="sxs-lookup"><span data-stu-id="b8219-256">See also</span></span>

- [<span data-ttu-id="b8219-257">開発者へのアクセスの新機能</span><span class="sxs-lookup"><span data-stu-id="b8219-257">What's new for Access 2013 developers</span></span>](https://msdn.microsoft.com/library/df778f51-d65e-4c30-b618-65003ceb39b3%28Office.15%29.aspx) 
- [<span data-ttu-id="b8219-258">Access カスタム Web アプリ リファレンス</span><span class="sxs-lookup"><span data-stu-id="b8219-258">Access custom web app reference</span></span>](access-custom-web-app-reference.md)
  

