---
title: Status プロパティ (ADO Recordset)
TOCTitle: Status property (ADO Recordset)
ms:assetid: bf3ccb36-c985-5fae-4f76-c48a0e20e6f7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249930(v=office.15)
ms:contentKeyID: 48547482
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: ef2978d699021ebfa0fad6f207778caa019d32b0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621760"
---
# <a name="status-property-ado-recordset"></a>Status プロパティ (ADO Recordset)


**適用先**: Access 2013、Office 2013

一括更新またはその他の一括操作に関して現在のレコードのステータスを示します。

## <a name="return-value"></a>戻り値

[RecordStatusEnum](recordstatusenum.md) 値の合計を返します。

## <a name="remarks"></a>注釈

一括更新中に変更されたレコードの保留中の変更を調べるには、**Status** プロパティを使用します。また、**Status** プロパティを使用して、[Recordset](recordset-object-ado.md) オブジェクトで [Resync](resync-method-ado.md) メソッド、[UpdateBatch](updatebatch-method-ado.md) メソッド、または [CancelBatch](cancelbatch-method-ado.md) メソッドなどを呼び出したときや、**Recordset** オブジェクトの [Filter](filter-property-ado.md) プロパティをブックマークの配列に設定したときのように、一括操作中に処理されなかったレコードの状態を確認することもできます。このプロパティを使用すると、特定のレコードが処理されなかった原因を調べて、問題を解決することができます。

