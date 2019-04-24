---
title: GetRows メソッド (ADO)
TOCTitle: GetRows method (ADO)
ms:assetid: 570e6f1c-c17a-7d9a-c172-387894a3a1f1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249292(v=office.15)
ms:contentKeyID: 48544963
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 61f7ce441eb837b76e824b55393741e0cf821bb5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292224"
---
# <a name="getrows-method-ado"></a>GetRows メソッド (ADO)

**適用先:** Access 2013、Office 2013

[Recordset](recordset-object-ado.md) オブジェクトの複数のレコードを配列に取り込みます。

## <a name="syntax"></a>構文

*配列* = *recordset*。GetRows (*行*、*開始*、*フィールド*)

## <a name="return-value"></a>戻り値

2 次元配列の値を持つバリアント型 (**Variant**) を返します。

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*Rows* |省略可能です。取得するレコード数を示す [GetRowsOptionEnum](getrowsoptionenum.md) 値を指定します。既定値は **adGetRowsRest** です。|
|*Start* |省略可能です。 **GetRows** 操作を開始するレコードへのブックマークとして評価される文字列型 ( **String** ) の値またはバリアント型 ( **Variant** ) を指定します。 [BookmarkEnum](bookmarkenum.md) 値を使用することもできます。|
|*Fields* |省略可能です。単一のフィールド名または順序を表す、あるいは複数のフィールド名または順序番号の配列を表す、バリアント型 ( **Variant** ) を指定します。指定したフィールドのデータだけが返されます。|

## <a name="remarks"></a>注釈

**GetRows** メソッドでは、**Recordset** のレコードを 2 次元配列にコピーします。1 番目の添え字でフィールドを指定し、2 番目の添え字でレコード番号を指定します。**GetRows** メソッドからデータが返されると、*array* 変数は自動的に適切なサイズに調整されます。

*Rows* 引数の値を指定しないと、**GetRows** メソッドは **Recordset** オブジェクトのすべてのレコードを自動的に取得します。要求したレコード数が使用可能なレコード数より多い場合、**GetRows** は使用可能なレコード数だけを返します。

**Recordset** オブジェクトがブックマークをサポートしている場合は、*Start* 引数にレコードの [Bookmark](bookmark-property-ado.md) プロパティの値を渡して、**GetRows** メソッドの取得開始レコードを指定できます。

**GetRows** の呼び出しで返されるフィールドを制限するには、*Fields* 引数に単一のフィールド名または番号、あるいは複数のフィールド名または番号の配列を渡します。

**GetRows** を呼び出すと、まだ読み込まれていない次のレコードがカレント レコードになるか、それ以上レコードがない場合は [EOF](bof-eof-properties-ado.md) プロパティが **True** に設定されます。

