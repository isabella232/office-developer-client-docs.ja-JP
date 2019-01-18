---
title: ユーザー オブジェクト (ADOX のデスクトップのデータベース参照のアクセス)
TOCTitle: User object (ADOX)
ms:assetid: e88b9a8a-e70f-c7ca-cb8c-bd274ff24948
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250178(v=office.15)
ms:contentKeyID: 48548426
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3299a6c0742e7fcbbd26532f3522fdc96b7956b2
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702615"
---
# <a name="user-object-adox"></a>User オブジェクト (ADOX)


**適用されます**Access 2013、Office 2013。

保護されているデータベースへの権限を持つユーザー アカウントを表します。

## <a name="remarks"></a>解説

[Catalog](users-collection-adox.md) の [Users](catalog-object-adox.md) コレクションは、カタログのすべてのユーザーを表します。 **Group** の [Users](group-object-adox.md) コレクションは、特定のグループのユーザーのみを表します。

**User** オブジェクトのプロパティ、コレクション、およびメソッドを使用すると、次の操作を実行できます。

  - [Name](name-property-adox.md) プロパティを使用して、ユーザーを識別します。

  - [ChangePassword](changepassword-method-adox.md) メソッドを使用して、ユーザーのパスワードを変更します。

  - [GetPermissions](getpermissions-method-adox.md) メソッドと [SetPermissions](setpermissions-method-adox.md) メソッドを使用して、ユーザーが読み取り、書き込み、および削除の各権限を持っているかどうかを確認します。

  - [Groups](groups-collection-adox.md) コレクションを使用して、ユーザーが属するグループにアクセスします。

  - [Properties](properties-collection-ado.md) コレクションを使用して、プロバイダー固有のプロパティにアクセスします。

