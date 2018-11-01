---
title: Procedure オブジェクト (ADOX)
TOCTitle: Procedure Object (ADOX)
ms:assetid: d5fcf0fe-f59f-e114-dc11-515f11c2a2c1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250076(v=office.15)
ms:contentKeyID: 48547972
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: afc4eae76395e7a15573ad5343955b0ab46df3db
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883352"
---
# <a name="procedure-object-adox"></a><span data-ttu-id="fa3a5-102">Procedure オブジェクト (ADOX)</span><span class="sxs-lookup"><span data-stu-id="fa3a5-102">Procedure Object (ADOX)</span></span>


<span data-ttu-id="fa3a5-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="fa3a5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fa3a5-p101">ストアド プロシージャを表します。ADO [Command](command-object-ado.md) オブジェクトと共に使用する場合、 **Procedure** オブジェクトを使用してストアド プロシージャを追加、削除、または変更できます。</span><span class="sxs-lookup"><span data-stu-id="fa3a5-p101">Represents a stored procedure. When used in conjunction with the ADO [Command](command-object-ado.md) object, the **Procedure** object can be used for adding, deleting, or modifying stored procedures.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa3a5-106">解説</span><span class="sxs-lookup"><span data-stu-id="fa3a5-106">Remarks</span></span>

<span data-ttu-id="fa3a5-107">**Procedure** オブジェクトを使用すると、プロバイダーの "CREATE PROCEDURE" の構文を使用せずにストアド プロシージャを作成できます。</span><span class="sxs-lookup"><span data-stu-id="fa3a5-107">The **Procedure** object allows you to create a stored procedure without having to know or use the provider's "CREATE PROCEDURE" syntax.</span></span>

<span data-ttu-id="fa3a5-108">**Procedure** オブジェクトのプロパティを使用すると、次の操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="fa3a5-108">With the properties of a **Procedure** object, you can:</span></span>

  - <span data-ttu-id="fa3a5-109">[Name](name-property-adox.md) プロパティを使用して、プロシージャを識別します。</span><span class="sxs-lookup"><span data-stu-id="fa3a5-109">Identify the procedure with the [Name](name-property-adox.md) property.</span></span>

  - <span data-ttu-id="fa3a5-110">**Command** プロパティを使用して、プロシージャの作成または実行に使用できる ADO [Command](command-property-adox.md) オブジェクトを指定します。</span><span class="sxs-lookup"><span data-stu-id="fa3a5-110">Specify the ADO **Command** object that can be used to create or execute the procedure with the [Command](command-property-adox.md) property.</span></span>

  - <span data-ttu-id="fa3a5-111">[DateCreated](datecreated-property-adox.md) プロパティと [DateModified](datemodified-property-adox.md) プロパティを使用して、日付情報を返します。</span><span class="sxs-lookup"><span data-stu-id="fa3a5-111">Return date information with the [DateCreated](datecreated-property-adox.md) and [DateModified](datemodified-property-adox.md) properties.</span></span>

