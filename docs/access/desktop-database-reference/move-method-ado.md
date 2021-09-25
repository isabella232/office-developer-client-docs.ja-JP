---
title: Move メソッド - ActiveX データ オブジェクト (ADO)
TOCTitle: Move method (ADO)
ms:assetid: 1f858654-5fa3-273d-7cdc-574c5f09a420
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248982(v=office.15)
ms:contentKeyID: 48543645
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 003c60e021ab773e4540af4739f5cf260048b63b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59606563"
---
# <a name="move-method-ado"></a>Move メソッド (ADO)

**適用先**: Access 2013、Office 2013

[Recordset](recordset-object-ado.md) オブジェクトでカレント レコードの位置を移動します。

## <a name="syntax"></a>構文

*recordset*.Move *NumRecords*, *Start*

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*NumRecords* |カレント レコードの位置を移動するレコード数を指定する、符号付きの長整数型 ( **Long** ) の式を指定します。|
|*Start* |省略可能です。ブックマークとして評価される文字列型 ( **String** ) の値またはバリアント型 ( **Variant** ) を指定します。 [BookmarkEnum](bookmarkenum.md) 値を使用することもできます。|

## <a name="remarks"></a>注釈

**Move** メソッドは、すべての **Recordset** オブジェクトでサポートされています。

*NumRecords* 引数がゼロより大きい場合、現在のレコードの位置は前方 (**Recordset** の末尾方向) に移動します。*NumRecords* がゼロより小さい場合、現在のレコードの位置は後方 (**Recordset** の先頭方向) に移動します。

Move 呼び **出** しで現在のレコード位置を最初のレコードの前の位置に移動する場合、ADO はレコードセットの最初のレコードの前の位置に現在のレコードを設定します [(BOF](bof-eof-properties-ado.md)は **True)。** **BOF** プロパティが既に **True** の場合、後方へ移動しようとすると、エラーが発生します。

**Move** メソッドを呼び出してカレント レコードの位置を最後のレコードの後に移動しようとすると、カレント レコードがレコードセットの最後のレコードの後に設定され、[EOF](bof-eof-properties-ado.md) が **True** になります。**EOF** プロパティが既に **True** の場合、前方へ移動しようとすると、エラーが発生します。

空の **Recordset** オブジェクトから **Move** メソッドを呼び出すと、エラーが発生します。

*Start* 引数を指定した場合、**Recordset** オブジェクトではブックマークがサポートされていると見なされ、このブックマークを持つレコードが移動の基準となります。指定しない場合は、カレント レコードが移動の基準となります。

[CacheSize](cachesize-property-ado.md) プロパティを使用してプロバイダーからのレコードをローカルにキャッシュしている場合、*NumRecords* 引数を渡して、現在キャッシュされているレコード グループの範囲外に現在のレコード位置を移動すると、移動先のレコードから始まる新規レコード グループが強制的に取得されます。**CacheSize** プロパティが、新規に取得されるグループのサイズを決定し、移動先のレコードが最初に取得されるレコードになります。

**Recordset** オブジェクトが前方スクロールのみ可能な場合でも、移動先が現在キャッシュされているレコードセットの範囲内であれば、*NumRecords* 引数に 0 より小さい値を指定できます。**Move** メソッドを呼び出して、カレント レコードの位置を、キャッシュされている最初のレコードより前のレコードに移動しようとすると、エラーが発生します。このように、前方スクロールのみをサポートするプロバイダーで、完全スクロールをサポートするレコード キャッシュを使用することができます。キャッシュされたレコードはメモリに読み込まれるため、必要以上のレコードのキャッシュは避けてください。前方スクロールのみ可能な **Recordset** オブジェクトでも、この方法で後方への移動をサポートできますが、前方スクロールのみ可能な **Recordset** オブジェクトで [MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) メソッドを呼び出すと、エラーが発生します。


> [!NOTE]
> [!メモ] 前方スクロールのみ可能な **Recordset** で後方への移動がサポートされているかどうかは、プロバイダーによります。カレント レコードが **Recordset** の最後のレコードの後にある場合、後方への **Move** を実行しても現在の位置が正しく示されないことがあります。


