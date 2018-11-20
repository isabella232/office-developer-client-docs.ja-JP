---
title: Index オブジェクト (ADOX)
TOCTitle: Index object (ADOX)
ms:assetid: fe368ab1-e396-4684-d930-18b0ba58a925
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250304(v=office.15)
ms:contentKeyID: 48548929
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5bc2eeaf4d26c957abb67780fe2f5d0df8f73049
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026177"
---
# <a name="index-object-adox"></a><span data-ttu-id="42627-102">Index オブジェクト (ADOX)</span><span class="sxs-lookup"><span data-stu-id="42627-102">Index object (ADOX)</span></span>

<span data-ttu-id="42627-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="42627-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="42627-104">データベース テーブルのインデックスを表します。</span><span class="sxs-lookup"><span data-stu-id="42627-104">Represents an index from a database table.</span></span>

## <a name="remarks"></a><span data-ttu-id="42627-105">解説</span><span class="sxs-lookup"><span data-stu-id="42627-105">Remarks</span></span>

<span data-ttu-id="42627-106">次のコードによって、新しい **Index** を作成できます。</span><span class="sxs-lookup"><span data-stu-id="42627-106">The following code creates a new **Index**:</span></span>

`Dim obj As New Index`

<span data-ttu-id="42627-107">**Index** オブジェクトのプロパティとコレクションを使用すると、次の操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="42627-107">With the properties and collections of an **Index** object, you can:</span></span>

- <span data-ttu-id="42627-108">[Name](name-property-adox.md) プロパティを使用して、インデックスを識別します。</span><span class="sxs-lookup"><span data-stu-id="42627-108">Identify the index with the [Name](name-property-adox.md) property.</span></span>

- <span data-ttu-id="42627-109">[Columns](columns-collection-adox.md) コレクションを使用して、インデックスによって指定されたデータベースの列にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="42627-109">Access the database columns of the index with the [Columns](columns-collection-adox.md) collection.</span></span>

- <span data-ttu-id="42627-110">[Unique](unique-property-adox.md) プロパティを使用して、インデックス キーを一意にする必要があるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="42627-110">Specify whether the index keys must be unique with the [Unique](unique-property-adox.md) property.</span></span>

- <span data-ttu-id="42627-111">[PrimaryKey](primarykey-property-adox.md) プロパティを使用して、インデックスがテーブルの主キーかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="42627-111">Specify whether the index is the primary key for a table with the [PrimaryKey](primarykey-property-adox.md) property.</span></span>

- <span data-ttu-id="42627-112">[IndexNulls](indexnulls-property-adox.md) プロパティを使用して、インデックス フィールドが Null 値のレコードがインデックス エントリを持っているかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="42627-112">Specify whether records that have null values in their index fields have index entries with the [IndexNulls](indexnulls-property-adox.md) property.</span></span>

- <span data-ttu-id="42627-113">[Clustered](clustered-property-adox.md) プロパティを使用して、インデックスがクラスター化されているかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="42627-113">Specify whether the index is clustered with the [Clustered](clustered-property-adox.md) property.</span></span>

- <span data-ttu-id="42627-114">[Properties](properties-collection-ado.md) コレクションを使用して、プロバイダー固有のインデックスのプロパティにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="42627-114">Access provider-specific index properties with the [Properties](properties-collection-ado.md) collection.</span></span>


> [!NOTE]
> <span data-ttu-id="42627-115">[!メモ] [Column](column-object-adox.md) を **Index** の **Columns** コレクションに追加するときに、 **Tables** コレクションに既に追加されている [Table](table-object-adox.md) オブジェクトに [Column](tables-collection-adox.md) が存在していない場合は、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="42627-115">An error will occur when appending a [Column](column-object-adox.md) to the **Columns** collection of an **Index** if the **Column** does not exist in a [Table](table-object-adox.md) object already appended to the [Tables](tables-collection-adox.md) collection.</span></span>

<span data-ttu-id="42627-p101">データ プロバイダーによっては、サポートされない **Index** オブジェクトのプロパティもあります。プロバイダーがサポートしていないプロパティに値を設定すると、エラーが発生します。新しい **Index** オブジェクトでは、オブジェクトをコレクションに追加するときにエラーが発生します。既存のオブジェクトでは、プロパティを設定するときにエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="42627-p101">Your data provider may not support all properties of **Index** objects. An error will occur if you have set a value for a property that is not supported by the provider. For new **Index** objects, the error will occur when the object is appended to the collection. For existing objects, the error will occur when setting the property.</span></span>

<span data-ttu-id="42627-p102">**Index** オブジェクトを作成するときは、オプションのプロパティに適切な既定値が存在する場合でも、プロバイダーがプロパティをサポートしているとは限りません。利用しているプロバイダーがサポートしているプロパティの詳細については、そのプロバイダーのドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="42627-p102">When creating **Index** objects, the existence of an appropriate default value for an optional property does not guarantee that your provider supports the property. For more information about which properties your provider supports, see your provider documentation.</span></span>

