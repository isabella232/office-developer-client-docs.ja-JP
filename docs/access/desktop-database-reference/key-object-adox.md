---
title: Key Object (ADOX - Access desktop database reference)
TOCTitle: Key object (ADOX)
ms:assetid: 727198ec-57d2-7766-790c-370beb931de6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249461(v=office.15)
ms:contentKeyID: 48545608
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 2c230b6ae88cbdfe1e39e4d2c19ad1a64a86283b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59626359"
---
# <a name="key-object-adox"></a>キー オブジェクト (ADOX)


**適用先**: Access 2013、Office 2013

データベース テーブルの主キー フィールド、外部キー フィールド、または一意なキー フィールドを表します。

## <a name="remarks"></a>注釈

次のコードによって、新しい **Key** を作成できます。

`Dim obj As New Key`

**Key** オブジェクトのプロパティとコレクションを使用すると、次の操作を実行できます。

- [Name](name-property-adox.md) プロパティを使用して、キーを識別します。

- [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-keyadox) プロパティを使用して、キーが主キー、外部キー、または一意キーのどれであるかを指定します。

- [Columns](columns-collection-adox.md) コレクションを使用して、キーによって指定されたデータベースの列にアクセスします。

- [RelatedTable](relatedtable-property-adox.md) プロパティを使用して、関連テーブルの名前を指定します。

- [DeleteRule](deleterule-property-adox.md) プロパティと [UpdateRule](updaterule-property-adox.md) プロパティを使用して、主キーが削除または更新された場合のアクションを指定します。

