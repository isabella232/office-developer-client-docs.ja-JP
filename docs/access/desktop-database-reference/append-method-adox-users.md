---
title: Append メソッド (ADOX Users)
TOCTitle: Append Method (ADOX Users)
ms:assetid: b7a1128b-c6e7-2071-c914-913b6bd245ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249884(v=office.15)
ms:contentKeyID: 48547302
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b8bce151e800b58e9c99c6dd6591114c53208a5c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477008"
---
# <a name="append-method-adox-users"></a>Append メソッド (ADOX Users)


**適用されます**Access 2013 |。Office 2013


新しい [User](user-object-adox.md) オブジェクトを [Users](users-collection-adox.md) コレクションに追加します。

## <a name="syntax"></a>構文

*ユーザー*です。*ユーザー*を追加する\[、*パスワード*\]

## <a name="parameters"></a>パラメーター

  - *User*

  - 追加する **User** オブジェクトを含むバリアント型 ( **Variant** ) の値を指定します。または、新たに作成して追加するユーザーの名前を指定します。

  - *Password*

  - 省略可能です。 このユーザーのパスワードを含む文字列型 ( **String** ) の値を指定します。 *パスワード*パラメーターは、**ユーザー**オブジェクトの[パスワードの変更](changepassword-method-adox.md)メソッドによって指定された値に対応します。

## <a name="remarks"></a>解説

**Catalog** の [Users](catalog-object-adox.md) コレクションは、そのカタログのすべてのユーザーを表します。 **Group** の [Users](group-object-adox.md) コレクションは、特定のグループでメンバーシップを持つユーザーのみを表します。

プロバイダーがユーザーの作成をサポートしていない場合は、エラーが発生します。


> [!NOTE]
> <P>[!メモ] <STRONG>User</STRONG> オブジェクトを <STRONG>Group</STRONG> オブジェクトの <STRONG>Users</STRONG> コレクションに追加する前に、追加するものと同じ <STRONG>Name プロパティ (ADOX)</STRONG> を持つ <A href="name-property-adox.md">User</A> オブジェクトが、あらかじめ <STRONG>Catalog</STRONG> の <STRONG>Users</STRONG> コレクションに存在している必要があります。</P>


