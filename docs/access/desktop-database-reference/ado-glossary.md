---
title: ActiveX データオブジェクト (ADO) の用語集
TOCTitle: ADO Glossary
ms:assetid: 40f00876-7525-4117-8f57-f3d87c54be99
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249184(v=office.15)
ms:contentKeyID: 48544438
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7ecb6208a8c970f037cb0ac699c947544eb8f547
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32284835"
---
# <a name="ado-glossary"></a><span data-ttu-id="5fde7-102">ADO 用語集</span><span class="sxs-lookup"><span data-stu-id="5fde7-102">ADO glossary</span></span>

<span data-ttu-id="5fde7-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="5fde7-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="a"></a><span data-ttu-id="5fde7-104">A</span><span class="sxs-lookup"><span data-stu-id="5fde7-104">A</span></span>

<span data-ttu-id="5fde7-105">**絶対 URL**</span><span class="sxs-lookup"><span data-stu-id="5fde7-105">**absolute URL**</span></span>

<span data-ttu-id="5fde7-p101">インターネットまたはイントラネット上にあるリソースの場所を指定する完全修飾 URL。 **URL** と **相対 URL** も参照。</span><span class="sxs-lookup"><span data-stu-id="5fde7-p101">A fully qualified URL that specifies the location of a resource that resides on the Internet or an intranet. See also **URL** and **relative URL**.</span></span>

<span data-ttu-id="5fde7-108">**ActiveX コントロール**</span><span class="sxs-lookup"><span data-stu-id="5fde7-108">**ActiveX control**</span></span>

<span data-ttu-id="5fde7-p102">一般的にデザイン時間または実行時で視覚的要素を持つ、自己登録型のインプロセス COM コンポーネント。また、ActiveX コントロールは、Microsoft Internet Explorer のようなアクティブ ドキュメント コンテナーと通信できます。</span><span class="sxs-lookup"><span data-stu-id="5fde7-p102">Self-registering, in-process COM component that often has a visual element either at design time or run time. ActiveX controls also have the ability to communicate with an Active Document container, such as Microsoft Internet Explorer.</span></span>

<span data-ttu-id="5fde7-111">**ADISAPI (Advanced Data Internet Server Application Programming Interface)**</span><span class="sxs-lookup"><span data-stu-id="5fde7-111">**ADISAPI (Advanced Data Internet Server Application Programming Interface)**</span></span>

<span data-ttu-id="5fde7-p103">解析、オートメーション コントロール、 **Recordset** マーシャリング、および MIME パッケージを提供する ISAPI DLL。ADISAPI コンポーネントは、インターネット インフォメーション サービス (IIS) が提供する API により機能します。 **ISAPI** も参照。</span><span class="sxs-lookup"><span data-stu-id="5fde7-p103">An ISAPI DLL that provides parsing, Automation control, **Recordset** marshaling, and MIME packaging. The ADISAPI component works through the API provided by Internet Information Services (IIS). See also **ISAPI**.</span></span>

<span data-ttu-id="5fde7-115">**集計関数**</span><span class="sxs-lookup"><span data-stu-id="5fde7-115">**aggregate function**</span></span>

<span data-ttu-id="5fde7-p104">クエリで、表の列内のすべての行を使用して値を計算する COUNT、AVG、または STDEV のような関数。式を作成するときやプログラミングで、(前述の 3 つを含む) SQL 集計関数とドメイン集計関数を使用してさまざまな統計を得ることができます。</span><span class="sxs-lookup"><span data-stu-id="5fde7-p104">In a query, a function such as COUNT, AVG, or STDEV that calculates a value using all the rows in a column of a table. In writing expressions and in programming, you can use SQL aggregate functions (including the three listed above) and domain aggregate functions to determine various statistics.</span></span>

<span data-ttu-id="5fde7-118">**エイリアス**</span><span class="sxs-lookup"><span data-stu-id="5fde7-118">**alias**</span></span>

<span data-ttu-id="5fde7-p105">SQL SELECT ステートメントで列または式に付ける、一般的にはより短いか、より分かりやすい代替の名前。たとえば、以下の SELECT ステートメントで BobSales がエイリアスとなります。"Select wr-Sales as BobSales from SalesDB"。エイリアスは、 **DataControl** オブジェクトのコントロール バインディングに動的に列を割り当てる目的で使用できます。</span><span class="sxs-lookup"><span data-stu-id="5fde7-p105">An alternate name you give to a column or expression in an SQL SELECT statement, often shorter or more meaningful. For example, BobSales is the alias in the following SELECT statement: "Select wr-Sales as BobSales from SalesDB". An alias can be used to dynamically assign columns to control bindings on the **DataControl** object.</span></span>

<span data-ttu-id="5fde7-122">**アパートメント スレッド**</span><span class="sxs-lookup"><span data-stu-id="5fde7-122">**apartment threading**</span></span>

<span data-ttu-id="5fde7-p106">オブジェクトへのすべての呼び出しが 1 つのスレッドで発生する COM スレッド モデル。アパートメント スレッドで、COM は呼び出しを同期させ、整理します。 **COM** も参照。</span><span class="sxs-lookup"><span data-stu-id="5fde7-p106">A COM threading model where all calls to an object occur on one thread. In apartment threading, COM synchronizes and marshals calls. See also **COM**.</span></span>

<span data-ttu-id="5fde7-126">**非同期処理**</span><span class="sxs-lookup"><span data-stu-id="5fde7-126">**asynchronous operation**</span></span>

<span data-ttu-id="5fde7-p107">処理の完了を待機中せずに、呼び出し元のプログラムにコントロールを戻す処理。処理が完了する前に、コードの実行は続行されます。 **同期処理** も参照。</span><span class="sxs-lookup"><span data-stu-id="5fde7-p107">An operation that returns control to the calling program without waiting for the operation to complete. Before the operation is complete, code execution continues. See also **synchronous operation**.</span></span>

<span data-ttu-id="5fde7-130">ページのトップへ</span><span class="sxs-lookup"><span data-stu-id="5fde7-130">Return to top</span></span>

## <a name="b"></a><span data-ttu-id="5fde7-131">B</span><span class="sxs-lookup"><span data-stu-id="5fde7-131">B</span></span>

<span data-ttu-id="5fde7-132">**バインディング エントリ**</span><span class="sxs-lookup"><span data-stu-id="5fde7-132">**binding entry**</span></span>

<span data-ttu-id="5fde7-p108">表内のフィールドと変数の間のマッピング。ADO Visual C++ Extensions では、 **Recordset** フィールドは C/C++ 変数にマップされます。</span><span class="sxs-lookup"><span data-stu-id="5fde7-p108">A mapping between a field in a table and a variable. In the ADO Visual C++ extensions, **Recordset** fields are mapped to C/C++ variables.</span></span>

<span data-ttu-id="5fde7-135">**ビットマスク**</span><span class="sxs-lookup"><span data-stu-id="5fde7-135">**bitmask**</span></span>

<span data-ttu-id="5fde7-136">通常、パラメーターまたは戻り値のフラグを設定するために、他の数値とビット単位の値を比較するための数値。</span><span class="sxs-lookup"><span data-stu-id="5fde7-136">A numeric value intended for a bit-by-bit value comparison with other numeric values, typically to flag options in parameter or return values.</span></span> <span data-ttu-id="5fde7-137">通常、この比較は、and や**or** 、Visual Basic \*\*\*\* 、 **&** **|** C++ などのビット単位の論理演算子を使用して行われます。</span><span class="sxs-lookup"><span data-stu-id="5fde7-137">Usually this comparison is done with bitwise logical operators, such as **And** and **Or** in Visual Basic, **&** and **|** in C++.</span></span>

<span data-ttu-id="5fde7-p110">たとえば、ADO **FieldAttributeEnum** 値はフィールドの属性を決定する目的でビットマスクとして使用できます。あるフィールドが更新可能か確認する場合を想定します。これは、Visual Basic で以下の式により確認できます。</span><span class="sxs-lookup"><span data-stu-id="5fde7-p110">For example, the ADO **FieldAttributeEnum** values can be used as bitmasks to determine the attributes of a field. Suppose you wanted to determine if a field was updateable. You could test for this with the following expression in Visual Basic:</span></span>  
  

<span data-ttu-id="5fde7-141">結果が TRUE の場合、フィールドは更新できます。</span><span class="sxs-lookup"><span data-stu-id="5fde7-141">If the result is TRUE, then the field is updateable.</span></span>

<span data-ttu-id="5fde7-142">**ブックマーク**</span><span class="sxs-lookup"><span data-stu-id="5fde7-142">**bookmark**</span></span>

<span data-ttu-id="5fde7-143">ユーザーがすばやく表示できるように、一連の行内で、一意的に特定の行を識別するマーカー。</span><span class="sxs-lookup"><span data-stu-id="5fde7-143">A marker that uniquely identifies a row within a set of rows so that a user can quickly navigate to it.</span></span>

<span data-ttu-id="5fde7-144">**ビジネス オブジェクト**</span><span class="sxs-lookup"><span data-stu-id="5fde7-144">**business object**</span></span>

<span data-ttu-id="5fde7-p111">データの入力規則またはビジネス ルール ロジックのような、一連の定義された操作を行うオブジェクト。ビジネス オブジェクトは、通常、中間層にあります。</span><span class="sxs-lookup"><span data-stu-id="5fde7-p111">An object that performs a defined set of operations, such as data validation or business rule logic. Business objects usually reside on the middle tier.</span></span>

<span data-ttu-id="5fde7-147">**ビジネス ルール**</span><span class="sxs-lookup"><span data-stu-id="5fde7-147">**business rule**</span></span>

<span data-ttu-id="5fde7-148">The combination of validation edits, logon verifications, database lookups, policies, and algorithmic transformations that constitute an enterprise's way of doing business.</span><span class="sxs-lookup"><span data-stu-id="5fde7-148">The combination of validation edits, logon verifications, database lookups, policies, and algorithmic transformations that constitute an enterprise's way of doing business.</span></span> <span data-ttu-id="5fde7-149">*ビジネスロジック*とも呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="5fde7-149">Also known as *business logic*.</span></span>

<span data-ttu-id="5fde7-150">ページのトップへ</span><span class="sxs-lookup"><span data-stu-id="5fde7-150">Return to top</span></span>

## <a name="c"></a><span data-ttu-id="5fde7-151">C</span><span class="sxs-lookup"><span data-stu-id="5fde7-151">C</span></span>

<span data-ttu-id="5fde7-152">**計算式**</span><span class="sxs-lookup"><span data-stu-id="5fde7-152">**calculated expression**</span></span>

<span data-ttu-id="5fde7-p113">定数ではないが、値がその他の値に依存する式。計算式が評価されるには、一般的には他のフィールドまたは行のような、その他のソースから値を取得して、計算する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5fde7-p113">An expression that is not constant, but whose value depends upon other values. To be evaluated, a calculated expression must obtain and compute values from other sources, typically in other fields or rows.</span></span>

<span data-ttu-id="5fde7-155">**チャプター**</span><span class="sxs-lookup"><span data-stu-id="5fde7-155">**chapter**</span></span>

<span data-ttu-id="5fde7-p114">データ ソースからの、特定の行の範囲への参照。ADO では、一般的に、チャプターは他の **レコードセット** への参照です。</span><span class="sxs-lookup"><span data-stu-id="5fde7-p114">A reference to a range of rows from a data source. In ADO, a chapter is typically a reference to another **Recordset**.</span></span>

<span data-ttu-id="5fde7-158">チャプター列を使用すると、親がチャプター列\*\*\*\* を含む**レコードセット**であり、*子*がチャプターで表される recordset である場合に、*親と子*のリレーションシップを定義できるようになります。 \*\*</span><span class="sxs-lookup"><span data-stu-id="5fde7-158">Chapter columns make it possible to define a *parent-child* relationship where the *parent* is the **Recordset** containing the chapter column and the *child* is the **Recordset** represented by the chapter.</span></span>

<span data-ttu-id="5fde7-159">**チャプター エイリアス**</span><span class="sxs-lookup"><span data-stu-id="5fde7-159">**chapter-alias**</span></span>

<span data-ttu-id="5fde7-160">親に追加された列を参照するエイリアス。</span><span class="sxs-lookup"><span data-stu-id="5fde7-160">An alias that refers to the column appended to the parent.</span></span>

<span data-ttu-id="5fde7-161">**文字セット**</span><span class="sxs-lookup"><span data-stu-id="5fde7-161">**character set**</span></span>

<span data-ttu-id="5fde7-p115">一連の文字の数値へのマッピング。たとえば、Unicode はすべての既知の文字をエンコードできる 16 ビットの文字セットで、世界的な文字エンコードの標準として使用されています。</span><span class="sxs-lookup"><span data-stu-id="5fde7-p115">A mapping of a set of characters to their numeric values. For example, Unicode is a 16-bit character set capable of encoding all known characters and used as a worldwide character-encoding standard.</span></span>

<span data-ttu-id="5fde7-164">**子**</span><span class="sxs-lookup"><span data-stu-id="5fde7-164">**child**</span></span>

<span data-ttu-id="5fde7-p116">階層的な関係で、依存をする側。子とは、階層的な構造で、(ルートにより近い方向で) そ上に他のノードを持つノードです。 **子エイリアス** 、 **親子関係** 、 **親** も参照。</span><span class="sxs-lookup"><span data-stu-id="5fde7-p116">The dependent side of a hierarchical relationship. A child is a node in a hierarchical structure that has another node above it (closer to the root). See also **child-alias**, **parent-child relationship**, **parent**.</span></span>

<span data-ttu-id="5fde7-168">**子エイリアス**</span><span class="sxs-lookup"><span data-stu-id="5fde7-168">**child-alias**</span></span>

<span data-ttu-id="5fde7-p117">子を参照するエイリアス。 **エイリアス** 、 **子** も参照。</span><span class="sxs-lookup"><span data-stu-id="5fde7-p117">An alias that refers to the child. See also **alias**, **child**.</span></span>

<span data-ttu-id="5fde7-171">**CLSID (クラス識別子)**</span><span class="sxs-lookup"><span data-stu-id="5fde7-171">**CLSID (class identifier)**</span></span>

<span data-ttu-id="5fde7-p118">COM コンポーネントを識別する、広範囲で使われる一意識別子 (UUID)。各 COM コンポーネントは、その他のアプリケーションに読み込まれることができるように、Windows レジストリにその CLSID を持っています。 **ProgID** 、 **COM** も参照。</span><span class="sxs-lookup"><span data-stu-id="5fde7-p118">A universally unique identifier (UUID) that identifies a COM component. Each COM component has its CLSID in the Windows Registry so that it can be loaded by other applications. See also **ProgID**, **COM**.</span></span>

<span data-ttu-id="5fde7-175">**クライアント層**</span><span class="sxs-lookup"><span data-stu-id="5fde7-175">**client tier**</span></span>

<span data-ttu-id="5fde7-176">通常、データを提供し、ユーザーからの入力を処理する分散システムの論理層 (*フロントエンド*と呼ばれることもあります)。</span><span class="sxs-lookup"><span data-stu-id="5fde7-176">A logical layer of a distributed system that typically presents data to and processes input from the user, sometimes referred to as the *front end*.</span></span> <span data-ttu-id="5fde7-177">Usually, the client tier requests data from a server based on input, and then formats and displays the result.</span><span class="sxs-lookup"><span data-stu-id="5fde7-177">Usually, the client tier requests data from a server based on input, and then formats and displays the result.</span></span> <span data-ttu-id="5fde7-178">See also **middle tier**, **data source tier**, **distributed application**.</span><span class="sxs-lookup"><span data-stu-id="5fde7-178">See also **middle tier**, **data source tier**, **distributed application**.</span></span>

<span data-ttu-id="5fde7-179">**COM (Component Object Model)**</span><span class="sxs-lookup"><span data-stu-id="5fde7-179">**COM (Component Object Model)**</span></span>

<span data-ttu-id="5fde7-p120">ネットワーク接続された環境で、開発された言語やどこのコンピューターにあるかにかかわらず、オブジェクトを相互運用できるようにするバイナリ標準規格。COM ベースのテクノロジには、ActiveX コントロール、オートメーション、および OLE (オブジェクトのリンクと埋め込み) が含まれます。COM により、オブジェクトは、その他のコンポーネントとホスト アプリケーションに、その機能を公開できます。COM は、オブジェクトがそれ自体を公開する方法と、この公開がプロセス間およびネットワーク間で機能する方法を定義します。また、COM は、オブジェクトのライフ サイクルを定義します。</span><span class="sxs-lookup"><span data-stu-id="5fde7-p120">A binary standard that enables objects to interoperate in a networked environment regardless of the language in which they were developed or on which computers they reside. COM-based technologies include ActiveX Controls, Automation, and object linking and embedding (OLE). COM allows an object to expose its functionality to other components and to host applications. It defines both how the object exposes itself and how this exposure works across processes and across networks. COM also defines the object's life cycle.</span></span>

<span data-ttu-id="5fde7-185">**COM コンポーネント**</span><span class="sxs-lookup"><span data-stu-id="5fde7-185">**COM component**</span></span>

<span data-ttu-id="5fde7-p121">オブジェクトの提供方法として COM 標準をサポートする, .dll, .ocx、および一部の .exe ファイルのようなバイナリ ファイル。このようなファイルには、1 つまたは複数のクラス ファクトリ、COM クラス、レジストリ入力メカニズム、読み込みコードなどのコードが含まれます。</span><span class="sxs-lookup"><span data-stu-id="5fde7-p121">Binary file — such as .dll, .ocx, and some .exe files — that supports the COM standard for providing objects. Such a file contains code for one or more class factories, COM classes, registry-entry mechanisms, loading code, and so on.</span></span>

<span data-ttu-id="5fde7-188">**比較演算子**</span><span class="sxs-lookup"><span data-stu-id="5fde7-188">**comparison operator**</span></span>

<span data-ttu-id="5fde7-189">2 つの式を比較して、Boolean 値を戻す演算子。</span><span class="sxs-lookup"><span data-stu-id="5fde7-189">An operator that compares two expressions and returns a Boolean value.</span></span>

<span data-ttu-id="5fde7-190">"\>" (より大きい)、"\<" (より小さい)、"=" (等しい)、"\>=" (以上)、"\<=" (以下)、"\<\>" (等しくない)、または "like" (パターン マッチング) として表現されるクライテリア パラメーター。</span><span class="sxs-lookup"><span data-stu-id="5fde7-190">A criteria parameter that may be expressed as "\>" (greater than), "\<" (less than), "=" (equal), "\>=" (greater than or equal), "\<=" (less than or equal), "\<\>" (not equal), or "like" (pattern matching).</span></span>

<span data-ttu-id="5fde7-191">**コンポーネント**</span><span class="sxs-lookup"><span data-stu-id="5fde7-191">**component**</span></span>

<span data-ttu-id="5fde7-192">データとコードの両方をカプセル化し、厳密に指定された、広く入手可能な一連のサービスを提供するオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="5fde7-192">An object that encapsulates both data and code, and provides a well-specified set of publicly available services.</span></span>

<span data-ttu-id="5fde7-193">**複合ファイル**</span><span class="sxs-lookup"><span data-stu-id="5fde7-193">**compound file**</span></span>

<span data-ttu-id="5fde7-p122">ファイル用の COM 構造化記憶域の実装。複合ファイルは、個別のオブジェクトを、単一の構造化されたファイルに保存します。このファイルは、記憶域オブジェクトとストリーム オブジェクトの 2 つの主な要素から構成されます。これらは、ファイル内でファイル システムのように動作します。詳細については、Microsoft プラットフォーム SDK で複合ファイルに関する情報を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5fde7-p122">An implementation of COM structured storage for files. A compound file stores separate objects in a single, structured file consisting of two main elements: storage objects and stream objects. Together, they function like a file system within a file. For more information, see Compound Files in the Microsoft Platform SDK.</span></span>

<span data-ttu-id="5fde7-p123">1 つの物理的ファイルにバインドされた、いくつかの個別のファイル。複合ファイル内の各個別のファイルは、単一の物理的ファイルと同様にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="5fde7-p123">A number of individual files bound together in one physical file. Each individual file in a compound file can be accessed as if it were a single physical file.</span></span>

<span data-ttu-id="5fde7-200">**定数**</span><span class="sxs-lookup"><span data-stu-id="5fde7-200">**constant**</span></span>

<span data-ttu-id="5fde7-p124">変化しない数値または文字列値。名前付き ADO 列挙体 (列挙された定数) を、実際の値の代わりにコードで使用できます。たとえば、 **adUseClient** は、値が 3 の定数です (Const adUseClient = 3)。 **列挙体** も参照。</span><span class="sxs-lookup"><span data-stu-id="5fde7-p124">A numeric or string value that does not change. Named ADO enumerations (enumerated constants) can be used in your code instead of actual values, for example, **adUseClient** is a constant whose value is 3. (Const adUseClient = 3). See also **enumeration**.</span></span>

<span data-ttu-id="5fde7-205">**カーソル**</span><span class="sxs-lookup"><span data-stu-id="5fde7-205">**cursor**</span></span>

<span data-ttu-id="5fde7-206">レコード ナビゲーション、データの更新可能性、およびその他のユーザーによるデータベースへの変更の可視性を制御するデータベース要素。</span><span class="sxs-lookup"><span data-stu-id="5fde7-206">A database element that controls record navigation, updateability of data, and the visibility of changes made to the database by other users.</span></span>

<span data-ttu-id="5fde7-207">ページのトップへ</span><span class="sxs-lookup"><span data-stu-id="5fde7-207">Return to top</span></span>

## <a name="d"></a><span data-ttu-id="5fde7-208">D</span><span class="sxs-lookup"><span data-stu-id="5fde7-208">D</span></span>

<span data-ttu-id="5fde7-209">**データ バインド**</span><span class="sxs-lookup"><span data-stu-id="5fde7-209">**data binding**</span></span>

<span data-ttu-id="5fde7-210">The process of associating the objects or controls of an application to a data source.</span><span class="sxs-lookup"><span data-stu-id="5fde7-210">The process of associating the objects or controls of an application to a data source.</span></span> <span data-ttu-id="5fde7-211">データソースに関連付けられたコントロールは、*データバインドコントロール*と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="5fde7-211">A control associated with a data source is called a *data-bound control*.</span></span>

<span data-ttu-id="5fde7-p126">データ連結コントロールの内容は、データベースからの値に関連付けられます。たとえば、 **レコードセット** 内の行が更新されたとき、 **Recordset** オブジェクトに連結されたグリッド コントロールは更新できます。新しい値が **レコードセット** により取得されたとき、その新しい値はグリッドに表示されます。</span><span class="sxs-lookup"><span data-stu-id="5fde7-p126">The contents of a data-bound control are associated with values from a database. For example, a grid control that is bound to a **Recordset** object can be updated when the rows in the **Recordset** are updated. When new values are retrieved by the **Recordset**, new values are displayed in the grid.</span></span>

<span data-ttu-id="5fde7-215">**データ プロバイダー**</span><span class="sxs-lookup"><span data-stu-id="5fde7-215">**data provider**</span></span>

<span data-ttu-id="5fde7-p127">直接、またはサービス プロバイダー経由で ADO アプリケーションにデータを公開するソフトウェア。 **サービス プロバイダー** も参照。</span><span class="sxs-lookup"><span data-stu-id="5fde7-p127">Software that exposes data to an ADO application either directly or via a service provider. See also **service provider**.</span></span>

<span data-ttu-id="5fde7-218">**データ シェイプ**</span><span class="sxs-lookup"><span data-stu-id="5fde7-218">**data shaping**</span></span>

<span data-ttu-id="5fde7-219">形式化された構文 (Shape language) を使用して、データだけでなく、他の**recordset**オブジェクト\*\*\*\* への参照も含む、特別な**recordset**オブジェクト (**シェイプ言語**と呼ばれる) を定義する手法です。その他の**Recordset**オブジェクトに基づいて計算された値。</span><span class="sxs-lookup"><span data-stu-id="5fde7-219">A technique which makes use of a formalized syntax (called **Shape language**) to define a specialized **Recordset** object (called a **shaped Recordset**) that contains not just data, but also references to other **Recordset** objects and/or computed values based on those other **Recordset** objects.</span></span>

<span data-ttu-id="5fde7-220">**データ ソース層**</span><span class="sxs-lookup"><span data-stu-id="5fde7-220">**data source tier**</span></span>

<span data-ttu-id="5fde7-p128">SQL Server データベースのような、DBMS を実行中のコンピューターを表す分散システムの論理的レイヤー。 **クライアント層** 、 **中間層** 、 **分散アプリケーション** も参照。</span><span class="sxs-lookup"><span data-stu-id="5fde7-p128">A logical layer of a distributed system that represents a computer running a DBMS, such as an SQL Server database. See also **client tier**, **middle tier**, **distributed application**.</span></span>

<span data-ttu-id="5fde7-223">**DCOM**</span><span class="sxs-lookup"><span data-stu-id="5fde7-223">**DCOM**</span></span>

<span data-ttu-id="5fde7-p129">COM コンポーネントが、ネットワーク上で、直接、相互に通信できるようにするワイヤー プロトコル。 **COM** 、 **コンポーネント** も参照。</span><span class="sxs-lookup"><span data-stu-id="5fde7-p129">A wire protocol that enables COM components to communicate directly with each other across a network. See also **COM**, **component**.</span></span>

<span data-ttu-id="5fde7-226">**DDL (データ定義言語)**</span><span class="sxs-lookup"><span data-stu-id="5fde7-226">**DDL (Data Definition Language)**</span></span>

<span data-ttu-id="5fde7-p130">SQL 内で、データを操作するのではなく、データを定義するステートメント。データベースのスキーマは、DDL により作成または変更されます。たとえば、 **CREATE TABLE** 、 **CREATE INDEX** 、 **GRANT** 、および **REVOKE** は、SQL DDL ステートメントです。</span><span class="sxs-lookup"><span data-stu-id="5fde7-p130">Those statements in SQL that define, as opposed to manipulate, data. The schema of a database is created or modified with DDL. For example, **CREATE TABLE**, **CREATE INDEX**, **GRANT**, and **REVOKE** are SQL DDL statements.</span></span>

<span data-ttu-id="5fde7-230">**既定ストリーム**</span><span class="sxs-lookup"><span data-stu-id="5fde7-230">**default stream**</span></span>

<span data-ttu-id="5fde7-231">Microsoft OLE DB Provider for Internet Publishing のような、特定の OLE DB プロバイダーを使用するとき、 **Record** または **Recordset** オブジェクトに関連付けられた、( **Stream** オブジェクトで表される) テキストまたはバイナリのストリーム。</span><span class="sxs-lookup"><span data-stu-id="5fde7-231">A text or binary stream (represented by a **Stream** object) that is associated with **Record** or **Recordset** objects when using certain OLE DB providers, such as the Microsoft OLE DB Provider for Internet Publishing.</span></span> <span data-ttu-id="5fde7-232">既定のストリームには、通常、web サイトのルートの HTML コードなどのファイルの内容が含まれています。</span><span class="sxs-lookup"><span data-stu-id="5fde7-232">The default stream typically contains the contents of a file such as the HTML code for the root of a website.</span></span>

<span data-ttu-id="5fde7-233">**分散アプリケーション**</span><span class="sxs-lookup"><span data-stu-id="5fde7-233">**distributed application**</span></span>

<span data-ttu-id="5fde7-234">A program written so that the processing can be divided across multiple computers over a network.</span><span class="sxs-lookup"><span data-stu-id="5fde7-234">A program written so that the processing can be divided across multiple computers over a network.</span></span> <span data-ttu-id="5fde7-235">通常、分散アプリケーションは、プレゼンテーション、ビジネスロジック、およびデータストア層 ( *tier*) に分かれています。</span><span class="sxs-lookup"><span data-stu-id="5fde7-235">Typically, a distributed application is divided into presentation, business logic, and data store layers, or *tiers*.</span></span> <span data-ttu-id="5fde7-236">See also **client tier**, **middle tier**, **data source tier**.</span><span class="sxs-lookup"><span data-stu-id="5fde7-236">See also **client tier**, **middle tier**, **data source tier**.</span></span>

<span data-ttu-id="5fde7-237">**切断された Recordset**</span><span class="sxs-lookup"><span data-stu-id="5fde7-237">**disconnected Recordset**</span></span>

<span data-ttu-id="5fde7-p133">サーバーへのライブ接続を失った、クライアント キャッシュ内の **Recordset** オブジェクト。データを更新するなどの理由で、元のデータ ソースに、再度、アクセスする必要がある場合、接続を、再度、確立する必要があります。しかし、切断された **Recordset** のコレクション、プロパティ、およびメソッドにはまだアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="5fde7-p133">A **Recordset** object in a client cache that no longer has a live connection to the server. If the original data source needs to be accessed again for some reason, such as updating data, the connection must be re-established. However, the collections, properties, and methods of a disconnected **Recordset** can still be accessed.</span></span>

<span data-ttu-id="5fde7-241">**DLL (ダイナミック リンク ライブラリ)**</span><span class="sxs-lookup"><span data-stu-id="5fde7-241">**DLL (dynamic-link library)**</span></span>

<span data-ttu-id="5fde7-p134">1 つまたは複数の関数を含むファイルは、それらを使用するプロセスとは別に、コンパイル、リンク、および保存する必要があります。オペレーティング システムは、プロセスが開始するとき、またはその実行中に、呼び出し元のプロセスのアドレス空間に DLL をマップします。</span><span class="sxs-lookup"><span data-stu-id="5fde7-p134">A file that contains one or more functions that are compiled, linked, and stored separately from the processes that use them. The operating system maps the DLLs into the address space of the calling process when the process is starting, or while it is running.</span></span>

<span data-ttu-id="5fde7-244">**DML (データ操作言語)**</span><span class="sxs-lookup"><span data-stu-id="5fde7-244">**DML (Data Manipulation Language)**</span></span>

<span data-ttu-id="5fde7-p135">SQL 内で、データを定義するのではなく、データを操作するステートメント。データベース内の値は、DML により選択され変更されます。たとえば、 **INSERT** 、 **UPDATE** 、 **DELETE** 、および **SELECT** は、SQL DML ステートメントです。</span><span class="sxs-lookup"><span data-stu-id="5fde7-p135">Those statements in SQL that manipulate, as opposed to define, data. The values in a database are selected and modified with DML. For example, **INSERT**, **UPDATE**, **DELETE**, and **SELECT** are SQL DML statements.</span></span>

<span data-ttu-id="5fde7-248">**ドキュメント ソース プロバイダー**</span><span class="sxs-lookup"><span data-stu-id="5fde7-248">**document source provider**</span></span>

<span data-ttu-id="5fde7-p136">フォルダーとドキュメントを管理する、プロバイダーの特殊なクラス。 **Record** オブジェクトがドキュメントを表しているか、または **Recordset** オブジェクトがドキュメントのフォルダーを表している場合には、ドキュメント ソース プロバイダーは、実際のドキュメント自体ではなくドキュメントの特徴を記述した固有のフィールドのセットで、これらのオブジェクトにデータを設定します。 **リソース レコード** も参照。</span><span class="sxs-lookup"><span data-stu-id="5fde7-p136">A special class of providers that manage folders and documents. When a document is represented by a **Record** object, or a folder of documents is represented by a **Recordset** object, the document source provider populates those objects with a unique set of fields that describe characteristics of the document, instead of the actual document itself. See also **resource record**.</span></span>

<span data-ttu-id="5fde7-252">**DSN (データ ソース名)**</span><span class="sxs-lookup"><span data-stu-id="5fde7-252">**DSN (data source name)**</span></span>

<span data-ttu-id="5fde7-p137">アプリケーションを特定の ODBC データベースに接続する目的で使用される情報のコレクション。ODBC ドライバー マネージャーは、この情報を使用してデータベースに接続します。DSN は、ファイル (ファイル DSN)、または Windows レジストリ (コンピューター DSN) に保存できます。</span><span class="sxs-lookup"><span data-stu-id="5fde7-p137">The collection of information used to connect your application to a particular ODBC database. The ODBC Driver Manager uses this information to create a connection to the database. A DSN can be stored in a file (a file DSN) or in the Windows Registry (a machine DSN).</span></span>

<span data-ttu-id="5fde7-256">**動的プロパティ**</span><span class="sxs-lookup"><span data-stu-id="5fde7-256">**dynamic property**</span></span>

<span data-ttu-id="5fde7-257">データプロバイダーまたは cursor service に固有のプロパティ。</span><span class="sxs-lookup"><span data-stu-id="5fde7-257">A property specific to a data provider or the cursor service.</span></span> <span data-ttu-id="5fde7-258">オブジェクトの**Properties**コレクションは、自動的に ("動的" に) 設定されます。</span><span class="sxs-lookup"><span data-stu-id="5fde7-258">The **Properties** collection of an object is populated with these automatically ("dynamically").</span></span> <span data-ttu-id="5fde7-259">オブジェクトには、特定のデータプロバイダーによってデータソースに接続されるまで、動的プロパティはありません。</span><span class="sxs-lookup"><span data-stu-id="5fde7-259">An object has no dynamic properties until it is connected to a data source through a particular data provider.</span></span> <span data-ttu-id="5fde7-260">**データプロバイダー**、**カーソル**も参照してください。</span><span class="sxs-lookup"><span data-stu-id="5fde7-260">See also **data provider**, **cursor**.</span></span>

<span data-ttu-id="5fde7-261">ページのトップへ</span><span class="sxs-lookup"><span data-stu-id="5fde7-261">Return to top</span></span>

## <a name="e-i"></a><span data-ttu-id="5fde7-262">E-I</span><span class="sxs-lookup"><span data-stu-id="5fde7-262">E-I</span></span>

<span data-ttu-id="5fde7-263">**体内**</span><span class="sxs-lookup"><span data-stu-id="5fde7-263">**enumeration**</span></span>

<span data-ttu-id="5fde7-264">名前付き定数のリスト。</span><span class="sxs-lookup"><span data-stu-id="5fde7-264">A list of named constants.</span></span> <span data-ttu-id="5fde7-265">列挙値は一意である必要はありません。</span><span class="sxs-lookup"><span data-stu-id="5fde7-265">Enumerated values need not be unique.</span></span> <span data-ttu-id="5fde7-266">ただし、各値の名前は、列挙が定義されているスコープ内で一意である必要があります。</span><span class="sxs-lookup"><span data-stu-id="5fde7-266">However the name of each value must be unique within the scope where the enumeration is defined.</span></span> <span data-ttu-id="5fde7-267">ado では、列挙体を数値パラメーターと戻り値に使用して、ado コードに意味を追加し、開発者に数値を適用することができます (バージョンからバージョンに変更される可能性があります)。</span><span class="sxs-lookup"><span data-stu-id="5fde7-267">In ADO, enumerations are used for numeric parameter and return values, to add meaning to ADO code and to shield the developer from the numeric values (which may change from version to version).</span></span> <span data-ttu-id="5fde7-268">たとえば、静的**Recordset**を開くには、 **adopenstatic**列挙値を使用します。</span><span class="sxs-lookup"><span data-stu-id="5fde7-268">For example, to open a static **Recordset**, use the **adOpenStatic** enumerated value:</span></span>  
  

<span data-ttu-id="5fde7-269">"*列挙定数*" とも呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="5fde7-269">Also referred to as *enumerated constant*.</span></span> <span data-ttu-id="5fde7-270">**定数**も参照してください。</span><span class="sxs-lookup"><span data-stu-id="5fde7-270">See also **constant**.</span></span>

<span data-ttu-id="5fde7-271">**event**</span><span class="sxs-lookup"><span data-stu-id="5fde7-271">**event**</span></span>

<span data-ttu-id="5fde7-272">オブジェクトによって認識されるアクション。これに対して、応答するコードを記述できます。</span><span class="sxs-lookup"><span data-stu-id="5fde7-272">An action recognized by an object, for which you can write code to respond.</span></span> <span data-ttu-id="5fde7-273">イベントは、他のアクションと共に、コマンドの実行、トランザクションの完了、レコードセットの移動、およびデータの更新によって生成できます。</span><span class="sxs-lookup"><span data-stu-id="5fde7-273">Events can be generated by command execution, transaction completion, recordset navigation, and data updates, among other actions.</span></span> <span data-ttu-id="5fde7-274">**イベントハンドラー**も参照してください。</span><span class="sxs-lookup"><span data-stu-id="5fde7-274">See also **event handler**.</span></span>

<span data-ttu-id="5fde7-275">**イベント ハンドラー**</span><span class="sxs-lookup"><span data-stu-id="5fde7-275">**event handler**</span></span>

<span data-ttu-id="5fde7-276">イベントハンドラーは、イベントが発生したときに実行されるコードです。</span><span class="sxs-lookup"><span data-stu-id="5fde7-276">An event handler is the code that is executed when an event occurs.</span></span> <span data-ttu-id="5fde7-277">**イベント**も参照してください。</span><span class="sxs-lookup"><span data-stu-id="5fde7-277">See also **event**.</span></span>

<span data-ttu-id="5fde7-278">**handler**</span><span class="sxs-lookup"><span data-stu-id="5fde7-278">**handler**</span></span>

<span data-ttu-id="5fde7-279">エラー回復またはデータ管理など、一般的で比較的単純な条件または操作を管理するルーチン。</span><span class="sxs-lookup"><span data-stu-id="5fde7-279">A routine that manages a common and relatively simple condition or operation, such as error recovery or data management.</span></span>

<span data-ttu-id="5fde7-280">**階層 Recordset**</span><span class="sxs-lookup"><span data-stu-id="5fde7-280">**hierarchical Recordset**</span></span>

<span data-ttu-id="5fde7-281">別の**recordset**を含む**recordset** 。</span><span class="sxs-lookup"><span data-stu-id="5fde7-281">A **Recordset** that contains another **Recordset**.</span></span> <span data-ttu-id="5fde7-282">**データシェイプ**、**チャプター**も参照。</span><span class="sxs-lookup"><span data-stu-id="5fde7-282">See also **data shaping**, **chapter**.</span></span>

<span data-ttu-id="5fde7-283">詳細については、「[階層 Recordset 内の行へのアクセス](accessing-rows-in-a-hierarchical-recordset.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5fde7-283">For more information, see [Accessing Rows in a Hierarchical Recordset](accessing-rows-in-a-hierarchical-recordset.md)</span></span>

<span data-ttu-id="5fde7-284">**階層**</span><span class="sxs-lookup"><span data-stu-id="5fde7-284">**hierarchy**</span></span>

<span data-ttu-id="5fde7-285">一般的に、階層とは、最上位レベルと下位レベルのランク構造です。</span><span class="sxs-lookup"><span data-stu-id="5fde7-285">In general, a hierarchy is a ranked structure with a top level and subordinate levels.</span></span> <span data-ttu-id="5fde7-286">ADO では、階層**recordset**を使用して、レコードとチャプター間の親子関係を表すことができます。</span><span class="sxs-lookup"><span data-stu-id="5fde7-286">In ADO, hierarchical **Recordsets** are used to represent the parent-child relationship between a record and a chapter.</span></span> <span data-ttu-id="5fde7-287">また、ADO では、 **Record**オブジェクトと**Stream**オブジェクトを使用して、フォルダーやドキュメントなどの階層ツリー構造にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="5fde7-287">Also in ADO, **Record** and **Stream** objects can be used to access hierarchical tree structures such as a folder and documents.</span></span> <span data-ttu-id="5fde7-288">ADO MD には、OLAP キューブのディメンションのレベル間の関係を表す**階層**オブジェクトも含まれています。</span><span class="sxs-lookup"><span data-stu-id="5fde7-288">ADO MD also includes **Hierarchy** objects to represent a relationship between the levels of a dimension in an OLAP cube.</span></span> <span data-ttu-id="5fde7-289">**階層 recordset**、**親子関係**、**チャプター**、**ツリー**も参照。</span><span class="sxs-lookup"><span data-stu-id="5fde7-289">See also **hierarchical Recordsets**, **parent-child relationship**, **chapter**, **tree**.</span></span>

<span data-ttu-id="5fde7-290">**ISAPI (インターネットサーバーアプリケーションプログラミングインターフェイス)**</span><span class="sxs-lookup"><span data-stu-id="5fde7-290">**ISAPI (Internet Server Application Programming Interface)**</span></span>

<span data-ttu-id="5fde7-291">Microsoft インターネットインフォメーションサービス (IIS) を実行している windows NT server/windows 2000 サーバーなど、インターネットサーバー用の一連の関数。</span><span class="sxs-lookup"><span data-stu-id="5fde7-291">A set of functions for Internet servers, such as a Windows NT Server/Windows 2000 Server running Microsoft Internet Information Services (IIS).</span></span>

<span data-ttu-id="5fde7-292">ページのトップへ</span><span class="sxs-lookup"><span data-stu-id="5fde7-292">Return to top</span></span>

## <a name="k-m"></a><span data-ttu-id="5fde7-293">K ~ M</span><span class="sxs-lookup"><span data-stu-id="5fde7-293">K-M</span></span>

<span data-ttu-id="5fde7-294">**key**</span><span class="sxs-lookup"><span data-stu-id="5fde7-294">**key**</span></span>

<span data-ttu-id="5fde7-295">行を一意に識別するテーブル内の1つまたは複数の列。多くの場合、テーブルにインデックスを作成するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="5fde7-295">A column or columns in a table that uniquely identify a row; often used to index a table.</span></span>

<span data-ttu-id="5fde7-296">**マーシャリング**</span><span class="sxs-lookup"><span data-stu-id="5fde7-296">**marshaling**</span></span>

<span data-ttu-id="5fde7-297">スレッドまたはプロセスの境界を越えて、インターフェイスメソッドのパラメーターをパッケージ化、送信、および越えするプロセス。</span><span class="sxs-lookup"><span data-stu-id="5fde7-297">The process of packaging, sending, and unpackaging interface method parameters across thread or process boundaries.</span></span>

<span data-ttu-id="5fde7-298">**中間層**</span><span class="sxs-lookup"><span data-stu-id="5fde7-298">**middle tier**</span></span>

<span data-ttu-id="5fde7-299">ユーザーインターフェイスまたは web クライアントとデータベースの間の分散システムの論理層。</span><span class="sxs-lookup"><span data-stu-id="5fde7-299">The logical layer in a distributed system between a user interface or web client and the database.</span></span> <span data-ttu-id="5fde7-300">通常は、ビジネスオブジェクトがインスタンス化されます。</span><span class="sxs-lookup"><span data-stu-id="5fde7-300">This is typically where business objects are instantiated.</span></span> <span data-ttu-id="5fde7-301">中間層は、情報を受信するときに生成および操作するビジネスルールおよび関数の集合です。</span><span class="sxs-lookup"><span data-stu-id="5fde7-301">The middle tier is a collection of business rules and functions that generate and operate upon receiving information.</span></span> <span data-ttu-id="5fde7-302">これは、ビジネスルールを使用して、頻繁に変更されることがあり、アプリケーションロジック自体から物理的に分離されたコンポーネントにカプセル化されます。</span><span class="sxs-lookup"><span data-stu-id="5fde7-302">They accomplish this through business rules, which can change frequently, and are thus encapsulated into components that are physically separate from the application logic itself.</span></span> <span data-ttu-id="5fde7-303">*アプリケーションサーバー層*とも呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="5fde7-303">Also known as *application server tier*.</span></span> <span data-ttu-id="5fde7-304">「**分散アプリケーション**」、「**クライアント層**」、および「**データソース層**」も参照してください。</span><span class="sxs-lookup"><span data-stu-id="5fde7-304">See also **distributed application**, **client tier**, **data source tier**.</span></span>

<span data-ttu-id="5fde7-305">**MIME (複数目的のインターネットメール内線番号)**</span><span class="sxs-lookup"><span data-stu-id="5fde7-305">**MIME (Multi-purpose Internet Mail Extension)**</span></span>

<span data-ttu-id="5fde7-306">最初に開発されたインターネットプロトコルで、異種のネットワーク、コンピューター、および電子メール環境にわたるリッチコンテンツで電子メールメッセージを交換できるようにしました。</span><span class="sxs-lookup"><span data-stu-id="5fde7-306">An Internet protocol originally developed to allow exchange of electronic mail messages with rich content across heterogeneous network, machine, and email environments.</span></span> <span data-ttu-id="5fde7-307">実際には、MIME はメール以外のアプリケーションによって採用および拡張されています。</span><span class="sxs-lookup"><span data-stu-id="5fde7-307">In practice, MIME has also been adopted and extended by non-mail applications.</span></span>

<span data-ttu-id="5fde7-308">MIME は、インターネット上でバイナリデータを公開および読み取りできるようにするための標準です。</span><span class="sxs-lookup"><span data-stu-id="5fde7-308">MIME is a standard that allows binary data to be published and read on the Internet.</span></span> <span data-ttu-id="5fde7-309">バイナリデータを含むファイルのヘッダーには、データの MIME タイプが含まれています。これにより、クライアントプログラム (web ブラウザー、メールパッケージなど) に対して、直線テキストを処理するのと異なる方法でデータを処理する必要があることが通知されます。</span><span class="sxs-lookup"><span data-stu-id="5fde7-309">The header of a file with binary data contains the MIME type of the data; this informs client programs (web browsers and mail packages, for instance) that they will need to handle the data in a different way than they handle straight text.</span></span> <span data-ttu-id="5fde7-310">たとえば、jpeg グラフィックを含む web ドキュメントのヘッダーには、jpeg ファイル形式に固有の MIME の種類が含まれています。</span><span class="sxs-lookup"><span data-stu-id="5fde7-310">For example, the header of a web document containing a JPEG graphic contains the MIME type specific to the JPEG file format.</span></span> <span data-ttu-id="5fde7-311">これにより、ブラウザーは、ファイルが存在する場合は、そのファイルを JPEG ビューアーで表示できます。</span><span class="sxs-lookup"><span data-stu-id="5fde7-311">This allows a browser to display the file with its JPEG viewer, if one is present.</span></span>

<span data-ttu-id="5fde7-312">ページのトップへ</span><span class="sxs-lookup"><span data-stu-id="5fde7-312">Return to top</span></span>

## <a name="n-o"></a><span data-ttu-id="5fde7-313">N-O</span><span class="sxs-lookup"><span data-stu-id="5fde7-313">N-O</span></span>

<span data-ttu-id="5fde7-314">**ノード**</span><span class="sxs-lookup"><span data-stu-id="5fde7-314">**node**</span></span>

<span data-ttu-id="5fde7-315">階層ツリー構造内の要素。</span><span class="sxs-lookup"><span data-stu-id="5fde7-315">An element in a hierarchical tree structure.</span></span> <span data-ttu-id="5fde7-316">ノードは、ルートまたは別のノードの子である場合があります。</span><span class="sxs-lookup"><span data-stu-id="5fde7-316">A node may be the root, or the child of another node.</span></span> <span data-ttu-id="5fde7-317">ノードは、複数の子の親にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="5fde7-317">A node can also be the parent of multiple children.</span></span> <span data-ttu-id="5fde7-318">**階層**、**ツリー**、**ルート**、**子**、**親**も参照。</span><span class="sxs-lookup"><span data-stu-id="5fde7-318">See also **hierarchy**, **tree**, **root**, **child**, **parent**.</span></span>

<span data-ttu-id="5fde7-319">**オブジェクト変数**</span><span class="sxs-lookup"><span data-stu-id="5fde7-319">**object variable**</span></span>

<span data-ttu-id="5fde7-320">オブジェクトに対する参照を含む変数。</span><span class="sxs-lookup"><span data-stu-id="5fde7-320">A variable that contains a reference to an object.</span></span> <span data-ttu-id="5fde7-321">たとえば、objcustomobject 指定する変数は、次のような型のオブジェクトを指す変数です。</span><span class="sxs-lookup"><span data-stu-id="5fde7-321">For example, objCustomObject is a variable that points to an object of type CustomObject:</span></span>  
  
<span data-ttu-id="5fde7-322">は、型が customobject オブジェクトを指す変数です。</span><span class="sxs-lookup"><span data-stu-id="5fde7-322">is a variable that points to an object of type CustomObject:</span></span>  
  
<span data-ttu-id="5fde7-323">objcustomobject を設定します (adodb)。レコード</span><span class="sxs-lookup"><span data-stu-id="5fde7-323">Set objCustomObject = CreateObject(adodb.Recordset)</span></span>

<span data-ttu-id="5fde7-324">**ODBC (Open Database Connectivity)**</span><span class="sxs-lookup"><span data-stu-id="5fde7-324">**ODBC (Open Database Connectivity)**</span></span>

<span data-ttu-id="5fde7-325">さまざまなデータソースに接続するために使用される標準のプログラミング言語インターフェイス。</span><span class="sxs-lookup"><span data-stu-id="5fde7-325">A standard programming language interface used to connect to a variety of data sources.</span></span> <span data-ttu-id="5fde7-326">これには、通常、特定の ODBC ドライバーを使用するようにデータソース名 (dsn) を割り当てることができるコントロールパネルからアクセスします。</span><span class="sxs-lookup"><span data-stu-id="5fde7-326">This is usually accessed through Control Panel, where data source names (DSNs) can be assigned to use specific ODBC drivers.</span></span>

<span data-ttu-id="5fde7-327">**OLE DB**</span><span class="sxs-lookup"><span data-stu-id="5fde7-327">**OLE DB**</span></span>

<span data-ttu-id="5fde7-328">COM を使用してさまざまなソースからデータを公開する一連のインターフェイス。</span><span class="sxs-lookup"><span data-stu-id="5fde7-328">A set of interfaces that expose data from a variety of sources using COM.</span></span> <span data-ttu-id="5fde7-329">OLE DB インターフェイスは、さまざまな情報ソースに格納されているデータへの一貫したアクセスをアプリケーションに提供します。</span><span class="sxs-lookup"><span data-stu-id="5fde7-329">OLE DB interfaces provide applications with uniform access to data stored in diverse information sources.</span></span> <span data-ttu-id="5fde7-330">これらのインターフェイスは、データソースに適した DBMS 機能の量をサポートし、データを共有できるようにします。</span><span class="sxs-lookup"><span data-stu-id="5fde7-330">These interfaces support the amount of DBMS functionality appropriate to the data source, enabling it to share its data.</span></span> <span data-ttu-id="5fde7-331">**COM** も参照。</span><span class="sxs-lookup"><span data-stu-id="5fde7-331">See also **COM**.</span></span>

<span data-ttu-id="5fde7-332">**共有的ロック**</span><span class="sxs-lookup"><span data-stu-id="5fde7-332">**optimistic locking**</span></span>

<span data-ttu-id="5fde7-333">ロックの種類。編集中のレコードを含む、1つまたは複数のレコードを含むデータページは、 **update**メソッドによってレコードが更新されている間のみ、他のユーザーが使用できなくなりますが、**更新**の呼び出し前後で利用できます。.</span><span class="sxs-lookup"><span data-stu-id="5fde7-333">A type of locking in which the data page containing one or more records, including the record being edited, is unavailable to other users only while the record is being updated by the **Update** method, but is available before and after the call to **Update**.</span></span>

<span data-ttu-id="5fde7-334">共有的ロックは、 **LockType**パラメーターまたはプロパティを**adlockoptimistic**または**adlockbatch楽観的**に設定して**Recordset**オブジェクトを開いたときに使用されます。</span><span class="sxs-lookup"><span data-stu-id="5fde7-334">Optimistic locking is used when the **Recordset** object is opened with the **LockType** parameter or property set to **adLockOptimistic** or **adLockBatchOptimistic**.</span></span> <span data-ttu-id="5fde7-335">**排他的ロック**も参照してください。</span><span class="sxs-lookup"><span data-stu-id="5fde7-335">See also **pessimistic locking**.</span></span>

<span data-ttu-id="5fde7-336">**序数値**</span><span class="sxs-lookup"><span data-stu-id="5fde7-336">**ordinal value**</span></span>

<span data-ttu-id="5fde7-337">順序内のアイテムの位置を表す数値を指定します。</span><span class="sxs-lookup"><span data-stu-id="5fde7-337">The numeric location of an item within an order.</span></span> <span data-ttu-id="5fde7-338">ADO コレクションでは、最初の項目の序数値はゼロ (0) になります。</span><span class="sxs-lookup"><span data-stu-id="5fde7-338">In an ADO collection, the ordinal value of the first item is zero (0).</span></span> <span data-ttu-id="5fde7-339">次のアイテムは 1 (1) というようになります。</span><span class="sxs-lookup"><span data-stu-id="5fde7-339">The next item is one (1), and so on.</span></span>

<span data-ttu-id="5fde7-340">ページのトップへ</span><span class="sxs-lookup"><span data-stu-id="5fde7-340">Return to top</span></span>

## <a name="p"></a><span data-ttu-id="5fde7-341">P</span><span class="sxs-lookup"><span data-stu-id="5fde7-341">P</span></span>

<span data-ttu-id="5fde7-342">**パラメーター化されたコマンド**</span><span class="sxs-lookup"><span data-stu-id="5fde7-342">**parameterized command**</span></span>

<span data-ttu-id="5fde7-343">コマンドを実行する前にパラメーター値を設定できるようにするクエリまたはコマンド。</span><span class="sxs-lookup"><span data-stu-id="5fde7-343">A query or command that allows you to set parameter values before the command is executed.</span></span> <span data-ttu-id="5fde7-344">たとえば、sql 文字列をパラメーター化するには、sql 文字列 ('? ' 文字で指定) にパラメーターマーカーを埋め込む必要があります。</span><span class="sxs-lookup"><span data-stu-id="5fde7-344">For example, a SQL string can be parameterized by embedding parameter markers in the SQL string (designated by the '?' character).</span></span> <span data-ttu-id="5fde7-345">次に、アプリケーションは各パラメーターの値を指定し、コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="5fde7-345">The application then specifies values for each parameter and executes the command.</span></span>

<span data-ttu-id="5fde7-346">**親行**</span><span class="sxs-lookup"><span data-stu-id="5fde7-346">**parent**</span></span>

<span data-ttu-id="5fde7-347">階層関係の制御側。</span><span class="sxs-lookup"><span data-stu-id="5fde7-347">The controlling side of a hierarchical relationship.</span></span> <span data-ttu-id="5fde7-348">階層構造では、親は階層の直下に1つ以上の子ノードを持っています。</span><span class="sxs-lookup"><span data-stu-id="5fde7-348">In a hierarchical structure, a parent has one or more child nodes directly beneath it in the hierarchy.</span></span> <span data-ttu-id="5fde7-349">**親-エイリアス**、**親子関係**、**子**も参照。</span><span class="sxs-lookup"><span data-stu-id="5fde7-349">See also **parent-alias**, **parent-child relationship**, **child**.</span></span>

<span data-ttu-id="5fde7-350">**parent-alias**</span><span class="sxs-lookup"><span data-stu-id="5fde7-350">**parent-alias**</span></span>

<span data-ttu-id="5fde7-351">親を参照する別名。</span><span class="sxs-lookup"><span data-stu-id="5fde7-351">An alias that refers to the parent.</span></span> <span data-ttu-id="5fde7-352">**エイリアス**、**親**も参照。</span><span class="sxs-lookup"><span data-stu-id="5fde7-352">See also **alias**, **parent**.</span></span>

<span data-ttu-id="5fde7-353">**親子関係**</span><span class="sxs-lookup"><span data-stu-id="5fde7-353">**parent-child relationship**</span></span>

<span data-ttu-id="5fde7-354">階層構造で、親が1レベル高く、1つまたは複数の子に直接関連付けられているリレーションシップ。</span><span class="sxs-lookup"><span data-stu-id="5fde7-354">A relationship in a hierarchical structure in which the parent is one level higher and directly associated with one or more children.</span></span> <span data-ttu-id="5fde7-355">子は1レベル下で、1つの親を持つ必要があります。</span><span class="sxs-lookup"><span data-stu-id="5fde7-355">A child is one level lower and must have one parent.</span></span> <span data-ttu-id="5fde7-356">**親**、**子**も参照。</span><span class="sxs-lookup"><span data-stu-id="5fde7-356">See also **parent**, **child**.</span></span>

<span data-ttu-id="5fde7-357">**続き**</span><span class="sxs-lookup"><span data-stu-id="5fde7-357">**persist**</span></span>

<span data-ttu-id="5fde7-358">ファイルに**Recordset**を保存するなど、データを永続的な状態で保存すること。</span><span class="sxs-lookup"><span data-stu-id="5fde7-358">To save data in a permanent state, such as saving a **Recordset** to a file.</span></span>

<span data-ttu-id="5fde7-359">**排他的ロック**</span><span class="sxs-lookup"><span data-stu-id="5fde7-359">**pessimistic locking**</span></span>

<span data-ttu-id="5fde7-360">ロックの種類。編集中のレコードを含む1つまたは複数のレコードを含むページを、他のユーザーが使用できないようにして、更新が行われるようにします。</span><span class="sxs-lookup"><span data-stu-id="5fde7-360">A type of locking in which the page containing one or more records, including the record being edited, is unavailable to other users to ensure that an update will be made.</span></span> <span data-ttu-id="5fde7-361">排他的ロック動作は、OLE DB プロバイダーによって定義されます。</span><span class="sxs-lookup"><span data-stu-id="5fde7-361">Pessimistic locking behavior is defined by the OLE DB provider.</span></span> <span data-ttu-id="5fde7-362">通常、レコードは編集時にロックされ、 **Update**メソッドが完了するまで使用できなくなります。</span><span class="sxs-lookup"><span data-stu-id="5fde7-362">Typically, records are locked upon editing and remain unavailable until the **Update** method has completed.</span></span>

<span data-ttu-id="5fde7-363">**Recordset**オブジェクトを開くときに、 **LockType**パラメーターまたはプロパティを**adlockpessimistic**に設定して、排他ロックが有効になります。</span><span class="sxs-lookup"><span data-stu-id="5fde7-363">Pessimistic locking is enabled when the **Recordset** object is opened with the **LockType** parameter or property set to **adLockPessimistic**.</span></span> <span data-ttu-id="5fde7-364">「**共有的ロック**」も参照してください。</span><span class="sxs-lookup"><span data-stu-id="5fde7-364">See also **optimistic locking**.</span></span>

<span data-ttu-id="5fde7-365">**待機**</span><span class="sxs-lookup"><span data-stu-id="5fde7-365">**pooling**</span></span>

<span data-ttu-id="5fde7-366">オブジェクトまたはデータベース接続など、事前に割り当てられたリソースのコレクションを使用することによるパフォーマンスの最適化。</span><span class="sxs-lookup"><span data-stu-id="5fde7-366">A performance optimization based on using collections of pre-allocated resources, such as objects or database connections.</span></span> <span data-ttu-id="5fde7-367">新しいリソースを作成するよりも、プールから既存のリソースを描画する方が効率的です。</span><span class="sxs-lookup"><span data-stu-id="5fde7-367">It is more efficient to draw an existing resource from the pool than to create a new resource.</span></span>

<span data-ttu-id="5fde7-368">**ProgID (プログラム識別子)**</span><span class="sxs-lookup"><span data-stu-id="5fde7-368">**ProgID (programmatic identifier)**</span></span>

<span data-ttu-id="5fde7-369">COM アプリケーションによって Windows レジストリにマップされた一意の名前。</span><span class="sxs-lookup"><span data-stu-id="5fde7-369">A unique name mapped to the Windows registry by a COM application.</span></span> <span data-ttu-id="5fde7-370">ADO 接続の ProgID は "ADODB" です。接続」を行います。</span><span class="sxs-lookup"><span data-stu-id="5fde7-370">The ProgID for an ADO Connection is "ADODB.Connection".</span></span> <span data-ttu-id="5fde7-371">**CLSID**、 **COM**も参照。</span><span class="sxs-lookup"><span data-stu-id="5fde7-371">See also **CLSID**, **COM**.</span></span>

<span data-ttu-id="5fde7-372">**プロキシ**</span><span class="sxs-lookup"><span data-stu-id="5fde7-372">**proxy**</span></span>

<span data-ttu-id="5fde7-373">クライアントが別のスレッドまたは別のプロセスなど、異なる実行環境で実行されているアプリケーションオブジェクトを呼び出すために必要なパラメーターのマーシャリングと通信を提供するインターフェイス固有のオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="5fde7-373">An interface-specific object that provides the parameter marshaling and communication required for a client to call an application object that is running in a different execution environment, such as on a different thread or in another process.</span></span> <span data-ttu-id="5fde7-374">プロキシはクライアントと共に配置され、呼び出されているアプリケーションオブジェクトにある対応するスタブと通信します。</span><span class="sxs-lookup"><span data-stu-id="5fde7-374">The proxy is located with the client and communicates with a corresponding stub that is located with the application object that is being called.</span></span> <span data-ttu-id="5fde7-375">「**スタブ**」も参照してください。</span><span class="sxs-lookup"><span data-stu-id="5fde7-375">See also **stub**.</span></span>

<span data-ttu-id="5fde7-376">ページのトップへ</span><span class="sxs-lookup"><span data-stu-id="5fde7-376">Return to top</span></span>

## <a name="r"></a><span data-ttu-id="5fde7-377">R</span><span class="sxs-lookup"><span data-stu-id="5fde7-377">R</span></span>

<span data-ttu-id="5fde7-378">**相対 URL**</span><span class="sxs-lookup"><span data-stu-id="5fde7-378">**relative URL**</span></span>

<span data-ttu-id="5fde7-379">絶対 url または同等の ADO Connection オブジェクトで指定された開始点を基準とした場所にあるインターネットまたはイントラネット上のリソースを指定する、部分的に修飾された url。</span><span class="sxs-lookup"><span data-stu-id="5fde7-379">A partially qualified URL that specifies a resource on the Internet or an intranet whose location is relative to a starting point specified by an absolute URL or equivalent ADO Connection object.</span></span> <span data-ttu-id="5fde7-380">実質的には、consitute の絶対 url と相対 url が完全な url になります。</span><span class="sxs-lookup"><span data-stu-id="5fde7-380">In effect, the concatenated absolute and relative URLs consitute a complete URL.</span></span> <span data-ttu-id="5fde7-381">**url**と**絶対 url**も参照してください。</span><span class="sxs-lookup"><span data-stu-id="5fde7-381">See also **URL** and **absolute URL**.</span></span>

<span data-ttu-id="5fde7-382">**リモートデータソース**</span><span class="sxs-lookup"><span data-stu-id="5fde7-382">**remote data source**</span></span>

<span data-ttu-id="5fde7-383">ローカルシステムではなく、(クライアントアプリケーションが実行されている) 別のコンピューター上に存在するデータソース。</span><span class="sxs-lookup"><span data-stu-id="5fde7-383">A data source that exists on a another computer, rather than on the local system (where the client application runs).</span></span>

<span data-ttu-id="5fde7-384">**リソースレコード**</span><span class="sxs-lookup"><span data-stu-id="5fde7-384">**resource record**</span></span>

<span data-ttu-id="5fde7-385">ドキュメントソースプロバイダーからのレコード。フォルダーまたはドキュメントの定義と説明のフィールドが含まれています。</span><span class="sxs-lookup"><span data-stu-id="5fde7-385">A record from a document source provider that contains fields for the definition and description of a folder or document.</span></span> <span data-ttu-id="5fde7-386">ドキュメント自体はリソースレコードに含まれていませんが、通常は、既定のストリーム、または URL を含むリソースレコードのフィールドによってアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="5fde7-386">The document itself is not contained in the resource record but typically can be accessed by the default stream or a field in the resource record containing a URL.</span></span> <span data-ttu-id="5fde7-387">「**ドキュメントソースプロバイダー**」、「**既定のストリーム**、 **URL**」も参照してください。</span><span class="sxs-lookup"><span data-stu-id="5fde7-387">See also **document source provider**, **default stream**, **URL**.</span></span>

<span data-ttu-id="5fde7-388">**root**</span><span class="sxs-lookup"><span data-stu-id="5fde7-388">**root**</span></span>

<span data-ttu-id="5fde7-389">階層ツリー構造の最上位レベル。</span><span class="sxs-lookup"><span data-stu-id="5fde7-389">The top level in a hierarchical tree structure.</span></span> <span data-ttu-id="5fde7-390">ルートノードには、親はありませんが、子がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="5fde7-390">The root node has no parents, but may have children.</span></span> <span data-ttu-id="5fde7-391">**階層**、**ツリー**、**親**、**子**も参照。</span><span class="sxs-lookup"><span data-stu-id="5fde7-391">See also **hierarchy**, **tree**, **parent**, **child**.</span></span>

<span data-ttu-id="5fde7-392">**行**</span><span class="sxs-lookup"><span data-stu-id="5fde7-392">**rowset**</span></span>

<span data-ttu-id="5fde7-393">同じフィールドスキーマを持つデータソースからの行のセット。</span><span class="sxs-lookup"><span data-stu-id="5fde7-393">A set of rows from a data source, all having the same field schema.</span></span> <span data-ttu-id="5fde7-394">行セットは、テーブルのすべてまたは一部のフィールドを表すことができます。</span><span class="sxs-lookup"><span data-stu-id="5fde7-394">A rowset can represent all or some fields from a table.</span></span> <span data-ttu-id="5fde7-395">行セットは、クエリによって作成された仮想テーブルや、2つ以上のテーブルの結合でも使用できます。</span><span class="sxs-lookup"><span data-stu-id="5fde7-395">A rowset can also represent a virtual table, created by a query or a join of two or more tables.</span></span> <span data-ttu-id="5fde7-396">ADO では、行セットは**Recordset**オブジェクトによって表されます。</span><span class="sxs-lookup"><span data-stu-id="5fde7-396">In ADO, rowsets are represented by **Recordset** objects.</span></span>

<span data-ttu-id="5fde7-397">ページのトップへ</span><span class="sxs-lookup"><span data-stu-id="5fde7-397">Return to top</span></span>

## <a name="s"></a><span data-ttu-id="5fde7-398">S</span><span class="sxs-lookup"><span data-stu-id="5fde7-398">S</span></span>

<span data-ttu-id="5fde7-399">**スキーマ**</span><span class="sxs-lookup"><span data-stu-id="5fde7-399">**schema**</span></span>

<span data-ttu-id="5fde7-400">データベース管理システム (dbms) へのデータベースの説明。通常、dbms によって提供されるデータ定義言語を使用して生成されます。</span><span class="sxs-lookup"><span data-stu-id="5fde7-400">A description of a database to the database management system (DBMS), typically generated using the data definition language provided by the DBMS.</span></span> <span data-ttu-id="5fde7-401">スキーマは、テーブル、列、プロパティなどのデータベースの属性を定義します。</span><span class="sxs-lookup"><span data-stu-id="5fde7-401">A schema defines attributes of the database, such as tables, columns, and properties.</span></span>

<span data-ttu-id="5fde7-402">**scope**</span><span class="sxs-lookup"><span data-stu-id="5fde7-402">**scope**</span></span>

<span data-ttu-id="5fde7-403">オブジェクトまたは変数の参照範囲、またはビューまたはテーブル内のレコードの範囲。</span><span class="sxs-lookup"><span data-stu-id="5fde7-403">The range of reference for an object or variable or a range of records in a view or table.</span></span> <span data-ttu-id="5fde7-404">たとえば、ローカル変数は、定義されたプロシージャ内でのみ参照できます。</span><span class="sxs-lookup"><span data-stu-id="5fde7-404">For example, local variables can be referenced only within the procedure in which they were defined.</span></span> <span data-ttu-id="5fde7-405">パブリック変数は、アプリケーションのどこからでもアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="5fde7-405">Public variables are accessible from anywhere in the application.</span></span> <span data-ttu-id="5fde7-406">現在のデータベースなどのオブジェクトは、定義済みの検索パスにある場合にスコープ内にあります。</span><span class="sxs-lookup"><span data-stu-id="5fde7-406">Objects, such as the current database, are in scope if they are in the defined search path.</span></span> <span data-ttu-id="5fde7-407">レコード範囲は、多くのコマンドで Scope 句を使用して指定できます。</span><span class="sxs-lookup"><span data-stu-id="5fde7-407">Record ranges can be specified with a Scope clause in many commands.</span></span>

<span data-ttu-id="5fde7-408">**サービスプロバイダー**</span><span class="sxs-lookup"><span data-stu-id="5fde7-408">**service provider**</span></span>

<span data-ttu-id="5fde7-409">データを作成して使用し、ADO アプリケーションの機能を強化することによってサービスをカプセル化するソフトウェア。</span><span class="sxs-lookup"><span data-stu-id="5fde7-409">Software that encapsulates a service by producing and consuming data, augmenting features in your ADO applications.</span></span> <span data-ttu-id="5fde7-410">これは、データを直接公開しないプロバイダーで、クエリ処理などのサービスを提供します。</span><span class="sxs-lookup"><span data-stu-id="5fde7-410">It is a provider that does not directly expose data, rather it provides a service, such as query processing.</span></span> <span data-ttu-id="5fde7-411">サービスプロバイダーは、データプロバイダーによって提供されるデータを処理することができます。</span><span class="sxs-lookup"><span data-stu-id="5fde7-411">The service provider may process data provided by a data provider.</span></span> <span data-ttu-id="5fde7-412">**データプロバイダー**も参照してください。</span><span class="sxs-lookup"><span data-stu-id="5fde7-412">See also **data provider**.</span></span>

<span data-ttu-id="5fde7-413">**シェイプがある recordset**</span><span class="sxs-lookup"><span data-stu-id="5fde7-413">**shaped Recordset**</span></span>

<span data-ttu-id="5fde7-414">データだけでなく、他の**recordset**オブジェクトに基づく参照 (チャプターと呼ばれます)、またはその他の**recordset**オブジェクトに基づいて計算された値を含む列を持つ**Recordset** 。</span><span class="sxs-lookup"><span data-stu-id="5fde7-414">A **Recordset** whose columns have been specifically defined to contain not just data, but also references (called chapters) to other **Recordset** objects and/or computed values based on other **Recordset** objects.</span></span>

<span data-ttu-id="5fde7-415">**競合**</span><span class="sxs-lookup"><span data-stu-id="5fde7-415">**sibling**</span></span>

<span data-ttu-id="5fde7-416">階層構造内の同じレベルにある階層構造内の2つ以上のノード。</span><span class="sxs-lookup"><span data-stu-id="5fde7-416">Any two or more nodes in a hierarchical structure that are on the same level in the hierarchy.</span></span> <span data-ttu-id="5fde7-417">階層内のルートノードには、兄弟はありません。</span><span class="sxs-lookup"><span data-stu-id="5fde7-417">The root node in a hierarchy has no siblings.</span></span>

<span data-ttu-id="5fde7-418">**ストアド プロシージャ**</span><span class="sxs-lookup"><span data-stu-id="5fde7-418">**stored procedure**</span></span>

<span data-ttu-id="5fde7-419">名前の下に保存された、1つの単位として処理される SQL ステートメントやオプションのフロー制御ステートメントなどの、プリコンパイルされたコードのコレクション。</span><span class="sxs-lookup"><span data-stu-id="5fde7-419">A precompiled collection of code such as SQL statements and optional control-of-flow statements stored under a name and processed as a unit.</span></span> <span data-ttu-id="5fde7-420">ストアドプロシージャはデータベース内に格納されます。アプリケーションからの1回の呼び出しで実行でき、ユーザー宣言変数、条件付き実行、およびその他の強力なプログラミング機能を使用できます。</span><span class="sxs-lookup"><span data-stu-id="5fde7-420">Stored procedures are stored within a database; they can be executed with one call from an application and allow user-declared variables, conditional execution, and other powerful programming features.</span></span>

<span data-ttu-id="5fde7-421">**スタブ**</span><span class="sxs-lookup"><span data-stu-id="5fde7-421">**stub**</span></span>

<span data-ttu-id="5fde7-422">アプリケーションオブジェクトが、別のスレッドまたは別のプロセスなど、別の実行環境で実行されているクライアントからの呼び出しを受信するために必要なパラメーターマーシャリングと通信を提供するインターフェイス固有のオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="5fde7-422">An interface-specific object that provides the parameter marshaling and communication required for an application object to receive calls from a client that is running in a different execution environment, such as on a different thread or in another process.</span></span> <span data-ttu-id="5fde7-423">スタブは application オブジェクトと共に配置され、それを呼び出すクライアントに配置されている対応するプロキシと通信します。</span><span class="sxs-lookup"><span data-stu-id="5fde7-423">The stub is located with the application object and communicates with a corresponding proxy that is located with the client that calls it.</span></span> <span data-ttu-id="5fde7-424">**プロキシ**も参照。</span><span class="sxs-lookup"><span data-stu-id="5fde7-424">See also **proxy**.</span></span>

<span data-ttu-id="5fde7-425">**サブノード**</span><span class="sxs-lookup"><span data-stu-id="5fde7-425">**sub-node**</span></span>

<span data-ttu-id="5fde7-426">**子**を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5fde7-426">See **child**.</span></span>

<span data-ttu-id="5fde7-427">**同期操作**</span><span class="sxs-lookup"><span data-stu-id="5fde7-427">**synchronous operation**</span></span>

<span data-ttu-id="5fde7-428">次の操作が開始される前に完了する、コードによって開始された操作。</span><span class="sxs-lookup"><span data-stu-id="5fde7-428">An operation initiated by code that completes before the next operation may start.</span></span> <span data-ttu-id="5fde7-429">「**非同期操作**」も参照してください。</span><span class="sxs-lookup"><span data-stu-id="5fde7-429">See also **asynchronous operation**.</span></span>

<span data-ttu-id="5fde7-430">ページのトップへ</span><span class="sxs-lookup"><span data-stu-id="5fde7-430">Return to top</span></span>

## <a name="t-w"></a><span data-ttu-id="5fde7-431">T-W</span><span class="sxs-lookup"><span data-stu-id="5fde7-431">T-W</span></span>

<span data-ttu-id="5fde7-432">**ディレクトリ**</span><span class="sxs-lookup"><span data-stu-id="5fde7-432">**tree**</span></span>

<span data-ttu-id="5fde7-433">要素 (ノード) 間の階層的な関係を表す構造。</span><span class="sxs-lookup"><span data-stu-id="5fde7-433">A structure representing a hierarchical relationship between elements (nodes).</span></span> <span data-ttu-id="5fde7-434">ツリーのトップレベル (ルート) にノードが1つあります。</span><span class="sxs-lookup"><span data-stu-id="5fde7-434">There is one node at the top level of a tree (the root).</span></span> <span data-ttu-id="5fde7-435">ルートの下には、複数の子があります。</span><span class="sxs-lookup"><span data-stu-id="5fde7-435">Underneath the root, there can be multiple children.</span></span> <span data-ttu-id="5fde7-436">各子は、他の子の親になることができます。したがって、ツリーのように分岐します。</span><span class="sxs-lookup"><span data-stu-id="5fde7-436">Each child may in turn be the parent of other children, thus branching like a tree.</span></span> <span data-ttu-id="5fde7-437">ツリー構造の一般的な例としては、ドキュメントやその他のフォルダーを含むフォルダーがあります。</span><span class="sxs-lookup"><span data-stu-id="5fde7-437">A folder containing documents and other folders is a typical example of a tree structure.</span></span> <span data-ttu-id="5fde7-438">**階層**、**ノード**、**ルート**、**子**、**親**も参照。</span><span class="sxs-lookup"><span data-stu-id="5fde7-438">See also **hierarchy**, **node**, **root**, **child**, **parent**.</span></span>

<span data-ttu-id="5fde7-439">**URL (Uniform resource Locator)**</span><span class="sxs-lookup"><span data-stu-id="5fde7-439">**URL (Uniform Resource Locator)**</span></span>

<span data-ttu-id="5fde7-440">インターネットまたはイントラネット上にあるリソースの場所を指定します。</span><span class="sxs-lookup"><span data-stu-id="5fde7-440">Specifies the location of a resource residing on the Internet or an intranet.</span></span> <span data-ttu-id="5fde7-441">完全な URL は、スキーム (FTP、HTTP、mailto、ファイルなど) の後に、コロン、サーバー名、およびリソースの完全なパス (ドキュメント、グラフィック、その他のファイルなど) で構成されます。</span><span class="sxs-lookup"><span data-stu-id="5fde7-441">A complete URL consists of a scheme (such as FTP, HTTP, mailto, file, and so on), followed by a colon, a server name, and the full path of a resource (such as a document, graphic, or other file).</span></span> <span data-ttu-id="5fde7-442">url の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="5fde7-442">Some examples of URLs are:</span></span>  
  
- https://www.domain.com/default.html  
- <span data-ttu-id="5fde7-443">ftp://ftp.server.somewhere/ftp.file</span><span class="sxs-lookup"><span data-stu-id="5fde7-443">ftp://ftp.server.somewhere/ftp.file</span></span>  
  
- <span data-ttu-id="5fde7-444">ftp://ftp.server.somewhere/ftp.file</span><span class="sxs-lookup"><span data-stu-id="5fde7-444">ftp://ftp.server.somewhere/ftp.file</span></span>  
- <span data-ttu-id="5fde7-445">file://Server/Share/File.doc</span><span class="sxs-lookup"><span data-stu-id="5fde7-445">file://Server/Share/File.doc</span></span>

<span data-ttu-id="5fde7-446">**絶対 url**と**相対 url**も参照。</span><span class="sxs-lookup"><span data-stu-id="5fde7-446">See also **absolute URL** and **relative URL**.</span></span>

<span data-ttu-id="5fde7-447">**web サーバー**</span><span class="sxs-lookup"><span data-stu-id="5fde7-447">**web server**</span></span>

<span data-ttu-id="5fde7-448">イントラネットおよびインターネットユーザーに web サービスとページを提供するコンピューター。</span><span class="sxs-lookup"><span data-stu-id="5fde7-448">A computer that provides web services and pages to intranet and Internet users.</span></span>



