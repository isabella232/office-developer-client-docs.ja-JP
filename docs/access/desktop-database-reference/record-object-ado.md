---
title: Record オブジェクト (ADO)
TOCTitle: Record object (ADO)
ms:assetid: 817aaf13-78d4-1134-aa94-997e92077c22
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249557(v=office.15)
ms:contentKeyID: 48545952
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 96ddc7fc1a93543f0eea2b42a3d423ec25a00636
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721508"
---
# <a name="record-object-ado"></a><span data-ttu-id="adae4-102">Record オブジェクト (ADO)</span><span class="sxs-lookup"><span data-stu-id="adae4-102">Record object (ADO)</span></span>


<span data-ttu-id="adae4-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="adae4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="adae4-104">[Recordset](recordset-object-ado.md) オブジェクトやデータ プロバイダーの行、または、半構造化データ プロバイダーから返されるファイルやディレクトリなどのオブジェクトを表します。</span><span class="sxs-lookup"><span data-stu-id="adae4-104">Represents a row from a [Recordset](recordset-object-ado.md) or the data provider, or an object returned by a semi-structured data provider, such as a file or directory.</span></span>

## <a name="remarks"></a><span data-ttu-id="adae4-105">備考</span><span class="sxs-lookup"><span data-stu-id="adae4-105">Remarks</span></span>

<span data-ttu-id="adae4-p101">**Record** オブジェクトはデータの 1 つの行を表し、1 行から成る **Recordset** に概念が似ています。プロバイダーの機能によっては、1 行から成る **Recordset** の代わりに、 **Record** オブジェクトが直接プロバイダーから返される場合があります (たとえば、1 行のみ選択する SQL クエリを実行したときなど)。また、 **Record** オブジェクトは、 **Recordset** オブジェクトから直接取得されることもあります。または、Microsoft Exchange OLE DB Provider などの半構造化データ プロバイダーから直接 **Record** オブジェクトが返される場合もあります。</span><span class="sxs-lookup"><span data-stu-id="adae4-p101">A **Record** object represents one row of data, and has some conceptual similarities with a one-row **Recordset**. Depending upon the capabilities of your provider, **Record** objects may be returned directly from your provider instead of a one-row **Recordset**, for example when an SQL query that selects only one row is executed. Or, a **Record** object can be obtained directly from a **Recordset** object. Or, a **Record** can be returned directly from a provider to semi-structured data, such as the Microsoft Exchange OLE DB provider.</span></span>

<span data-ttu-id="adae4-p102">**Record** オブジェクトに関連付けられたフィールドは、 [Record](fields-collection-ado.md) オブジェクトの **Fields** コレクションを使用して表示できます。ADO では、 **Recordset** 、 **SafeArray** 、および **Record** オブジェクトの **Fields** コレクションのスカラー値などの、オブジェクト値の列を利用できます。</span><span class="sxs-lookup"><span data-stu-id="adae4-p102">You can view the fields associated with the **Record** object by way of the [Fields](fields-collection-ado.md) collection on the **Record** object. ADO allows object-valued columns including **Recordset**, **SafeArray**, and scalar values in the **Fields** collection of **Record** objects.</span></span>

<span data-ttu-id="adae4-112">**Record** オブジェクトが **Recordset** の行を表す場合、 **Source** プロパティを使用して元の [Recordset](source-property-ado-record.md) に戻すことができます。</span><span class="sxs-lookup"><span data-stu-id="adae4-112">If the **Record** object represents a row in a **Recordset**, then it is possible to return to that original **Recordset** with the [Source](source-property-ado-record.md) property.</span></span>

<span data-ttu-id="adae4-p103">また、**Microsoft OLE DB Provider for Internet Publishing** などの半構造化データ プロバイダーは、 [Record](microsoft-ole-db-provider-for-internet-publishing.md) オブジェクトを使用してツリー構造の名前空間をモデル化することができます。ツリー内のノードは、関連付けられた列を持つ **Record** オブジェクトを表します。列は、そのノードの属性とその他の関連情報を表します。 **Record** オブジェクトは、ツリー構造のリーフ ノードと非リーフ ノードの両方を表すことができます。非リーフ ノードは、そのコンテンツとしてほかのノードを持っていますが、リーフ ノードはそのようなコンテンツを持ちません。リーフ ノードは、通常、データのバイナリ ストリームを格納していますが、非リーフ ノードも、関連付けられた既定のバイナリ ストリームを格納している場合があります。 **Record** オブジェクトのプロパティで、ノードの種類を識別することができます。</span><span class="sxs-lookup"><span data-stu-id="adae4-p103">The **Record** object can also be used by semi-structured data providers such as the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md), to model tree-structured namespaces. Each node in the tree is a **Record** object with associated columns. The columns can represent the attributes of that node and other relevant information. The **Record** object can represent both a leaf node and a non-leaf node in the tree structure. Non-leaf nodes have other nodes as their contents while leaf nodes do not have such contents. Leaf nodes typically contain binary streams of data while non-leaf nodes may also have a default binary stream associated with them. Properties on the **Record** object identify the type of node.</span></span>

<span data-ttu-id="adae4-p104">**Record** オブジェクトは、階層構造のデータ間を移動する手段としても使用できます。 **Record** オブジェクトを作成して、それを大規模なツリー構造の特定のサブツリーのルートにすると、新しい **Record** オブジェクトを子ノードとして開くことができます。</span><span class="sxs-lookup"><span data-stu-id="adae4-p104">The **Record** object also represents an alternative way for navigating hierarchically organized data. A **Record** object may be created to represent the root of a specific sub-tree in a large tree structure and new **Record** objects may be opened to represent child nodes.</span></span>

<span data-ttu-id="adae4-122">リソース (たとえば、ファイルまたはディレクトリ) は、絶対 URL で一意に識別できます。</span><span class="sxs-lookup"><span data-stu-id="adae4-122">A resource (for example, a file or directory) can be uniquely identified by an absolute URL.</span></span> <span data-ttu-id="adae4-123">暗黙的に[接続](connection-object-ado.md)オブジェクトが作成され、絶対 URL を持つ**レコード**を開くと**Record**オブジェクトに設定します。</span><span class="sxs-lookup"><span data-stu-id="adae4-123">A [Connection](connection-object-ado.md) object is implicitly created and set to the **Record** object when the **Record** is opened with an absolute URL.</span></span> <span data-ttu-id="adae4-124">**接続**オブジェクトは、 [ActiveConnection](activeconnection-property-ado.md)プロパティを使用して**Record**オブジェクトに明示的に設定することがあります。</span><span class="sxs-lookup"><span data-stu-id="adae4-124">A **Connection** object may explicitly be set to the **Record** object via the [ActiveConnection](activeconnection-property-ado.md) property.</span></span> <span data-ttu-id="adae4-125">ファイルとディレクトリの**接続**オブジェクトを通じてアクセス可能な\*コンテキスト\***レコード**操作が発生する可能性を定義します。</span><span class="sxs-lookup"><span data-stu-id="adae4-125">The files and directories accessible via the **Connection** object define the *context* in which **Record** operations may occur.</span></span>

<span data-ttu-id="adae4-126">データを変更または移動する **Record** オブジェクトのメソッドでは相対 URL も利用でき、相対 URL では、絶対 URL または **Connection** オブジェクト コンテキストを起点としてリソースを検索します。</span><span class="sxs-lookup"><span data-stu-id="adae4-126">Data modification and navigation methods on the **Record** object also accept a relative URL, which locates a resource using an absolute URL or the **Connection** object context as a starting point.</span></span>

> [!NOTE]
> <span data-ttu-id="adae4-127">[!メモ] http スキームを使用している URL は、[Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) を自動的に呼び出します。</span><span class="sxs-lookup"><span data-stu-id="adae4-127">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="adae4-128">詳細については、[絶対と相対 Url](absolute-and-relative-urls.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="adae4-128">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>



<span data-ttu-id="adae4-p107">**Connection** オブジェクトは各 **Record** オブジェクトに関連付けられています。したがって、 **Connection** オブジェクトのトランザクション メソッドを呼び出せば、 **Record** オブジェクトの操作をトランザクションの一部にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="adae4-p107">A **Connection** object is associated with each **Record** object. Therefore, **Record** object operations can be part of a transaction by invoking **Connection** object transaction methods.</span></span>

<span data-ttu-id="adae4-131">**Record** オブジェクトは ADO イベントをサポートしていないので、通知には応答しません。</span><span class="sxs-lookup"><span data-stu-id="adae4-131">The **Record** object does not support ADO events, and therefore will not respond to notifications.</span></span>

<span data-ttu-id="adae4-132">**Record** オブジェクトのメソッドとプロパティを使用すると、次の操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="adae4-132">With the methods and properties of a **Record** object, you can do the following:</span></span>

  - <span data-ttu-id="adae4-133">**ActiveConnection** プロパティを使用して、関連する [Connection](activeconnection-property-ado.md) オブジェクトを設定または取得できます。</span><span class="sxs-lookup"><span data-stu-id="adae4-133">Set or return the associated **Connection** object with the [ActiveConnection](activeconnection-property-ado.md) property.</span></span>

  - <span data-ttu-id="adae4-134">[Mode](mode-property-ado.md) プロパティを使用して、アクセス権限を示すことができます。</span><span class="sxs-lookup"><span data-stu-id="adae4-134">Indicate access permissions with the [Mode](mode-property-ado.md) property.</span></span>

  - <span data-ttu-id="adae4-135">**ParentURL** プロパティを使用して、 [Record](parenturl-property-ado.md) が表すリソースを格納しているディレクトリの URL を取得できます。</span><span class="sxs-lookup"><span data-stu-id="adae4-135">Return the URL of the directory, if any, that contains the resource represented by the **Record** with the [ParentURL](parenturl-property-ado.md) property.</span></span>

  - <span data-ttu-id="adae4-136">**Source** プロパティを使用して、 **Record** の派生元となる絶対 URL、相対 URL、または [Recordset](source-property-ado-record.md) を示すことができます。</span><span class="sxs-lookup"><span data-stu-id="adae4-136">Indicate the absolute URL, relative URL, or **Recordset** from which the **Record** is derived with the [Source](source-property-ado-record.md) property.</span></span>

  - <span data-ttu-id="adae4-137">**State** プロパティを使用して、 [Record](state-property-ado.md) の現在のステータスを示すことができます。</span><span class="sxs-lookup"><span data-stu-id="adae4-137">Indicate the current status of the **Record** with the [State](state-property-ado.md) property.</span></span>

  - <span data-ttu-id="adae4-138">**レコード**の種類を示す、*単純な\*\*コレクション*、または*構造化されたドキュメント*: [RecordType](recordtype-property-ado.md)プロパティを使用して。</span><span class="sxs-lookup"><span data-stu-id="adae4-138">Indicate the type of **Record** — *simple*, *collection*, or *structured document* — with the [RecordType](recordtype-property-ado.md) property.</span></span>

  - <span data-ttu-id="adae4-139">[Cancel](cancel-method-ado.md) メソッドを使用して、非同期操作の実行を停止できます。</span><span class="sxs-lookup"><span data-stu-id="adae4-139">Halt execution of an asynchronous operation with the [Cancel](cancel-method-ado.md) method.</span></span>

  - <span data-ttu-id="adae4-140">**Close** メソッドを使用して、データ ソースと [Record](close-method-ado.md) との関連付けを解除できます。</span><span class="sxs-lookup"><span data-stu-id="adae4-140">Disassociate the **Record** from a data source with the [Close](close-method-ado.md) method.</span></span>

  - <span data-ttu-id="adae4-141">**CopyRecord** メソッドを使用して、 [Record](copyrecord-method-ado.md) が表すファイルまたはディレクトリを別の場所にコピーできます。</span><span class="sxs-lookup"><span data-stu-id="adae4-141">Copy the file or directory represented by a **Record** to another location with the [CopyRecord](copyrecord-method-ado.md) method.</span></span>

  - <span data-ttu-id="adae4-142">**DeleteRecord** メソッドを使用して、 [Record](deleterecord-method-ado.md) が表すファイル、ディレクトリ、またはサブディレクトリを削除できます。</span><span class="sxs-lookup"><span data-stu-id="adae4-142">Delete the file, or directory and subdirectories, represented by a **Record** with the [DeleteRecord](deleterecord-method-ado.md) method.</span></span>

  - <span data-ttu-id="adae4-143">**GetChildren** メソッドを使用して、 **Record** が表すエンティティのサブディレクトリおよびファイルを表す行を格納している [Recordset](getchildren-method-ado.md) を開くことができます。</span><span class="sxs-lookup"><span data-stu-id="adae4-143">Open a **Recordset** containing rows that represent the subdirectories and files of the entity represented by the **Record** with the [GetChildren](getchildren-method-ado.md) method.</span></span>

  - <span data-ttu-id="adae4-144">**MoveRecord** メソッドを使用して、 [Record](moverecord-method-ado.md) が表すファイル、ディレクトリ、またはサブディレクトリを別の場所に移動 (名前変更) できます。</span><span class="sxs-lookup"><span data-stu-id="adae4-144">Move (rename) the file, or directory and subdirectories, represented by a **Record** to another location with the [MoveRecord](moverecord-method-ado.md) method.</span></span>

  - <span data-ttu-id="adae4-145">**Open** メソッドを使用して、 [Record](open-method-ado-record.md) を既存のデータ ソースに関連付けたり、新規ファイルまたは新規ディレクトリを作成したりできます。</span><span class="sxs-lookup"><span data-stu-id="adae4-145">Associate the **Record** with an existing data source, or create a new file or directory with the [Open](open-method-ado-record.md) method.</span></span>

