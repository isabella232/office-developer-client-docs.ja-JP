---
title: Find メソッド - ActiveX データ オブジェクト (ADO)
TOCTitle: Find method (ADO)
ms:assetid: a7cc9ceb-fdb9-73e2-8328-70b174f93cda
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249776(v=office.15)
ms:contentKeyID: 48546887
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: f1ba79981e59ad18bad6be2046a020b32dd2101c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59602543"
---
# <a name="find-method-ado"></a>Find メソッド (ADO)

**適用先**: Access 2013、Office 2013

[Recordset](recordset-object-ado.md) から、指定した条件を満たす行を検索します。必要に応じて、検索の方向、開始行、および開始行からのオフセットを指定できます。条件が一致すると、カレント行の位置は、検出されたレコードに設定され、条件を満たす行がない場合は、 **Recordset** の最後 (または最初) に設定されます。

## <a name="syntax"></a>構文

Find (*Criteria*, *SkipRows*, *SearchDirection*, *Start*)

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*基準* |検索に使用する列の名前、比較演算子、および値を指定するステートメントを含む文字列型 ( **String** ) の値を指定します。|
|*SkipRows* |オプション。 現在 **の行** からの行オフセットまたは検索を開始するブックマークの開始を指定する、既定値が 0 の長い値。  By default, the search will start on the current row.|
|*SearchDirection* |オプション。 A [SearchDirectionEnum](searchdirectionenum.md) value that specifies whether the search should begin on the current row or the next available row in the direction of the search. An unsuccessful search stops at the end of the **Recordset** if the value is **adSearchForward**. An unsuccessful search stops at the start of the **Recordset** if the value is **adSearchBackward**.|
|*Start* |省略可能です。検索の開始位置として使用する、バリアント型 ( **Variant** ) のブックマークを指定します。|

## <a name="remarks"></a>注釈

*criteria* には、列の名前を 1 つだけ指定できます。このメソッドでは、複数列の検索はサポートしていません。

*Criteria* の比較演算子には、" (より大きい)、"** =" (以上)、" (等しくない)、または **\>** \<**" (less than), "=" (equal), "\> \<=" (less than or equal), "\<\> "like" (パターンマッチング) を指定できます。

Criteria の *値には* 、文字列、浮動小数点数、または日付を指定できます。 文字列値は、単一引用符または " \# (番号記号) マーク ("state = 'WA'" や "state = WA ") で区切 \# \# ります。 日付の値は "" (数値記号) で区切られたマーク (たとえば、"開始日 \# \_ \> \# 7/22/97") で区切り、タイム スタンプを示すために時間、分、秒を含めることができますが、ミリ秒単位を含めず、エラーが発生します。 \#

比較演算子に "like"を使用する場合、文字列値にアスタリスク (\*) を含めると、1 つまたは複数の文字、または部分文字列を検索することができます。たとえば、「state like 'M\*'」と指定すると、Maine や Massachusetts が該当します。また、文字列の先頭と末尾にアスタリスクを使用して、その間に含まれる部分文字列を検索対象として指定することもできます。たとえば、「state like '\*as\*'」と指定すると、Alaska、Arkansas、および Massachusetts が該当します。

上の例のように、アスタリスクは、検索文字列の末尾のみに使用するか、または検索文字列の先頭と末尾の両方で使用することができます。ただし、先頭のみのワイルドカード ('\*str') または文字列中のワイルドカード ('s\*r') としてアスタリスクを使用することはできません。この場合はエラーが発生します。

> [!NOTE]
> [!メモ] **Find** メソッドを呼び出す前にカレント行の位置が設定されていない場合は、エラーが発生します。 [Find](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) メソッドを呼び出す前に、 **MoveFirst** などの、行の位置を設定するメソッドを呼び出す必要があります。

> [!NOTE]
> [!メモ] レコードセットに対して **Find** メソッドを呼び出す場合で、レコードセット内の現在の位置が最後のレコードまたはファイルの最後 (EOF) の場合、何も検索されません。あらかじめ **MoveFirst** メソッドを呼び出して、現在の位置またはカーソルをレコードセットの先頭に設定する必要があります。


