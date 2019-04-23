---
title: パラメーター化コマンドの操作
TOCTitle: Operation of parameterized commands
ms:assetid: 71edbd16-21db-7afa-356b-d8e7afb92b3a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249456(v=office.15)
ms:contentKeyID: 48545596
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 145a2ee6c3d3c614eb9660350a0bb8a00d44d04c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288288"
---
# <a name="operation-of-parameterized-commands"></a><span data-ttu-id="c651a-102">パラメーター化コマンドの操作</span><span class="sxs-lookup"><span data-stu-id="c651a-102">Operation of parameterized commands</span></span>

<span data-ttu-id="c651a-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="c651a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c651a-104">大きな子 **Recordset** を処理するとき、特に親 **Recordset** のサイズと比べて大きいにもかかわらず、わずかな子チャプターにアクセスするだけの場合は、パラメーター化コマンドを使用する方が効率的です。</span><span class="sxs-lookup"><span data-stu-id="c651a-104">If you are working with a large child **Recordset**, especially compared to the size of the parent **Recordset**, but need to access only a few child chapters, you might find it more efficient to use a parameterized command.</span></span>

<span data-ttu-id="c651a-105">*非パラメーター化コマンド*は、親と子の両方の**recordset**全体を取得し、チャプター列を親に追加して、親の各行に関連する子チャプターへの参照を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="c651a-105">A *non-parameterized command* retrieves both the entire parent and child **Recordsets**, appends a chapter column to the parent, and then assigns a reference to the related child chapter for each parent row.</span></span>

<span data-ttu-id="c651a-106">*パラメーター化*されたコマンドは親**recordset**全体を取得しますが、チャプター列にアクセスしたときにはチャプター **recordset**のみを取得します。</span><span class="sxs-lookup"><span data-stu-id="c651a-106">A *parameterized command* retrieves the entire parent **Recordset**, but retrieves only the chapter **Recordset** when the chapter column is accessed.</span></span> <span data-ttu-id="c651a-107">This difference in retrieval strategy can yield significant performance benefits.</span><span class="sxs-lookup"><span data-stu-id="c651a-107">This difference in retrieval strategy can yield significant performance benefits.</span></span>

<span data-ttu-id="c651a-108">たとえば、次のように指定することができます。</span><span class="sxs-lookup"><span data-stu-id="c651a-108">For example, you can specify the following:</span></span>

```vb 
 
SHAPE {SELECT * FROM customer} 
 APPEND ({SELECT * FROM orders WHERE cust_id = ?} 
 RELATE cust_id TO PARAMETER 0) 
```

<span data-ttu-id="c651a-109">親と子のテーブルには、共通の cust\_id の列名があり*ます。*</span><span class="sxs-lookup"><span data-stu-id="c651a-109">The parent and child tables have a column name in common, cust\_id *.*</span></span> <span data-ttu-id="c651a-110">*child-command* には、RELATE 句の参照先 ("...PARAMETER 0") へのプレースホルダー "?" が指定されています。</span><span class="sxs-lookup"><span data-stu-id="c651a-110">The *child-command* has a "?" placeholder, to which the RELATE clause refers (that is, "...PARAMETER 0").</span></span>

> [!NOTE]
> <span data-ttu-id="c651a-p103">[!メモ] PARAMETER 句は、Shape コマンドの構文にのみ影響します。ADO の [Parameter](parameter-object-ado.md) オブジェクトまたは [Parameters](parameters-collection-ado.md) コレクションとは関係ありません。</span><span class="sxs-lookup"><span data-stu-id="c651a-p103">The PARAMETER clause pertains solely to the shape command syntax. It is not associated with either the ADO [Parameter](parameter-object-ado.md) object or the [Parameters](parameters-collection-ado.md) collection.</span></span>

<span data-ttu-id="c651a-113">パラメーター化された Shape コマンドが実行されると、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="c651a-113">When the parameterized shape command is executed, the following occurs:</span></span>

1.  <span data-ttu-id="c651a-114">*parent-command* が実行され、Customers テーブルから親 **Recordset** が返されます。</span><span class="sxs-lookup"><span data-stu-id="c651a-114">The *parent-command* is executed and returns a parent **Recordset** from the Customers table.</span></span>

2.  <span data-ttu-id="c651a-115">チャプター列が親 **Recordset** に追加されます。</span><span class="sxs-lookup"><span data-stu-id="c651a-115">A chapter column is appended to the parent **Recordset**.</span></span>

3.  <span data-ttu-id="c651a-116">親の行のチャプター列にアクセスすると、customer の値を使用して*子コマンド*が実行されます\_。 cust id は、パラメーターの値として指定します。</span><span class="sxs-lookup"><span data-stu-id="c651a-116">When the chapter column of a parent row is accessed, the *child-command* is executed using the value of the customer.cust\_id as the value of the parameter.</span></span>

4.  <span data-ttu-id="c651a-117">手順3で作成したデータプロバイダーの行セット内のすべての行を使用して、子**Recordset**にデータを設定します。</span><span class="sxs-lookup"><span data-stu-id="c651a-117">All rows in the data provider rowset created in step 3 are used to populate the child **Recordset**.</span></span> <span data-ttu-id="c651a-118">この例では、Orders テーブルには、cust\_id が customers\_id の値と等しい行がすべて含まれています。</span><span class="sxs-lookup"><span data-stu-id="c651a-118">In this example, that is all the rows in the Orders table in which the cust\_id equals the value of customer.cust\_id.</span></span> <span data-ttu-id="c651a-119">既定では、親**recordset**への参照がすべて解放されるまで、子**recordset**s はクライアント上にキャッシュされます。</span><span class="sxs-lookup"><span data-stu-id="c651a-119">By default, the child **Recordset**s will be cached on the client until all references to the parent **Recordset** are released.</span></span> <span data-ttu-id="c651a-120">この動作を変更するには、 **Recordset**の[動的プロパティ](ado-dynamic-property-index.md)**キャッシュの子の行**を**False**に設定します。</span><span class="sxs-lookup"><span data-stu-id="c651a-120">To change this behavior, set the **Recordset** [dynamic property](ado-dynamic-property-index.md)**Cache Child Rows** to **False**.</span></span>

5.  <span data-ttu-id="c651a-121">取得された子の行への参照 (つまり、子 **Recordset** のチャプター) は、親 **Recordset** のカレント行のチャプター列に配置されます。</span><span class="sxs-lookup"><span data-stu-id="c651a-121">A reference to the retrieved child rows (that is, the chapter of the child **Recordset**) is placed in the chapter column of the current row of the parent **Recordset**.</span></span>

6.  <span data-ttu-id="c651a-122">別の行のチャプター列にアクセスすると、手順 3. ～ 5. が繰り返されます。</span><span class="sxs-lookup"><span data-stu-id="c651a-122">Steps 3–5 are repeated when the chapter column of another row is accessed.</span></span>

<span data-ttu-id="c651a-p105">既定では、 **Cache Child Rows** 動的プロパティは **True** に設定されています。キャッシュの動作は、クエリのパラメーター値によって異なります。単一のパラメーターが指定されたクエリの場合、指定されたパラメーター値に対応する子 **Recordset** は、その値を持つ子に対する要求があるまでキャッシュに保持されます。次のコードにこの例を示します。</span><span class="sxs-lookup"><span data-stu-id="c651a-p105">The **Cache Child Rows** dynamic property is set to **True** by default. The caching behavior varies depending upon the parameter values of the query. In a query with a single parameter, the child **Recordset** for a given parameter value will be cached between requests for a child with that value. The following code demonstrates this:</span></span>

```vb
... 
SCmd = "SHAPE {select * from customer} " & _ 
 "APPEND({select * from orders where cust_id = ?} " & _ 
 "RELATE cust_id TO PARAMETER 0) AS chpCustOrder" 
Rst1.Open sCmd, Cnn1 
Set RstChild = Rst1("chpCustOrder").Value 
Rst1.MoveNext ' Next cust_id passed to Param 0, & new rs fetched 
 ' into RstChild. 
Rst1.MovePrevious ' RstChild now holds cached rs, saving round trip. 
... 
```

<span data-ttu-id="c651a-127">2 つ以上のパラメーターが指定されたクエリでは、すべてのパラメーター値がキャッシュに入れられた値と等しい場合のみ、キャッシュに入れられた子が使用されます。</span><span class="sxs-lookup"><span data-stu-id="c651a-127">In a query with two or more parameters, a cached child is used only if all the parameter values match the cached values.</span></span>

## <a name="parameterized-commands-and-complex-parent-child-relations"></a><span data-ttu-id="c651a-128">パラメーター化されたコマンドと複雑な親子関係</span><span class="sxs-lookup"><span data-stu-id="c651a-128">Parameterized commands and complex parent child relations</span></span>

<span data-ttu-id="c651a-129">パラメーター化されたコマンドを使用すると、等結合タイプの階層のパフォーマンスを向上できるだけでなく、より複雑な親子関係をサポートできます。</span><span class="sxs-lookup"><span data-stu-id="c651a-129">In addition to using parameterized commands to improve performance of an equi-join type hierarchy, parameterized commands can be used to support more complex parent-child relationships.</span></span> <span data-ttu-id="c651a-130">\_たとえば、teams (チーム id、チーム\_名) と、その他のゲーム (日付、自宅\_チーム、訪問\_チーム) の2つのテーブルで構成されるちょっとしたリーグデータベースを考えてみます。</span><span class="sxs-lookup"><span data-stu-id="c651a-130">For example, consider a Little League database with two tables: one consisting of the teams (team\_id, team\_name) and the other of games (date, home\_team, visiting\_team).</span></span>

<span data-ttu-id="c651a-131">非パラメーター化階層を使用する場合、各チームの子 **Recordset** にその完全な日程が含まれるように、チーム テーブルと試合テーブルを関連付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="c651a-131">Using a non-parameterized hierarchy, there is no way to relate the teams and games tables in such a way that the child **Recordset** for each team contains its complete schedule.</span></span> <span data-ttu-id="c651a-132">ホームの日程または遠征の日程のいずれかを含むチャプターを作成することはできますが、両方を含むチャプターは作成できません。</span><span class="sxs-lookup"><span data-stu-id="c651a-132">You can create chapters that contain the home schedule or the road schedule, but not both.</span></span> <span data-ttu-id="c651a-133">これは、RELATE 句では、親子関係が (pc1=cc1) AND (pc2=pc2) 形式に制限されるためです。</span><span class="sxs-lookup"><span data-stu-id="c651a-133">This is because the RELATE clause limits you to parent-child relationships of the form (pc1=cc1) AND (pc2=pc2).</span></span> <span data-ttu-id="c651a-134">\_そのため、「team id からホーム\_チームへのチーム id への\_\_関連付け」というコマンドを使用した場合、チームが自分たちをプレイしていたゲームのみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c651a-134">So, if your command included "RELATE team\_id TO home\_team, team\_id TO visiting\_team", you would get only games where a team was playing itself.</span></span> <span data-ttu-id="c651a-135">必要なのは、"(\_チーム id =\_ホームチーム)" また\_は (team\_id = 訪問チーム) "ですが、Shape プロバイダーは OR 句をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="c651a-135">What you want is "(team\_id=home\_team) OR (team\_id=visiting\_team)", but the Shape provider does not support the OR clause.</span></span>

<span data-ttu-id="c651a-p108">必要な結果を取得するには、パラメーター化されたコマンドを使用します。次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="c651a-p108">To obtain the desired result, you can use a parameterized command. For example:</span></span>

```vb 
 
SHAPE {SELECT * FROM teams} 
APPEND ({SELECT * FROM games WHERE home_team = ? OR visiting_team = ?} 
 RELATE team_id TO PARAMETER 0, 
 team_id TO PARAMETER 1) 
```

<span data-ttu-id="c651a-138">この例では、必要な結果を取得するため、より柔軟に SQL WHERE 句を利用しています。</span><span class="sxs-lookup"><span data-stu-id="c651a-138">This example exploits the greater flexibility of the SQL WHERE clause to get the result you need.</span></span>

