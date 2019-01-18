---
title: CancelUpdate メソッド (ADO)
TOCTitle: CancelUpdate method (ADO)
ms:assetid: 2bd4d168-ba52-7786-5046-44febeda88e1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249065(v=office.15)
ms:contentKeyID: 48543938
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4585679688929532d7f50be9efc71b2830bb6587
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711246"
---
# <a name="cancelupdate-method-ado"></a>CancelUpdate メソッド (ADO)


**適用されます**Access 2013、Office 2013。

[Update](recordset-object-ado.md) メソッドを呼び出す前に行った、 [Recordset](fields-collection-ado.md) オブジェクトのカレント行や新規行に対する変更、または [Record](record-object-ado.md) オブジェクトの [Fields](update-method-ado.md) コレクションに対する変更を、すべてキャンセルします。

## <a name="syntax"></a>構文

*レコード セット*です。CancelUpdate

*レコード*です。*フィールド*です。CancelUpdate

## <a name="remarks"></a>解説

**Recordset**

**CancelUpdate** メソッドは、カレント行に対する変更を取り消す場合、または新しく追加した行を破棄する場合に使用します。 **Update** メソッドを呼び出した後では、カレント行に対する変更または新規行を取り消すことはできません。ただし、変更が [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) メソッドでロールバックできるトランザクションの一部である場合、またはバッチ更新の一部である場合を除きます。バッチ更新の場合は、 **CancelUpdate** メソッドまたは **CancelBatch** メソッドで [Update](cancelbatch-method-ado.md) を取り消すこどができます。

新しい行を追加している場合は、 **CancelUpdate** メソッドを呼び出すと、 [AddNew](addnew-method-ado.md) を呼び出す前にカレントであった行がカレント行になります。

編集モードでカレント レコードから移動する (たとえば、[Move](move-method-ado.md)、[NextRecordset](nextrecordset-method-ado.md)、または [Close](close-method-ado.md) を使用して) 場合は、 **CancelUpdate** を使用して、保留中のすべての変更を取り消すこどができます。データ ソースの更新が成功しなかった場合 (たとえば、参照整合性違反のために削除の試みが失敗し、 **Delete** の呼び出しの後で [Recordset](delete-method-ado-recordset.md) が編集モードのままになった場合) には、この処理が必要になることがあります。

**Record**

**CancelUpdate** メソッドは、 [Field](field-object-ado.md) オブジェクトの保留中の挿入または削除をすべてキャンセルし、既存のフィールドの保留中の更新をキャンセルして元の値に戻します。 [Fields](status-property-ado-recordset.md) コレクションのすべてのフィールドの **Status** プロパティは、 **adFieldOK** に設定されます。

