---
title: Requery メソッド (ADO)
TOCTitle: Requery method (ADO)
ms:assetid: 1062d907-979f-020a-b2ed-94e11c0e7d08
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248871(v=office.15)
ms:contentKeyID: 48543292
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 249dc236d730cf773ec38fe5dd903cb64ca9b594
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705681"
---
# <a name="requery-method-ado"></a>Requery メソッド (ADO)

**適用されます**Access 2013、Office 2013。

オブジェクトの基になるクエリを再実行して、[Recordset](recordset-object-ado.md) オブジェクトのデータを更新します。

## <a name="syntax"></a>構文

*レコード セット*です。*オプション*のクエリを再実行します。

## <a name="parameters"></a>パラメーター

|名前 |説明|
|:----|:----------|
|*Options* |省略可能です。この操作に対する [ExecuteOptionEnum](executeoptionenum.md) 値と [CommandTypeEnum](commandtypeenum.md) 値を含む、ビットマスクを指定します。|

> [!NOTE]
> *オプション*は、 **adAsyncExecute**に設定されている場合、この操作を非同期に実行され、 [RecordsetChangeComplete](willchangerecordset-and-recordsetchangecomplete-events-ado.md)イベントが終了するときに発行されます。

**Requery** では、 **ExecuteOpenEnum** の値 **adExecuteNoRecords** または **adExecuteStream** は使用できません。

## <a name="remarks"></a>解説

**Requery** メソッドは、元のコマンドを再実行してデータをもう一度取得することにより、データ ソースで **Recordset** オブジェクトの内容全体を更新する場合に使用します。このメソッドの呼び出しは、 [Close](close-method-ado.md) メソッドと [Open](open-method-ado-recordset.md) メソッドを連続して呼び出すことと同じです。カレント レコードを編集しているとき、または新規レコードを追加しているときにこのメソッドを呼び出すと、エラーが発生します。

**Recordset** オブジェクトを開いている間は、カーソルの属性を定義するプロパティ ([CursorType](cursortype-property-ado.md)、[LockType](locktype-property-ado.md)、[MaxRecords](maxrecords-property-ado.md) など) は、読み取り専用になります。したがって、**Requery** メソッドでは、現在のカーソルの更新のみを行うことができます。カーソルのプロパティを変更して結果を確認するには、[Close](close-method-ado.md) メソッドを使用して、プロパティを再度読み取り/書き込み可能にする必要があります。その後、目的のプロパティの設定を変更し、[Open](open-method-ado-recordset.md) メソッドを呼び出してカーソルを再度開きます。

