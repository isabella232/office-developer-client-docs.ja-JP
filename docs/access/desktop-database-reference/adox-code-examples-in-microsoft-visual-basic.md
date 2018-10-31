---
title: Microsoft Visual Basic での ADOX コードの例
TOCTitle: ADOX Code Examples in Microsoft Visual Basic
ms:assetid: 685ae6cf-4b56-f7af-3210-ab0142a30855
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249407(v=office.15)
ms:contentKeyID: 48545383
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f810da6a4f979dac8d974fe50a6f615022d1cdaa
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862969"
---
# <a name="adox-code-examples-in-microsoft-visual-basic"></a><span data-ttu-id="9353f-102">Microsoft Visual Basic での ADOX コードの例</span><span class="sxs-lookup"><span data-stu-id="9353f-102">ADOX Code Examples in Microsoft Visual Basic</span></span>


<span data-ttu-id="9353f-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="9353f-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="9353f-p101">これらのトピックでは、ADOX の使用方法を理解するのに役立つサンプル コードを提供しています。すべてのコード例は、Microsoft Visual Basic で記述されています。</span><span class="sxs-lookup"><span data-stu-id="9353f-p101">These topics provide sample code to help you understand how to use ADOX. All code examples are written using Microsoft Visual Basic.</span></span>


> [!NOTE]
> <span data-ttu-id="9353f-p102">[!メモ] Sub から End Sub までのコード例全体をコピーして、コード エディターに貼り付けてください。この例は、一部分だけ使用したり、段落書式が失われると、正常に動作しない場合があります。</span><span class="sxs-lookup"><span data-stu-id="9353f-p102">Paste the entire code example, from Sub to End Sub, into your code editor. The example may not run correctly if you use partial examples or if paragraph formatting is lost.</span></span>



<span data-ttu-id="9353f-108">**メソッド**</span><span class="sxs-lookup"><span data-stu-id="9353f-108">**Methods**</span></span>

<span data-ttu-id="9353f-109"><<<<<<< 見出し</span><span class="sxs-lookup"><span data-stu-id="9353f-109"><<<<<<< HEAD</span></span>
  - [<span data-ttu-id="9353f-110">列とテーブルの Append メソッドと Name プロパティの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="9353f-110">Columns and Tables Append Methods, Name Property Example (VB)</span></span>](columns-and-tables-append-methods-name-property-example-vb.md)

  - <span data-ttu-id="9353f-111">[Close メソッドの接続、テーブルの種類プロパティの使用例 (VB)](connection-close-method-table-type-property-example-vb.md)
=======</span><span class="sxs-lookup"><span data-stu-id="9353f-111">[Connection Close Method, Table Type Property Example (VB)](connection-close-method-table-type-property-example-vb.md)
=======</span></span>
  - [<span data-ttu-id="9353f-112">列とテーブルの追加方法、名前プロパティの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="9353f-112">Columns and Tables Append Methods, Name property example (VB)</span></span>](columns-and-tables-append-methods-name-property-example-vb.md)

  - [<span data-ttu-id="9353f-113">接続の Close メソッドをテーブル型のプロパティの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="9353f-113">Connection Close Method, Table Type property example (VB)</span></span>](connection-close-method-table-type-property-example-vb.md)
>>>>>>> <span data-ttu-id="9353f-114">master</span><span class="sxs-lookup"><span data-stu-id="9353f-114">master</span></span>

  - [<span data-ttu-id="9353f-115">Create メソッドの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="9353f-115">Create method example (VB)</span></span>](create-method-example-vb.md)

  - [<span data-ttu-id="9353f-116">GetObjectOwner メソッドと SetObjectOwner メソッドの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="9353f-116">GetObjectOwner and SetObjectOwner methods example (VB)</span></span>](getobjectowner-and-setobjectowner-methods-example-vb.md)

  - [<span data-ttu-id="9353f-117">GetPermissions メソッドと SetPermissions メソッドの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="9353f-117">GetPermissions and SetPermissions methods example (VB)</span></span>](getpermissions-and-setpermissions-methods-example-vb.md)

  - [<span data-ttu-id="9353f-118">Groups と Users の Append メソッドおよび ChangePassword メソッドの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="9353f-118">Groups and Users Append, ChangePassword methods example (VB)</span></span>](groups-and-users-append-changepassword-methods-example-vb.md)

  - [<span data-ttu-id="9353f-119">Indexes の Append メソッドの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="9353f-119">Indexes Append method example (VB)</span></span>](indexes-append-method-example-vb.md)

<span data-ttu-id="9353f-120"><<<<<<< 見出し</span><span class="sxs-lookup"><span data-stu-id="9353f-120"><<<<<<< HEAD</span></span>
  - <span data-ttu-id="9353f-121">[キーが追加され、メソッド、キーの種類、RelatedColumn、RelatedTable、UpdateRule プロパティの使用例 (VB)](keys-append-method-key-type-relatedcolumn-relatedtable-and-updaterule-properties-example-vb.md)
=======</span><span class="sxs-lookup"><span data-stu-id="9353f-121">[Keys Append Method, Key Type, RelatedColumn, RelatedTable, and UpdateRule Properties Example (VB)](keys-append-method-key-type-relatedcolumn-relatedtable-and-updaterule-properties-example-vb.md)
=======</span></span>
  - [<span data-ttu-id="9353f-122">キーの追加方法、キーの種類、RelatedColumn、RelatedTable、および UpdateRule プロパティの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="9353f-122">Keys Append Method, Key Type, RelatedColumn, RelatedTable, and UpdateRule properties example (VB)</span></span>](keys-append-method-key-type-relatedcolumn-relatedtable-and-updaterule-properties-example-vb.md)
>>>>>>> <span data-ttu-id="9353f-123">master</span><span class="sxs-lookup"><span data-stu-id="9353f-123">master</span></span>

  - [<span data-ttu-id="9353f-124">Procedures の Append メソッドの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="9353f-124">Procedures Append method example (VB)</span></span>](procedures-append-method-example-vb.md)

  - [<span data-ttu-id="9353f-125">Procedures の Delete メソッドの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="9353f-125">Procedures Delete method example (VB)</span></span>](procedures-delete-method-example-vb.md)

  - [<span data-ttu-id="9353f-126">Procedures の Refresh メソッドの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="9353f-126">Procedures Refresh method example (VB)</span></span>](procedures-refresh-method-example-vb.md)

  - [<span data-ttu-id="9353f-127">Views の Append メソッドの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="9353f-127">Views Append method example (VB)</span></span>](views-append-method-example-vb.md)

  - [<span data-ttu-id="9353f-128">Views の Delete メソッドの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="9353f-128">Views Delete method example (VB)</span></span>](views-delete-method-example-vb.md)

  - [<span data-ttu-id="9353f-129">ビュー更新メソッドの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="9353f-129">Views Refresh method example (VB)</span></span>](views-refresh-method-example-vb.md)

<span data-ttu-id="9353f-130">**新しいプロパティ**</span><span class="sxs-lookup"><span data-stu-id="9353f-130">**Properties**</span></span>

<span data-ttu-id="9353f-131"><<<<<<< 見出し</span><span class="sxs-lookup"><span data-stu-id="9353f-131"><<<<<<< HEAD</span></span>
  - [<span data-ttu-id="9353f-132">Attributes プロパティの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="9353f-132">Attributes Property Example (VB)</span></span>](attributes-property-example-vb.md)

  - [<span data-ttu-id="9353f-133">Catalog の ActiveConnection プロパティの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="9353f-133">Catalog ActiveConnection Property Example (VB)</span></span>](catalog-activeconnection-property-example-vb.md)

  - [<span data-ttu-id="9353f-134">Clustered プロパティの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="9353f-134">Clustered Property Example (VB)</span></span>](clustered-property-example-vb.md)

  - <span data-ttu-id="9353f-135">[コマンドと CommandText プロパティの使用例 (VB)](command-and-commandtext-properties-example-vb.md)
=======</span><span class="sxs-lookup"><span data-stu-id="9353f-135">[Command and CommandText Properties Example (VB)](command-and-commandtext-properties-example-vb.md)
=======</span></span>
  - [<span data-ttu-id="9353f-136">Attributes プロパティの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="9353f-136">Attributes property example (VB)</span></span>](attributes-property-example-vb.md)

  - [<span data-ttu-id="9353f-137">Catalog の ActiveConnection プロパティの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="9353f-137">Catalog ActiveConnection property example (VB)</span></span>](catalog-activeconnection-property-example-vb.md)

  - [<span data-ttu-id="9353f-138">Clustered プロパティの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="9353f-138">Clustered property example (VB)</span></span>](clustered-property-example-vb.md)

  - [<span data-ttu-id="9353f-139">Command プロパティと CommandText プロパティの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="9353f-139">Command and CommandText properties example (VB)</span></span>](command-and-commandtext-properties-example-vb.md)
>>>>>>> <span data-ttu-id="9353f-140">master</span><span class="sxs-lookup"><span data-stu-id="9353f-140">master</span></span>

  - [<span data-ttu-id="9353f-141">コマンドのプロパティ、パラメーター コレクションの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="9353f-141">Command Property, Parameters Collection example (VB)</span></span>](parameters-collection-command-property-example-vb.md)

  - [<span data-ttu-id="9353f-142">CommandText プロパティ、Views コレクションの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="9353f-142">CommandText Property, Views Collection example (VB)</span></span>](views-collection-commandtext-property-example-vb.md)

<span data-ttu-id="9353f-143"><<<<<<< 見出し</span><span class="sxs-lookup"><span data-stu-id="9353f-143"><<<<<<< HEAD</span></span>
  - [<span data-ttu-id="9353f-144">DateCreated プロパティと DateModified プロパティの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="9353f-144">DateCreated and DateModified Properties Example (VB)</span></span>](datecreated-and-datemodified-properties-example-vb.md)

  - [<span data-ttu-id="9353f-145">DefinedSize プロパティの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="9353f-145">DefinedSize Property Example (VB)</span></span>](definedsize-property-example-vb.md)

  - [<span data-ttu-id="9353f-146">DeleteRule プロパティの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="9353f-146">DeleteRule Property Example (VB)</span></span>](deleterule-property-example-vb.md)

  - <span data-ttu-id="9353f-147">[IndexNulls プロパティの使用例 (VB)](indexnulls-property-example-vb.md)
=======</span><span class="sxs-lookup"><span data-stu-id="9353f-147">[IndexNulls Property Example (VB)](indexnulls-property-example-vb.md)
=======</span></span>
  - [<span data-ttu-id="9353f-148">DateCreated プロパティと DateModified プロパティの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="9353f-148">DateCreated and DateModified properties example (VB)</span></span>](datecreated-and-datemodified-properties-example-vb.md)

  - [<span data-ttu-id="9353f-149">DefinedSize プロパティの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="9353f-149">DefinedSize property example (VB)</span></span>](definedsize-property-example-vb.md)

  - [<span data-ttu-id="9353f-150">DeleteRule プロパティの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="9353f-150">DeleteRule property example (VB)</span></span>](deleterule-property-example-vb.md)

  - [<span data-ttu-id="9353f-151">IndexNulls プロパティの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="9353f-151">IndexNulls property example (VB)</span></span>](indexnulls-property-example-vb.md)
>>>>>>> <span data-ttu-id="9353f-152">master</span><span class="sxs-lookup"><span data-stu-id="9353f-152">master</span></span>

  - [<span data-ttu-id="9353f-153">Key Type、RelatedColumn、RelatedTable、UpdateRule プロパティ、メソッドの例をキーに追加する (VB)</span><span class="sxs-lookup"><span data-stu-id="9353f-153">Key Type, RelatedColumn, RelatedTable, and UpdateRule Properties, Keys Append method example (VB)</span></span>](keys-append-method-key-type-relatedcolumn-relatedtable-and-updaterule-properties-example-vb.md)

  - [<span data-ttu-id="9353f-154">プロパティの名前、列、およびテーブルの追加のメソッドの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="9353f-154">Name Property, Columns and Tables Append methods example (VB)</span></span>](columns-and-tables-append-methods-name-property-example-vb.md)

<span data-ttu-id="9353f-155"><<<<<<< 見出し</span><span class="sxs-lookup"><span data-stu-id="9353f-155"><<<<<<< HEAD</span></span>
  - [<span data-ttu-id="9353f-156">NumericScale プロパティと Precision プロパティの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="9353f-156">NumericScale and Precision Properties Example (VB)</span></span>](numericscale-and-precision-properties-example-vb.md)

  - [<span data-ttu-id="9353f-157">ParentCatalog プロパティの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="9353f-157">ParentCatalog Property Example (VB)</span></span>](parentcatalog-property-example-vb.md)

  - [<span data-ttu-id="9353f-158">PrimaryKey プロパティと Unique プロパティの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="9353f-158">PrimaryKey and Unique Properties Example (VB)</span></span>](primarykey-and-unique-properties-example-vb.md)

  - <span data-ttu-id="9353f-159">[SortOrder プロパティの使用例 (VB)](sortorder-property-example-vb.md)
=======</span><span class="sxs-lookup"><span data-stu-id="9353f-159">[SortOrder Property Example (VB)](sortorder-property-example-vb.md)
=======</span></span>
  - [<span data-ttu-id="9353f-160">NumericScale プロパティと Precision プロパティの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="9353f-160">NumericScale and Precision properties example (VB)</span></span>](numericscale-and-precision-properties-example-vb.md)

  - [<span data-ttu-id="9353f-161">ParentCatalog プロパティの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="9353f-161">ParentCatalog property example (VB)</span></span>](parentcatalog-property-example-vb.md)

  - [<span data-ttu-id="9353f-162">PrimaryKey プロパティと Unique プロパティの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="9353f-162">PrimaryKey and Unique properties example (VB)</span></span>](primarykey-and-unique-properties-example-vb.md)

  - [<span data-ttu-id="9353f-163">SortOrder プロパティの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="9353f-163">SortOrder property example (VB)</span></span>](sortorder-property-example-vb.md)
>>>>>>> <span data-ttu-id="9353f-164">master</span><span class="sxs-lookup"><span data-stu-id="9353f-164">master</span></span>

  - [<span data-ttu-id="9353f-165">テーブルな型のプロパティ、接続の終了方法、使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="9353f-165">Table Type Property, Connection Close Method, example (VB)</span></span>](connection-close-method-table-type-property-example-vb.md)

<span data-ttu-id="9353f-166">**コレクション**</span><span class="sxs-lookup"><span data-stu-id="9353f-166">**Collections**</span></span>

<span data-ttu-id="9353f-167"><<<<<<< 見出し</span><span class="sxs-lookup"><span data-stu-id="9353f-167"><<<<<<< HEAD</span></span>
  - [<span data-ttu-id="9353f-168">Parameters コレクションの Command プロパティの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="9353f-168">Parameters Collection, Command Property Example (VB)</span></span>](parameters-collection-command-property-example-vb.md)

  - [<span data-ttu-id="9353f-169">Views コレクションと Fields コレクションの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="9353f-169">Views and Fields Collections Example (VB)</span></span>](views-and-fields-collections-example-vb.md)

  - <span data-ttu-id="9353f-170">[Views コレクションでは、CommandText プロパティの使用例 (VB)](views-collection-commandtext-property-example-vb.md)
=======</span><span class="sxs-lookup"><span data-stu-id="9353f-170">[Views Collection, CommandText Property Example (VB)](views-collection-commandtext-property-example-vb.md)
=======</span></span>
  - [<span data-ttu-id="9353f-171">Parameters コレクションのコマンド プロパティの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="9353f-171">Parameters Collection, Command property example (VB)</span></span>](parameters-collection-command-property-example-vb.md)

  - [<span data-ttu-id="9353f-172">ビューとフィールドのコレクションの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="9353f-172">Views and Fields Collections example (VB)</span></span>](views-and-fields-collections-example-vb.md)

  - [<span data-ttu-id="9353f-173">Views コレクションでは、CommandText プロパティの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="9353f-173">Views Collection, CommandText property example (VB)</span></span>](views-collection-commandtext-property-example-vb.md)
>>>>>>> <span data-ttu-id="9353f-174">master</span><span class="sxs-lookup"><span data-stu-id="9353f-174">master</span></span>

