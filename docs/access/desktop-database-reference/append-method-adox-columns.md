---
title: Append メソッド (ADOX Columns)
TOCTitle: Append Method (ADOX Columns)
ms:assetid: e256a478-abc0-f15b-fc29-1b52e354144a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250152(v=office.15)
ms:contentKeyID: 48548285
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ec64241bf63719fe4f5c547d60a93f7804f181ca
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25877661"
---
# <a name="append-method-adox-columns"></a>Append メソッド (ADOX Columns)


**適用されます**Access 2013、Office 2013。

新しい [Column](column-object-adox.md) オブジェクトを [Columns](columns-collection-adox.md) コレクションに追加します。

## <a name="syntax"></a>構文

*列*です。 *列*を追加する\[、*タイプ*\] \[、*DefinedSize*\]

## <a name="parameters"></a>パラメーター

  - *Column*

  - 追加する **Column** オブジェクトを指定します。または、新たに作成して追加する列の名前を指定します。

  - *Type*

  - 省略可能です。 列のデータ型を指定する長整数型 ( **Long** ) の値を指定します。 *型*パラメーターは、**列**オブジェクトの[Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\))プロパティに対応します。

  - *DefinedSize*

  - 省略可能です。 列のサイズを指定する長整数型 ( **Long** ) の値を指定します。 *DefinedSize*パラメーターは、**列**オブジェクトの[DefinedSize](definedsize-property-adox.md)プロパティに対応します。


> [!NOTE]
> [!メモ] **Column** を **Index** の [Columns](index-object-adox.md) コレクションに追加するときに、 **Tables** コレクションに既に追加されている [Table](table-object-adox.md) にまだ [Column](tables-collection-adox.md) が存在していない場合は、エラーが発生します。


