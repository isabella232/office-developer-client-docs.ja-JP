---
title: Status プロパティ (ADO Recordset)
TOCTitle: Status Property (ADO Recordset)
ms:assetid: bf3ccb36-c985-5fae-4f76-c48a0e20e6f7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249930(v=office.15)
ms:contentKeyID: 48547482
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1979ad721a01ef72c08da1531a8826ec320915e5
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/17/2018
ms.locfileid: "25604618"
---
# <a name="status-property-ado-recordset"></a>Status プロパティ (ADO Recordset)


**適用されます**Access 2013 |。Office 2013

一括更新またはその他の一括操作に関して現在のレコードのステータスを示します。

<<<<<<< ヘッド
## <a name="return-value"></a>戻り値
=======
## <a name="return-value"></a>戻り値
>>>>>>> master

[RecordStatusEnum](recordstatusenum.md) 値の合計を返します。

## <a name="remarks"></a>解説

一括更新中に変更されたレコードの保留中の変更を調べるには、 **Status** プロパティを使用します。また、 **Status** プロパティを使用して、 [Recordset](resync-method-ado.md) オブジェクトで [Resync](updatebatch-method-ado.md) メソッド、 [UpdateBatch](cancelbatch-method-ado.md) メソッド、または [CancelBatch](recordset-object-ado.md) メソッドなどを呼び出したときや、 [Recordset](filter-property-ado.md) オブジェクトの **Filter** プロパティをブックマークの配列に設定したときのように、一括操作中に処理されなかったレコードの状態を確認することもできます。このプロパティを使用すると、特定のレコードが処理されなかった原因を調べて、問題を解決することができます。

