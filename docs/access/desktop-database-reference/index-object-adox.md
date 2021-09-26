---
title: Index オブジェクト (ADOX)
TOCTitle: Index object (ADOX)
ms:assetid: fe368ab1-e396-4684-d930-18b0ba58a925
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250304(v=office.15)
ms:contentKeyID: 48548929
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 4044e6a65f07671a855492539ef4d1c8833ce374
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59612030"
---
# <a name="index-object-adox"></a>Index オブジェクト (ADOX)

**適用先**: Access 2013、Office 2013

データベース テーブルのインデックスを表します。

## <a name="remarks"></a>注釈

次のコードによって、新しい **Index** を作成できます。

`Dim obj As New Index`

**Index** オブジェクトのプロパティとコレクションを使用すると、次の操作を実行できます。

- [Name](name-property-adox.md) プロパティを使用して、インデックスを識別します。

- [Columns](columns-collection-adox.md) コレクションを使用して、インデックスによって指定されたデータベースの列にアクセスします。

- [Unique](unique-property-adox.md) プロパティを使用して、インデックス キーを一意にする必要があるかどうかを指定します。

- [PrimaryKey](primarykey-property-adox.md) プロパティを使用して、インデックスがテーブルの主キーかどうかを指定します。

- [IndexNulls](indexnulls-property-adox.md) プロパティを使用して、インデックス フィールドが Null 値のレコードがインデックス エントリを持っているかどうかを指定します。

- [Clustered](clustered-property-adox.md) プロパティを使用して、インデックスがクラスター化されているかどうかを指定します。

- [Properties](properties-collection-ado.md) コレクションを使用して、プロバイダー固有のインデックスのプロパティにアクセスします。


> [!NOTE]
> [!メモ] [Column](column-object-adox.md) を **Index** の **Columns** コレクションに追加するときに、 **Tables** コレクションに既に追加されている [Table](table-object-adox.md) オブジェクトに [Column](tables-collection-adox.md) が存在していない場合は、エラーが発生します。

データ プロバイダーによっては、サポートされない **Index** オブジェクトのプロパティもあります。プロバイダーがサポートしていないプロパティに値を設定すると、エラーが発生します。新しい **Index** オブジェクトでは、オブジェクトをコレクションに追加するときにエラーが発生します。既存のオブジェクトでは、プロパティを設定するときにエラーが発生します。

**Index** オブジェクトを作成するときは、オプションのプロパティに適切な既定値が存在する場合でも、プロバイダーがプロパティをサポートしているとは限りません。利用しているプロバイダーがサポートしているプロパティの詳細については、そのプロバイダーのドキュメントを参照してください。

