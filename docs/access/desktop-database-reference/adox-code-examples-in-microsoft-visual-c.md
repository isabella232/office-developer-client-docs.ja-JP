---
title: Microsoft Visual C++ での ADOX コードの例
TOCTitle: ADOX Code Examples in Microsoft Visual C++
ms:assetid: cf95d93d-c14d-5dcd-4b3a-f872d91a322f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250033(v=office.15)
ms:contentKeyID: 48547814
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dd2ebb1a6baa30912594db8e2e9ff9ebc9e374c5
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606011"
---
# <a name="adox-code-examples-in-microsoft-visual-c"></a><span data-ttu-id="a18f7-102">Microsoft Visual C++ での ADOX コードの例</span><span class="sxs-lookup"><span data-stu-id="a18f7-102">ADOX Code Examples in Microsoft Visual C++</span></span>


<span data-ttu-id="a18f7-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="a18f7-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="a18f7-p101">これらのトピックでは、ADOX の使用方法を理解するのに役立つサンプル コードを提供しています。すべてのコード例は、Microsoft Visual C++ を使用して記述されています。</span><span class="sxs-lookup"><span data-stu-id="a18f7-p101">These topics provide sample code to help you understand how to use ADOX. All code examples are written using Microsoft Visual C++.</span></span>


> [!NOTE]
> <span data-ttu-id="a18f7-p102">[!メモ] コード例全体を最初から最後までコピーして、コード エディターに貼り付けてください。この例は、一部分だけ使用したり、段落書式が失われると、正常に動作しない場合があります。</span><span class="sxs-lookup"><span data-stu-id="a18f7-p102">Paste the entire code example, from beginning to end, into your code editor. The example may not run correctly if you use partial examples or if paragraph formatting is lost.</span></span>



<span data-ttu-id="a18f7-108">**メソッド**</span><span class="sxs-lookup"><span data-stu-id="a18f7-108">**Methods**</span></span>

<span data-ttu-id="a18f7-109"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="a18f7-109"><<<<<<< HEAD</span></span>
  - [<span data-ttu-id="a18f7-110">列とテーブルの Append メソッドと Name プロパティの使用例 (VC++)</span><span class="sxs-lookup"><span data-stu-id="a18f7-110">Columns and Tables Append Methods, Name Property Example (VC++)</span></span>](columns-and-tables-append-methods-name-property-example-vc.md)

  - <span data-ttu-id="a18f7-111">[Close メソッドの接続、テーブルの種類プロパティの使用例 (vc++)](connection-close-method-table-type-property-example-vc.md)
=======</span><span class="sxs-lookup"><span data-stu-id="a18f7-111">[Connection Close Method, Table Type Property Example (VC++)](connection-close-method-table-type-property-example-vc.md)
=======</span></span>
  - [<span data-ttu-id="a18f7-112">列とテーブルの追加方法、名前プロパティの使用例 (vc++)</span><span class="sxs-lookup"><span data-stu-id="a18f7-112">Columns and Tables Append Methods, Name property example (VC++)</span></span>](columns-and-tables-append-methods-name-property-example-vc.md)

  - [<span data-ttu-id="a18f7-113">接続の Close メソッドをテーブル型のプロパティの使用例 (vc++)</span><span class="sxs-lookup"><span data-stu-id="a18f7-113">Connection Close Method, Table Type property example (VC++)</span></span>](connection-close-method-table-type-property-example-vc.md)
>>>>>>> <span data-ttu-id="a18f7-114">master</span><span class="sxs-lookup"><span data-stu-id="a18f7-114">master</span></span>

  - [<span data-ttu-id="a18f7-115">Create メソッドの使用例 (VC++)</span><span class="sxs-lookup"><span data-stu-id="a18f7-115">Create Method Example (VC++)</span></span>](create-method-example-vc.md)

  - [<span data-ttu-id="a18f7-116">GetObjectOwner メソッドと SetObjectOwner メソッドの使用例 (VC++)</span><span class="sxs-lookup"><span data-stu-id="a18f7-116">GetObjectOwner and SetObjectOwner Methods Example (VC++)</span></span>](getobjectowner-and-setobjectowner-methods-example-vc.md)

  - [<span data-ttu-id="a18f7-117">GetPermissions メソッドと SetPermissions メソッドの使用例 (VC++)</span><span class="sxs-lookup"><span data-stu-id="a18f7-117">GetPermissions and SetPermissions Methods Example (VC++)</span></span>](getpermissions-and-setpermissions-methods-example-vc.md)

  - [<span data-ttu-id="a18f7-118">Groups と Users の Append メソッドおよび ChangePassword メソッドの使用例 (VC++)</span><span class="sxs-lookup"><span data-stu-id="a18f7-118">Groups and Users Append, ChangePassword Methods Example (VC++)</span></span>](groups-and-users-append-changepassword-methods-example-vc.md)

  - [<span data-ttu-id="a18f7-119">Indexes の Append メソッドの使用例 (VC++)</span><span class="sxs-lookup"><span data-stu-id="a18f7-119">Indexes Append Method Example (VC++)</span></span>](indexes-append-method-example-vc.md)

<span data-ttu-id="a18f7-120"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="a18f7-120"><<<<<<< HEAD</span></span>
  - [<span data-ttu-id="a18f7-121">Keys の Append メソッド、および Key の Type、RelatedColumn、RelatedTable、UpdateRule プロパティの使用例 (VC++)</span><span class="sxs-lookup"><span data-stu-id="a18f7-121">Keys Append Method, Key Type, RelatedColumn, RelatedTable, and UpdateRule Properties Example (VC++)</span></span>](keys-append-method-key-type-relatedcolumn-relatedtable-and-updaterule-properties-example-vc.md)

<span data-ttu-id="a18f7-122">**プロパティ**</span><span class="sxs-lookup"><span data-stu-id="a18f7-122">**Properties**</span></span>

  - [<span data-ttu-id="a18f7-123">Attributes プロパティの使用例 (VC++)</span><span class="sxs-lookup"><span data-stu-id="a18f7-123">Attributes Property Example (VC++)</span></span>](attributes-property-example-vc.md)

  - [<span data-ttu-id="a18f7-124">Catalog の ActiveConnection プロパティの使用例 (VC++)</span><span class="sxs-lookup"><span data-stu-id="a18f7-124">Catalog ActiveConnection Property Example (VC++)</span></span>](catalog-activeconnection-property-example-vc.md)

  - [<span data-ttu-id="a18f7-125">Clustered プロパティの使用例 (VC++)</span><span class="sxs-lookup"><span data-stu-id="a18f7-125">Clustered Property Example (VC++)</span></span>](clustered-property-example-vc.md)

  - [<span data-ttu-id="a18f7-126">Command プロパティと CommandText プロパティの使用例 (VC++)</span><span class="sxs-lookup"><span data-stu-id="a18f7-126">Command and CommandText Properties Example (VC++)</span></span>](command-and-commandtext-properties-example-vc.md)

  - [<span data-ttu-id="a18f7-127">Parameters コレクションの Command プロパティの使用例 (VC++)</span><span class="sxs-lookup"><span data-stu-id="a18f7-127">Command Property, Parameters Collection Example (VC++)</span></span>](parameters-collection-command-property-example-vc.md)

  - [<span data-ttu-id="a18f7-128">DateCreated プロパティと DateModified プロパティの使用例 (VC++)</span><span class="sxs-lookup"><span data-stu-id="a18f7-128">DateCreated and DateModified Properties Example (VC++)</span></span>](datecreated-and-datemodified-properties-example-vc.md)

  - [<span data-ttu-id="a18f7-129">DefinedSize プロパティの使用例 (VC++)</span><span class="sxs-lookup"><span data-stu-id="a18f7-129">DefinedSize Property Example (VC++)</span></span>](definedsize-property-example-vc.md)

  - [<span data-ttu-id="a18f7-130">DeleteRule プロパティの使用例 (VC++)</span><span class="sxs-lookup"><span data-stu-id="a18f7-130">DeleteRule Property Example (VC++)</span></span>](deleterule-property-example-vc.md)

  - <span data-ttu-id="a18f7-131">[IndexNulls プロパティの使用例 (vc++)](indexnulls-property-example-vc.md)
=======</span><span class="sxs-lookup"><span data-stu-id="a18f7-131">[IndexNulls Property Example (VC++)](indexnulls-property-example-vc.md)
=======</span></span>
  - [<span data-ttu-id="a18f7-132">キーの追加方法、キーの種類、RelatedColumn、RelatedTable、および UpdateRule プロパティの使用例 (vc++)</span><span class="sxs-lookup"><span data-stu-id="a18f7-132">Keys Append Method, Key Type, RelatedColumn, RelatedTable, and UpdateRule properties example (VC++)</span></span>](keys-append-method-key-type-relatedcolumn-relatedtable-and-updaterule-properties-example-vc.md)

<span data-ttu-id="a18f7-133">**新しいプロパティ**</span><span class="sxs-lookup"><span data-stu-id="a18f7-133">**Properties**</span></span>

  - [<span data-ttu-id="a18f7-134">属性プロパティの使用例 (vc++)</span><span class="sxs-lookup"><span data-stu-id="a18f7-134">Attributes property example (VC++)</span></span>](attributes-property-example-vc.md)

  - [<span data-ttu-id="a18f7-135">カタログの ActiveConnection プロパティの使用例 (vc++)</span><span class="sxs-lookup"><span data-stu-id="a18f7-135">Catalog ActiveConnection property example (VC++)</span></span>](catalog-activeconnection-property-example-vc.md)

  - [<span data-ttu-id="a18f7-136">クラスター化プロパティの使用例 (vc++)</span><span class="sxs-lookup"><span data-stu-id="a18f7-136">Clustered property example (VC++)</span></span>](clustered-property-example-vc.md)

  - [<span data-ttu-id="a18f7-137">コマンドと CommandText プロパティの使用例 (vc++)</span><span class="sxs-lookup"><span data-stu-id="a18f7-137">Command and CommandText properties example (VC++)</span></span>](command-and-commandtext-properties-example-vc.md)

  - [<span data-ttu-id="a18f7-138">Parameters コレクションの Command プロパティの使用例 (VC++)</span><span class="sxs-lookup"><span data-stu-id="a18f7-138">Command Property, Parameters Collection Example (VC++)</span></span>](parameters-collection-command-property-example-vc.md)

  - [<span data-ttu-id="a18f7-139">作成日時と最終更新日時プロパティの使用例 (vc++)</span><span class="sxs-lookup"><span data-stu-id="a18f7-139">DateCreated and DateModified properties example (VC++)</span></span>](datecreated-and-datemodified-properties-example-vc.md)

  - [<span data-ttu-id="a18f7-140">DefinedSize プロパティの使用例 (vc++)</span><span class="sxs-lookup"><span data-stu-id="a18f7-140">DefinedSize property example (VC++)</span></span>](definedsize-property-example-vc.md)

  - [<span data-ttu-id="a18f7-141">DeleteRule プロパティの使用例 (vc++)</span><span class="sxs-lookup"><span data-stu-id="a18f7-141">DeleteRule property example (VC++)</span></span>](deleterule-property-example-vc.md)

  - [<span data-ttu-id="a18f7-142">IndexNulls プロパティの使用例 (vc++)</span><span class="sxs-lookup"><span data-stu-id="a18f7-142">IndexNulls property example (VC++)</span></span>](indexnulls-property-example-vc.md)
>>>>>>> <span data-ttu-id="a18f7-143">master</span><span class="sxs-lookup"><span data-stu-id="a18f7-143">master</span></span>

  - [<span data-ttu-id="a18f7-144">Keys の Append メソッド、および Key の Type、RelatedColumn、RelatedTable、UpdateRule プロパティの使用例 (VC++)</span><span class="sxs-lookup"><span data-stu-id="a18f7-144">Key Type, RelatedColumn, RelatedTable, UpdateRule Properties, Keys Append Method Example (VC++)</span></span>](keys-append-method-key-type-relatedcolumn-relatedtable-and-updaterule-properties-example-vc.md)

  - [<span data-ttu-id="a18f7-145">列とテーブルの Append メソッドと Name プロパティの使用例 (VC++)</span><span class="sxs-lookup"><span data-stu-id="a18f7-145">Name Property, Columns and Tables Append Methods Example (VC++)</span></span>](columns-and-tables-append-methods-name-property-example-vc.md)

<span data-ttu-id="a18f7-146"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="a18f7-146"><<<<<<< HEAD</span></span>
  - [<span data-ttu-id="a18f7-147">NumericScale プロパティと Precision プロパティの使用例 (VC++)</span><span class="sxs-lookup"><span data-stu-id="a18f7-147">NumericScale and Precision Properties Example (VC++)</span></span>](numericscale-and-precision-properties-example-vc.md)

  - [<span data-ttu-id="a18f7-148">ParentCatalog プロパティの使用例 (VC++)</span><span class="sxs-lookup"><span data-stu-id="a18f7-148">ParentCatalog Property Example (VC++)</span></span>](parentcatalog-property-example-vc.md)

  - <span data-ttu-id="a18f7-149">[主キーおよび一意なプロパティの使用例 (vc++)](primarykey-and-unique-properties-example-vc.md)
=======</span><span class="sxs-lookup"><span data-stu-id="a18f7-149">[PrimaryKey and Unique Properties Example (VC++)](primarykey-and-unique-properties-example-vc.md)
=======</span></span>
  - [<span data-ttu-id="a18f7-150">NumericScale と Precision プロパティの使用例 (vc++)</span><span class="sxs-lookup"><span data-stu-id="a18f7-150">NumericScale and Precision properties example (VC++)</span></span>](numericscale-and-precision-properties-example-vc.md)

  - [<span data-ttu-id="a18f7-151">ParentCatalog プロパティの使用例 (vc++)</span><span class="sxs-lookup"><span data-stu-id="a18f7-151">ParentCatalog property example (VC++)</span></span>](parentcatalog-property-example-vc.md)

  - [<span data-ttu-id="a18f7-152">主キーや Unique プロパティの使用例 (vc++)</span><span class="sxs-lookup"><span data-stu-id="a18f7-152">PrimaryKey and Unique properties example (VC++)</span></span>](primarykey-and-unique-properties-example-vc.md)
>>>>>>> <span data-ttu-id="a18f7-153">master</span><span class="sxs-lookup"><span data-stu-id="a18f7-153">master</span></span>

  - [<span data-ttu-id="a18f7-154">Connection の Close メソッドおよび Table の Type プロパティの使用例 (VC++)</span><span class="sxs-lookup"><span data-stu-id="a18f7-154">Table Type Property, Connection Close Method Example (VC++)</span></span>](connection-close-method-table-type-property-example-vc.md)

<span data-ttu-id="a18f7-155">**コレクション**</span><span class="sxs-lookup"><span data-stu-id="a18f7-155">**Collections**</span></span>

<span data-ttu-id="a18f7-156"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="a18f7-156"><<<<<<< HEAD</span></span>
  - <span data-ttu-id="a18f7-157">[Parameters コレクションのコマンド プロパティの使用例 (vc++)](parameters-collection-command-property-example-vc.md)
=======</span><span class="sxs-lookup"><span data-stu-id="a18f7-157">[Parameters Collection, Command Property Example (VC++)](parameters-collection-command-property-example-vc.md)
=======</span></span>
  - [<span data-ttu-id="a18f7-158">Parameters コレクションのコマンド プロパティの使用例 (vc++)</span><span class="sxs-lookup"><span data-stu-id="a18f7-158">Parameters Collection, Command property example (VC++)</span></span>](parameters-collection-command-property-example-vc.md)
>>>>>>> <span data-ttu-id="a18f7-159">master</span><span class="sxs-lookup"><span data-stu-id="a18f7-159">master</span></span>

