---
title: Append メソッド (ADOX Columns)
TOCTitle: Append method (ADOX Columns)
ms:assetid: e256a478-abc0-f15b-fc29-1b52e354144a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250152(v=office.15)
ms:contentKeyID: 48548285
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 2827fa16ce33903b7e220797ea51d4098b866e7a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559046"
---
# <a name="append-method-adox-columns"></a>Append メソッド (ADOX Columns)

**適用先:** Access 2013、Office 2013

新しい [Column](column-object-adox.md) オブジェクトを [Columns](columns-collection-adox.md) コレクションに追加します。

## <a name="syntax"></a>構文

*列*. Append *Column* \[ ,*Type* \] \[ ,*DefinedSize*\]

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*Column* |追加する **Column** オブジェクトを指定します。または、新たに作成して追加する列の名前を指定します。|
|*Type* |省略可能です。列のデータ型を指定する長整数型 (**Long**) の値を指定します。*Type* パラメーターは、**Column** オブジェクトの [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) プロパティに対応します。|
|*DefinedSize* |省略可能です。列のサイズを指定する長整数型 (**Long**) の値を指定します。*DefinedSize* パラメーターは、**Column** オブジェクトの [DefinedSize](definedsize-property-adox.md) プロパティに対応します。|


> [!NOTE]
> [!メモ] **Column** を **Index** の [Columns](index-object-adox.md) コレクションに追加するときに、 **Tables** コレクションに既に追加されている [Table](table-object-adox.md) にまだ [Column](tables-collection-adox.md) が存在していない場合は、エラーが発生します。


