---
title: Columns コレクション (ADOX)
TOCTitle: Columns collection (ADOX)
ms:assetid: 231645db-70da-9ad1-fb27-02145ce32e66
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249008(v=office.15)
ms:contentKeyID: 48543723
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 4c06199be9f5d5145e4fe205a3f42a91cd39f717
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59612331"
---
# <a name="columns-collection-adox"></a>Columns コレクション (ADOX)


**適用先**: Access 2013、Office 2013

テーブル、インデックス、またはキーのすべての [Column](column-object-adox.md) オブジェクトを含みます。

## <a name="remarks"></a>注釈

[Columns](append-method-adox-columns.md) コレクションの **Append** メソッドは、ADOX に対して一意です。次のことができます。

  - **Append** メソッドを使用して、新しい列をコレクションに追加します。

残りのプロパティとメソッドは、ADO コレクションに標準で装備されています。次のことができます。

  - [Item](item-property-ado.md) プロパティを使用して、コレクションの列にアクセスします。

  - [Count](count-property-ado.md) プロパティを使用して、コレクションに含まれる列の数を返します。

  - [Delete](delete-method-adox-collections.md) メソッドを使用して、コレクションから列を削除します。

  - [Refresh](refresh-method-ado.md) メソッドを使用して、コレクションのオブジェクトを更新し、カレント データベースのスキーマを反映します。


> [!NOTE]
> [!メモ] **Column** を **Index** の [Columns](index-object-adox.md) コレクションに追加するときに、 **Tables** コレクションに既に追加されている [Table](table-object-adox.md) にまだ [Column](tables-collection-adox.md) が存在していない場合は、エラーが発生します。


