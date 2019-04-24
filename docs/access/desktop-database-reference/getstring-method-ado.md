---
title: GetString メソッド (ADO)
TOCTitle: GetString method (ADO)
ms:assetid: f496305e-a1f5-7014-7808-7e4961e5f0fa
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250242(v=office.15)
ms:contentKeyID: 48548693
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4ea28efb8fdeaa0643d1d940419b7650527ddf6e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292189"
---
# <a name="getstring-method-ado"></a>GetString メソッド (ADO)

**適用先:** Access 2013、Office 2013

[Recordset](recordset-object-ado.md) を文字列として返します。

## <a name="syntax"></a>構文

*バリアント型 (Variant* = ) の*recordset*。GetString (*StringFormat*、 *numrows*、 *columndelimiter*、 *rowdelimiter*、 *nullexpr*)

## <a name="return-value"></a>戻り値

**Recordset** を文字列値を持つバリアント型 (**Variant**)、つまり、BSTR として返します。

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*StringFormat* |**Recordset** を文字列に変換する方法を示す [StringFormatEnum](stringformatenum.md) 値を指定します。*RowDelimiter*、*ColumnDelimiter*、および *NullExpr* パラメーターは、*StringFormat* に **adClipString** を指定した場合にのみ使用できます。|
|*NumRows* |省略可能です。**Recordset** から変換する行数を指定します。*NumRows* を指定しない場合、または **Recordset** の行の総数より大きい値を指定した場合は、**Recordset** のすべての行が変換されます。|
|*columndelimiter* |省略可能です。列間に使用する区切り記号を指定し、指定しないとタブ文字が使用されます。|
|*rowdelimiter* |省略可能です。行間に使用する区切り記号を指定し、指定しないとキャリッジ リターン文字が使用されます。|
|*nullexpr* |省略可能です。Null 値の代わりに使用する表現を指定し、指定しないと空文字列が使用されます。|

## <a name="remarks"></a>注釈

文字列には行データが保存され、スキーマ データは保存されません。したがって、この文字列を使用して **Recordset** を再度開くことはできません。

このメソッドは、RDO の **GetClipString** メソッドと同等です。

