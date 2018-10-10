---
title: Columns コレクション (ADOX)
TOCTitle: Columns Collection (ADOX)
ms:assetid: 231645db-70da-9ad1-fb27-02145ce32e66
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249008(v=office.15)
ms:contentKeyID: 48543723
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 13f9a17d7dfcd9e621e4f4b1f1fcc03e88b4d832
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479022"
---
# <a name="columns-collection-adox"></a><span data-ttu-id="ac63f-102">Columns コレクション (ADOX)</span><span class="sxs-lookup"><span data-stu-id="ac63f-102">Columns Collection (ADOX)</span></span>


<span data-ttu-id="ac63f-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="ac63f-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ac63f-104">テーブル、インデックス、またはキーのすべての [Column](column-object-adox.md) オブジェクトを含みます。</span><span class="sxs-lookup"><span data-stu-id="ac63f-104">Contains all [Column](column-object-adox.md) objects of a table, index, or key.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac63f-105">解説</span><span class="sxs-lookup"><span data-stu-id="ac63f-105">Remarks</span></span>

<span data-ttu-id="ac63f-p101">[Columns](append-method-adox-columns.md) コレクションの **Append** メソッドは、ADOX に対して一意です。次のことができます。</span><span class="sxs-lookup"><span data-stu-id="ac63f-p101">The [Append](append-method-adox-columns.md) method for a **Columns** collection is unique for ADOX. You can:</span></span>

  - <span data-ttu-id="ac63f-108">**Append** メソッドを使用して、新しい列をコレクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="ac63f-108">Add a new column to the collection with the **Append** method.</span></span>

<span data-ttu-id="ac63f-p102">残りのプロパティとメソッドは、ADO コレクションに標準で装備されています。次のことができます。</span><span class="sxs-lookup"><span data-stu-id="ac63f-p102">The remaining properties and methods are standard to ADO collections. You can:</span></span>

  - <span data-ttu-id="ac63f-111">[Item](item-property-ado.md) プロパティを使用して、コレクションの列にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="ac63f-111">Access a column in the collection with the [Item](item-property-ado.md) property.</span></span>

  - <span data-ttu-id="ac63f-112">[Count](count-property-ado.md) プロパティを使用して、コレクションに含まれる列の数を返します。</span><span class="sxs-lookup"><span data-stu-id="ac63f-112">Return the number of columns contained in the collection with the [Count](count-property-ado.md) property.</span></span>

  - <span data-ttu-id="ac63f-113">[Delete](delete-method-adox-collections.md) メソッドを使用して、コレクションから列を削除します。</span><span class="sxs-lookup"><span data-stu-id="ac63f-113">Remove a column from the collection with the [Delete](delete-method-adox-collections.md) method.</span></span>

  - <span data-ttu-id="ac63f-114">[Refresh](refresh-method-ado.md) メソッドを使用して、コレクションのオブジェクトを更新し、カレント データベースのスキーマを反映します。</span><span class="sxs-lookup"><span data-stu-id="ac63f-114">Update the objects in the collection to reflect the current database's schema with the [Refresh](refresh-method-ado.md) method.</span></span>


> [!NOTE]
> <P><span data-ttu-id="ac63f-115">[!メモ] <STRONG>Column</STRONG> を <STRONG>Index</STRONG> の <A href="index-object-adox.md">Columns</A> コレクションに追加するときに、 <STRONG>Tables</STRONG> コレクションに既に追加されている <A href="table-object-adox.md">Table</A> にまだ <A href="tables-collection-adox.md">Column</A> が存在していない場合は、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="ac63f-115">An error will occur when appending a <STRONG>Column</STRONG> to the <STRONG>Columns</STRONG> collection of an <A href="index-object-adox.md">Index</A> if the <STRONG>Column</STRONG> does not exist in a <A href="table-object-adox.md">Table</A> that is already appended to the <A href="tables-collection-adox.md">Tables</A> collection.</span></span></P>


