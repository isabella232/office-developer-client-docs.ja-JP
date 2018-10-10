---
title: メソッドを ActiveX データ オブジェクト (ADO) の移動します。
TOCTitle: Move Method (ADO)
ms:assetid: 1f858654-5fa3-273d-7cdc-574c5f09a420
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248982(v=office.15)
ms:contentKeyID: 48543645
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 88787d1f76f84db13feea4bac0e8febd2db1e473
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477093"
---
# <a name="move-method-ado"></a>Move メソッド (ADO)


**適用されます**Access 2013 |。Office 2013



[Recordset](recordset-object-ado.md) オブジェクトでカレント レコードの位置を移動します。

## <a name="syntax"></a>構文

*レコード セット*です。*NumRecords*、*起動*に移動します。

## <a name="parameters"></a>パラメーター

  - *NumRecords*

  - カレント レコードの位置を移動するレコード数を指定する、符号付きの長整数型 ( **Long** ) の式を指定します。

  - *Start*

  - 省略可能です。ブックマークとして評価される文字列型 ( **String** ) の値またはバリアント型 ( **Variant** ) を指定します。 [BookmarkEnum](bookmarkenum.md) 値を使用することもできます。

## <a name="remarks"></a>解説

**Move** メソッドは、すべての **Recordset** オブジェクトでサポートされています。

*NumRecords* 引数がゼロより大きい場合、現在のレコードの位置は前方 (**Recordset** の末尾方向) に移動します。*NumRecords* がゼロより小さい場合、現在のレコードの位置は後方 (**Recordset** の先頭方向) に移動します。

**Move**メソッドを呼び出しては、最初のレコードよりも前にカレント レコードの位置を移動すると、現在のレコードに設定 (されます[BOF](bof-eof-properties-ado.md)が**True**になる)、レコード セットの最初のレコードより前に位置します。 **BOF** プロパティが既に **True** の場合、後方へ移動しようとすると、エラーが発生します。

**Move**メソッドを呼び出しては、最後のレコードの後のポイントにカレント レコードの位置を移動に設定され、現在のレコード位置 ([EOF](bof-eof-properties-ado.md)は**True**)、レコード セットの最後のレコードより後にします。 **EOF** プロパティが既に **True** の場合、前方へ移動しようとすると、エラーが発生します。

空の **Recordset** オブジェクトから **Move** メソッドを呼び出すと、エラーが発生します。

*起動*引数を渡すと、移動は、 **Recordset**オブジェクトがブックマークをサポートするいると仮定して、このブックマークを持つレコードを基準にしては。 指定しない場合は、カレント レコードが移動の基準となります。

*NumRecords*引数を現在のレコード位置が現在キャッシュされているレコード グループの範囲外に移動する、プロバイダーからのレコードをローカルにキャッシュ、 [CacheSize](cachesize-property-ado.md)プロパティを使用する場合、レコードの新しいグループを取得するために ADO を強制的に移動先のレコードから開始しています。 新しく取り込まれるグループのサイズは **CacheSize** プロパティによって決まり、移動先のレコードが最初に取得されるレコードになります。

場合は、 **Recordset**オブジェクトが前方スクロールのみ、ユーザー渡すこともできます、 *NumRecords*引数より小さい値 0、リンク先が現在キャッシュされているレコードのセット内では。 **Move** メソッドを呼び出して、カレント レコードの位置を、キャッシュされている最初のレコードより前のレコードに移動しようとすると、エラーが発生します。 このように、前方スクロールのみをサポートするプロバイダーで、完全スクロールをサポートするレコード キャッシュを使用することができます。 キャッシュされたレコードはメモリに読み込まれるため、必要以上のレコードのキャッシュは避けてください。 前方スクロールのみ可能な **Recordset** オブジェクトでも、この方法で後方への移動をサポートできますが、前方スクロールのみ可能な [Recordset](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) オブジェクトで **MovePrevious** メソッドを呼び出すと、エラーが発生します。


> [!NOTE]
> [!メモ] 前方スクロールのみ可能な **Recordset** で後方への移動がサポートされているかどうかは、プロバイダーによります。カレント レコードが **Recordset** の最後のレコードの後にある場合、後方への **Move** を実行しても現在の位置が正しく示されないことがあります。


