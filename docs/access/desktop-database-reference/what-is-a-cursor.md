---
title: カーソルとは  (デスクトップ データベースの参照にアクセス)
TOCTitle: What is a Cursor?
ms:assetid: cc70d941-05e0-9b14-1c5d-6b1a5802f546
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250013(v=office.15)
ms:contentKeyID: 48547738
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2023b39620f80e6f770153e381c74d5285d027c6
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718939"
---
# <a name="what-is-a-cursor"></a><span data-ttu-id="1321f-103">カーソルとは</span><span class="sxs-lookup"><span data-stu-id="1321f-103">What is a cursor?</span></span>


<span data-ttu-id="1321f-104">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="1321f-104">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1321f-p102">リレーショナル データベースの操作は、完全な行セットに対して行われます。SELECT ステートメントが返す行セットには、ステートメントの WHERE 句の条件を満たす行がすべて含まれます。ステートメントから返されるこの完全な行セットは、結果セットと呼ばれます。アプリケーション、特に対話型アプリケーションおよびオンライン アプリケーションでは、結果セット全体を 1 つの単位として効率的に処理できるとは限りません。このようなアプリケーションには、一時点で 1 行または小さい行ブロックを処理する機構が必要です。カーソルは、このような機構を提供する、結果セットの拡張機能です。</span><span class="sxs-lookup"><span data-stu-id="1321f-p102">Operations in a relational database act on a complete set of rows. The set of rows returned by a SELECT statement consists of all the rows that satisfy the conditions in the WHERE clause of the statement. This complete set of rows returned by the statement is known as the result set. Applications, especially those that are interactive and online, cannot always work effectively with the entire result set as a unit. These applications need a mechanism to work with one row or a small block of rows at a time. Cursors are an extension to result sets that provide that mechanism.</span></span>

<span data-ttu-id="1321f-p103">カーソルは、カーソル ライブラリによって実装されます。カーソル ライブラリは、しばしばデータベース システムまたはデータ アクセス API の一部として実装されるソフトウェアで、データ ソース (結果セット) から返されるデータの属性を管理するために使用されます。これらの属性には、同時実行管理、結果セット内の位置、返される行数、結果セット内を前方と後方のいずれかまたは両方に移動できるかどうか (スクロール機能) などがあります。</span><span class="sxs-lookup"><span data-stu-id="1321f-p103">A cursor is implemented by a cursor library. A cursor library is software, often implemented as a part of a database system or a data access API, that is used to manage attributes of data returned from a data source (a result set). These attributes include concurrency management, position in the result set, number of rows returned, and whether or not you can move forward and/or backward through the result set (scrollability).</span></span>

<span data-ttu-id="1321f-p104">カーソルは、結果セット内の位置を記録するため、元のテーブルに結果を返すかどうかに関係なく、結果セットに対して 1 行ずつ複数の操作を実行できます。つまり、カーソルは、概念的にはデータベース内のテーブルに基づいて結果セットを返します。カーソルと呼ばれるのは、コンピューター画面上のカーソルが現在の位置を示すのと同じように、結果セット内の現在の位置を示すためです。</span><span class="sxs-lookup"><span data-stu-id="1321f-p104">A cursor keeps track of the position in the result set, and allows you to perform multiple operations row by row against a result set, with or without returning to the original table. In other words, cursors conceptually return a result set based on tables within the databases. The cursor is so named because it indicates the current position in the result set, just as the cursor on a computer screen indicates current position.</span></span>

<span data-ttu-id="1321f-117">ADO でのカーソルの使用方法を習得する前に、カーソルの概念に精通しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="1321f-117">It is important to become familiar with the concept of cursors before moving on to learn the specifics of their usage in ADO.</span></span>

<span data-ttu-id="1321f-118">カーソルを使用すると、次の処理を実行できます。</span><span class="sxs-lookup"><span data-stu-id="1321f-118">Using cursors, you can:</span></span>

  - <span data-ttu-id="1321f-119">結果セット内の特定の行の位置を指定します。</span><span class="sxs-lookup"><span data-stu-id="1321f-119">Specify positioning at specific rows in the result set.</span></span>

  - <span data-ttu-id="1321f-120">現在の結果セットの位置に基づいて 1 行または 1 つの行ブロックを取得します。</span><span class="sxs-lookup"><span data-stu-id="1321f-120">Retrieve one row or a block of rows based on the current result set position.</span></span>

  - <span data-ttu-id="1321f-121">結果セット内の現在の位置にある行のデータを変更します。</span><span class="sxs-lookup"><span data-stu-id="1321f-121">Modify data in the rows at the current position in the result set.</span></span>

  - <span data-ttu-id="1321f-122">他のユーザーによるデータ変更の検出レベルを定義できます。</span><span class="sxs-lookup"><span data-stu-id="1321f-122">Define different levels of sensitivity to data changes made by other users.</span></span>

<span data-ttu-id="1321f-p105">たとえば、潜在的なお客様に購入可能な製品の一覧を表示するアプリケーションを考えてみます。お客様は一覧をスクロールして、製品の詳細と価格を確認し、購入する製品を最後に選択します。さらにスクロールして、一覧の他の製品を選択することもできます。お客様にとっては、製品が 1 つずつ表示されていますが、アプリケーションではスクロール可能なカーソルを使用して、結果セット内を上下に移動することで製品を表示しています。</span><span class="sxs-lookup"><span data-stu-id="1321f-p105">For example, consider an application that displays a list of available products to a potential buyer. The buyer scrolls through the list to see product details and cost, and finally selects a product for purchase. Additional scrolling and selection occurs for the remainder of the list. As far as the buyer is concerned, the products appear one at a time, but the application uses a scrollable cursor to browse up and down through the result set.</span></span>

<span data-ttu-id="1321f-127">カーソルは、次のようなさまざまな方法で使用できます。</span><span class="sxs-lookup"><span data-stu-id="1321f-127">You can use cursors in a variety of ways:</span></span>

  - <span data-ttu-id="1321f-128">行なしで使用</span><span class="sxs-lookup"><span data-stu-id="1321f-128">With no rows at all.</span></span>

  - <span data-ttu-id="1321f-129">1 つのテーブル内にある一部またはすべての行と共に使用</span><span class="sxs-lookup"><span data-stu-id="1321f-129">With some or all of the rows in a single table.</span></span>

  - <span data-ttu-id="1321f-130">論理的に結合された複数のテーブル内にある一部またはすべての行と共に使用</span><span class="sxs-lookup"><span data-stu-id="1321f-130">With some or all of the rows from logically joined tables.</span></span>

  - <span data-ttu-id="1321f-131">カーソル レベルまたはフィールド レベルの読み取り専用カーソルまたは更新可能カーソルとして使用</span><span class="sxs-lookup"><span data-stu-id="1321f-131">As read-only or updateable at the cursor or field level.</span></span>

  - <span data-ttu-id="1321f-132">前方のみカーソルまたは完全にスクロール可能なカーソルとして使用</span><span class="sxs-lookup"><span data-stu-id="1321f-132">As forward-only or fully scrollable.</span></span>

  - <span data-ttu-id="1321f-133">サーバー上にあるカーソル キーセットと共に使用</span><span class="sxs-lookup"><span data-stu-id="1321f-133">With the cursor keyset located on the server.</span></span>

  - <span data-ttu-id="1321f-134">他のアプリケーションによる、基になるテーブルの変更 (メンバーシップ、並べ替え、挿入、更新、および削除) に合わせて使用</span><span class="sxs-lookup"><span data-stu-id="1321f-134">Sensitive to underlying table changes caused by other applications (such as membership, sort, inserts, updates, and deletes).</span></span>

  - <span data-ttu-id="1321f-135">サーバー側またはクライアント側での使用</span><span class="sxs-lookup"><span data-stu-id="1321f-135">Existing on either the server or the client.</span></span>

<span data-ttu-id="1321f-p106">読み取り専用カーソルを使用すると、結果セットの参照に便利で、読み取り/書き込みカーソルを使用すると、個別の行の更新を実行できます。ベース テーブルの行を指すキーセットを持つ、複雑なカーソルを定義することもできます。前方に移動する読み取り専用カーソルもあれば、前方と後方の両方に移動し、他のアプリケーションによるデータベースの変更に基づいて結果セットを動的に更新できるカーソルもあります。</span><span class="sxs-lookup"><span data-stu-id="1321f-p106">Read-only cursors help users browse through the result set, and read/write cursors can implement individual row updates. Complex cursors can be defined with keysets that point back to base table rows. While some cursors are read-only in a forward direction, others can move back and forth and provide a dynamic refresh of the result set based on changes that other applications are making to the database.</span></span>

<span data-ttu-id="1321f-p107">カーソルを使用しなくても、データのアクセスまたは更新が可能なアプリケーションもあります。カーソルを使用して行を直接更新することが不要なクエリもあります。データの取得にカーソルを使用するかどうかは、慎重に検討する必要があり、カーソルを使用する場合は、影響が最も少ないカーソルを選択する必要があります。ストアド プロシージャを使用して結果セットを作成した場合、カーソルの編集メソッドまたは更新メソッドを使用してその結果セットを更新することはできません。</span><span class="sxs-lookup"><span data-stu-id="1321f-p107">Not all applications need to use cursors to access or update data. Some queries simply do not require direct row updating by using a cursor. Cursors should be one of the last techniques you choose to retrieve data — and then you should choose the lowest impact cursor possible. When you create a result set by using a stored procedure, the result set is not updateable using cursor edit or update methods.</span></span>

## <a name="concurrency"></a><span data-ttu-id="1321f-143">同時実行</span><span class="sxs-lookup"><span data-stu-id="1321f-143">Concurrency</span></span>

<span data-ttu-id="1321f-p108">マルチユーザー アプリケーションでは、エンド ユーザーにできる限り最新のデータを提供することが非常に重要な場合があります。そのようなシステムの典型的な例は、航空券予約システムで、特定のフライトの同じ座席、つまり 1 つのレコードに対して多数のユーザーが競合する可能性があります。このような場合、アプリケーションは、1 つのレコードに対する複数の同時操作を処理できるように設計する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1321f-p108">In some multi-user applications it is vitally important for the data presented to the end user to be as current as possible. A classic example of such a system is an airline reservation system, where many users might be contending for the same seat on a given flight (and thus, a single record). In a case like this, the application design must handle concurrent operations on a single record.</span></span>

<span data-ttu-id="1321f-p109">同時実行がそれほど重要ではないアプリケーションもあります。そのような場合、データを常に最新の状態に保つために負荷をかける必要はありません。</span><span class="sxs-lookup"><span data-stu-id="1321f-p109">In other applications, concurrency is not as important. In such cases, the expense involved in keeping the data current at all times cannot be justified.</span></span>

## <a name="position"></a><span data-ttu-id="1321f-149">位置</span><span class="sxs-lookup"><span data-stu-id="1321f-149">Position</span></span>

<span data-ttu-id="1321f-p110">カーソルでは、結果セット内の現在位置の記録も行われます。カーソルの位置は、配列内の特定の位置にある値を指す配列インデックスのような、現在のレコードへのポインターと考えてください。</span><span class="sxs-lookup"><span data-stu-id="1321f-p110">A cursor also keeps track of the current position in a result set. Think of the cursor position as a pointer to the current record, similar to the way an array index points to the value at that particular location in the array.</span></span>

## <a name="scrollability"></a><span data-ttu-id="1321f-152">スクロール機能</span><span class="sxs-lookup"><span data-stu-id="1321f-152">Scrollability</span></span>

<span data-ttu-id="1321f-153">結果セット内の行を前方と後方に移動する機能、アプリケーションで使用されるカーソルの種類にも影響します。スクロール機能とも呼びます。</span><span class="sxs-lookup"><span data-stu-id="1321f-153">The type of cursor employed by your application also affects the ability to move forward and backward through the rows in a result set; this is sometimes called scrollability.</span></span> <span data-ttu-id="1321f-154">前方*と*後方の結果セットを移動することは、カーソルの複雑さに追加し、されるため、実装するために高価です。</span><span class="sxs-lookup"><span data-stu-id="1321f-154">The ability to move forward *and* backward through a result set adds to the complexity of the cursor, and is therefore more expensive to implement.</span></span> <span data-ttu-id="1321f-155">このため、この機能が必要な場合のみにカーソルを依頼します。</span><span class="sxs-lookup"><span data-stu-id="1321f-155">For this reason, you should ask for a cursor with this functionality only when necessary.</span></span>

