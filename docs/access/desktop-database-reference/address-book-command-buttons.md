---
title: アドレス帳のコマンド ボタン
TOCTitle: Address Book command buttons
ms:assetid: bcea6f53-3e36-b067-03c2-b157ed02d41d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249908(v=office.15)
ms:contentKeyID: 48547422
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 09f2513a3c541c76352e773f7f2a8f0c24f78850
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282479"
---
# <a name="address-book-command-buttons"></a><span data-ttu-id="03de0-102">アドレス帳のコマンド ボタン</span><span class="sxs-lookup"><span data-stu-id="03de0-102">Address Book command buttons</span></span>


<span data-ttu-id="03de0-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="03de0-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="03de0-104">アドレス帳アプリケーションには次のコマンド ボタンがあります。</span><span class="sxs-lookup"><span data-stu-id="03de0-104">The Address Book application includes the following command buttons:</span></span>

- <span data-ttu-id="03de0-105">クエリをデータベースに送信するための **[検索]** ボタン。</span><span class="sxs-lookup"><span data-stu-id="03de0-105">A **Find** button to submit a query to the database.</span></span>

- <span data-ttu-id="03de0-106">新しい検索を開始する前にテキスト ボックスをクリアするための **[クリア]** ボタン。</span><span class="sxs-lookup"><span data-stu-id="03de0-106">A **Clear** button to clear the text boxes before starting a new search.</span></span>

- <span data-ttu-id="03de0-107">従業員レコードに対する変更を保存するための  **[プロファイルの更新]** ボタン。</span><span class="sxs-lookup"><span data-stu-id="03de0-107">An **Update Profile** button to save changes to an employee record.</span></span>

- <span data-ttu-id="03de0-108">変更を破棄するための **[変更の取り消し]** ボタン。</span><span class="sxs-lookup"><span data-stu-id="03de0-108">A **Cancel Changes** button to discard changes.</span></span>

## <a name="find-button"></a><span data-ttu-id="03de0-109">[検索] ボタン</span><span class="sxs-lookup"><span data-stu-id="03de0-109">Find Button</span></span>

<span data-ttu-id="03de0-110">[**検索**] ボタンをクリックすると\_、VBScript 検索の OnClick Sub プロシージャがアクティブになり、SQL クエリが作成されて送信されます。</span><span class="sxs-lookup"><span data-stu-id="03de0-110">Clicking the **Find** button activates the VBScript Find\_OnClick Sub procedure, which builds and sends the SQL query.</span></span> <span data-ttu-id="03de0-111">このボタンをクリックすると、データ グリッドが設定されます。</span><span class="sxs-lookup"><span data-stu-id="03de0-111">Clicking this button populates the data grid.</span></span>

## <a name="building-the-sql-query"></a><span data-ttu-id="03de0-112">SQL クエリの作成</span><span class="sxs-lookup"><span data-stu-id="03de0-112">Building the SQL Query</span></span>

<span data-ttu-id="03de0-113">OnClick Sub の検索\_プロシージャの最初の部分では、sql クエリを作成します。これは、1つの文字列をグローバル sql SELECT ステートメントに追加することによって行います。</span><span class="sxs-lookup"><span data-stu-id="03de0-113">The first part of the Find\_OnClick Sub procedure builds the SQL query, one phrase at a time, by appending text strings to a global SQL SELECT statement.</span></span> <span data-ttu-id="03de0-114">この Sub プロシージャは、データ ソース テーブルからすべてのデータ行を要求する SQL SELECT ステートメントに変数を設定することから始まります。</span><span class="sxs-lookup"><span data-stu-id="03de0-114">It begins by setting the variable to a SQL SELECT statement that requests all rows of data from the data source table.</span></span> <span data-ttu-id="03de0-115">次に、ページ上の 4 つの入力ボックスをそれぞれスキャンします。</span><span class="sxs-lookup"><span data-stu-id="03de0-115">Next, the Sub procedure scans each of the four input boxes on the page.</span></span>

<span data-ttu-id="03de0-116">プログラムでは、SQL ステートメントの作成時にワードを使用するため、クエリは完全一致ではなく、サブ文字列検索になります。</span><span class="sxs-lookup"><span data-stu-id="03de0-116">Because the program uses the word in building the SQL statements, the queries are substring searches rather than exact matches.</span></span>

<span data-ttu-id="03de0-117">たとえば、[ **姓** ] ボックスに "Berge" が入力され、[ **タイトル** ] ボックスに "Program Manager" が入力された場合、SQL ステートメント (値) は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="03de0-117">For example, if the **Last Name** box contained the entry "Berge" and the **Title** box contained the entry "Program Manager", the SQL statement (value of ) would read:</span></span>

```vb 
 
Select FirstName, LastName, Title, Email, Building, Room, Phone from Employee where lastname like 'Berge%' and title like 'Program Manager%' 
```

<span data-ttu-id="03de0-118">クエリが成功すると、"Berge" という文字を含む姓  (Berge や Berger など) と、"Program Manager" という単語を含むタイトル (Program Manager, Advanced Technologies など) が HTML データ グリッドに表示されます。</span><span class="sxs-lookup"><span data-stu-id="03de0-118">If the query was successful, all persons with a last name containing the text "Berge" (such as Berge and Berger) and with a title containing the words "Program Manager" (for example, Program Manager, Advanced Technologies) are displayed in the HTML data grid.</span></span>

## <a name="preparing-and-sending-the-query"></a><span data-ttu-id="03de0-119">クエリの準備と送信</span><span class="sxs-lookup"><span data-stu-id="03de0-119">Preparing and Sending the Query</span></span>

<span data-ttu-id="03de0-120">OnClick Sub の検索\_プロシージャの最後の部分は、2つのステートメントで構成されます。</span><span class="sxs-lookup"><span data-stu-id="03de0-120">The last part of the Find\_OnClick Sub procedure consists of two statements.</span></span> <span data-ttu-id="03de0-121">最初のステートメントは、RDS.DataControl オブジェクトの SQL プロパティを、動的に作成される SQL クエリと等しくなるように割り当てます。</span><span class="sxs-lookup"><span data-stu-id="03de0-121">The first statement assigns the SQL property of the RDS.DataControl object equal to the dynamically built SQL query.</span></span> <span data-ttu-id="03de0-122">2 番目のステートメントでは、**RDS.DataControl** オブジェクト ( ) でデータベースにクエリを実行した後、クエリの新しい結果をグリッドに表示します。</span><span class="sxs-lookup"><span data-stu-id="03de0-122">The second statement causes the **RDS.DataControl** object () to query the database, and then display the new results of the query in the grid.</span></span>

```vb 
 
Sub Find_OnClick 
 '... 
 DC1.SQL = myQuery 
 DC1.Refresh 
End Sub 
```

## <a name="update-profile-button"></a><span data-ttu-id="03de0-123">[プロファイルの更新] ボタン</span><span class="sxs-lookup"><span data-stu-id="03de0-123">Update Profile Button</span></span>

<span data-ttu-id="03de0-124">[**プロファイルの更新**] ボタンをクリックする\_と、VBScript update OnClick Sub プロシージャがアクティブになります。これにより、RDS が実行されます。DataControl オブジェクトの () SubmitChanges メソッドおよび Refresh メソッド</span><span class="sxs-lookup"><span data-stu-id="03de0-124">Clicking the **Update Profile** button activates the VBScript Update\_OnClick Sub procedure, which executes the RDS.DataControl object's () SubmitChanges and Refresh methods.</span></span>

```vb 
 
Sub Update_OnClick 
 DC1.SubmitChanges 
 DC1.Refresh 
End Sub 
```

<span data-ttu-id="03de0-125">DC1。SubmitChanges が実行されると、リモートデータサービスはすべての更新情報をパッケージ化し、HTTP を介してサーバーに送信します。</span><span class="sxs-lookup"><span data-stu-id="03de0-125">When DC1.SubmitChanges executes, the Remote Data Service packages all the update information and sends it to the server via HTTP.</span></span> <span data-ttu-id="03de0-126">update は all または nothing です。更新の一部が失敗した場合、変更は一切行われず、ステータスメッセージが返されます。</span><span class="sxs-lookup"><span data-stu-id="03de0-126">The update is all-or-nothing; if a part of the update is unsuccessful, none of the changes is made, and a status message is returned.</span></span> <span data-ttu-id="03de0-127">が実行されると、リモートデータサービスはすべての更新情報をパッケージ化し、HTTP を介してサーバーに送信します。</span><span class="sxs-lookup"><span data-stu-id="03de0-127">executes, the Remote Data Service packages all the update information and sends it to the server via HTTP.</span></span> <span data-ttu-id="03de0-128">update は all または nothing です。更新の一部が失敗した場合、変更は一切行われず、ステータスメッセージが返されます。</span><span class="sxs-lookup"><span data-stu-id="03de0-128">The update is all-or-nothing; if a part of the update is unsuccessful, none of the changes is made, and a status message is returned.</span></span> <span data-ttu-id="03de0-129">DC1.リモートデータサービスを使用して**SubmitChanges**を実行した後に更新する必要はありませんが、最新のデータが保証されます。</span><span class="sxs-lookup"><span data-stu-id="03de0-129">DC1.Refresh isn't necessary after **SubmitChanges** with Remote Data Service, but it ensures fresh data.</span></span>

## <a name="cancel-changes-button"></a><span data-ttu-id="03de0-130">[変更の取り消し] ボタン</span><span class="sxs-lookup"><span data-stu-id="03de0-130">Cancel Changes Button</span></span>

<span data-ttu-id="03de0-131">**[変更のキャンセル]** をクリック\_すると、VBScript のキャンセル OnClick Sub プロシージャがアクティブになります。これにより、RDS が実行されます。DataControl オブジェクト (CancelUpdate メソッド)。</span><span class="sxs-lookup"><span data-stu-id="03de0-131">Clicking **Cancel Changes** activates the VBScript Cancel\_OnClick Sub procedure, which executes the RDS.DataControl object's ( CancelUpdate method.</span></span>

```vb 
 
Sub Cancel_OnClick 
 DC1.CancelUpdate 
End Sub 
```

<span data-ttu-id="03de0-p105">実行すると、前回のクエリまたは更新後にユーザーがデータ グリッドの従業員レコードに対して行ったすべての編集が破棄されます。</span><span class="sxs-lookup"><span data-stu-id="03de0-p105">When executes, it discards any edits that a user has made to an employee record on the data grid since the last query or update. It restores the original values.</span></span>

