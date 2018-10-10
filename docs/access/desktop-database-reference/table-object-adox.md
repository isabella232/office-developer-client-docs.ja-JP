---
title: Table オブジェクト (ADOX)
TOCTitle: Table Object (ADOX)
ms:assetid: 53a3e2f9-4ec0-8fed-d482-4f995921587b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249273(v=office.15)
ms:contentKeyID: 48544874
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fa7ea75110587dc9c32cfe8c2c6c0c1862243ffa
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477674"
---
# <a name="table-object-adox"></a>Table オブジェクト (ADOX)


**適用されます**Access 2013 |。Office 2013

列、インデックス、およびキーを含むデータベース テーブルを表します。

## <a name="remarks"></a>解説

次のコードによって、新しい **Table** を作成できます。

`Dim obj As New Table`

**Table** オブジェクトのプロパティとコレクションを使用すると、次の操作を実行できます。

  - [Name](name-property-adox.md) プロパティを使用して、テーブルを識別します。

  - [Type](https://msdn.microsoft.com/library/jj250042\(v=office.15\)) プロパティを使用して、テーブルの種類を特定します。

  - [Columns](columns-collection-adox.md) コレクションを使用して、データベース テーブルの列にアクセスします。

  - [Indexes](indexes-collection-adox.md) コレクションを使用して、テーブルのインデックスにアクセスします。

  - [Keys](keys-collection-adox.md) コレクションを使用して、テーブルのキーにアクセスします。

  - [ParentCatalog](catalog-object-adox.md) プロパティを使用して、テーブルを所有する [Catalog](parentcatalog-property-adox.md) を指定します。

  - [DateCreated](datecreated-property-adox.md) プロパティと [DateModified](datemodified-property-adox.md) プロパティを使用して、日付情報を返します。

  - [Properties](properties-collection-ado.md) コレクションを使用して、プロバイダー固有のテーブルのプロパティにアクセスします。


> [!NOTE]
> <P>[!メモ] データ プロバイダーによっては、サポートされない <STRONG>Table</STRONG> オブジェクトのプロパティもあります。プロバイダーがサポートしていないプロパティに値を設定すると、エラーが発生します。新しい <STRONG>Table</STRONG> オブジェクトでは、オブジェクトをコレクションに追加するときにエラーが発生します。既存のオブジェクトでは、プロパティを設定するときにエラーが発生します。</P>



**Table** オブジェクトを作成するときは、オプションのプロパティに適切な既定値が存在する場合でも、プロバイダーがプロパティをサポートしているとは限りません。利用しているプロバイダーがサポートしているプロパティの詳細については、そのプロバイダーのドキュメントを参照してください。

