---
title: originalvalue プロパティ (ADO)
TOCTitle: OriginalValue property (ADO)
ms:assetid: 02ffc728-4692-d439-e2a6-2f02cca53a71
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248798(v=office.15)
ms:contentKeyID: 48542974
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0724320e1aaa1e7bfd3ceab8cf54afd5921c7425
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288183"
---
# <a name="originalvalue-property-ado"></a>originalvalue プロパティ (ADO)

**適用先:** Access 2013、Office 2013

変更が行われる前のレコードに存在していた [Field](field-object-ado.md) の値を示します。

## <a name="return-value"></a>戻り値

変更前のフィールドの値を表すバリアント型 (**Variant**) の値を返します。

## <a name="remarks"></a>注釈

現在のレコードからフィールドの元の値を返すには、**OriginalValue** プロパティを使用します。

*即時更新モード*(プロバイダーが[update](update-method-ado.md)メソッドを呼び出した後に、基になるデータソースに変更を書き込む) では、 **originalvalue**プロパティは、変更の前に存在したフィールド値を返します (つまり、last **Update**メソッドの呼び出し)。 This is the same value that the [CancelUpdate](cancelupdate-method-ado.md) method uses to replace the [Value](value-property-ado.md) property.

*バッチ更新モード*(プロバイダーが複数の変更をキャッシュし、 [UpdateBatch](updatebatch-method-ado.md)メソッドを呼び出したときに、基になるデータソースにそれらを書き込みます) では、 **originalvalue**プロパティは、いずれかの前にあったフィールド値を返します。変更 (前回の**UpdateBatch**メソッドの呼び出し以降)。 This is the same value that the [CancelBatch](cancelbatch-method-ado.md) method uses to replace the **Value** property. When you use this property with the [UnderlyingValue](underlyingvalue-property-ado.md) property, you can resolve conflicts that arise from batch updates.

## <a name="record"></a>Record

[Record](record-object-ado.md) オブジェクトの場合、[Update](update-method-ado.md) を呼び出す前に追加されたフィールドの **OriginalValue** プロパティは空になります。

