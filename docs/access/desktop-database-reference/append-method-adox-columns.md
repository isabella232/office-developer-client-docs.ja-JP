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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297124"
---
# <a name="append-method-adox-columns"></a>Append メソッド (ADOX Columns)

**適用先:** Access 2013、Office 2013

新しい [Column](column-object-adox.md) オブジェクトを [Columns](columns-collection-adox.md) コレクションに追加します。

## <a name="syntax"></a>構文

*列*。 *列* \[、*型*\] ** 、および未定義のサイズを追加する\[\]

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*Column* |追加する **Column** オブジェクトを指定します。または、新たに作成して追加する列の名前を指定します。|
|*Type* |省略可能です。列のデータ型を指定する長整数型 (**Long**) の値を指定します。*Type* パラメーターは、**Column** オブジェクトの [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) プロパティに対応します。|
|*DefinedSize* |省略可能です。 列のサイズを指定する長整数型 (**Long**) の値を指定します。 *DefinedSize* パラメーターは、**Column** オブジェクトの [DefinedSize](definedsize-property-adox.md) プロパティに対応します。|


> [!NOTE]
> **Column** を [Index](index-object-adox.md) の **Columns** コレクションに追加するときに、[Tables](tables-collection-adox.md) コレクションに既に追加されている [Table](table-object-adox.md) にまだ **Column** が存在していない場合は、エラーが発生します。


