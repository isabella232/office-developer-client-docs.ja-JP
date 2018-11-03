---
title: Source プロパティ (ADO Recordset)
TOCTitle: Source property (ADO Recordset)
ms:assetid: 523ea81e-d011-8d87-436e-084b6eba0908
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249269(v=office.15)
ms:contentKeyID: 48544843
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a58ac3c5315daef040ba6a999753a19f76504087
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947572"
---
# <a name="source-property-ado-recordset"></a>Source プロパティ (ADO Recordset)


**適用されます**Access 2013、Office 2013。

[Recordset](recordset-object-ado.md) オブジェクトのデータ ソースを示します。

## <a name="settings-and-return-values"></a>設定値および戻り値

文字列型 ( **String** ) の値または [Command](command-object-ado.md) オブジェクトへの参照を設定し、 **Recordset** のソースを示す文字列型 ( **String** ) の値のみを返します。

## <a name="remarks"></a>解説

**Command** オブジェクト変数、SQL ステートメント、ストアド プロシージャ、またはテーブル名のいずれかを使用して、 **Recordset** オブジェクトのデータ ソースを指定するには、 **Source** プロパティを使用します。

**Source** プロパティを **Command** オブジェクトに設定した場合、 [Recordset](activeconnection-property-ado.md) オブジェクトの **ActiveConnection** プロパティは、指定した **Command** オブジェクトの **ActiveConnection** プロパティの値を継承します。ただし、 **Source** プロパティの値を取得しても **Command** オブジェクトは返されず、代わりに [Source](commandtext-property-ado.md) プロパティで設定した **Command** オブジェクトの **CommandText** プロパティが返されます。

**Source**プロパティが、SQL ステートメント、ストアド プロシージャ、またはテーブル名の場合は、 [Open](open-method-ado-recordset.md)メソッドの呼び出しで適切な*Options*引数を渡すことによってパフォーマンスを最適化できます。

**Source** プロパティは、 **Recordset** オブジェクトが閉じている場合は値の取得および設定が可能で、 **Recordset** オブジェクトが開いている場合は値の取得のみ可能です。

