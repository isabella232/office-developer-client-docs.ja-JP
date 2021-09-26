---
title: LockType プロパティ (ADO)
TOCTitle: LockType property (ADO)
ms:assetid: 1d2622dc-6cab-1b7f-98a8-97a41d5c047f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248965(v=office.15)
ms:contentKeyID: 48543589
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: dcd615e36fc031c52a8f3de084d7d117752f4a23
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59622236"
---
# <a name="locktype-property-ado"></a>LockType プロパティ (ADO)


**適用先**: Access 2013、Office 2013

編集時にレコードに適用されるロックの種類を示します。

## <a name="settings-and-return-values"></a>設定および戻り値

[LockTypeEnum](locktypeenum.md) の値を設定または取得します。既定値は **adLockReadOnly** です。

## <a name="remarks"></a>注釈

プロバイダーが **Recordset** を開くときに使用するロックの種類は、 [LockType](recordset-object-ado.md) プロパティを使用して事前に設定します。開いている **Recordset** オブジェクトで使用されているロックの種類は、このプロパティを取得することで確認できます。

プロバイダーによってはすべての種類のロックをサポートしていないものもあります。要求した **LockType** 設定をプロバイダーがサポートしていない場合は、他の種類のロックに置き換えられます。 **Recordset** オブジェクトで実際に使用可能なロック機能を調べるには、 [adUpdate](supports-method-ado.md) と **adUpdateBatch** で **Supports** メソッドを使用します。

**CursorLocation** が [adUseClient](cursorlocation-property-ado.md) に設定されている場合、 **adLockPessimistic** 設定はサポートされません。サポートされていない値を設定してもエラーにはなりませんが、サポートされる **LockType** のうち、最も近いロックが使用されます。

**LockType** プロパティは、 **Recordset** が閉じているときは読み取り/書き込み可能で、開いているときは読み取り専用になります。

**リモート データ サービスの使用状況** クライアント側の Recordset オブジェクトで使用する場合 **、LockType** プロパティは **adLockBatchOptimistic にしか設定できません**。

