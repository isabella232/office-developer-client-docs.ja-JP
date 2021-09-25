---
title: グループ オブジェクト (ADOX)
TOCTitle: Group object (ADOX)
ms:assetid: 91cf1b87-c928-1d89-2731-138f6299cc60
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249642(v=office.15)
ms:contentKeyID: 48546359
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 3d131d89dbcc67f244010fc0cee86bad30f78c2d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59606696"
---
# <a name="group-object-adox"></a>グループ オブジェクト (ADOX)


**適用先**: Access 2013、Office 2013

保護されているデータベースへの権限を持つグループ アカウントを表します。

## <a name="remarks"></a>注釈

[Catalog](groups-collection-adox.md) の [Groups](catalog-object-adox.md) コレクションは、カタログのすべてのグループ アカウントを表します。 **User** の [Groups](user-object-adox.md) コレクションは、ユーザーが属するグループのみを表します。

**Group** オブジェクトのプロパティ、コレクション、およびメソッドを使用すると、次の操作を実行できます。

  - [Name](name-property-adox.md) プロパティを使用して、グループを識別します。

  - [GetPermissions](getpermissions-method-adox.md) メソッドと [SetPermissions](setpermissions-method-adox.md) メソッドを使用して、グループが読み取り、書き込み、および削除の各権限を持っているかどうかを確認します。

  - [Users](users-collection-adox.md) コレクションを使用して、グループのメンバーシップを持っているユーザー アカウントにアクセスします。

  - [Properties](properties-collection-ado.md) コレクションを使用して、プロバイダー固有のプロパティにアクセスします。

