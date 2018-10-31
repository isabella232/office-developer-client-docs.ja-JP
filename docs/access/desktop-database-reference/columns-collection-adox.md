---
title: Columns コレクション (ADOX)
TOCTitle: Columns Collection (ADOX)
ms:assetid: 231645db-70da-9ad1-fb27-02145ce32e66
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249008(v=office.15)
ms:contentKeyID: 48543723
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d49fa1bf77a66dbab829aff20ee666ae1a5082cc
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862219"
---
# <a name="columns-collection-adox"></a><span data-ttu-id="c68f4-102">Columns コレクション (ADOX)</span><span class="sxs-lookup"><span data-stu-id="c68f4-102">Columns Collection (ADOX)</span></span>


<span data-ttu-id="c68f4-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="c68f4-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c68f4-104">テーブル、インデックス、またはキーのすべての [Column](column-object-adox.md) オブジェクトを含みます。</span><span class="sxs-lookup"><span data-stu-id="c68f4-104">Contains all [Column](column-object-adox.md) objects of a table, index, or key.</span></span>

## <a name="remarks"></a><span data-ttu-id="c68f4-105">解説</span><span class="sxs-lookup"><span data-stu-id="c68f4-105">Remarks</span></span>

<span data-ttu-id="c68f4-p101">[Columns](append-method-adox-columns.md) コレクションの **Append** メソッドは、ADOX に対して一意です。次のことができます。</span><span class="sxs-lookup"><span data-stu-id="c68f4-p101">The [Append](append-method-adox-columns.md) method for a **Columns** collection is unique for ADOX. You can:</span></span>

  - <span data-ttu-id="c68f4-108">**Append** メソッドを使用して、新しい列をコレクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="c68f4-108">Add a new column to the collection with the **Append** method.</span></span>

<span data-ttu-id="c68f4-p102">残りのプロパティとメソッドは、ADO コレクションに標準で装備されています。次のことができます。</span><span class="sxs-lookup"><span data-stu-id="c68f4-p102">The remaining properties and methods are standard to ADO collections. You can:</span></span>

  - <span data-ttu-id="c68f4-111">[Item](item-property-ado.md) プロパティを使用して、コレクションの列にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="c68f4-111">Access a column in the collection with the [Item](item-property-ado.md) property.</span></span>

  - <span data-ttu-id="c68f4-112">[Count](count-property-ado.md) プロパティを使用して、コレクションに含まれる列の数を返します。</span><span class="sxs-lookup"><span data-stu-id="c68f4-112">Return the number of columns contained in the collection with the [Count](count-property-ado.md) property.</span></span>

  - <span data-ttu-id="c68f4-113">[Delete](delete-method-adox-collections.md) メソッドを使用して、コレクションから列を削除します。</span><span class="sxs-lookup"><span data-stu-id="c68f4-113">Remove a column from the collection with the [Delete](delete-method-adox-collections.md) method.</span></span>

  - <span data-ttu-id="c68f4-114">[Refresh](refresh-method-ado.md) メソッドを使用して、コレクションのオブジェクトを更新し、カレント データベースのスキーマを反映します。</span><span class="sxs-lookup"><span data-stu-id="c68f4-114">Update the objects in the collection to reflect the current database's schema with the [Refresh](refresh-method-ado.md) method.</span></span>


> [!NOTE]
> <span data-ttu-id="c68f4-115">[!メモ] **Column** を **Index** の [Columns](index-object-adox.md) コレクションに追加するときに、 **Tables** コレクションに既に追加されている [Table](table-object-adox.md) にまだ [Column](tables-collection-adox.md) が存在していない場合は、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="c68f4-115">An error will occur when appending a **Column** to the **Columns** collection of an [Index](index-object-adox.md) if the **Column** does not exist in a [Table](table-object-adox.md) that is already appended to the [Tables](tables-collection-adox.md) collection.</span></span>


