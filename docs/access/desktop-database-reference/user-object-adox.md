---
title: User Object (ADOX - Access desktop database reference)
TOCTitle: User object (ADOX)
ms:assetid: e88b9a8a-e70f-c7ca-cb8c-bd274ff24948
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250178(v=office.15)
ms:contentKeyID: 48548426
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 8bd62da5b813985c725703cca80a75aabbac73fb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59593356"
---
# <a name="user-object-adox"></a>ユーザー オブジェクト (ADOX)


**適用先**: Access 2013、Office 2013

保護されているデータベースへの権限を持つユーザー アカウントを表します。

## <a name="remarks"></a>注釈

[Catalog](users-collection-adox.md) の [Users](catalog-object-adox.md) コレクションは、カタログのすべてのユーザーを表します。 **Group** の [Users](group-object-adox.md) コレクションは、特定のグループのユーザーのみを表します。

**User** オブジェクトのプロパティ、コレクション、およびメソッドを使用すると、次の操作を実行できます。

  - [Name](name-property-adox.md) プロパティを使用して、ユーザーを識別します。

  - [ChangePassword](changepassword-method-adox.md) メソッドを使用して、ユーザーのパスワードを変更します。

  - [GetPermissions](getpermissions-method-adox.md) メソッドと [SetPermissions](setpermissions-method-adox.md) メソッドを使用して、ユーザーが読み取り、書き込み、および削除の各権限を持っているかどうかを確認します。

  - [Groups](groups-collection-adox.md) コレクションを使用して、ユーザーが属するグループにアクセスします。

  - [Properties](properties-collection-ado.md) コレクションを使用して、プロバイダー固有のプロパティにアクセスします。

