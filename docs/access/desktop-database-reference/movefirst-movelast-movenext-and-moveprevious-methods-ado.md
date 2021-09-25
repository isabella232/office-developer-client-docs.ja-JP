---
title: MoveFirst、MoveLast、MoveNext、および MovePrevious メソッド (ADO)
TOCTitle: MoveFirst, MoveLast, MoveNext, and MovePrevious methods (ADO)
ms:assetid: d04ce41c-77c9-df42-115a-65c50a38518a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250039(v=office.15)
ms:contentKeyID: 48547836
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 3e4c0ba5e5475ccf957eb63056fb38940864caa4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59593958"
---
# <a name="movefirst-movelast-movenext-and-moveprevious-methods-ado"></a>MoveFirst、MoveLast、MoveNext、および MovePrevious メソッド (ADO)


**適用先**: Access 2013、Office 2013

指定された [Recordset](recordset-object-ado.md) オブジェクトの最初、最後、次、または前のレコードに移動して、そのレコードをカレント レコードにします。

## <a name="syntax"></a>構文

*recordset*.{ MoveFirst |MoveLast |MoveNext |MovePrevious}

## <a name="remarks"></a>注釈

**MoveFirst** メソッドを使用して、カレント レコードの位置を **Recordset** の最初のレコードに移動します。

**MoveLast** メソッドを使用して、カレント レコードの位置を **Recordset** の最後のレコードに移動します。 **Recordset** オブジェクトはブックマークまたは後方へのカーソル移動をサポートしている必要があり、サポートしていない場合、このメソッドを呼び出すとエラーが発生します。

**Recordset** が空 ( **BOF** と **EOF** の両方が True) の場合、 **MoveFirst** または **MoveLast** を呼び出すとエラーが発生します。

**MoveNext** メソッドを使用して、カレント レコードの位置を 1 レコード前方 (**Recordset** の終端方向) に移動します。カレント レコードが最後のレコードの場合に **MoveNext** メソッドを呼び出すと、カレント レコードが **Recordset** の最後のレコードの後に設定され、[EOF](bof-eof-properties-ado.md) が **True** になります。**EOF** プロパティが既に **True** の場合、前方へ移動しようとするとエラーが発生します。

フィルターまたはソートが実行された **Recordset** でカレント レコードのデータを変更すると、その位置も変更されることがあります。 その場合、 **MoveNext** メソッドは正常に動作しますが、その位置が、元の位置からではなく、変更後の位置から 1 レコード先に移動されることに注意する必要があります。 たとえば、レコードが並べ替えた **Recordset** の末尾に移動されるなど、現在のレコード内のデータを変更すると **、MoveNext** を呼び出した場合、ADO は Recordset **(EOF**   =  **True)** の最後のレコードの後の位置に現在のレコードを設定します。

**MovePrevious** メソッドを使用して、カレント レコードの位置を 1 レコード後方 (**Recordset** の始端方向) に移動します。**Recordset** オブジェクトはブックマークまたは後方へのカーソル移動をサポートしている必要があり、サポートしていない場合、このメソッドを呼び出すとエラーが発生します。カレント レコードが最初のレコードの場合に **MovePrevious** メソッドを呼び出すと、カレント レコードは **Recordset** の最初のレコードの前に設定され、[BOF](bof-eof-properties-ado.md) が **True** になります。**BOF** プロパティが既に **True** の場合、後方へ移動しようとすると、エラーが発生します。**Recordset** オブジェクトがブックマークまたは後方へのカーソル移動をサポートしていない場合、**MovePrevious** メソッドを実行すると、エラーが発生します。

前方スクロールのみ可能な **Recordset** で両方向スクロールのサポートが必要な場合、 [CacheSize](cachesize-property-ado.md) プロパティを使用して後方へのカーソル移動をサポートするレコード キャッシュを作成し、 [Move](move-method-ado.md) メソッドを使用して移動することができます。キャッシュされたレコードはメモリに読み込まれるため、必要以上のレコードのキャッシュは避けてください。前方スクロールのみ可能な **Recordset** オブジェクトで **MoveFirst** メソッドを呼び出すことはできますが、その場合、 **Recordset** オブジェクトを生成するコマンドがプロバイダーで再度実行されることがあります。

