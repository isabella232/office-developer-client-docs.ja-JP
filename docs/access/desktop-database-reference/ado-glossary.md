---
title: ActiveX データ オブジェクト (ADO) の用語集
TOCTitle: ADO Glossary
ms:assetid: 40f00876-7525-4117-8f57-f3d87c54be99
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249184(v=office.15)
ms:contentKeyID: 48544438
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7ecb6208a8c970f037cb0ac699c947544eb8f547
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720843"
---
# <a name="ado-glossary"></a><span data-ttu-id="e7951-102">ADO 用語集</span><span class="sxs-lookup"><span data-stu-id="e7951-102">ADO glossary</span></span>

<span data-ttu-id="e7951-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="e7951-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="a"></a><span data-ttu-id="e7951-104">A</span><span class="sxs-lookup"><span data-stu-id="e7951-104">A</span></span>

<span data-ttu-id="e7951-105">**絶対 URL**</span><span class="sxs-lookup"><span data-stu-id="e7951-105">**absolute URL**</span></span>

<span data-ttu-id="e7951-p101">インターネットまたはイントラネット上にあるリソースの場所を指定する完全修飾 URL。 **URL** と **相対 URL** も参照。</span><span class="sxs-lookup"><span data-stu-id="e7951-p101">A fully qualified URL that specifies the location of a resource that resides on the Internet or an intranet. See also **URL** and **relative URL**.</span></span>

<span data-ttu-id="e7951-108">**ActiveX コントロール**</span><span class="sxs-lookup"><span data-stu-id="e7951-108">**ActiveX control**</span></span>

<span data-ttu-id="e7951-p102">一般的にデザイン時間または実行時で視覚的要素を持つ、自己登録型のインプロセス COM コンポーネント。また、ActiveX コントロールは、Microsoft Internet Explorer のようなアクティブ ドキュメント コンテナーと通信できます。</span><span class="sxs-lookup"><span data-stu-id="e7951-p102">Self-registering, in-process COM component that often has a visual element either at design time or run time. ActiveX controls also have the ability to communicate with an Active Document container, such as Microsoft Internet Explorer.</span></span>

<span data-ttu-id="e7951-111">**ADISAPI (Advanced Data Internet Server Application Programming Interface)**</span><span class="sxs-lookup"><span data-stu-id="e7951-111">**ADISAPI (Advanced Data Internet Server Application Programming Interface)**</span></span>

<span data-ttu-id="e7951-p103">解析、オートメーション コントロール、 **Recordset** マーシャリング、および MIME パッケージを提供する ISAPI DLL。ADISAPI コンポーネントは、インターネット インフォメーション サービス (IIS) が提供する API により機能します。 **ISAPI** も参照。</span><span class="sxs-lookup"><span data-stu-id="e7951-p103">An ISAPI DLL that provides parsing, Automation control, **Recordset** marshaling, and MIME packaging. The ADISAPI component works through the API provided by Internet Information Services (IIS). See also **ISAPI**.</span></span>

<span data-ttu-id="e7951-115">**集計関数**</span><span class="sxs-lookup"><span data-stu-id="e7951-115">**aggregate function**</span></span>

<span data-ttu-id="e7951-p104">クエリで、表の列内のすべての行を使用して値を計算する COUNT、AVG、または STDEV のような関数。式を作成するときやプログラミングで、(前述の 3 つを含む) SQL 集計関数とドメイン集計関数を使用してさまざまな統計を得ることができます。</span><span class="sxs-lookup"><span data-stu-id="e7951-p104">In a query, a function such as COUNT, AVG, or STDEV that calculates a value using all the rows in a column of a table. In writing expressions and in programming, you can use SQL aggregate functions (including the three listed above) and domain aggregate functions to determine various statistics.</span></span>

<span data-ttu-id="e7951-118">**エイリアス**</span><span class="sxs-lookup"><span data-stu-id="e7951-118">**alias**</span></span>

<span data-ttu-id="e7951-p105">SQL SELECT ステートメントで列または式に付ける、一般的にはより短いか、より分かりやすい代替の名前。たとえば、以下の SELECT ステートメントで BobSales がエイリアスとなります。"Select wr-Sales as BobSales from SalesDB"。エイリアスは、 **DataControl** オブジェクトのコントロール バインディングに動的に列を割り当てる目的で使用できます。</span><span class="sxs-lookup"><span data-stu-id="e7951-p105">An alternate name you give to a column or expression in an SQL SELECT statement, often shorter or more meaningful. For example, BobSales is the alias in the following SELECT statement: "Select wr-Sales as BobSales from SalesDB". An alias can be used to dynamically assign columns to control bindings on the **DataControl** object.</span></span>

<span data-ttu-id="e7951-122">**アパートメント スレッド**</span><span class="sxs-lookup"><span data-stu-id="e7951-122">**apartment threading**</span></span>

<span data-ttu-id="e7951-p106">オブジェクトへのすべての呼び出しが 1 つのスレッドで発生する COM スレッド モデル。アパートメント スレッドで、COM は呼び出しを同期させ、整理します。 **COM** も参照。</span><span class="sxs-lookup"><span data-stu-id="e7951-p106">A COM threading model where all calls to an object occur on one thread. In apartment threading, COM synchronizes and marshals calls. See also **COM**.</span></span>

<span data-ttu-id="e7951-126">**非同期処理**</span><span class="sxs-lookup"><span data-stu-id="e7951-126">**asynchronous operation**</span></span>

<span data-ttu-id="e7951-p107">処理の完了を待機中せずに、呼び出し元のプログラムにコントロールを戻す処理。処理が完了する前に、コードの実行は続行されます。 **同期処理** も参照。</span><span class="sxs-lookup"><span data-stu-id="e7951-p107">An operation that returns control to the calling program without waiting for the operation to complete. Before the operation is complete, code execution continues. See also **synchronous operation**.</span></span>

<span data-ttu-id="e7951-130">トップに戻る</span><span class="sxs-lookup"><span data-stu-id="e7951-130">Return to top</span></span>

## <a name="b"></a><span data-ttu-id="e7951-131">B</span><span class="sxs-lookup"><span data-stu-id="e7951-131">B</span></span>

<span data-ttu-id="e7951-132">**バインディング エントリ**</span><span class="sxs-lookup"><span data-stu-id="e7951-132">**binding entry**</span></span>

<span data-ttu-id="e7951-p108">表内のフィールドと変数の間のマッピング。ADO Visual C++ Extensions では、 **Recordset** フィールドは C/C++ 変数にマップされます。</span><span class="sxs-lookup"><span data-stu-id="e7951-p108">A mapping between a field in a table and a variable. In the ADO Visual C++ extensions, **Recordset** fields are mapped to C/C++ variables.</span></span>

<span data-ttu-id="e7951-135">**ビットマスク**</span><span class="sxs-lookup"><span data-stu-id="e7951-135">**bitmask**</span></span>

<span data-ttu-id="e7951-136">数値のもので他の数値とビット単位での値の比較のため通常パラメーターまたは戻り値のオプションのフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="e7951-136">A numeric value intended for a bit-by-bit value comparison with other numeric values, typically to flag options in parameter or return values.</span></span> <span data-ttu-id="e7951-137">など **、** **または**Visual Basic では、ビットごとの論理演算子で比較が行われる通常**&** と**|** C で。</span><span class="sxs-lookup"><span data-stu-id="e7951-137">Usually this comparison is done with bitwise logical operators, such as **And** and **Or** in Visual Basic, **&** and **|** in C++.</span></span>

<span data-ttu-id="e7951-p110">たとえば、ADO **FieldAttributeEnum** 値はフィールドの属性を決定する目的でビットマスクとして使用できます。あるフィールドが更新可能か確認する場合を想定します。これは、Visual Basic で以下の式により確認できます。</span><span class="sxs-lookup"><span data-stu-id="e7951-p110">For example, the ADO **FieldAttributeEnum** values can be used as bitmasks to determine the attributes of a field. Suppose you wanted to determine if a field was updateable. You could test for this with the following expression in Visual Basic:</span></span>  
  

<span data-ttu-id="e7951-141">結果が TRUE の場合、フィールドは更新できます。</span><span class="sxs-lookup"><span data-stu-id="e7951-141">If the result is TRUE, then the field is updateable.</span></span>

<span data-ttu-id="e7951-142">**ブックマーク**</span><span class="sxs-lookup"><span data-stu-id="e7951-142">**bookmark**</span></span>

<span data-ttu-id="e7951-143">ユーザーがすばやく表示できるように、一連の行内で、一意的に特定の行を識別するマーカー。</span><span class="sxs-lookup"><span data-stu-id="e7951-143">A marker that uniquely identifies a row within a set of rows so that a user can quickly navigate to it.</span></span>

<span data-ttu-id="e7951-144">**ビジネス オブジェクト**</span><span class="sxs-lookup"><span data-stu-id="e7951-144">**business object**</span></span>

<span data-ttu-id="e7951-p111">データの入力規則またはビジネス ルール ロジックのような、一連の定義された操作を行うオブジェクト。ビジネス オブジェクトは、通常、中間層にあります。</span><span class="sxs-lookup"><span data-stu-id="e7951-p111">An object that performs a defined set of operations, such as data validation or business rule logic. Business objects usually reside on the middle tier.</span></span>

<span data-ttu-id="e7951-147">**ビジネス ルール**</span><span class="sxs-lookup"><span data-stu-id="e7951-147">**business rule**</span></span>

<span data-ttu-id="e7951-p112">企業がビジネスをする方法を構成する、検証編集、ログオン検証、データベース ルックアップ、ポリシー、およびアルゴリズム変換の組み合わせ。\*\* ビジネス ロジックとも呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="e7951-p112">The combination of validation edits, logon verifications, database lookups, policies, and algorithmic transformations that constitute an enterprise's way of doing business. Also known as *business logic*.</span></span>

<span data-ttu-id="e7951-150">トップに戻る</span><span class="sxs-lookup"><span data-stu-id="e7951-150">Return to top</span></span>

## <a name="c"></a><span data-ttu-id="e7951-151">C</span><span class="sxs-lookup"><span data-stu-id="e7951-151">C</span></span>

<span data-ttu-id="e7951-152">**計算式**</span><span class="sxs-lookup"><span data-stu-id="e7951-152">**calculated expression**</span></span>

<span data-ttu-id="e7951-p113">定数ではないが、値がその他の値に依存する式。計算式が評価されるには、一般的には他のフィールドまたは行のような、その他のソースから値を取得して、計算する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e7951-p113">An expression that is not constant, but whose value depends upon other values. To be evaluated, a calculated expression must obtain and compute values from other sources, typically in other fields or rows.</span></span>

<span data-ttu-id="e7951-155">**チャプター**</span><span class="sxs-lookup"><span data-stu-id="e7951-155">**chapter**</span></span>

<span data-ttu-id="e7951-p114">データ ソースからの、特定の行の範囲への参照。ADO では、一般的に、チャプターは他の **レコードセット** への参照です。</span><span class="sxs-lookup"><span data-stu-id="e7951-p114">A reference to a range of rows from a data source. In ADO, a chapter is typically a reference to another **Recordset**.</span></span>

<span data-ttu-id="e7951-158">チャプター列では、\*\* 親子関係を定義できます。\*\* 親とは、チャプター列を含む**レコードセット**で、\*\* 子とは、チャプターで表される**レコードセット**です。</span><span class="sxs-lookup"><span data-stu-id="e7951-158">Chapter columns make it possible to define a *parent-child* relationship where the *parent* is the **Recordset** containing the chapter column and the *child* is the **Recordset** represented by the chapter.</span></span>

<span data-ttu-id="e7951-159">**チャプター エイリアス**</span><span class="sxs-lookup"><span data-stu-id="e7951-159">**chapter-alias**</span></span>

<span data-ttu-id="e7951-160">親に追加された列を参照するエイリアス。</span><span class="sxs-lookup"><span data-stu-id="e7951-160">An alias that refers to the column appended to the parent.</span></span>

<span data-ttu-id="e7951-161">**文字セット**</span><span class="sxs-lookup"><span data-stu-id="e7951-161">**character set**</span></span>

<span data-ttu-id="e7951-p115">一連の文字の数値へのマッピング。たとえば、Unicode はすべての既知の文字をエンコードできる 16 ビットの文字セットで、世界的な文字エンコードの標準として使用されています。</span><span class="sxs-lookup"><span data-stu-id="e7951-p115">A mapping of a set of characters to their numeric values. For example, Unicode is a 16-bit character set capable of encoding all known characters and used as a worldwide character-encoding standard.</span></span>

<span data-ttu-id="e7951-164">**子**</span><span class="sxs-lookup"><span data-stu-id="e7951-164">**child**</span></span>

<span data-ttu-id="e7951-p116">階層的な関係で、依存をする側。子とは、階層的な構造で、(ルートにより近い方向で) そ上に他のノードを持つノードです。 **子エイリアス** 、 **親子関係** 、 **親** も参照。</span><span class="sxs-lookup"><span data-stu-id="e7951-p116">The dependent side of a hierarchical relationship. A child is a node in a hierarchical structure that has another node above it (closer to the root). See also **child-alias**, **parent-child relationship**, **parent**.</span></span>

<span data-ttu-id="e7951-168">**子エイリアス**</span><span class="sxs-lookup"><span data-stu-id="e7951-168">**child-alias**</span></span>

<span data-ttu-id="e7951-p117">子を参照するエイリアス。 **エイリアス** 、 **子** も参照。</span><span class="sxs-lookup"><span data-stu-id="e7951-p117">An alias that refers to the child. See also **alias**, **child**.</span></span>

<span data-ttu-id="e7951-171">**CLSID (クラス識別子)**</span><span class="sxs-lookup"><span data-stu-id="e7951-171">**CLSID (class identifier)**</span></span>

<span data-ttu-id="e7951-p118">COM コンポーネントを識別する、広範囲で使われる一意識別子 (UUID)。各 COM コンポーネントは、その他のアプリケーションに読み込まれることができるように、Windows レジストリにその CLSID を持っています。 **ProgID** 、 **COM** も参照。</span><span class="sxs-lookup"><span data-stu-id="e7951-p118">A universally unique identifier (UUID) that identifies a COM component. Each COM component has its CLSID in the Windows Registry so that it can be loaded by other applications. See also **ProgID**, **COM**.</span></span>

<span data-ttu-id="e7951-175">**クライアント層**</span><span class="sxs-lookup"><span data-stu-id="e7951-175">**client tier**</span></span>

<span data-ttu-id="e7951-p119">一般的には、ユーザーにデータを示し、ユーザーの入力を処理する、分散システムの論理的レイヤー。\*\* フロント エンドと呼ばれることもあります。通常、クライアント層は、入力に基づいてサーバーからデータを要求し、次に結果を書式付けして表示します。**中間層**、**データ ソース層**、**分散アプリケーション**も参照。</span><span class="sxs-lookup"><span data-stu-id="e7951-p119">A logical layer of a distributed system that typically presents data to and processes input from the user, sometimes referred to as the *front end*. Usually, the client tier requests data from a server based on input, and then formats and displays the result. See also **middle tier**, **data source tier**, **distributed application**.</span></span>

<span data-ttu-id="e7951-179">**COM (Component Object Model)**</span><span class="sxs-lookup"><span data-stu-id="e7951-179">**COM (Component Object Model)**</span></span>

<span data-ttu-id="e7951-p120">ネットワーク接続された環境で、開発された言語やどこのコンピューターにあるかにかかわらず、オブジェクトを相互運用できるようにするバイナリ標準規格。COM ベースのテクノロジには、ActiveX コントロール、オートメーション、および OLE (オブジェクトのリンクと埋め込み) が含まれます。COM により、オブジェクトは、その他のコンポーネントとホスト アプリケーションに、その機能を公開できます。COM は、オブジェクトがそれ自体を公開する方法と、この公開がプロセス間およびネットワーク間で機能する方法を定義します。また、COM は、オブジェクトのライフ サイクルを定義します。</span><span class="sxs-lookup"><span data-stu-id="e7951-p120">A binary standard that enables objects to interoperate in a networked environment regardless of the language in which they were developed or on which computers they reside. COM-based technologies include ActiveX Controls, Automation, and object linking and embedding (OLE). COM allows an object to expose its functionality to other components and to host applications. It defines both how the object exposes itself and how this exposure works across processes and across networks. COM also defines the object's life cycle.</span></span>

<span data-ttu-id="e7951-185">**COM コンポーネント**</span><span class="sxs-lookup"><span data-stu-id="e7951-185">**COM component**</span></span>

<span data-ttu-id="e7951-p121">オブジェクトの提供方法として COM 標準をサポートする, .dll, .ocx、および一部の .exe ファイルのようなバイナリ ファイル。このようなファイルには、1 つまたは複数のクラス ファクトリ、COM クラス、レジストリ入力メカニズム、読み込みコードなどのコードが含まれます。</span><span class="sxs-lookup"><span data-stu-id="e7951-p121">Binary file — such as .dll, .ocx, and some .exe files — that supports the COM standard for providing objects. Such a file contains code for one or more class factories, COM classes, registry-entry mechanisms, loading code, and so on.</span></span>

<span data-ttu-id="e7951-188">**比較演算子**</span><span class="sxs-lookup"><span data-stu-id="e7951-188">**comparison operator**</span></span>

<span data-ttu-id="e7951-189">2 つの式を比較して、Boolean 値を戻す演算子。</span><span class="sxs-lookup"><span data-stu-id="e7951-189">An operator that compares two expressions and returns a Boolean value.</span></span>

<span data-ttu-id="e7951-190">"\>" (より大きい)、"\<" (より小さい)、"=" (等しい)、"\>=" (以上)、"\<=" (以下)、"\<\>" (等しくない)、または "like" (パターン マッチング) として表現されるクライテリア パラメーター。</span><span class="sxs-lookup"><span data-stu-id="e7951-190">A criteria parameter that may be expressed as "\>" (greater than), "\<" (less than), "=" (equal), "\>=" (greater than or equal), "\<=" (less than or equal), "\<\>" (not equal), or "like" (pattern matching).</span></span>

<span data-ttu-id="e7951-191">**コンポーネント**</span><span class="sxs-lookup"><span data-stu-id="e7951-191">**component**</span></span>

<span data-ttu-id="e7951-192">データとコードの両方をカプセル化し、厳密に指定された、広く入手可能な一連のサービスを提供するオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="e7951-192">An object that encapsulates both data and code, and provides a well-specified set of publicly available services.</span></span>

<span data-ttu-id="e7951-193">**複合ファイル**</span><span class="sxs-lookup"><span data-stu-id="e7951-193">**compound file**</span></span>

<span data-ttu-id="e7951-p122">ファイル用の COM 構造化記憶域の実装。複合ファイルは、個別のオブジェクトを、単一の構造化されたファイルに保存します。このファイルは、記憶域オブジェクトとストリーム オブジェクトの 2 つの主な要素から構成されます。これらは、ファイル内でファイル システムのように動作します。詳細については、Microsoft プラットフォーム SDK で複合ファイルに関する情報を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e7951-p122">An implementation of COM structured storage for files. A compound file stores separate objects in a single, structured file consisting of two main elements: storage objects and stream objects. Together, they function like a file system within a file. For more information, see Compound Files in the Microsoft Platform SDK.</span></span>

<span data-ttu-id="e7951-p123">1 つの物理的ファイルにバインドされた、いくつかの個別のファイル。複合ファイル内の各個別のファイルは、単一の物理的ファイルと同様にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="e7951-p123">A number of individual files bound together in one physical file. Each individual file in a compound file can be accessed as if it were a single physical file.</span></span>

<span data-ttu-id="e7951-200">**定数**</span><span class="sxs-lookup"><span data-stu-id="e7951-200">**constant**</span></span>

<span data-ttu-id="e7951-p124">変化しない数値または文字列値。名前付き ADO 列挙体 (列挙された定数) を、実際の値の代わりにコードで使用できます。たとえば、 **adUseClient** は、値が 3 の定数です (Const adUseClient = 3)。 **列挙体** も参照。</span><span class="sxs-lookup"><span data-stu-id="e7951-p124">A numeric or string value that does not change. Named ADO enumerations (enumerated constants) can be used in your code instead of actual values, for example, **adUseClient** is a constant whose value is 3. (Const adUseClient = 3). See also **enumeration**.</span></span>

<span data-ttu-id="e7951-205">**カーソル**</span><span class="sxs-lookup"><span data-stu-id="e7951-205">**cursor**</span></span>

<span data-ttu-id="e7951-206">レコード ナビゲーション、データの更新可能性、およびその他のユーザーによるデータベースへの変更の可視性を制御するデータベース要素。</span><span class="sxs-lookup"><span data-stu-id="e7951-206">A database element that controls record navigation, updateability of data, and the visibility of changes made to the database by other users.</span></span>

<span data-ttu-id="e7951-207">トップに戻る</span><span class="sxs-lookup"><span data-stu-id="e7951-207">Return to top</span></span>

## <a name="d"></a><span data-ttu-id="e7951-208">D</span><span class="sxs-lookup"><span data-stu-id="e7951-208">D</span></span>

<span data-ttu-id="e7951-209">**データ バインド**</span><span class="sxs-lookup"><span data-stu-id="e7951-209">**data binding**</span></span>

<span data-ttu-id="e7951-p125">オブジェクトまたはアプリケーションのコントロールをデータ ソースに関連付けるプロセス。データ ソースに関連付けられたコントロールは、\*\* データ連結コントロールと呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="e7951-p125">The process of associating the objects or controls of an application to a data source. A control associated with a data source is called a *data-bound control*.</span></span>

<span data-ttu-id="e7951-p126">データ連結コントロールの内容は、データベースからの値に関連付けられます。たとえば、 **レコードセット** 内の行が更新されたとき、 **Recordset** オブジェクトに連結されたグリッド コントロールは更新できます。新しい値が **レコードセット** により取得されたとき、その新しい値はグリッドに表示されます。</span><span class="sxs-lookup"><span data-stu-id="e7951-p126">The contents of a data-bound control are associated with values from a database. For example, a grid control that is bound to a **Recordset** object can be updated when the rows in the **Recordset** are updated. When new values are retrieved by the **Recordset**, new values are displayed in the grid.</span></span>

<span data-ttu-id="e7951-215">**データ プロバイダー**</span><span class="sxs-lookup"><span data-stu-id="e7951-215">**data provider**</span></span>

<span data-ttu-id="e7951-p127">直接、またはサービス プロバイダー経由で ADO アプリケーションにデータを公開するソフトウェア。 **サービス プロバイダー** も参照。</span><span class="sxs-lookup"><span data-stu-id="e7951-p127">Software that exposes data to an ADO application either directly or via a service provider. See also **service provider**.</span></span>

<span data-ttu-id="e7951-218">**データ シェイプ**</span><span class="sxs-lookup"><span data-stu-id="e7951-218">**data shaping**</span></span>

<span data-ttu-id="e7951-219">(**シェイプされた Recordset** と呼ばれる) 特殊な **Recordset** オブジェクトを定義する目的で、(**シェイプ言語**と呼ばれる) 定式化された構文を使用する方法。シェイプされた Recordset には、データだけではなく、その他の **Recordset** オブジェクト、またはそれらのその他の **Recordset** オブジェクトに基づいて計算された値、あるいはその両方が含まれます。</span><span class="sxs-lookup"><span data-stu-id="e7951-219">A technique which makes use of a formalized syntax (called **Shape language**) to define a specialized **Recordset** object (called a **shaped Recordset**) that contains not just data, but also references to other **Recordset** objects and/or computed values based on those other **Recordset** objects.</span></span>

<span data-ttu-id="e7951-220">**データ ソース層**</span><span class="sxs-lookup"><span data-stu-id="e7951-220">**data source tier**</span></span>

<span data-ttu-id="e7951-p128">SQL Server データベースのような、DBMS を実行中のコンピューターを表す分散システムの論理的レイヤー。 **クライアント層** 、 **中間層** 、 **分散アプリケーション** も参照。</span><span class="sxs-lookup"><span data-stu-id="e7951-p128">A logical layer of a distributed system that represents a computer running a DBMS, such as an SQL Server database. See also **client tier**, **middle tier**, **distributed application**.</span></span>

<span data-ttu-id="e7951-223">**DCOM**</span><span class="sxs-lookup"><span data-stu-id="e7951-223">**DCOM**</span></span>

<span data-ttu-id="e7951-p129">COM コンポーネントが、ネットワーク上で、直接、相互に通信できるようにするワイヤー プロトコル。 **COM** 、 **コンポーネント** も参照。</span><span class="sxs-lookup"><span data-stu-id="e7951-p129">A wire protocol that enables COM components to communicate directly with each other across a network. See also **COM**, **component**.</span></span>

<span data-ttu-id="e7951-226">**DDL (データ定義言語)**</span><span class="sxs-lookup"><span data-stu-id="e7951-226">**DDL (Data Definition Language)**</span></span>

<span data-ttu-id="e7951-p130">SQL 内で、データを操作するのではなく、データを定義するステートメント。データベースのスキーマは、DDL により作成または変更されます。たとえば、 **CREATE TABLE** 、 **CREATE INDEX** 、 **GRANT** 、および **REVOKE** は、SQL DDL ステートメントです。</span><span class="sxs-lookup"><span data-stu-id="e7951-p130">Those statements in SQL that define, as opposed to manipulate, data. The schema of a database is created or modified with DDL. For example, **CREATE TABLE**, **CREATE INDEX**, **GRANT**, and **REVOKE** are SQL DDL statements.</span></span>

<span data-ttu-id="e7951-230">**既定ストリーム**</span><span class="sxs-lookup"><span data-stu-id="e7951-230">**default stream**</span></span>

<span data-ttu-id="e7951-231">Microsoft OLE DB Provider for Internet Publishing のような、特定の OLE DB プロバイダーを使用するとき、 **Record** または **Recordset** オブジェクトに関連付けられた、( **Stream** オブジェクトで表される) テキストまたはバイナリのストリーム。</span><span class="sxs-lookup"><span data-stu-id="e7951-231">A text or binary stream (represented by a **Stream** object) that is associated with **Record** or **Recordset** objects when using certain OLE DB providers, such as the Microsoft OLE DB Provider for Internet Publishing.</span></span> <span data-ttu-id="e7951-232">通常、既定のストリームには、HTML コードに web サイトのルートに対するファイルの内容が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e7951-232">The default stream typically contains the contents of a file such as the HTML code for the root of a website.</span></span>

<span data-ttu-id="e7951-233">**分散アプリケーション**</span><span class="sxs-lookup"><span data-stu-id="e7951-233">**distributed application**</span></span>

<span data-ttu-id="e7951-p132">処理をネットワーク上にある複数のコンピューター間で分散できるように作成されたプログラム。一般的には、分散アプリケーションは、プレゼンテーション、ビジネス ロジック、およびデータ ストアのレイヤー (または\*\* 層) に分かれています。**クライアント層**、**中間層**、**データ ソース層**も参照。</span><span class="sxs-lookup"><span data-stu-id="e7951-p132">A program written so that the processing can be divided across multiple computers over a network. Typically, a distributed application is divided into presentation, business logic, and data store layers, or *tiers*. See also **client tier**, **middle tier**, **data source tier**.</span></span>

<span data-ttu-id="e7951-237">**切断された Recordset**</span><span class="sxs-lookup"><span data-stu-id="e7951-237">**disconnected Recordset**</span></span>

<span data-ttu-id="e7951-p133">サーバーへのライブ接続を失った、クライアント キャッシュ内の **Recordset** オブジェクト。データを更新するなどの理由で、元のデータ ソースに、再度、アクセスする必要がある場合、接続を、再度、確立する必要があります。しかし、切断された **Recordset** のコレクション、プロパティ、およびメソッドにはまだアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="e7951-p133">A **Recordset** object in a client cache that no longer has a live connection to the server. If the original data source needs to be accessed again for some reason, such as updating data, the connection must be re-established. However, the collections, properties, and methods of a disconnected **Recordset** can still be accessed.</span></span>

<span data-ttu-id="e7951-241">**DLL (ダイナミック リンク ライブラリ)**</span><span class="sxs-lookup"><span data-stu-id="e7951-241">**DLL (dynamic-link library)**</span></span>

<span data-ttu-id="e7951-p134">1 つまたは複数の関数を含むファイルは、それらを使用するプロセスとは別に、コンパイル、リンク、および保存する必要があります。オペレーティング システムは、プロセスが開始するとき、またはその実行中に、呼び出し元のプロセスのアドレス空間に DLL をマップします。</span><span class="sxs-lookup"><span data-stu-id="e7951-p134">A file that contains one or more functions that are compiled, linked, and stored separately from the processes that use them. The operating system maps the DLLs into the address space of the calling process when the process is starting, or while it is running.</span></span>

<span data-ttu-id="e7951-244">**DML (データ操作言語)**</span><span class="sxs-lookup"><span data-stu-id="e7951-244">**DML (Data Manipulation Language)**</span></span>

<span data-ttu-id="e7951-p135">SQL 内で、データを定義するのではなく、データを操作するステートメント。データベース内の値は、DML により選択され変更されます。たとえば、 **INSERT** 、 **UPDATE** 、 **DELETE** 、および **SELECT** は、SQL DML ステートメントです。</span><span class="sxs-lookup"><span data-stu-id="e7951-p135">Those statements in SQL that manipulate, as opposed to define, data. The values in a database are selected and modified with DML. For example, **INSERT**, **UPDATE**, **DELETE**, and **SELECT** are SQL DML statements.</span></span>

<span data-ttu-id="e7951-248">**ドキュメント ソース プロバイダー**</span><span class="sxs-lookup"><span data-stu-id="e7951-248">**document source provider**</span></span>

<span data-ttu-id="e7951-p136">フォルダーとドキュメントを管理する、プロバイダーの特殊なクラス。 **Record** オブジェクトがドキュメントを表しているか、または **Recordset** オブジェクトがドキュメントのフォルダーを表している場合には、ドキュメント ソース プロバイダーは、実際のドキュメント自体ではなくドキュメントの特徴を記述した固有のフィールドのセットで、これらのオブジェクトにデータを設定します。 **リソース レコード** も参照。</span><span class="sxs-lookup"><span data-stu-id="e7951-p136">A special class of providers that manage folders and documents. When a document is represented by a **Record** object, or a folder of documents is represented by a **Recordset** object, the document source provider populates those objects with a unique set of fields that describe characteristics of the document, instead of the actual document itself. See also **resource record**.</span></span>

<span data-ttu-id="e7951-252">**DSN (データ ソース名)**</span><span class="sxs-lookup"><span data-stu-id="e7951-252">**DSN (data source name)**</span></span>

<span data-ttu-id="e7951-p137">アプリケーションを特定の ODBC データベースに接続する目的で使用される情報のコレクション。ODBC ドライバー マネージャーは、この情報を使用してデータベースに接続します。DSN は、ファイル (ファイル DSN)、または Windows レジストリ (コンピューター DSN) に保存できます。</span><span class="sxs-lookup"><span data-stu-id="e7951-p137">The collection of information used to connect your application to a particular ODBC database. The ODBC Driver Manager uses this information to create a connection to the database. A DSN can be stored in a file (a file DSN) or in the Windows Registry (a machine DSN).</span></span>

<span data-ttu-id="e7951-256">**動的プロパティ**</span><span class="sxs-lookup"><span data-stu-id="e7951-256">**dynamic property**</span></span>

<span data-ttu-id="e7951-p138">データ プロバイダーまたはカーソル サービスに固有のプロパティ。オブジェクトの **Properties** コレクションは、動的プロパティにより自動的に (動的に) 設定されます。特定のデータ プロバイダーによりデータ ソースに接続されるまで、オブジェクトは動的プロパティを持っていません。 **データ プロバイダー** 、 **カーソル** も参照。</span><span class="sxs-lookup"><span data-stu-id="e7951-p138">A property specific to a data provider or the cursor service. The **Properties** collection of an object is populated with these automatically ("dynamically"). An object has no dynamic properties until it is connected to a data source through a particular data provider. See also **data provider**, **cursor**.</span></span>

<span data-ttu-id="e7951-261">トップに戻る</span><span class="sxs-lookup"><span data-stu-id="e7951-261">Return to top</span></span>

## <a name="e-i"></a><span data-ttu-id="e7951-262">E-I</span><span class="sxs-lookup"><span data-stu-id="e7951-262">E-I</span></span>

<span data-ttu-id="e7951-263">**列挙体**</span><span class="sxs-lookup"><span data-stu-id="e7951-263">**enumeration**</span></span>

<span data-ttu-id="e7951-p139">名前付き定数のリスト。列挙値は、一意である必要はありません。しかし、各値の名前は、列挙体が定義された範囲で一意である必要があります。ADO では、列挙体は数値パラメーターと戻り値で使用されます。これにより、ADO コードに意味を追加して、開発者は (バージョンごとに変更される) 数値を使わずに済むようになります。たとえば、静的な **Recordset** を開く目的で、 **adOpenStatic** 列挙値を使用します。</span><span class="sxs-lookup"><span data-stu-id="e7951-p139">A list of named constants. Enumerated values need not be unique. However the name of each value must be unique within the scope where the enumeration is defined. In ADO, enumerations are used for numeric parameter and return values, to add meaning to ADO code and to shield the developer from the numeric values (which may change from version to version). For example, to open a static **Recordset**, use the **adOpenStatic** enumerated value:</span></span>  
  

<span data-ttu-id="e7951-p140">また、\*\* 列挙定数とも呼ばれます。**定数**も参照。</span><span class="sxs-lookup"><span data-stu-id="e7951-p140">Also referred to as *enumerated constant*. See also **constant**.</span></span>

<span data-ttu-id="e7951-271">**イベント**</span><span class="sxs-lookup"><span data-stu-id="e7951-271">**event**</span></span>

<span data-ttu-id="e7951-p141">オブジェクトにより認識されるアクション。コードを作成することにより、対応できます。イベントは、コマンドの実行、トランザクションの完了、レコードセットの操作、データ更新などのアクションによって生成されます。 **イベント ハンドラー** も参照。</span><span class="sxs-lookup"><span data-stu-id="e7951-p141">An action recognized by an object, for which you can write code to respond. Events can be generated by command execution, transaction completion, recordset navigation, and data updates, among other actions. See also **event handler**.</span></span>

<span data-ttu-id="e7951-275">**イベント ハンドラー**</span><span class="sxs-lookup"><span data-stu-id="e7951-275">**event handler**</span></span>

<span data-ttu-id="e7951-p142">イベント ハンドラーは、イベントが発生したときに実行されるコードです。 **イベント** も参照。</span><span class="sxs-lookup"><span data-stu-id="e7951-p142">An event handler is the code that is executed when an event occurs. See also **event**.</span></span>

<span data-ttu-id="e7951-278">**ハンドラー**</span><span class="sxs-lookup"><span data-stu-id="e7951-278">**handler**</span></span>

<span data-ttu-id="e7951-279">エラー回復またはデータ管理のような、一般的で、比較的、単純な条件または操作を処理するルーチン。</span><span class="sxs-lookup"><span data-stu-id="e7951-279">A routine that manages a common and relatively simple condition or operation, such as error recovery or data management.</span></span>

<span data-ttu-id="e7951-280">**階層 Recordset**</span><span class="sxs-lookup"><span data-stu-id="e7951-280">**hierarchical Recordset**</span></span>

<span data-ttu-id="e7951-p143">他の **レコードセット** を含む **レコードセット** 。 **データ シェイプ** 、 **チャプター** も参照。</span><span class="sxs-lookup"><span data-stu-id="e7951-p143">A **Recordset** that contains another **Recordset**. See also **data shaping**, **chapter**.</span></span>

<span data-ttu-id="e7951-283">詳細については、「[階層 Recordset 内の行にアクセスする](accessing-rows-in-a-hierarchical-recordset.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e7951-283">For more information, see [Accessing Rows in a Hierarchical Recordset](accessing-rows-in-a-hierarchical-recordset.md)</span></span>

<span data-ttu-id="e7951-284">**階層**</span><span class="sxs-lookup"><span data-stu-id="e7951-284">**hierarchy**</span></span>

<span data-ttu-id="e7951-p144">一般に、階層とは、単一の最上位のレベルと複数の従属的なレベルでランク付けされた構造です。ADO では、階層 **Recordsets** は、レコードおよびチャプター間の親子関係を表す目的で使用されます。また ADO では、 **Record** および **Stream** オブジェクトが、フォルダーとドキュメントのような階層的なツリー構造にアクセスする目的で使用できます。また、ADO MD には、OLAP キューブでディメンションのレベル間の関係を表す、 **Hierarchy** オブジェクトがあります。 **階層 Recordset** 、 **親子関係** 、 **チャプター** 、 **ツリー** も参照。</span><span class="sxs-lookup"><span data-stu-id="e7951-p144">In general, a hierarchy is a ranked structure with a top level and subordinate levels. In ADO, hierarchical **Recordsets** are used to represent the parent-child relationship between a record and a chapter. Also in ADO, **Record** and **Stream** objects can be used to access hierarchical tree structures such as a folder and documents. ADO MD also includes **Hierarchy** objects to represent a relationship between the levels of a dimension in an OLAP cube. See also **hierarchical Recordsets**, **parent-child relationship**, **chapter**, **tree**.</span></span>

<span data-ttu-id="e7951-290">**ISAPI (Internet Server Application Programming Interface)**</span><span class="sxs-lookup"><span data-stu-id="e7951-290">**ISAPI (Internet Server Application Programming Interface)**</span></span>

<span data-ttu-id="e7951-291">Microsoft インターネット インフォメーション サービス (IIS) を実行中の Windows NT サーバー /Windows 2000 サーバーのようなインターネットサーバー用の一連の関数。</span><span class="sxs-lookup"><span data-stu-id="e7951-291">A set of functions for Internet servers, such as a Windows NT Server/Windows 2000 Server running Microsoft Internet Information Services (IIS).</span></span>

<span data-ttu-id="e7951-292">トップに戻る</span><span class="sxs-lookup"><span data-stu-id="e7951-292">Return to top</span></span>

## <a name="k-m"></a><span data-ttu-id="e7951-293">K-M</span><span class="sxs-lookup"><span data-stu-id="e7951-293">K-M</span></span>

<span data-ttu-id="e7951-294">**キー**</span><span class="sxs-lookup"><span data-stu-id="e7951-294">**key**</span></span>

<span data-ttu-id="e7951-295">表内で、一意的に行を識別する 1 つまたは複数の列。一般的に、表にインデックスを作成する目的で使用されます。</span><span class="sxs-lookup"><span data-stu-id="e7951-295">A column or columns in a table that uniquely identify a row; often used to index a table.</span></span>

<span data-ttu-id="e7951-296">**マーシャリング**</span><span class="sxs-lookup"><span data-stu-id="e7951-296">**marshaling**</span></span>

<span data-ttu-id="e7951-297">スレッドまたはプロセスの境界を越えてインターフェイス メソッドのパラメーターをパッケージ化、送信、およびパッケージ化解除するプロセス。</span><span class="sxs-lookup"><span data-stu-id="e7951-297">The process of packaging, sending, and unpackaging interface method parameters across thread or process boundaries.</span></span>

<span data-ttu-id="e7951-298">**中間層**</span><span class="sxs-lookup"><span data-stu-id="e7951-298">**middle tier**</span></span>

<span data-ttu-id="e7951-299">ユーザー インターフェイスまたは web クライアントとデータベース間で分散システム内の論理層です。</span><span class="sxs-lookup"><span data-stu-id="e7951-299">The logical layer in a distributed system between a user interface or web client and the database.</span></span> <span data-ttu-id="e7951-300">通常、ビジネス オブジェクトがインスタンス化されます。</span><span class="sxs-lookup"><span data-stu-id="e7951-300">This is typically where business objects are instantiated.</span></span> <span data-ttu-id="e7951-301">中間層は、ビジネス ルールと生成され、情報の受信時に操作する機能のコレクションです。</span><span class="sxs-lookup"><span data-stu-id="e7951-301">The middle tier is a collection of business rules and functions that generate and operate upon receiving information.</span></span> <span data-ttu-id="e7951-302">これを実行するとき、頻繁に変更することができ、アプリケーション ロジックから物理的に分離されたコンポーネントにカプセル化されているビジネス ルールを使用します。</span><span class="sxs-lookup"><span data-stu-id="e7951-302">They accomplish this through business rules, which can change frequently, and are thus encapsulated into components that are physically separate from the application logic itself.</span></span> <span data-ttu-id="e7951-303">呼ばれる*アプリケーション サーバー層*です。</span><span class="sxs-lookup"><span data-stu-id="e7951-303">Also known as *application server tier*.</span></span> <span data-ttu-id="e7951-304">**分散アプリケーション\*\*\*\*クライアント層**、および**データ ソース層**」も参照してください。</span><span class="sxs-lookup"><span data-stu-id="e7951-304">See also **distributed application**, **client tier**, **data source tier**.</span></span>

<span data-ttu-id="e7951-305">**MIME (Multi-purpose Internet Mail Extension)**</span><span class="sxs-lookup"><span data-stu-id="e7951-305">**MIME (Multi-purpose Internet Mail Extension)**</span></span>

<span data-ttu-id="e7951-306">異機種混在環境のネットワーク、コンピューター、および電子メール環境間でのリッチ コンテンツを含む電子メール メッセージの交換を許可するインターネット プロトコルが開発されました。</span><span class="sxs-lookup"><span data-stu-id="e7951-306">An Internet protocol originally developed to allow exchange of electronic mail messages with rich content across heterogeneous network, machine, and email environments.</span></span> <span data-ttu-id="e7951-307">実際には、MIME は、メール以外のアプリケーションにも採用され、拡張されています。</span><span class="sxs-lookup"><span data-stu-id="e7951-307">In practice, MIME has also been adopted and extended by non-mail applications.</span></span>

<span data-ttu-id="e7951-308">MIME は、バイナリ データの発行やインターネット上の読み取りを可能にする標準です。</span><span class="sxs-lookup"><span data-stu-id="e7951-308">MIME is a standard that allows binary data to be published and read on the Internet.</span></span> <span data-ttu-id="e7951-309">バイナリ データを含むファイルのヘッダーには、データの MIME タイプが含まれています。クライアント プログラムに通知 (たとえば web ブラウザーやメール パッケージなど) よりも、純粋なテキストを処理する別の方法でデータを処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e7951-309">The header of a file with binary data contains the MIME type of the data; this informs client programs (web browsers and mail packages, for instance) that they will need to handle the data in a different way than they handle straight text.</span></span> <span data-ttu-id="e7951-310">たとえば、JPEG 画像を含む web 文書のヘッダーには、JPEG ファイル形式に固有の MIME の種類が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e7951-310">For example, the header of a web document containing a JPEG graphic contains the MIME type specific to the JPEG file format.</span></span> <span data-ttu-id="e7951-311">こうと、JPEG ビューアーでファイルを表示するブラウザーが存在する場合。</span><span class="sxs-lookup"><span data-stu-id="e7951-311">This allows a browser to display the file with its JPEG viewer, if one is present.</span></span>

<span data-ttu-id="e7951-312">トップに戻る</span><span class="sxs-lookup"><span data-stu-id="e7951-312">Return to top</span></span>

## <a name="n-o"></a><span data-ttu-id="e7951-313">N-O</span><span class="sxs-lookup"><span data-stu-id="e7951-313">N-O</span></span>

<span data-ttu-id="e7951-314">**ノード**</span><span class="sxs-lookup"><span data-stu-id="e7951-314">**node**</span></span>

<span data-ttu-id="e7951-p148">階層ツリー構造内の要素。ノードは、ルート、または他のノードの子であることができます。また、ノードは、複数の子の親であることができます。 **階層** 、 **ツリー** 、 **ルート** 、 **子** 、 **親** も参照。</span><span class="sxs-lookup"><span data-stu-id="e7951-p148">An element in a hierarchical tree structure. A node may be the root, or the child of another node. A node can also be the parent of multiple children. See also **hierarchy**, **tree**, **root**, **child**, **parent**.</span></span>

<span data-ttu-id="e7951-319">**オブジェクト変数**</span><span class="sxs-lookup"><span data-stu-id="e7951-319">**object variable**</span></span>

<span data-ttu-id="e7951-320">オブジェクトへの参照を含む変数。</span><span class="sxs-lookup"><span data-stu-id="e7951-320">A variable that contains a reference to an object.</span></span> <span data-ttu-id="e7951-321">たとえば、objCustomObject は、[customobject] の種類のオブジェクトを指す変数です。</span><span class="sxs-lookup"><span data-stu-id="e7951-321">For example, objCustomObject is a variable that points to an object of type CustomObject:</span></span>  
  
<span data-ttu-id="e7951-322">is a variable that points to an object of type CustomObject:</span><span class="sxs-lookup"><span data-stu-id="e7951-322">is a variable that points to an object of type CustomObject:</span></span>  
  
<span data-ttu-id="e7951-323">設定 objCustomObject = CreateObject (adodb。レコード セット)</span><span class="sxs-lookup"><span data-stu-id="e7951-323">Set objCustomObject = CreateObject(adodb.Recordset)</span></span>

<span data-ttu-id="e7951-324">**ODBC (Open Database Connectivity)**</span><span class="sxs-lookup"><span data-stu-id="e7951-324">**ODBC (Open Database Connectivity)**</span></span>

<span data-ttu-id="e7951-p150">さまざまなデータ ソースに接続する目的で使用される標準プログラミング言語インターフェイス。これは、通常、コントロール パネルによりアクセスされます。コントロール パネルでは、特定の ODBC ドライバーを使用する目的でデータ ソース名 (DSN) が割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="e7951-p150">A standard programming language interface used to connect to a variety of data sources. This is usually accessed through Control Panel, where data source names (DSNs) can be assigned to use specific ODBC drivers.</span></span>

<span data-ttu-id="e7951-327">**OLE DB**</span><span class="sxs-lookup"><span data-stu-id="e7951-327">**OLE DB**</span></span>

<span data-ttu-id="e7951-p151">COM を使用して、さまざまなソースからデータを公開する一連のインターフェイス。さまざまな情報ソースに格納されているデータに、各アプリケーションから同じようにアクセスできるインターフェイスを提供します。これらのインターフェイスは、データ共有を可能にする目的で、データ ソースに適した豊富な DBMS 機能をサポートします。 **COM** も参照。</span><span class="sxs-lookup"><span data-stu-id="e7951-p151">A set of interfaces that expose data from a variety of sources using COM. OLE DB interfaces provide applications with uniform access to data stored in diverse information sources. These interfaces support the amount of DBMS functionality appropriate to the data source, enabling it to share its data. See also **COM**.</span></span>

<span data-ttu-id="e7951-332">**共有的ロック**</span><span class="sxs-lookup"><span data-stu-id="e7951-332">**optimistic locking**</span></span>

<span data-ttu-id="e7951-333">ロックの種類。レコードが **Update** メソッドで更新されている間は、その他のユーザーは、編集中のレコードを含め、1 つまたは複数のレコードを含むデータ ページを使用できません。 **Update** の呼び出しの前と後では使用できます。</span><span class="sxs-lookup"><span data-stu-id="e7951-333">A type of locking in which the data page containing one or more records, including the record being edited, is unavailable to other users only while the record is being updated by the **Update** method, but is available before and after the call to **Update**.</span></span>

<span data-ttu-id="e7951-p152">共有的ロックは、 **Recordset** オブジェクトが **LockType** パラメーターを付けて、あるいはプロパティが **adLockOptimistic** または **adLockBatchOptimistic** に設定された状態で開かれたときたときに使用されます。 **排他的ロック** も参照。</span><span class="sxs-lookup"><span data-stu-id="e7951-p152">Optimistic locking is used when the **Recordset** object is opened with the **LockType** parameter or property set to **adLockOptimistic** or **adLockBatchOptimistic**. See also **pessimistic locking**.</span></span>

<span data-ttu-id="e7951-336">**序数**</span><span class="sxs-lookup"><span data-stu-id="e7951-336">**ordinal value**</span></span>

<span data-ttu-id="e7951-p153">特定の順序内でのアイテムの数値的な場所。ADO コレクションで、最初のアイテムの序数はゼロ (0) です。次のアイテムは 1 で、以下も同様です。</span><span class="sxs-lookup"><span data-stu-id="e7951-p153">The numeric location of an item within an order. In an ADO collection, the ordinal value of the first item is zero (0). The next item is one (1), and so on.</span></span>

<span data-ttu-id="e7951-340">トップに戻る</span><span class="sxs-lookup"><span data-stu-id="e7951-340">Return to top</span></span>

## <a name="p"></a><span data-ttu-id="e7951-341">P</span><span class="sxs-lookup"><span data-stu-id="e7951-341">P</span></span>

<span data-ttu-id="e7951-342">**パラメーター化されたコマンド**</span><span class="sxs-lookup"><span data-stu-id="e7951-342">**parameterized command**</span></span>

<span data-ttu-id="e7951-p154">コマンドが実行される前に、パラメーター値を設定できるクエリまたはコマンド。たとえば、SQL 文字列は、その中に ("?" 文字で表される) パラメーターマーカーを埋め込むことでパラメーター化できます。次に、アプリケーションは各パラメーターの値を指定して、コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="e7951-p154">A query or command that allows you to set parameter values before the command is executed. For example, a SQL string can be parameterized by embedding parameter markers in the SQL string (designated by the '?' character). The application then specifies values for each parameter and executes the command.</span></span>

<span data-ttu-id="e7951-346">**親**</span><span class="sxs-lookup"><span data-stu-id="e7951-346">**parent**</span></span>

<span data-ttu-id="e7951-p155">階層的な関係で、制御をする側。階層的な構造で、親は、それ自体の階層の直下に、1 つまたは複数の子ノードを持っています。 **親エイリアス** 、 **親子関係** 、 **子** も参照。</span><span class="sxs-lookup"><span data-stu-id="e7951-p155">The controlling side of a hierarchical relationship. In a hierarchical structure, a parent has one or more child nodes directly beneath it in the hierarchy. See also **parent-alias**, **parent-child relationship**, **child**.</span></span>

<span data-ttu-id="e7951-350">**親エイリアス**</span><span class="sxs-lookup"><span data-stu-id="e7951-350">**parent-alias**</span></span>

<span data-ttu-id="e7951-p156">親であるエイリアス。 **エイリアス** 、 **親** も参照。</span><span class="sxs-lookup"><span data-stu-id="e7951-p156">An alias that refers to the parent. See also **alias**, **parent**.</span></span>

<span data-ttu-id="e7951-353">**親子関係**</span><span class="sxs-lookup"><span data-stu-id="e7951-353">**parent-child relationship**</span></span>

<span data-ttu-id="e7951-p157">階層的な構造内での関係。親は 1 つまたは複数の子より高く、直接、関連付けられたレベルにあります。子は 1 段階低いレベルにあり、1 つの親を持つ必要があります。 **親** 、 **子** も参照。</span><span class="sxs-lookup"><span data-stu-id="e7951-p157">A relationship in a hierarchical structure in which the parent is one level higher and directly associated with one or more children. A child is one level lower and must have one parent. See also **parent**, **child**.</span></span>

<span data-ttu-id="e7951-357">**常設**</span><span class="sxs-lookup"><span data-stu-id="e7951-357">**persist**</span></span>

<span data-ttu-id="e7951-358">ファイルに **レコードセット** を保存する場合のように、データを恒久的な状態で保存すること。</span><span class="sxs-lookup"><span data-stu-id="e7951-358">To save data in a permanent state, such as saving a **Recordset** to a file.</span></span>

<span data-ttu-id="e7951-359">**排他的ロック**</span><span class="sxs-lookup"><span data-stu-id="e7951-359">**pessimistic locking**</span></span>

<span data-ttu-id="e7951-p158">ロックの種類。更新ができるように、その他のユーザーに対して、編集中のレコードを含め、1 つまたは複数のレコードを含むデータページを使用できないようにします。排他的ロック動作は、OLE DB プロバイダーにより定義されます。一般的には、 **Update** メソッドが完了するまで、レコードは編集時にロックされ使用できなくなります。</span><span class="sxs-lookup"><span data-stu-id="e7951-p158">A type of locking in which the page containing one or more records, including the record being edited, is unavailable to other users to ensure that an update will be made. Pessimistic locking behavior is defined by the OLE DB provider. Typically, records are locked upon editing and remain unavailable until the **Update** method has completed.</span></span>

<span data-ttu-id="e7951-p159">排他的ロックは、 **Recordset** オブジェクトが **LockType** パラメーターを付けて、あるいはプロパティが **adLockPessimistic** に設定された状態で開かれたときに有効にされます。 **共有的ロック** も参照。</span><span class="sxs-lookup"><span data-stu-id="e7951-p159">Pessimistic locking is enabled when the **Recordset** object is opened with the **LockType** parameter or property set to **adLockPessimistic**. See also **optimistic locking**.</span></span>

<span data-ttu-id="e7951-365">**プール**</span><span class="sxs-lookup"><span data-stu-id="e7951-365">**pooling**</span></span>

<span data-ttu-id="e7951-p160">オブジェクトまたはデータベース接続のような、事前に割り当てられたリソースのコレクションを使用することに基づくパフォーマンス最適化。新しいリソースを作成するより、プールから既存のリソースを利用するほうが効率的です。</span><span class="sxs-lookup"><span data-stu-id="e7951-p160">A performance optimization based on using collections of pre-allocated resources, such as objects or database connections. It is more efficient to draw an existing resource from the pool than to create a new resource.</span></span>

<span data-ttu-id="e7951-368">**ProgID (プログラム識別子)**</span><span class="sxs-lookup"><span data-stu-id="e7951-368">**ProgID (programmatic identifier)**</span></span>

<span data-ttu-id="e7951-p161">COM アプリケーションで Windows レジストリにマップされた一意名。ADO 接続の ProgID は "ADODB.Connection" です。 **CLSID** 、 **COM** も参照。</span><span class="sxs-lookup"><span data-stu-id="e7951-p161">A unique name mapped to the Windows registry by a COM application. The ProgID for an ADO Connection is "ADODB.Connection". See also **CLSID**, **COM**.</span></span>

<span data-ttu-id="e7951-372">**プロキシ**</span><span class="sxs-lookup"><span data-stu-id="e7951-372">**proxy**</span></span>

<span data-ttu-id="e7951-p162">インターフェイス固有のオブジェクト。別のスレッド、他のプロセスなど、異なる実行環境で実行中のアプリケーション オブジェクトを、クライアントが呼び出す目的で必要とする、パラメーター マーシャリングと通信を提供します。プロキシはクライアントにあり、呼び出し対象のアプリケーション オブジェクトにある、対応するスタブと通信します。 **スタブ** も参照。</span><span class="sxs-lookup"><span data-stu-id="e7951-p162">An interface-specific object that provides the parameter marshaling and communication required for a client to call an application object that is running in a different execution environment, such as on a different thread or in another process. The proxy is located with the client and communicates with a corresponding stub that is located with the application object that is being called. See also **stub**.</span></span>

<span data-ttu-id="e7951-376">トップに戻る</span><span class="sxs-lookup"><span data-stu-id="e7951-376">Return to top</span></span>

## <a name="r"></a><span data-ttu-id="e7951-377">R</span><span class="sxs-lookup"><span data-stu-id="e7951-377">R</span></span>

<span data-ttu-id="e7951-378">**相対 URL**</span><span class="sxs-lookup"><span data-stu-id="e7951-378">**relative URL**</span></span>

<span data-ttu-id="e7951-p163">インターネットまたはイントラネット上のリソースを指定する部分修飾 URL。その場所は、絶対 URL または同等の ADO Connection オブジェクトで指定される出発点に対して相対的になります。連結された絶対および相対 URL は完全な URL を構成します。 **URL** と **絶対 URL** も参照。</span><span class="sxs-lookup"><span data-stu-id="e7951-p163">A partially qualified URL that specifies a resource on the Internet or an intranet whose location is relative to a starting point specified by an absolute URL or equivalent ADO Connection object. In effect, the concatenated absolute and relative URLs consitute a complete URL. See also **URL** and **absolute URL**.</span></span>

<span data-ttu-id="e7951-382">**リモート データ ソース**</span><span class="sxs-lookup"><span data-stu-id="e7951-382">**remote data source**</span></span>

<span data-ttu-id="e7951-383">(クライアント アプリケーションが実行される) ローカル システムではなく、他のコンピューターに存在するデータ ソース。</span><span class="sxs-lookup"><span data-stu-id="e7951-383">A data source that exists on a another computer, rather than on the local system (where the client application runs).</span></span>

<span data-ttu-id="e7951-384">**リソース レコード**</span><span class="sxs-lookup"><span data-stu-id="e7951-384">**resource record**</span></span>

<span data-ttu-id="e7951-p164">フォルダーまたはドキュメントの定義と詳細のフィールドを含む、ドキュメント ソース プロバイダーからのレコード。ドキュメント自体はリソース レコードに含まれませんが、一般的には、URL を含むリソース レコード内のフィールドまたは既定ストリームでアクセスできます。 **ドキュメント ソース プロバイダー** 、 **既定ストリーム** 、 **URL** も参照。</span><span class="sxs-lookup"><span data-stu-id="e7951-p164">A record from a document source provider that contains fields for the definition and description of a folder or document. The document itself is not contained in the resource record but typically can be accessed by the default stream or a field in the resource record containing a URL. See also **document source provider**, **default stream**, **URL**.</span></span>

<span data-ttu-id="e7951-388">**ルート**</span><span class="sxs-lookup"><span data-stu-id="e7951-388">**root**</span></span>

<span data-ttu-id="e7951-p165">階層ツリー構造の最上位レベル。ルート ノードは親を持ちませんが、子を持つことができます。 **階層** 、 **ツリー** 、 **親** 、 **子** も参照。</span><span class="sxs-lookup"><span data-stu-id="e7951-p165">The top level in a hierarchical tree structure. The root node has no parents, but may have children. See also **hierarchy**, **tree**, **parent**, **child**.</span></span>

<span data-ttu-id="e7951-392">**行セット**</span><span class="sxs-lookup"><span data-stu-id="e7951-392">**rowset**</span></span>

<span data-ttu-id="e7951-p166">すべて同じフィールド スキーマを持つ、データ ソースからの一連の行。行セットは、表の、すべてまたは一部のフィールドを表すことができます。また、行セットは、クエリまたは複数のテーブルの結合により作成された仮想表を表すことがあります。ADO では、行セットは **Recordset** オブジェクトで表されます。</span><span class="sxs-lookup"><span data-stu-id="e7951-p166">A set of rows from a data source, all having the same field schema. A rowset can represent all or some fields from a table. A rowset can also represent a virtual table, created by a query or a join of two or more tables. In ADO, rowsets are represented by **Recordset** objects.</span></span>

<span data-ttu-id="e7951-397">トップに戻る</span><span class="sxs-lookup"><span data-stu-id="e7951-397">Return to top</span></span>

## <a name="s"></a><span data-ttu-id="e7951-398">S</span><span class="sxs-lookup"><span data-stu-id="e7951-398">S</span></span>

<span data-ttu-id="e7951-399">**スキーマ**</span><span class="sxs-lookup"><span data-stu-id="e7951-399">**schema**</span></span>

<span data-ttu-id="e7951-p167">データベース管理システム (DBMS) でのデータベースの詳細。一般的には DBMS が提供するデータ定義言語を使用して生成されます。スキーマは、表、列、およびプロパティのような、データベースの属性を定義します。</span><span class="sxs-lookup"><span data-stu-id="e7951-p167">A description of a database to the database management system (DBMS), typically generated using the data definition language provided by the DBMS. A schema defines attributes of the database, such as tables, columns, and properties.</span></span>

<span data-ttu-id="e7951-402">**範囲**</span><span class="sxs-lookup"><span data-stu-id="e7951-402">**scope**</span></span>

<span data-ttu-id="e7951-p168">オブジェクトまたは変数の参照の範囲、あるいはビューまたは表内のレコードの範囲。たとえば、ローカル変数は定義されたプロシージャ内でのみ参照されます。パブリック変数はアプリケーション内のどこからでもアクセスできます。カレント データベースのような、オブジェクトは、定義された検索パスにある場合は、範囲内にあることになります。レコード範囲は、多くのコマンドで Scope 句により指定できます。</span><span class="sxs-lookup"><span data-stu-id="e7951-p168">The range of reference for an object or variable or a range of records in a view or table. For example, local variables can be referenced only within the procedure in which they were defined. Public variables are accessible from anywhere in the application. Objects, such as the current database, are in scope if they are in the defined search path. Record ranges can be specified with a Scope clause in many commands.</span></span>

<span data-ttu-id="e7951-408">**サービス プロバイダー**</span><span class="sxs-lookup"><span data-stu-id="e7951-408">**service provider**</span></span>

<span data-ttu-id="e7951-p169">データの作成と使用によりサービスをカプセル化して、ADO アプリケーションの機能を強化するソフトウェア。サービス プロバイダーは、データを、直接、公開するのではなく、クエリ処理のような、サービスを提供します。サービス プロバイダーは、データ プロバイダーが提供するデータを処理できます。 **データ プロバイダー** も参照。</span><span class="sxs-lookup"><span data-stu-id="e7951-p169">Software that encapsulates a service by producing and consuming data, augmenting features in your ADO applications. It is a provider that does not directly expose data, rather it provides a service, such as query processing. The service provider may process data provided by a data provider. See also **data provider**.</span></span>

<span data-ttu-id="e7951-413">**シェイプされた Recordset**</span><span class="sxs-lookup"><span data-stu-id="e7951-413">**shaped Recordset**</span></span>

<span data-ttu-id="e7951-414">列が明示的に定義された **レコードセット** の一種。データだけではなく、その他の **Recordset** オブジェクトへの参照 (チャプターと呼ばれます)、またはその他の **Recordset** オブジェクトに基づく計算された値、もしくはその両方を含みます。</span><span class="sxs-lookup"><span data-stu-id="e7951-414">A **Recordset** whose columns have been specifically defined to contain not just data, but also references (called chapters) to other **Recordset** objects and/or computed values based on other **Recordset** objects.</span></span>

<span data-ttu-id="e7951-415">**兄弟**</span><span class="sxs-lookup"><span data-stu-id="e7951-415">**sibling**</span></span>

<span data-ttu-id="e7951-p170">階層構造内で、同じレベルの階層にある、任意の複数のノード。階層内のルート ノードには兄弟はありません。</span><span class="sxs-lookup"><span data-stu-id="e7951-p170">Any two or more nodes in a hierarchical structure that are on the same level in the hierarchy. The root node in a hierarchy has no siblings.</span></span>

<span data-ttu-id="e7951-418">**ストアド プロシージャ**</span><span class="sxs-lookup"><span data-stu-id="e7951-418">**stored procedure**</span></span>

<span data-ttu-id="e7951-p171">名前を付けて保存され、1 単位として処理される、SQL ステートメント、および省略可の "フロー コントロール" ステートメントのような、コンパイル済みのコードのコレクション。ストアド プロシージャは、データベースに保存されます。これらは、アプリケーションからの呼び出しにより実行され、ユーザー宣言変数、条件付きの実行、およびその他の高機能なプログラミング機能を可能にします。</span><span class="sxs-lookup"><span data-stu-id="e7951-p171">A precompiled collection of code such as SQL statements and optional control-of-flow statements stored under a name and processed as a unit. Stored procedures are stored within a database; they can be executed with one call from an application and allow user-declared variables, conditional execution, and other powerful programming features.</span></span>

<span data-ttu-id="e7951-421">**スタブ**</span><span class="sxs-lookup"><span data-stu-id="e7951-421">**stub**</span></span>

<span data-ttu-id="e7951-p172">インターフェイス固有のオブジェクト。アプリケーション オブジェクトが、別のスレッド、他のプロセスなど、異なる実行環境で実行中のクライアントからの呼び出しを受信する目的で必要とする、パラメーター マーシャリングと通信を提供します。スタブはアプリケーション オブジェクトにあり、呼び出し元のクライアントにある、対応するプロキシと通信します。 **プロキシ** も参照。</span><span class="sxs-lookup"><span data-stu-id="e7951-p172">An interface-specific object that provides the parameter marshaling and communication required for an application object to receive calls from a client that is running in a different execution environment, such as on a different thread or in another process. The stub is located with the application object and communicates with a corresponding proxy that is located with the client that calls it. See also **proxy**.</span></span>

<span data-ttu-id="e7951-425">**下位ノード**</span><span class="sxs-lookup"><span data-stu-id="e7951-425">**sub-node**</span></span>

<span data-ttu-id="e7951-426">**子** を参照。</span><span class="sxs-lookup"><span data-stu-id="e7951-426">See **child**.</span></span>

<span data-ttu-id="e7951-427">**同期処理**</span><span class="sxs-lookup"><span data-stu-id="e7951-427">**synchronous operation**</span></span>

<span data-ttu-id="e7951-p173">次の処理が開始する前に完了する必要がある、コードにより開始された処理。 **非同期処理** も参照。</span><span class="sxs-lookup"><span data-stu-id="e7951-p173">An operation initiated by code that completes before the next operation may start. See also **asynchronous operation**.</span></span>

<span data-ttu-id="e7951-430">トップに戻る</span><span class="sxs-lookup"><span data-stu-id="e7951-430">Return to top</span></span>

## <a name="t-w"></a><span data-ttu-id="e7951-431">T-W</span><span class="sxs-lookup"><span data-stu-id="e7951-431">T-W</span></span>

<span data-ttu-id="e7951-432">**ツリー**</span><span class="sxs-lookup"><span data-stu-id="e7951-432">**tree**</span></span>

<span data-ttu-id="e7951-p174">要素 (ノード) 間の階層的な関係を表す構造。ツリーの最上位レベルには、ルートと呼ばれる 1 つのノードがあります。ルートの下には、複数の子があることがあります。各子は、その他の子の親になることができ、木のように枝分かれします。ツリー構造の一般的な例としては、ドキュメントやその他のフォルダーを含むフォルダーがあります。 **階層** 、 **ノード** 、 **ルート** 、 **子** 、 **親** も参照。</span><span class="sxs-lookup"><span data-stu-id="e7951-p174">A structure representing a hierarchical relationship between elements (nodes). There is one node at the top level of a tree (the root). Underneath the root, there can be multiple children. Each child may in turn be the parent of other children, thus branching like a tree. A folder containing documents and other folders is a typical example of a tree structure. See also **hierarchy**, **node**, **root**, **child**, **parent**.</span></span>

<span data-ttu-id="e7951-439">**URL (Uniform Resource Locator)**</span><span class="sxs-lookup"><span data-stu-id="e7951-439">**URL (Uniform Resource Locator)**</span></span>

<span data-ttu-id="e7951-p175">インターネットまたはイントラネット上にあるリソースの場所を指定します。完全な URL は、(FTP、HTTP、mailto、file のような) スキームと、それに続くコロン、サーバー名、(ドキュメント、グラフィックス、またはその他のファイルのような) リソースの完全パスから構成されます。以下は、いくつかの URL の例です。</span><span class="sxs-lookup"><span data-stu-id="e7951-p175">Specifies the location of a resource residing on the Internet or an intranet. A complete URL consists of a scheme (such as FTP, HTTP, mailto, file, and so on), followed by a colon, a server name, and the full path of a resource (such as a document, graphic, or other file). Some examples of URLs are:</span></span>  
  
- https://www.domain.com/default.html  
- <span data-ttu-id="e7951-443">ftp://ftp.server.somewhere/ftp.file</span><span class="sxs-lookup"><span data-stu-id="e7951-443">ftp://ftp.server.somewhere/ftp.file</span></span>  
  
- <span data-ttu-id="e7951-444">ftp://ftp.server.somewhere/ftp.file</span><span class="sxs-lookup"><span data-stu-id="e7951-444">ftp://ftp.server.somewhere/ftp.file</span></span>  
- <span data-ttu-id="e7951-445">file://Server/Share/File.doc</span><span class="sxs-lookup"><span data-stu-id="e7951-445">file://Server/Share/File.doc</span></span>

<span data-ttu-id="e7951-446">**絶対 URL** と **相対 URL** も参照。</span><span class="sxs-lookup"><span data-stu-id="e7951-446">See also **absolute URL** and **relative URL**.</span></span>

<span data-ttu-id="e7951-447">**web サーバー**</span><span class="sxs-lookup"><span data-stu-id="e7951-447">**web server**</span></span>

<span data-ttu-id="e7951-448">Web サービスとイントラネットとインターネットのユーザーにページを提供するコンピューターです。</span><span class="sxs-lookup"><span data-stu-id="e7951-448">A computer that provides web services and pages to intranet and Internet users.</span></span>



