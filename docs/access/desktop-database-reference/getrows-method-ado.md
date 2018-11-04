---
title: GetRows メソッド (ADO)
TOCTitle: GetRows method (ADO)
ms:assetid: 570e6f1c-c17a-7d9a-c172-387894a3a1f1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249292(v=office.15)
ms:contentKeyID: 48544963
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 853f971f68bb0ec4069ba58e04b7cf9d231c6467
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949860"
---
# <a name="getrows-method-ado"></a>GetRows メソッド (ADO)

**適用されます**Access 2013、Office 2013。

[Recordset](recordset-object-ado.md) オブジェクトの複数のレコードを配列に取り込みます。

## <a name="syntax"></a>構文

*配列* = *レコード セット*です。GetRows (*行*を*開始*する*フィールド*)

## <a name="return-value"></a>戻り値

2 次元配列の値を持つバリアント型 ( **Variant** ) を返します。

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*Rows* |省略可能です。取得するレコード数を示す [GetRowsOptionEnum](getrowsoptionenum.md) 値を指定します。既定値は **adGetRowsRest** です。|
|*Start* |省略可能です。 **GetRows** 操作を開始するレコードへのブックマークとして評価される文字列型 ( **String** ) の値またはバリアント型 ( **Variant** ) を指定します。 [BookmarkEnum](bookmarkenum.md) 値を使用することもできます。|
|*Fields* |省略可能です。単一のフィールド名または順序を表す、あるいは複数のフィールド名または順序番号の配列を表す、バリアント型 ( **Variant** ) を指定します。指定したフィールドのデータだけが返されます。|

## <a name="remarks"></a>解説

**GetRows** メソッドでは、 **Recordset** のレコードを 2 次元配列にコピーします。 1 番目の添え字でフィールドを指定し、2 番目の添え字でレコード番号を指定します。 **GetRows**メソッドにはデータが返されるときに、*配列*変数の次元は適切なサイズに自動的が。

*行*の引数の値を指定しないと、 **GetRows**メソッドは、 **Recordset**オブジェクト内のすべてのレコードを自動的に取得します。 要求したレコード数が使用可能なレコード数より多い場合、 **GetRows** は使用可能なレコード数だけを返します。

**Recordset**オブジェクトはブックマークをサポートする場合は、どのレコードを**GetRows**メソッドを開始引数*Start*にレコードの[Bookmark](bookmark-property-ado.md)プロパティの値を渡すことによってデータを取得するを指定できます。

**GetRows**の呼び出しを返すフィールドを制限する場合は、 *Fields*引数に単一のフィールド名または番号またはフィールド名または番号の配列を渡すことができます。

**GetRows** を呼び出すと、まだ読み込まれていない次のレコードがカレント レコードになるか、それ以上レコードがない場合は [EOF](bof-eof-properties-ado.md) プロパティが **True** に設定されます。

