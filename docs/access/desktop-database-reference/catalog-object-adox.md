---
title: Catalog オブジェクト (ADOX)
TOCTitle: Catalog object (ADOX)
ms:assetid: d9e8d94b-9161-3eb6-abaf-00d1244d1f2d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250097(v=office.15)
ms:contentKeyID: 48548068
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 31a0d2212f063eca013c1668b47e548df1405366
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922574"
---
# <a name="catalog-object-adox"></a><span data-ttu-id="e432e-102">Catalog オブジェクト (ADOX)</span><span class="sxs-lookup"><span data-stu-id="e432e-102">Catalog object (ADOX)</span></span>


<span data-ttu-id="e432e-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="e432e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e432e-104">データ ソースのスキーマ カタログを表すコレクションを含みます ([Tables](tables-collection-adox.md)、[Views](views-collection-adox.md)、[Users](users-collection-adox.md)、[Groups](groups-collection-adox.md)、および [Procedures](procedures-collection-adox.md))。</span><span class="sxs-lookup"><span data-stu-id="e432e-104">Contains collections ([Tables](tables-collection-adox.md), [Views](views-collection-adox.md), [Users](users-collection-adox.md), [Groups](groups-collection-adox.md), and [Procedures](procedures-collection-adox.md)) that describe the schema catalog of a data source.</span></span>

## <a name="remarks"></a><span data-ttu-id="e432e-105">解説</span><span class="sxs-lookup"><span data-stu-id="e432e-105">Remarks</span></span>

<span data-ttu-id="e432e-p101">**Catalog** オブジェクトは、オブジェクトを追加または削除するか、既存のオブジェクトを変更することによって変更できます。すべての **Catalog** オブジェクトをサポートしていないプロバイダーもあり、スキーマ情報の閲覧のみをサポートするプロバイダーもあります。</span><span class="sxs-lookup"><span data-stu-id="e432e-p101">You can modify the **Catalog** object by adding or removing objects or by modifying existing objects. Some providers may not support all of the **Catalog** objects or may support only viewing schema information.</span></span>

<span data-ttu-id="e432e-108">**Catalog** オブジェクトのプロパティとメソッドを使用すると、次の操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="e432e-108">With the properties and methods of a **Catalog** object, you can:</span></span>

  - <span data-ttu-id="e432e-109">[ActiveConnection](activeconnection-property-adox.md) プロパティを ADO [Connection](connection-object-ado.md) オブジェクトまたは有効な接続文字列に設定して、カタログを開きます。</span><span class="sxs-lookup"><span data-stu-id="e432e-109">Open the catalog by setting the [ActiveConnection](activeconnection-property-adox.md) property to an ADO [Connection](connection-object-ado.md) object or a valid connection string.</span></span>

  - <span data-ttu-id="e432e-110">[Create](create-method-adox.md) メソッドを使用して、新しいカタログを作成します。</span><span class="sxs-lookup"><span data-stu-id="e432e-110">Create a new catalog with the [Create](create-method-adox.md) method.</span></span>

  - <span data-ttu-id="e432e-111">**GetObjectOwner** メソッドと [SetObjectOwner](getobjectowner-method-adox.md) メソッドを使用して、 [Catalog](https://msdn.microsoft.com/library/jj249006\(v=office.15\)) 内のオブジェクトの所有者を特定します。</span><span class="sxs-lookup"><span data-stu-id="e432e-111">Determine the owners of the objects in a **Catalog** with the [GetObjectOwner](getobjectowner-method-adox.md) and [SetObjectOwner](https://msdn.microsoft.com/library/jj249006\(v=office.15\)) methods.</span></span>

