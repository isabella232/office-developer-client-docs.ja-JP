---
title: Column オブジェクト (ADOX)
TOCTitle: Column Object (ADOX)
ms:assetid: ad38c2df-f704-0599-4b7a-8556e430ba46
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249811(v=office.15)
ms:contentKeyID: 48547034
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: be5af50dd17934ece6ae3a00242a86e691ff337e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478539"
---
# <a name="column-object-adox"></a><span data-ttu-id="2a6cf-102">Column オブジェクト (ADOX)</span><span class="sxs-lookup"><span data-stu-id="2a6cf-102">Column Object (ADOX)</span></span>


<span data-ttu-id="2a6cf-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="2a6cf-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2a6cf-104">テーブル、インデックス、またはキーの列を表します。</span><span class="sxs-lookup"><span data-stu-id="2a6cf-104">Represents a column from a table, index, or key.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a6cf-105">解説</span><span class="sxs-lookup"><span data-stu-id="2a6cf-105">Remarks</span></span>

<span data-ttu-id="2a6cf-106">次のコードによって、新しい **Column** を作成できます。</span><span class="sxs-lookup"><span data-stu-id="2a6cf-106">The following code creates a new **Column**:</span></span>

`Dim obj As New Column`

<span data-ttu-id="2a6cf-107">**Column** オブジェクトのプロパティとコレクションを使用すると、次の操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="2a6cf-107">With the properties and collections of a **Column** object, you can:</span></span>

  - <span data-ttu-id="2a6cf-108">[Name](name-property-adox.md) プロパティを使用して、列を識別します。</span><span class="sxs-lookup"><span data-stu-id="2a6cf-108">Identify the column with the [Name](name-property-adox.md) property.</span></span>

  - <span data-ttu-id="2a6cf-109">[Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) プロパティを使用して、列のデータ型を指定します。</span><span class="sxs-lookup"><span data-stu-id="2a6cf-109">Specify the data type of the column with the [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) property.</span></span>

  - <span data-ttu-id="2a6cf-110">[Attributes](attributes-property-adox.md) プロパティを使用して、列が固定長かどうか、または Null 値を含めることができるかどうかを特定します。</span><span class="sxs-lookup"><span data-stu-id="2a6cf-110">Determine if the column is fixed-length, or if it can contain null values with the [Attributes](attributes-property-adox.md) property.</span></span>

  - <span data-ttu-id="2a6cf-111">[DefinedSize](definedsize-property-adox.md) プロパティを使用して、列の最大サイズを指定します。</span><span class="sxs-lookup"><span data-stu-id="2a6cf-111">Specify the maximum size of the column with the [DefinedSize](definedsize-property-adox.md) property.</span></span>

  - <span data-ttu-id="2a6cf-112">数値型データに対しては、[NumericScale](numericscale-property-adox.md) プロパティを使用して、小数部の桁数を指定します。</span><span class="sxs-lookup"><span data-stu-id="2a6cf-112">For numeric data values, specify the scale with the [NumericScale](numericscale-property-adox.md) property.</span></span>

  - <span data-ttu-id="2a6cf-113">数値型データに対しては、[Precision](precision-property-adox.md) プロパティを使用して、最大有効桁数を指定します。</span><span class="sxs-lookup"><span data-stu-id="2a6cf-113">For numeric data value, specify the maximum precision with the [Precision](precision-property-adox.md) property.</span></span>

  - <span data-ttu-id="2a6cf-114">[ParentCatalog](catalog-object-adox.md) プロパティを使用して、列を所有する [Catalog](parentcatalog-property-adox.md) を指定します。</span><span class="sxs-lookup"><span data-stu-id="2a6cf-114">Specify the [Catalog](catalog-object-adox.md) that owns the column with the [ParentCatalog](parentcatalog-property-adox.md) property.</span></span>

  - <span data-ttu-id="2a6cf-115">キー列では、[RelatedColumn](relatedcolumn-property-adox.md) プロパティを使用して、関連テーブルの関連する列の名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="2a6cf-115">For key columns, specify the name of the related column in the related table with the [RelatedColumn](relatedcolumn-property-adox.md) property.</span></span>

  - <span data-ttu-id="2a6cf-116">インデックス列では、[SortOrder](sortorder-property-adox.md) プロパティを使用して、並べ替え順序 (昇順または降順) を指定します。</span><span class="sxs-lookup"><span data-stu-id="2a6cf-116">For index columns, specify whether the sort order is ascending or descending with the [SortOrder](sortorder-property-adox.md) property.</span></span>

  - <span data-ttu-id="2a6cf-117">[Properties](properties-collection-ado.md) コレクションを使用して、プロバイダー固有のプロパティにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="2a6cf-117">Access provider-specific properties with the [Properties](properties-collection-ado.md) collection.</span></span>


> [!NOTE]
> <span data-ttu-id="2a6cf-p101">[!メモ] データ プロバイダーによっては、サポートされない **Column** オブジェクトのプロパティもあります。プロバイダーがサポートしていないプロパティに値を設定すると、エラーが発生します。新しい **Column** オブジェクトでは、オブジェクトをコレクションに追加するときにエラーが発生します。既存のオブジェクトでは、プロパティを設定するときにエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="2a6cf-p101">Not all properties of **Column** objects may be supported by your data provider. An error will occur if you have set a value for a property that the provider does not support. For new **Column** objects, the error will occur when the object is appended to the collection. For existing objects, the error will occur when setting the property.</span></span>
> 
> <span data-ttu-id="2a6cf-p102">**Column** オブジェクトを作成するときは、オプションのプロパティに適切な既定値が存在する場合でも、プロバイダーがプロパティをサポートしているとは限りません。利用しているプロバイダーがサポートしているプロパティの詳細については、そのプロバイダーのドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="2a6cf-p102">When creating **Column** objects, the existence of an appropriate default value for an optional property does not guarantee that your provider supports the property. For more information about which properties your provider supports, see your provider documentation.</span></span>

