---
title: Table オブジェクト (ADOX)
TOCTitle: Table object (ADOX)
ms:assetid: 53a3e2f9-4ec0-8fed-d482-4f995921587b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249273(v=office.15)
ms:contentKeyID: 48544874
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 19f30bec624a43bc1b821d8bef01afa166b0c544
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026429"
---
# <a name="table-object-adox"></a><span data-ttu-id="8ba1d-102">Table オブジェクト (ADOX)</span><span class="sxs-lookup"><span data-stu-id="8ba1d-102">Table object (ADOX)</span></span>

<span data-ttu-id="8ba1d-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="8ba1d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8ba1d-104">列、インデックス、およびキーを含むデータベース テーブルを表します。</span><span class="sxs-lookup"><span data-stu-id="8ba1d-104">Represents a database table including columns, indexes, and keys.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ba1d-105">解説</span><span class="sxs-lookup"><span data-stu-id="8ba1d-105">Remarks</span></span>

<span data-ttu-id="8ba1d-106">次のコードによって、新しい **Table** を作成できます。</span><span class="sxs-lookup"><span data-stu-id="8ba1d-106">The following code creates a new **Table**:</span></span>

`Dim obj As New Table`

<span data-ttu-id="8ba1d-107">**Table** オブジェクトのプロパティとコレクションを使用すると、次の操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="8ba1d-107">With the properties and collections of a **Table** object, you can:</span></span>

- <span data-ttu-id="8ba1d-108">[Name](name-property-adox.md) プロパティを使用して、テーブルを識別します。</span><span class="sxs-lookup"><span data-stu-id="8ba1d-108">Identify the table with the [Name](name-property-adox.md) property.</span></span>

- <span data-ttu-id="8ba1d-109">[Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-tableadox) プロパティを使用して、テーブルの種類を特定します。</span><span class="sxs-lookup"><span data-stu-id="8ba1d-109">Determine the type of table with the [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-tableadox) property.</span></span>

- <span data-ttu-id="8ba1d-110">[Columns](columns-collection-adox.md) コレクションを使用して、データベース テーブルの列にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="8ba1d-110">Access the database columns of the table with the [Columns](columns-collection-adox.md) collection.</span></span>

- <span data-ttu-id="8ba1d-111">[Indexes](indexes-collection-adox.md) コレクションを使用して、テーブルのインデックスにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="8ba1d-111">Access the indexes of the table with the [Indexes](indexes-collection-adox.md) collection.</span></span>

- <span data-ttu-id="8ba1d-112">[Keys](keys-collection-adox.md) コレクションを使用して、テーブルのキーにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="8ba1d-112">Access the keys of the table with the [Keys](keys-collection-adox.md) collection.</span></span>

- <span data-ttu-id="8ba1d-113">[ParentCatalog](catalog-object-adox.md) プロパティを使用して、テーブルを所有する [Catalog](parentcatalog-property-adox.md) を指定します。</span><span class="sxs-lookup"><span data-stu-id="8ba1d-113">Specify the [Catalog](catalog-object-adox.md) that owns the table with the [ParentCatalog](parentcatalog-property-adox.md) property.</span></span>

- <span data-ttu-id="8ba1d-114">[DateCreated](datecreated-property-adox.md) プロパティと [DateModified](datemodified-property-adox.md) プロパティを使用して、日付情報を返します。</span><span class="sxs-lookup"><span data-stu-id="8ba1d-114">Return date information with the [DateCreated](datecreated-property-adox.md) and [DateModified](datemodified-property-adox.md) properties.</span></span>

- <span data-ttu-id="8ba1d-115">[Properties](properties-collection-ado.md) コレクションを使用して、プロバイダー固有のテーブルのプロパティにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="8ba1d-115">Access provider-specific table properties with the [Properties](properties-collection-ado.md) collection.</span></span>


> [!NOTE]
> <span data-ttu-id="8ba1d-p101">[!メモ] データ プロバイダーによっては、サポートされない **Table** オブジェクトのプロパティもあります。プロバイダーがサポートしていないプロパティに値を設定すると、エラーが発生します。新しい **Table** オブジェクトでは、オブジェクトをコレクションに追加するときにエラーが発生します。既存のオブジェクトでは、プロパティを設定するときにエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="8ba1d-p101">Your data provider may not support all properties of **Table** objects. An error will occur if you have set a value for a property that the provider does not support. For new **Table** objects, the error will occur when the object is appended to the collection. For existing objects, the error will occur when setting the property.</span></span>

<span data-ttu-id="8ba1d-p102">**Table** オブジェクトを作成するときは、オプションのプロパティに適切な既定値が存在する場合でも、プロバイダーがプロパティをサポートしているとは限りません。利用しているプロバイダーがサポートしているプロパティの詳細については、そのプロバイダーのドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="8ba1d-p102">When creating **Table** objects, the existence of an appropriate default value for an optional property does not guarantee that your provider supports the property. For more information about which properties your provider supports, see your provider documentation.</span></span>

