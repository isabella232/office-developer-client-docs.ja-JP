---
title: Key オブジェクト (ADOX のデスクトップのデータベース参照のアクセス)
TOCTitle: Key Object (ADOX)
ms:assetid: 727198ec-57d2-7766-790c-370beb931de6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249461(v=office.15)
ms:contentKeyID: 48545608
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2edda6dfe7dd9ec28f3eb4cb11714d59806c80e0
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25871361"
---
# <a name="key-object-adox"></a>Key オブジェクト (ADOX)


**適用されます**Access 2013、Office 2013。

データベース テーブルの主キー フィールド、外部キー フィールド、または一意なキー フィールドを表します。

## <a name="remarks"></a>解説

次のコードによって、新しい **Key** を作成できます。

`Dim obj As New Key`

**Key** オブジェクトのプロパティとコレクションを使用すると、次の操作を実行できます。

- [Name](name-property-adox.md) プロパティを使用して、キーを識別します。

- [Type](https://msdn.microsoft.com/library/jj248879\(v=office.15\)) プロパティを使用して、キーが主キー、外部キー、または一意キーのどれであるかを指定します。

- [Columns](columns-collection-adox.md) コレクションを使用して、キーによって指定されたデータベースの列にアクセスします。

- [RelatedTable](relatedtable-property-adox.md) プロパティを使用して、関連テーブルの名前を指定します。

- [DeleteRule](deleterule-property-adox.md) プロパティと [UpdateRule](updaterule-property-adox.md) プロパティを使用して、主キーが削除または更新された場合のアクションを指定します。

