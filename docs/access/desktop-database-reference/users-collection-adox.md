---
title: Users コレクション (ADOX)
TOCTitle: Users collection (ADOX)
ms:assetid: bc61c862-1637-02e7-4b56-5ad984bdbcb0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249905(v=office.15)
ms:contentKeyID: 48547413
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b44b7b858adca5672266eb1898213d8f28429f2e
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25931135"
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
> <P>[!メモ] <STRONG>User</STRONG> オブジェクトを <STRONG>Group</STRONG> オブジェクトの <STRONG>Users</STRONG> コレクションに追加する前に、追加するものと同じ <STRONG>Name プロパティ (ADOX)</STRONG> を持つ <A href="name-property-adox.md">User</A> オブジェクトが、あらかじめ <STRONG>Catalog</STRONG> の <STRONG>Users</STRONG> コレクションに存在している必要があります。</P>


