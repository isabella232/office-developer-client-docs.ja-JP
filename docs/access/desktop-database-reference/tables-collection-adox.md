---
title: Tables コレクション (ADOX)
TOCTitle: Tables Collection (ADOX)
ms:assetid: 07bc0541-c528-1c25-c8c4-05736836eda3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248821(v=office.15)
ms:contentKeyID: 48543082
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 43ca716cf03579c5c4cacf3f6b83a56d549b1433
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478059"
---
# <a name="tables-collection-adox"></a><span data-ttu-id="33b27-102">Tables コレクション (ADOX)</span><span class="sxs-lookup"><span data-stu-id="33b27-102">Tables Collection (ADOX)</span></span>


<span data-ttu-id="33b27-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="33b27-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="33b27-104">カタログのすべての [Table](table-object-adox.md) オブジェクトを含みます。</span><span class="sxs-lookup"><span data-stu-id="33b27-104">Contains all [Table](table-object-adox.md) objects of a catalog.</span></span>

## <a name="remarks"></a><span data-ttu-id="33b27-105">解説</span><span class="sxs-lookup"><span data-stu-id="33b27-105">Remarks</span></span>

<span data-ttu-id="33b27-p101">[Tables](append-method-adox-tables.md) コレクションの **Append** メソッドは、ADOX に対して一意です。次のことができます。</span><span class="sxs-lookup"><span data-stu-id="33b27-p101">The [Append](append-method-adox-tables.md) method for a **Tables** collection is unique for ADOX. You can:</span></span>

  - <span data-ttu-id="33b27-108">**Append** メソッドを使用して、新しいテーブルをコレクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="33b27-108">Add a new table to the collection with the **Append** method.</span></span>

<span data-ttu-id="33b27-p102">残りのプロパティとメソッドは、ADO コレクションに標準で装備されています。次のことができます。</span><span class="sxs-lookup"><span data-stu-id="33b27-p102">The remaining properties and methods are standard to ADO collections. You can:</span></span>

  - <span data-ttu-id="33b27-111">[Item](item-property-ado.md) プロパティを使用して、コレクションのテーブルにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="33b27-111">Access a table in the collection with the [Item](item-property-ado.md) property.</span></span>

  - <span data-ttu-id="33b27-112">[Count](count-property-ado.md) プロパティを使用して、コレクションに含まれるテーブルの数を返します。</span><span class="sxs-lookup"><span data-stu-id="33b27-112">Return the number of tables contained in the collection with the [Count](count-property-ado.md) property.</span></span>

  - <span data-ttu-id="33b27-113">[Delete](delete-method-adox-collections.md) メソッドを使用して、コレクションからテーブルを削除します。</span><span class="sxs-lookup"><span data-stu-id="33b27-113">Remove a table from the collection with the [Delete](delete-method-adox-collections.md) method.</span></span>

  - <span data-ttu-id="33b27-114">[Refresh](refresh-method-ado.md) メソッドを使用して、コレクションのオブジェクトを更新し、カレント データベースのスキーマを反映します。</span><span class="sxs-lookup"><span data-stu-id="33b27-114">Update the objects in the collection to reflect the current database's schema with the [Refresh](refresh-method-ado.md) method.</span></span>

<span data-ttu-id="33b27-p103">プロバイダーによっては、Tables コレクションで他のスキーマ オブジェクト (View など) を返すことがあります。したがって、複数の ADOX コレクションに同じオブジェクトへの参照が含まれることになります。1 つのコレクションからオブジェクトを削除すると、削除されたオブジェクトを参照する別のコレクションでは、コレクションで Refresh メソッドを呼び出すまで変更内容が反映されません。たとえば、Microsoft Jet の OLE DB Provider では、View は Tables コレクションで返されます。View を削除した場合は、Tables コレクションにその変更を反映するために、コレクションで Refresh を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="33b27-p103">Some providers may return other schema objects, such as a View, in the Tables collection. Therefore, some ADOX collections may contain references to the same object. Should you delete the object from one collection, the change will not be visible in another collection that references the deleted object until the Refresh method is called on the collection. For example, with the OLE DB Provider for Microsoft Jet, Views are returned with the Tables collection. If you drop a View, you must Refresh the Tables collection before the collection will reflect the change.</span></span>
