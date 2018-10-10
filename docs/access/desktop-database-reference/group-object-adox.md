---
title: Group オブジェクト (ADOX)
TOCTitle: Group Object (ADOX)
ms:assetid: 91cf1b87-c928-1d89-2731-138f6299cc60
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249642(v=office.15)
ms:contentKeyID: 48546359
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 21caab66c16c4ca9f77c49f33bf99f4df7be79c7
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478612"
---
# <a name="group-object-adox"></a>Group オブジェクト (ADOX)


**適用されます**Access 2013 |。Office 2013

保護されているデータベースへの権限を持つグループ アカウントを表します。

## <a name="remarks"></a>解説

[Catalog](groups-collection-adox.md) の [Groups](catalog-object-adox.md) コレクションは、カタログのすべてのグループ アカウントを表します。 **User** の [Groups](user-object-adox.md) コレクションは、ユーザーが属するグループのみを表します。

**Group** オブジェクトのプロパティ、コレクション、およびメソッドを使用すると、次の操作を実行できます。

  - [Name](name-property-adox.md) プロパティを使用して、グループを識別します。

  - [GetPermissions](getpermissions-method-adox.md) メソッドと [SetPermissions](setpermissions-method-adox.md) メソッドを使用して、グループが読み取り、書き込み、および削除の各権限を持っているかどうかを確認します。

  - [Users](users-collection-adox.md) コレクションを使用して、グループのメンバーシップを持っているユーザー アカウントにアクセスします。

  - [Properties](properties-collection-ado.md) コレクションを使用して、プロバイダー固有のプロパティにアクセスします。

