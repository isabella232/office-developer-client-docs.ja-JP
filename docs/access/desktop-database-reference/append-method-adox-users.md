---
title: Append メソッド (ADOX Users)
TOCTitle: Append Method (ADOX Users)
ms:assetid: b7a1128b-c6e7-2071-c914-913b6bd245ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249884(v=office.15)
ms:contentKeyID: 48547302
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dc8f7a2d217a25a8404765aa05bae19fdccad2c3
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863865"
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
> [!メモ] **User** オブジェクトを **Group** オブジェクトの **Users** コレクションに追加する前に、追加するものと同じ **Name プロパティ (ADOX)** を持つ [User](name-property-adox.md) オブジェクトが、あらかじめ **Catalog** の **Users** コレクションに存在している必要があります。


