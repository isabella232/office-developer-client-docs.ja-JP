---
title: CancelBatch メソッド (ADO)
TOCTitle: CancelBatch method (ADO)
ms:assetid: be7bf073-ed0b-e24c-7ec0-b7379236782a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249925(v=office.15)
ms:contentKeyID: 48547463
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 88bf83cad220056d9ee21f300e5543030e5d18cd
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25950079"
---
# <a name="cancelbatch-method-ado"></a>CancelBatch メソッド (ADO)

**適用されます**Access 2013、Office 2013。

保留中のバッチ更新をキャンセルします。

## <a name="syntax"></a>構文

*レコード セット*です。CancelBatch *AffectRecords*

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*AffectRecords* |省略可能です。 [CancelBatch](affectenum.md) メソッドで処理するレコードの数を示す **AffectEnum** 値です。 |

## <a name="remarks"></a>解説

**CancelBatch** メソッドは、バッチ更新モードの [Recordset](recordset-object-ado.md) で保留中の更新をすべて取り消す場合に使用します。即時更新モードの **Recordset** では、 **adAffectCurrent** を指定しないで **CancelBatch** を呼び出すと、エラーが発生します。

カレント レコードの編集中または新規レコードの追加中に **CancelBatch** メソッドを呼び出すと、最初に [CancelUpdate](cancelupdate-method-ado.md) メソッドが呼び出されて、キャッシュされているすべての変更が取り消されます。その後、 **Recordset** で保留中のすべての変更が取り消されます。

**CancelBatch** を呼び出した後は、カレント レコードを特定できない可能性があります。特に、新規レコードの追加処理中の場合は、その可能性が高くなります。このため、 **CancelBatch** の呼び出し後は、カレント レコードの位置を **Recordset** 内の既知の位置に設定することをお勧めします。たとえば、 [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) メソッドを呼び出します。

基になるデータとの競合 (たとえば、他のユーザーによってレコードが削除されている場合) が原因で保留中の更新を取り消すこどができない場合、プロバイダーは [Errors](errors-collection-ado.md) コレクションに警告を返しますが、プログラムの実行は停止しません。要求したすべてのレコードで競合が発生した場合にのみ、実行時エラーが発生します。競合しているレコードを特定するには、[Filter](filter-property-ado.md) プロパティ (**adFilterAffectedRecords**) と [Status](status-property-ado-recordset.md) プロパティを使用します。

