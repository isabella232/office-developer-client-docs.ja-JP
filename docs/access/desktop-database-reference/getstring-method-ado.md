---
title: GetString メソッド (ADO)
TOCTitle: GetString Method (ADO)
ms:assetid: f496305e-a1f5-7014-7808-7e4961e5f0fa
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250242(v=office.15)
ms:contentKeyID: 48548693
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b6c4de1278a093a1b0d4493c5dd994afe6a5d1b8
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879873"
---
# <a name="getstring-method-ado"></a>GetString メソッド (ADO)


**適用されます**Access 2013、Office 2013。


[Recordset](recordset-object-ado.md) を文字列として返します。

## <a name="syntax"></a>構文

*バリアント* = *レコード セット*です。GetString (*StringFormat*、 *NumRows*、 *";"と*、 *RowDelimiter*、 *NullExpr*)

## <a name="return-value"></a>戻り値

**Recordset** を文字列値を持つバリアント型 ( **Variant** )、つまり、BSTR として返します。

## <a name="parameters"></a>パラメーター

  - *StringFormat*

  - **Recordset** を文字列に変換する方法を示す [StringFormatEnum](stringformatenum.md) 値を指定します。*RowDelimiter*、*ColumnDelimiter*、および *NullExpr* パラメーターは、*StringFormat* に **adClipString** を指定した場合にのみ使用できます。

  - *NumRows*

  - 省略可能です。 **Recordset** から変換する行数を指定します。 *NumRows*を指定しない場合、または**レコード セット**内の行の合計数より大きい場合は、**レコード セット**内のすべての行は変換されます。

  - *";"と*

  - 省略可能です。列間に使用する区切り記号を指定し、指定しないとタブ文字が使用されます。

  - *RowDelimiter*

  - 省略可能です。行間に使用する区切り記号を指定し、指定しないとキャリッジ リターン文字が使用されます。

  - *NullExpr*

  - 省略可能です。Null 値の代わりに使用する表現を指定し、指定しないと空文字列が使用されます。

## <a name="remarks"></a>解説

文字列には行データが保存され、スキーマ データは保存されません。したがって、この文字列を使用して **Recordset** を再度開くことはできません。

このメソッドは、RDO の **GetClipString** メソッドと同等です。

