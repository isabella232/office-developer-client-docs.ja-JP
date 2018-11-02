---
title: Procedure オブジェクト (ADOX)
TOCTitle: Procedure object (ADOX)
ms:assetid: d5fcf0fe-f59f-e114-dc11-515f11c2a2c1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250076(v=office.15)
ms:contentKeyID: 48547972
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 72f0475aeca38b5c6ba6cd2954ff894f00fb6f7f
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922651"
---
# <a name="procedure-object-adox"></a>Procedure オブジェクト (ADOX)


**適用されます**Access 2013、Office 2013。

ストアド プロシージャを表します。ADO [Command](command-object-ado.md) オブジェクトと共に使用する場合、 **Procedure** オブジェクトを使用してストアド プロシージャを追加、削除、または変更できます。

## <a name="remarks"></a>解説

**Procedure** オブジェクトを使用すると、プロバイダーの "CREATE PROCEDURE" の構文を使用せずにストアド プロシージャを作成できます。

**Procedure** オブジェクトのプロパティを使用すると、次の操作を実行できます。

  - [Name](name-property-adox.md) プロパティを使用して、プロシージャを識別します。

  - **Command** プロパティを使用して、プロシージャの作成または実行に使用できる ADO [Command](command-property-adox.md) オブジェクトを指定します。

  - [DateCreated](datecreated-property-adox.md) プロパティと [DateModified](datemodified-property-adox.md) プロパティを使用して、日付情報を返します。

