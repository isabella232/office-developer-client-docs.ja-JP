---
title: Address Book のコマンド ボタン
TOCTitle: Address Book Command Buttons
ms:assetid: bcea6f53-3e36-b067-03c2-b157ed02d41d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249908(v=office.15)
ms:contentKeyID: 48547422
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 15a79db455032ddf2eb9fa0d9555d8f7a4959313
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479407"
---
# <a name="address-book-command-buttons"></a><span data-ttu-id="fa8d5-102">Address Book のコマンド ボタン</span><span class="sxs-lookup"><span data-stu-id="fa8d5-102">Address Book Command Buttons</span></span>


<span data-ttu-id="fa8d5-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="fa8d5-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="fa8d5-104">アドレス帳アプリケーションには次のコマンド ボタンがあります。</span><span class="sxs-lookup"><span data-stu-id="fa8d5-104">The Address Book application includes the following command buttons:</span></span>

  - <span data-ttu-id="fa8d5-105">クエリをデータベースに送信するための [検索] ボタン。</span><span class="sxs-lookup"><span data-stu-id="fa8d5-105">A Find button to submit a query to the database.</span></span>

  - <span data-ttu-id="fa8d5-106">新しい検索を開始する前にテキスト ボックスをクリアするための **[クリア]** ボタン。</span><span class="sxs-lookup"><span data-stu-id="fa8d5-106">A **Clear** button to clear the text boxes before starting a new search.</span></span>

  - <span data-ttu-id="fa8d5-107">従業員レコードに対する変更を保存するための  [プロファイルの更新] ボタン。</span><span class="sxs-lookup"><span data-stu-id="fa8d5-107">An Update Profile button to save changes to an employee record.</span></span>

  - <span data-ttu-id="fa8d5-108">変更を破棄するための [変更の取り消し] ボタン。</span><span class="sxs-lookup"><span data-stu-id="fa8d5-108">A Cancel Changes button to discard changes.</span></span>

## <a name="find-button"></a><span data-ttu-id="fa8d5-109">[検索] ボタン</span><span class="sxs-lookup"><span data-stu-id="fa8d5-109">Find Button</span></span>

<span data-ttu-id="fa8d5-110">VBScript の検索をアクティブに、[**検索**] ボタンをクリックすると\_OnClick の Sub プロシージャは、ビルドし、SQL クエリを送信します。</span><span class="sxs-lookup"><span data-stu-id="fa8d5-110">Clicking the **Find** button activates the VBScript Find\_OnClick Sub procedure, which builds and sends the SQL query.</span></span> <span data-ttu-id="fa8d5-111">このボタンをクリックすると、データ グリッドが設定されます。</span><span class="sxs-lookup"><span data-stu-id="fa8d5-111">Clicking this button populates the data grid.</span></span>

## <a name="building-the-sql-query"></a><span data-ttu-id="fa8d5-112">SQL クエリの作成</span><span class="sxs-lookup"><span data-stu-id="fa8d5-112">Building the SQL Query</span></span>

<span data-ttu-id="fa8d5-113">検索する文字列の最初の部分\_OnClick Sub プロシージャはテキスト文字列をグローバル SQL SELECT ステートメントに追加することによって、一度に 1 つの語句であり、SQL クエリを構築します。</span><span class="sxs-lookup"><span data-stu-id="fa8d5-113">The first part of the Find\_OnClick Sub procedure builds the SQL query, one phrase at a time, by appending text strings to a global SQL SELECT statement.</span></span> <span data-ttu-id="fa8d5-114">この Sub プロシージャは、データ ソース テーブルからすべてのデータ行を要求する SQL SELECT ステートメントに変数を設定することから始まります。</span><span class="sxs-lookup"><span data-stu-id="fa8d5-114">It begins by setting the variable to a SQL SELECT statement that requests all rows of data from the data source table.</span></span> <span data-ttu-id="fa8d5-115">次に、ページ上の 4 つの入力ボックスをそれぞれスキャンします。</span><span class="sxs-lookup"><span data-stu-id="fa8d5-115">Next, the Sub procedure scans each of the four input boxes on the page.</span></span>

<span data-ttu-id="fa8d5-116">プログラムでは、SQL ステートメントの作成時にワードを使用するため、クエリは完全一致ではなく、サブ文字列検索になります。</span><span class="sxs-lookup"><span data-stu-id="fa8d5-116">Because the program uses the word in building the SQL statements, the queries are substring searches rather than exact matches.</span></span>

<span data-ttu-id="fa8d5-117">たとえば、[ **姓** ] ボックスに "Berge" が入力され、[ **タイトル** ] ボックスに "Program Manager" が入力された場合、SQL ステートメント (値) は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="fa8d5-117">For example, if the **Last Name** box contained the entry "Berge" and the **Title** box contained the entry "Program Manager", the SQL statement (value of ) would read:</span></span>

```vb 
 
Select FirstName, LastName, Title, Email, Building, Room, Phone from Employee where lastname like 'Berge%' and title like 'Program Manager%' 
```

<span data-ttu-id="fa8d5-118">クエリが成功すると、"Berge" という文字を含む姓 (Berge や Berger など) と、"Program Manager" という単語を含むタイトル (Program Manager, Advanced Technologies など) が HTML データ グリッドに表示されます。</span><span class="sxs-lookup"><span data-stu-id="fa8d5-118">If the query was successful, all persons with a last name containing the text "Berge" (such as Berge and Berger) and with a title containing the words "Program Manager" (for example, Program Manager, Advanced Technologies) are displayed in the HTML data grid.</span></span>

## <a name="preparing-and-sending-the-query"></a><span data-ttu-id="fa8d5-119">クエリの準備と送信</span><span class="sxs-lookup"><span data-stu-id="fa8d5-119">Preparing and Sending the Query</span></span>

<span data-ttu-id="fa8d5-120">検索する文字列の最後の部分\_OnClick Sub プロシージャは、2 つのステートメントで構成されています。</span><span class="sxs-lookup"><span data-stu-id="fa8d5-120">The last part of the Find\_OnClick Sub procedure consists of two statements.</span></span> <span data-ttu-id="fa8d5-121">最初のステートメントは、RDS.DataControl オブジェクトの SQL プロパティを、動的に作成される SQL クエリと等しくなるように割り当てます。</span><span class="sxs-lookup"><span data-stu-id="fa8d5-121">The first statement assigns the SQL property of the RDS.DataControl object equal to the dynamically built SQL query.</span></span> <span data-ttu-id="fa8d5-122">2 番目のステートメントでは、 **RDS.DataControl** オブジェクト ( ) でデータベースにクエリを実行した後、クエリの新しい結果をグリッドに表示します。</span><span class="sxs-lookup"><span data-stu-id="fa8d5-122">The second statement causes the **RDS.DataControl** object () to query the database, and then display the new results of the query in the grid.</span></span>

```vb 
 
Sub Find_OnClick 
 '... 
 DC1.SQL = myQuery 
 DC1.Refresh 
End Sub 
```

## <a name="update-profile-button"></a><span data-ttu-id="fa8d5-123">[プロファイルの更新] ボタン</span><span class="sxs-lookup"><span data-stu-id="fa8d5-123">Update Profile Button</span></span>

<span data-ttu-id="fa8d5-124">VBScript の更新プログラムをアクティブに、[**プロファイルの更新**] ボタンをクリックすると\_OnClick Sub プロシージャは、実行 rds.DataControl オブジェクトの () SubmitChanges メソッドと更新メソッド。</span><span class="sxs-lookup"><span data-stu-id="fa8d5-124">Clicking the **Update Profile** button activates the VBScript Update\_OnClick Sub procedure, which executes the RDS.DataControl object's () SubmitChanges and Refresh methods.</span></span>

```vb 
 
Sub Update_OnClick 
 DC1.SubmitChanges 
 DC1.Refresh 
End Sub 
```

<span data-ttu-id="fa8d5-125">DC1 です。SubmitChanges を実行、リモート データ サービスは、すべての更新プログラムに関する情報をパッケージ化し、HTTP 経由でサーバーに送信します。</span><span class="sxs-lookup"><span data-stu-id="fa8d5-125">When DC1.SubmitChanges executes, the Remote Data Service packages all the update information and sends it to the server via HTTP.</span></span> <span data-ttu-id="fa8d5-126">更新プログラムは、まったく。更新プログラムの一部が失敗した場合のすべての更新を行い、ステータス メッセージが返されます。</span><span class="sxs-lookup"><span data-stu-id="fa8d5-126">The update is all-or-nothing; if a part of the update is unsuccessful, none of the changes is made, and a status message is returned.</span></span> <span data-ttu-id="fa8d5-127">これを実行すると、リモート データ サービスは、すべての更新プログラムに関する情報をパッケージ化し、HTTP 経由でサーバーに送信します。</span><span class="sxs-lookup"><span data-stu-id="fa8d5-127">executes, the Remote Data Service packages all the update information and sends it to the server via HTTP.</span></span> <span data-ttu-id="fa8d5-128">更新プログラムは、まったく。更新プログラムの一部が失敗した場合のすべての更新を行い、ステータス メッセージが返されます。</span><span class="sxs-lookup"><span data-stu-id="fa8d5-128">The update is all-or-nothing; if a part of the update is unsuccessful, none of the changes is made, and a status message is returned.</span></span> <span data-ttu-id="fa8d5-129">DC1 です。リモート データ サービスでは、 **SubmitChanges**の後更新する必要はありませんが、最新のデータになります。</span><span class="sxs-lookup"><span data-stu-id="fa8d5-129">DC1.Refresh isn't necessary after **SubmitChanges** with Remote Data Service, but it ensures fresh data.</span></span>

## <a name="cancel-changes-button"></a><span data-ttu-id="fa8d5-130">[変更の取り消し] ボタン</span><span class="sxs-lookup"><span data-stu-id="fa8d5-130">Cancel Changes Button</span></span>

<span data-ttu-id="fa8d5-131">VBScript の [キャンセル] をアクティブに**変更をキャンセル**をクリックすると\_OnClick Sub プロシージャは、実行 rds.DataControl オブジェクトの (CancelUpdate メソッドです。</span><span class="sxs-lookup"><span data-stu-id="fa8d5-131">Clicking **Cancel Changes** activates the VBScript Cancel\_OnClick Sub procedure, which executes the RDS.DataControl object's ( CancelUpdate method.</span></span>

```vb 
 
Sub Cancel_OnClick 
 DC1.CancelUpdate 
End Sub 
```

<span data-ttu-id="fa8d5-p105">実行すると、前回のクエリまたは更新後にユーザーがデータ グリッドの従業員レコードに対して行ったすべての編集が破棄されます。</span><span class="sxs-lookup"><span data-stu-id="fa8d5-p105">When executes, it discards any edits that a user has made to an employee record on the data grid since the last query or update. It restores the original values.</span></span>

