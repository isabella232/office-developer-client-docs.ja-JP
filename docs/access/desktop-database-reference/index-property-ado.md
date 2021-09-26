---
title: Index プロパティ (ADO)
TOCTitle: Index property (ADO)
ms:assetid: 4cc00521-dcb4-19b2-2174-6e0e9bd42e62
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249241(v=office.15)
ms:contentKeyID: 48544715
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 28769059f6a7ab2ab6edd0723ad81d1fc156e43c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59626387"
---
# <a name="index-property-ado"></a>Index プロパティ (ADO)


**適用先**: Access 2013、Office 2013

[Recordset](recordset-object-ado.md) オブジェクトに対して現在有効なインデックスの名前を示します。

## <a name="settings-and-return-values"></a>設定および戻り値

インデックス名を表す文字列型 (**String**) の値を設定または取得します。

## <a name="remarks"></a>注釈

**Index** プロパティで指定したインデックスは、 **Recordset** オブジェクトの基になるベース テーブルで事前に宣言しておく必要があります。つまり、インデックスは、ADOX [Index](index-object-adox.md) オブジェクトとしてプログラムで宣言しておくか、ベース テーブルの作成時に宣言しておきます。

インデックスを設定できないと、実行時エラーが発生します。次の条件では、 **Index** プロパティを設定できません。

  - [WillChangeRecordset](willchangerecordset-and-recordsetchangecomplete-events-ado.md) イベント ハンドラーまたは **RecordsetChangeComplete** イベント ハンドラー内。

  - **Recordset** の操作が実行中である ( [State](state-property-ado.md) プロパティで判別可能)。

  - **Filter** プロパティにより [Recordset](filter-property-ado.md) にフィルターが設定されている。

**Recordset** が閉じていれば、 **Index** プロパティは正常に設定できますが、基になるプロバイダーがインデックスをサポートしていない場合は、 **Recordset** が正常に開かなかったり、インデックスを使うことができないことがあります。

インデックスを設定すると、現在の行の位置が変更されることがあります。その場合は、[AbsolutePosition](absoluteposition-property-ado.md) プロパティが更新され、 **WillChangeRecordset** イベント、 **RecordsetChangeComplete** イベント、 [WillMove](willmove-and-movecomplete-events-ado.md) イベント、および [MoveComplete](willmove-and-movecomplete-events-ado.md) イベントが生成されます。

インデックスの設定が可能で、[LockType](locktype-property-ado.md) プロパティが **adLockPessimistic** または **adLockOptimistic** の場合は、 [UpdateBatch](updatebatch-method-ado.md) 操作が暗黙的に実行されます。これによって、現在のグループと、影響下のグループが解放されます。既存のフィルターがすべて解放され、現在の行の位置は、並べ替えられた **Recordset** の最初の行に移動します。

**Index** プロパティは、 [Seek](seek-method-ado.md) メソッドと一緒に使用します。 基になるプロバイダーが **Index** プロパティをサポートしていないために **Seek** メソッドがサポートされていない場合は、代わりに [Find](find-method-ado.md) メソッドを使用してください。 Recordset オブジェクト [](supports-method-ado.md)が **サポート****(adIndex)** メソッドを使用してインデックスをサポートするかどうかを判断します。

どちらもインデックスを扱いますが、組み込み **Index** プロパティは、動的な [Optimize](optimize-property-dynamic-ado.md) プロパティとは無関係です。

