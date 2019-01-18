---
title: View オブジェクト (ADOX のデスクトップのデータベース参照のアクセス)
TOCTitle: View object (ADOX)
ms:assetid: 3b2e9972-8a0d-eaa3-1c93-ae0665a47f02
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249149(v=office.15)
ms:contentKeyID: 48544280
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b3b5d25a727233b5fda5627df8dff952003bbfe3
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722474"
---
# <a name="view-object-adox"></a><span data-ttu-id="bc4bc-102">View オブジェクト (ADOX)</span><span class="sxs-lookup"><span data-stu-id="bc4bc-102">View object (ADOX)</span></span>


<span data-ttu-id="bc4bc-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="bc4bc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bc4bc-p101">抽出されたレコードのセットまたは仮想テーブルを表します。ADO [Command](command-object-ado.md) オブジェクトと共に使用する場合、 **View** オブジェクトを使用してビューを追加、削除、または変更できます。</span><span class="sxs-lookup"><span data-stu-id="bc4bc-p101">Represents a filtered set of records or a virtual table. When used in conjunction with the ADO [Command](command-object-ado.md) object, the **View** object can be used for adding, deleting, or modifying views.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc4bc-106">解説</span><span class="sxs-lookup"><span data-stu-id="bc4bc-106">Remarks</span></span>

<span data-ttu-id="bc4bc-p102">ビューは、他のデータベースまたはビューから作成された仮想テーブルです。 **View** オブジェクトを使用すると、プロバイダーの "CREATE VIEW" の構文を使用せずにストアド プロシージャを作成できます。</span><span class="sxs-lookup"><span data-stu-id="bc4bc-p102">A view is a virtual table, created from other database tables or views. The **View** object allows you to create a view without having to know or use the provider's "CREATE VIEW" syntax.</span></span>

<span data-ttu-id="bc4bc-109">**View** オブジェクトのプロパティを使用すると、次の操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="bc4bc-109">With the properties of a **View** object, you can:</span></span>

  - <span data-ttu-id="bc4bc-110">[Name](name-property-adox.md) プロパティを使用して、ビューを識別します。</span><span class="sxs-lookup"><span data-stu-id="bc4bc-110">Identify the view with the [Name](name-property-adox.md) property.</span></span>

  - <span data-ttu-id="bc4bc-111">**Command** プロパティを使用して、ビューの追加、削除、または変更に使用できる ADO [Command](command-property-adox.md) オブジェクトを指定します。</span><span class="sxs-lookup"><span data-stu-id="bc4bc-111">Specify the ADO **Command** object that can be used to add, delete, or modify views with the [Command](command-property-adox.md) property.</span></span>

  - <span data-ttu-id="bc4bc-112">[DateCreated](datecreated-property-adox.md) プロパティと [DateModified](datemodified-property-adox.md) プロパティを使用して、日付情報を返します。</span><span class="sxs-lookup"><span data-stu-id="bc4bc-112">Return date information with the [DateCreated](datecreated-property-adox.md) and [DateModified](datemodified-property-adox.md) properties.</span></span>

