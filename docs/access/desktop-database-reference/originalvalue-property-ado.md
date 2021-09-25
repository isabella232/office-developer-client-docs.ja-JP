---
title: OriginalValue プロパティ (ADO)
TOCTitle: OriginalValue property (ADO)
ms:assetid: 02ffc728-4692-d439-e2a6-2f02cca53a71
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248798(v=office.15)
ms:contentKeyID: 48542974
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 45ca3e5f2ef978a759b39f2ed4ef763d48570f87
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59589294"
---
# <a name="originalvalue-property-ado"></a>OriginalValue プロパティ (ADO)

**適用先**: Access 2013、Office 2013

変更が行われる前のレコードに存在していた [Field](field-object-ado.md) の値を示します。

## <a name="return-value"></a>戻り値

変更前のフィールドの値を表すバリアント型 (**Variant**) の値を返します。

## <a name="remarks"></a>注釈

現在のレコードからフィールドの元の値を返すには、**OriginalValue** プロパティを使用します。

即時 *更新* モード [(Update](update-method-ado.md) メソッドの呼び出し後にプロバイダーが基になるデータ ソースに変更を書き込む) では **、OriginalValue** プロパティは、変更の前に存在していたフィールド値 (つまり、最後の **Update** メソッド呼び出し以降) を返します。 This is the same value that the [CancelUpdate](cancelupdate-method-ado.md) method uses to replace the [Value](value-property-ado.md) property.

バッチ *更新* モード (プロバイダーが複数の変更をキャッシュし [、UpdateBatch](updatebatch-method-ado.md) メソッドを呼び出す場合にのみ基になるデータ ソースに書き込む) では **、OriginalValue** プロパティは、変更の前に存在していたフィールド値 (つまり、最後の **UpdateBatch** メソッド呼び出し以降) を返します。 This is the same value that the [CancelBatch](cancelbatch-method-ado.md) method uses to replace the **Value** property. When you use this property with the [UnderlyingValue](underlyingvalue-property-ado.md) property, you can resolve conflicts that arise from batch updates.

## <a name="record"></a>Record

[Record](record-object-ado.md) オブジェクトの場合、[Update](update-method-ado.md) を呼び出す前に追加されたフィールドの **OriginalValue** プロパティは空になります。

