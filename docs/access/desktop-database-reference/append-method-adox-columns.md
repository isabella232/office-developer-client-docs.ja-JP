---
title: Append メソッド (ADOX Columns)
TOCTitle: Append method (ADOX Columns)
ms:assetid: e256a478-abc0-f15b-fc29-1b52e354144a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250152(v=office.15)
ms:contentKeyID: 48548285
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 48bc100b7b56265a570ce963b80f569f1d827150
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711232"
---
# <a name="append-method-adox-columns"></a>Append メソッド (ADOX Columns)

**適用されます**Access 2013、Office 2013。

新しい [Column](column-object-adox.md) オブジェクトを [Columns](columns-collection-adox.md) コレクションに追加します。

## <a name="syntax"></a>構文

*列*です。 *列*を追加する\[、*タイプ*\] \[、*DefinedSize*\]

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*Column* |追加する **Column** オブジェクトを指定します。または、新たに作成して追加する列の名前を指定します。|
|*Type* |省略可能です。 列のデータ型を指定する長整数型 ( **Long** ) の値を指定します。 *型*パラメーターは、**列**オブジェクトの[Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox)プロパティに対応します。|
|*DefinedSize* |省略可能です。 列のサイズを指定する長整数型 ( **Long** ) の値を指定します。 *DefinedSize*パラメーターは、**列**オブジェクトの[DefinedSize](definedsize-property-adox.md)プロパティに対応します。|


> [!NOTE]
> [!メモ] **Column** を **Index** の [Columns](index-object-adox.md) コレクションに追加するときに、 **Tables** コレクションに既に追加されている [Table](table-object-adox.md) にまだ [Column](tables-collection-adox.md) が存在していない場合は、エラーが発生します。


