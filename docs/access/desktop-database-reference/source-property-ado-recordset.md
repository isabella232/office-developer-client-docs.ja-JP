---
title: Source プロパティ (ADO Recordset)
TOCTitle: Source Property (ADO Recordset)
ms:assetid: 523ea81e-d011-8d87-436e-084b6eba0908
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249269(v=office.15)
ms:contentKeyID: 48544843
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: db44459bf3629f6cedfbee023b0be9161ed3bb14
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/17/2018
ms.locfileid: "25605262"
---
# <a name="source-property-ado-recordset"></a>Source プロパティ (ADO Recordset)


**適用されます**Access 2013 |。Office 2013

[Recordset](recordset-object-ado.md) オブジェクトのデータ ソースを示します。

<<<<<<< ヘッド
## <a name="settings-and-return-values"></a>設定値と戻り値
=======
## <a name="settings-and-return-values"></a>設定値および戻り値
>>>>>>> master

文字列型 ( **String** ) の値または [Command](command-object-ado.md) オブジェクトへの参照を設定し、 **Recordset** のソースを示す文字列型 ( **String** ) の値のみを返します。

## <a name="remarks"></a>解説

**Command** オブジェクト変数、SQL ステートメント、ストアド プロシージャ、またはテーブル名のいずれかを使用して、 **Recordset** オブジェクトのデータ ソースを指定するには、 **Source** プロパティを使用します。

**Source** プロパティを **Command** オブジェクトに設定した場合、 [Recordset](activeconnection-property-ado.md) オブジェクトの **ActiveConnection** プロパティは、指定した **Command** オブジェクトの **ActiveConnection** プロパティの値を継承します。ただし、 **Source** プロパティの値を取得しても **Command** オブジェクトは返されず、代わりに [Source](commandtext-property-ado.md) プロパティで設定した **Command** オブジェクトの **CommandText** プロパティが返されます。

**Source**プロパティが、SQL ステートメント、ストアド プロシージャ、またはテーブル名の場合は、 [Open](open-method-ado-recordset.md)メソッドの呼び出しで適切な*Options*引数を渡すことによってパフォーマンスを最適化できます。

**Source** プロパティは、 **Recordset** オブジェクトが閉じている場合は値の取得および設定が可能で、 **Recordset** オブジェクトが開いている場合は値の取得のみ可能です。

