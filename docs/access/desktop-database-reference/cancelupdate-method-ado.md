---
title: CancelUpdate メソッド (ADO)
TOCTitle: CancelUpdate method (ADO)
ms:assetid: 2bd4d168-ba52-7786-5046-44febeda88e1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249065(v=office.15)
ms:contentKeyID: 48543938
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: f5b72c3e801ce746f406685f27cbeccd481d3925
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59558609"
---
# <a name="cancelupdate-method-ado"></a>CancelUpdate メソッド (ADO)


**適用先:** Access 2013、Office 2013

[Update](update-method-ado.md) メソッドを呼び出す前に行った、[Recordset](recordset-object-ado.md) オブジェクトのカレント行や新規行に対する変更、または [Record](record-object-ado.md) オブジェクトの [Fields](fields-collection-ado.md) コレクションに対する変更を、すべてキャンセルします。

## <a name="syntax"></a>構文

*recordset*.CancelUpdate

*record*.*フィールド*。CancelUpdate

## <a name="remarks"></a>注釈

**Recordset**

**CancelUpdate** メソッドは、カレント行に対する変更を取り消す場合、または新しく追加した行を破棄する場合に使用します。 **Update** メソッドを呼び出した後では、カレント行に対する変更または新規行を取り消すことはできません。ただし、変更が [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) メソッドでロールバックできるトランザクションの一部である場合、またはバッチ更新の一部である場合を除きます。バッチ更新の場合は、 **CancelUpdate** メソッドまたは **CancelBatch** メソッドで [Update](cancelbatch-method-ado.md) を取り消すこどができます。

新しい行を追加している場合は、 **CancelUpdate** メソッドを呼び出すと、 [AddNew](addnew-method-ado.md) を呼び出す前にカレントであった行がカレント行になります。

編集モードでカレント レコードから移動する (たとえば、[Move](move-method-ado.md)、[NextRecordset](nextrecordset-method-ado.md)、または [Close](close-method-ado.md) を使用して) 場合は、 **CancelUpdate** を使用して、保留中のすべての変更を取り消すこどができます。データ ソースの更新が成功しなかった場合 (たとえば、参照整合性違反のために削除の試みが失敗し、 **Delete** の呼び出しの後で [Recordset](delete-method-ado-recordset.md) が編集モードのままになった場合) には、この処理が必要になることがあります。

**Record**

**CancelUpdate** メソッドは、 [Field](field-object-ado.md) オブジェクトの保留中の挿入または削除をすべてキャンセルし、既存のフィールドの保留中の更新をキャンセルして元の値に戻します。 [Fields](status-property-ado-recordset.md) コレクションのすべてのフィールドの **Status** プロパティは、 **adFieldOK** に設定されます。

