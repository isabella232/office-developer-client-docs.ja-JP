---
title: Key オブジェクト (ADOX のデスクトップのデータベース参照のアクセス)
TOCTitle: Key Object (ADOX)
ms:assetid: 727198ec-57d2-7766-790c-370beb931de6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249461(v=office.15)
ms:contentKeyID: 48545608
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c77e45f52994f14d79acf424da14b55b2cdd9814
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479714"
---
# <a name="key-object-adox"></a>Key オブジェクト (ADOX)


**適用されます**Access 2013 |。Office 2013

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

