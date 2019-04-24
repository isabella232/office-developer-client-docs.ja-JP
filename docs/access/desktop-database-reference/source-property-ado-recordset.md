---
title: Source プロパティ (ADO Recordset)
TOCTitle: Source property (ADO Recordset)
ms:assetid: 523ea81e-d011-8d87-436e-084b6eba0908
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249269(v=office.15)
ms:contentKeyID: 48544843
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 26f41181f1233931f24ff091b3009dfa7a5d6ff3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306413"
---
# <a name="source-property-ado-recordset"></a>Source プロパティ (ADO Recordset)


**適用先:** Access 2013、Office 2013

[Recordset](recordset-object-ado.md) オブジェクトのデータ ソースを示します。

## <a name="settings-and-return-values"></a>設定値と戻り値

文字列型 (**String**) の値または [Command](command-object-ado.md) オブジェクトへの参照を設定し、**Recordset** のソースを示す文字列型 (**String**) の値のみを返します。

## <a name="remarks"></a>注釈

**Command** オブジェクト変数、SQL ステートメント、ストアド プロシージャ、またはテーブル名のいずれかを使用して、**Recordset** オブジェクトのデータ ソースを指定するには、**Source** プロパティを使用します。

**Source** プロパティを **Command** オブジェクトに設定した場合、 [Recordset](activeconnection-property-ado.md) オブジェクトの **ActiveConnection** プロパティは、指定した **Command** オブジェクトの **ActiveConnection** プロパティの値を継承します。ただし、 **Source** プロパティの値を取得しても **Command** オブジェクトは返されず、代わりに [Source](commandtext-property-ado.md) プロパティで設定した **Command** オブジェクトの **CommandText** プロパティが返されます。

**Source** プロパティが SQL ステートメント、ストアド プロシージャ、またはテーブル名である場合、[Open](open-method-ado-recordset.md) メソッドの呼び出しで適切な *Options* 引数を渡すことによって、パフォーマンスを最適化できます。

**Source** プロパティは、**Recordset** オブジェクトが閉じている場合は値の取得および設定が可能で、**Recordset** オブジェクトが開いている場合は値の取得のみ可能です。

