---
title: Index オブジェクト (ADOX)
TOCTitle: Index Object (ADOX)
ms:assetid: fe368ab1-e396-4684-d930-18b0ba58a925
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250304(v=office.15)
ms:contentKeyID: 48548929
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 535ca6a597c6dd580146f6142731897600264526
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477614"
---
# <a name="index-object-adox"></a>Index オブジェクト (ADOX)

**適用されます**Access 2013 |。Office 2013

データベース テーブルのインデックスを表します。

## <a name="remarks"></a>解説

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

