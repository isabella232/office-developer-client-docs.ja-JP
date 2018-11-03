---
title: Column オブジェクト (ADOX)
TOCTitle: Column object (ADOX)
ms:assetid: ad38c2df-f704-0599-4b7a-8556e430ba46
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249811(v=office.15)
ms:contentKeyID: 48547034
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ac4416dce7d3f9fa52c4b948b1e8d3e0167c2751
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25930631"
---
# <a name="column-object-adox"></a><span data-ttu-id="5a315-102">Column オブジェクト (ADOX)</span><span class="sxs-lookup"><span data-stu-id="5a315-102">Column object (ADOX)</span></span>


<span data-ttu-id="5a315-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="5a315-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5a315-104">テーブル、インデックス、またはキーの列を表します。</span><span class="sxs-lookup"><span data-stu-id="5a315-104">Represents a column from a table, index, or key.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a315-105">解説</span><span class="sxs-lookup"><span data-stu-id="5a315-105">Remarks</span></span>

<span data-ttu-id="5a315-106">次のコードによって、新しい **Column** を作成できます。</span><span class="sxs-lookup"><span data-stu-id="5a315-106">The following code creates a new **Column**:</span></span>

`Dim obj As New Column`

<span data-ttu-id="5a315-107">**Column** オブジェクトのプロパティとコレクションを使用すると、次の操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="5a315-107">With the properties and collections of a **Column** object, you can:</span></span>

  - <span data-ttu-id="5a315-108">[Name](name-property-adox.md) プロパティを使用して、列を識別します。</span><span class="sxs-lookup"><span data-stu-id="5a315-108">Identify the column with the [Name](name-property-adox.md) property.</span></span>

  - <span data-ttu-id="5a315-109">[Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) プロパティを使用して、列のデータ型を指定します。</span><span class="sxs-lookup"><span data-stu-id="5a315-109">Specify the data type of the column with the [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) property.</span></span>

  - <span data-ttu-id="5a315-110">[Attributes](attributes-property-adox.md) プロパティを使用して、列が固定長かどうか、または Null 値を含めることができるかどうかを特定します。</span><span class="sxs-lookup"><span data-stu-id="5a315-110">Determine if the column is fixed-length, or if it can contain null values with the [Attributes](attributes-property-adox.md) property.</span></span>

  - <span data-ttu-id="5a315-111">[DefinedSize](definedsize-property-adox.md) プロパティを使用して、列の最大サイズを指定します。</span><span class="sxs-lookup"><span data-stu-id="5a315-111">Specify the maximum size of the column with the [DefinedSize](definedsize-property-adox.md) property.</span></span>

  - <span data-ttu-id="5a315-112">数値型データに対しては、[NumericScale](numericscale-property-adox.md) プロパティを使用して、小数部の桁数を指定します。</span><span class="sxs-lookup"><span data-stu-id="5a315-112">For numeric data values, specify the scale with the [NumericScale](numericscale-property-adox.md) property.</span></span>

  - <span data-ttu-id="5a315-113">数値型データに対しては、[Precision](precision-property-adox.md) プロパティを使用して、最大有効桁数を指定します。</span><span class="sxs-lookup"><span data-stu-id="5a315-113">For numeric data value, specify the maximum precision with the [Precision](precision-property-adox.md) property.</span></span>

  - <span data-ttu-id="5a315-114">[ParentCatalog](catalog-object-adox.md) プロパティを使用して、列を所有する [Catalog](parentcatalog-property-adox.md) を指定します。</span><span class="sxs-lookup"><span data-stu-id="5a315-114">Specify the [Catalog](catalog-object-adox.md) that owns the column with the [ParentCatalog](parentcatalog-property-adox.md) property.</span></span>

  - <span data-ttu-id="5a315-115">キー列では、[RelatedColumn](relatedcolumn-property-adox.md) プロパティを使用して、関連テーブルの関連する列の名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="5a315-115">For key columns, specify the name of the related column in the related table with the [RelatedColumn](relatedcolumn-property-adox.md) property.</span></span>

  - <span data-ttu-id="5a315-116">インデックス列では、[SortOrder](sortorder-property-adox.md) プロパティを使用して、並べ替え順序 (昇順または降順) を指定します。</span><span class="sxs-lookup"><span data-stu-id="5a315-116">For index columns, specify whether the sort order is ascending or descending with the [SortOrder](sortorder-property-adox.md) property.</span></span>

  - <span data-ttu-id="5a315-117">[Properties](properties-collection-ado.md) コレクションを使用して、プロバイダー固有のプロパティにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="5a315-117">Access provider-specific properties with the [Properties](properties-collection-ado.md) collection.</span></span>


> [!NOTE]
> <span data-ttu-id="5a315-p101">[!メモ] データ プロバイダーによっては、サポートされない **Column** オブジェクトのプロパティもあります。プロバイダーがサポートしていないプロパティに値を設定すると、エラーが発生します。新しい **Column** オブジェクトでは、オブジェクトをコレクションに追加するときにエラーが発生します。既存のオブジェクトでは、プロパティを設定するときにエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="5a315-p101">Not all properties of **Column** objects may be supported by your data provider. An error will occur if you have set a value for a property that the provider does not support. For new **Column** objects, the error will occur when the object is appended to the collection. For existing objects, the error will occur when setting the property.</span></span>
> 
> <span data-ttu-id="5a315-p102">**Column** オブジェクトを作成するときは、オプションのプロパティに適切な既定値が存在する場合でも、プロバイダーがプロパティをサポートしているとは限りません。利用しているプロバイダーがサポートしているプロパティの詳細については、そのプロバイダーのドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="5a315-p102">When creating **Column** objects, the existence of an appropriate default value for an optional property does not guarantee that your provider supports the property. For more information about which properties your provider supports, see your provider documentation.</span></span>

