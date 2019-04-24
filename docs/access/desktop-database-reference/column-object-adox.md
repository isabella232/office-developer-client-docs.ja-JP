---
title: Column オブジェクト (ADOX)
TOCTitle: Column object (ADOX)
ms:assetid: ad38c2df-f704-0599-4b7a-8556e430ba46
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249811(v=office.15)
ms:contentKeyID: 48547034
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 188f70d32237385cd82979589aecb989f18748b0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296249"
---
# <a name="column-object-adox"></a>Column オブジェクト (ADOX)


**適用先:** Access 2013、Office 2013

テーブル、インデックス、またはキーの列を表します。

## <a name="remarks"></a>注釈

次のコードによって、新しい **Column** を作成できます。

`Dim obj As New Column`

**Column** オブジェクトのプロパティとコレクションを使用すると、次の操作を実行できます。

  - [Name](name-property-adox.md) プロパティを使用して、列を識別します。

  - [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) プロパティを使用して、列のデータ型を指定します。

  - [Attributes](attributes-property-adox.md) プロパティを使用して、列が固定長かどうか、または Null 値を含めることができるかどうかを特定します。

  - [DefinedSize](definedsize-property-adox.md) プロパティを使用して、列の最大サイズを指定します。

  - 数値型データに対しては、[NumericScale](numericscale-property-adox.md) プロパティを使用して、小数部の桁数を指定します。

  - 数値型データに対しては、[Precision](precision-property-adox.md) プロパティを使用して、最大有効桁数を指定します。

  - [ParentCatalog](catalog-object-adox.md) プロパティを使用して、列を所有する [Catalog](parentcatalog-property-adox.md) を指定します。

  - キー列では、[RelatedColumn](relatedcolumn-property-adox.md) プロパティを使用して、関連テーブルの関連する列の名前を指定します。

  - インデックス列では、[SortOrder](sortorder-property-adox.md) プロパティを使用して、並べ替え順序 (昇順または降順) を指定します。

  - [Properties](properties-collection-ado.md) コレクションを使用して、プロバイダー固有のプロパティにアクセスします。


> [!NOTE]
> [!メモ] データ プロバイダーによっては、サポートされない **Column** オブジェクトのプロパティもあります。プロバイダーがサポートしていないプロパティに値を設定すると、エラーが発生します。新しい **Column** オブジェクトでは、オブジェクトをコレクションに追加するときにエラーが発生します。既存のオブジェクトでは、プロパティを設定するときにエラーが発生します。
> 
> **Column** オブジェクトを作成するときは、オプションのプロパティに適切な既定値が存在する場合でも、プロバイダーがプロパティをサポートしているとは限りません。利用しているプロバイダーがサポートしているプロパティの詳細については、そのプロバイダーのドキュメントを参照してください。

