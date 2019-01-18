---
title: Columns コレクション (ADOX)
TOCTitle: Columns collection (ADOX)
ms:assetid: 231645db-70da-9ad1-fb27-02145ce32e66
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249008(v=office.15)
ms:contentKeyID: 48543723
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c1827fe11696e28871bdd03594ff0d7057c377dc
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720486"
---
# <a name="columns-collection-adox"></a>Columns コレクション (ADOX)


**適用されます**Access 2013、Office 2013。

テーブル、インデックス、またはキーのすべての [Column](column-object-adox.md) オブジェクトを含みます。

## <a name="remarks"></a>解説

[Columns](append-method-adox-columns.md) コレクションの **Append** メソッドは、ADOX に対して一意です。次のことができます。

  - **Append** メソッドを使用して、新しい列をコレクションに追加します。

残りのプロパティとメソッドは、ADO コレクションに標準で装備されています。次のことができます。

  - [Item](item-property-ado.md) プロパティを使用して、コレクションの列にアクセスします。

  - [Count](count-property-ado.md) プロパティを使用して、コレクションに含まれる列の数を返します。

  - [Delete](delete-method-adox-collections.md) メソッドを使用して、コレクションから列を削除します。

  - [Refresh](refresh-method-ado.md) メソッドを使用して、コレクションのオブジェクトを更新し、カレント データベースのスキーマを反映します。


> [!NOTE]
> [!メモ] **Column** を **Index** の [Columns](index-object-adox.md) コレクションに追加するときに、 **Tables** コレクションに既に追加されている [Table](table-object-adox.md) にまだ [Column](tables-collection-adox.md) が存在していない場合は、エラーが発生します。


