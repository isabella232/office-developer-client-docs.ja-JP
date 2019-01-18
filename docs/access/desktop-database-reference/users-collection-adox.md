---
title: Users コレクション (ADOX)
TOCTitle: Users collection (ADOX)
ms:assetid: bc61c862-1637-02e7-4b56-5ad984bdbcb0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249905(v=office.15)
ms:contentKeyID: 48547413
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 24d7a5cab3260dac80b39e5134938c5f55175851
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720409"
---
# <a name="users-collection-adox"></a>Users コレクション (ADOX)

**適用されます**Access 2013、Office 2013。

カタログまたはグループのすべての格納された [User](user-object-adox.md) オブジェクトを含みます。

## <a name="remarks"></a>解説

**Catalog** の [Users](catalog-object-adox.md) コレクションは、そのカタログのすべてのユーザーを表します。 **Group** の [Users](group-object-adox.md) コレクションは、特定のグループでメンバーシップを持つユーザーのみを表します。

[Users](append-method-adox-users.md) コレクションの **Append** メソッドは、ADOX に対して一意です。次のことができます。

- **Append** メソッドを使用して、新しいユーザーをコレクションに追加します。

残りのプロパティとメソッドは、ADO コレクションに標準で装備されています。次のことができます。

- [Item](item-property-ado.md) プロパティを使用して、コレクションのユーザーにアクセスします。

- [Count](count-property-ado.md) プロパティを使用して、コレクションに含まれるユーザーの数を返します。

- [Delete](delete-method-adox-collections.md) メソッドを使用して、コレクションからユーザーを削除します。

- [Refresh](refresh-method-ado.md) メソッドを使用して、コレクションのオブジェクトを更新し、カレント データベースのスキーマを反映します。

> [!NOTE]
> [!メモ] **User** オブジェクトを **Group** オブジェクトの **Users** コレクションに追加する前に、追加するものと同じ **Name プロパティ (ADOX)** を持つ [User](name-property-adox.md) オブジェクトが、あらかじめ **Catalog** の **Users** コレクションに存在している必要があります。

