---
title: Field オブジェクト - ActiveX データ オブジェクト (ADO)
TOCTitle: Field object (ADO)
ms:assetid: 1dbd535e-48ad-a5c8-a1b2-6776c1e3e19d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248968(v=office.15)
ms:contentKeyID: 48543600
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: b71007884534f556c36462cb3f925b1807308268
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59552980"
---
# <a name="field-object-ado"></a>Field オブジェクト (ADO)


**適用先:** Access 2013、Office 2013

共通のデータ型を持つデータの列を表します。

## <a name="remarks"></a>注釈

各 **Field** オブジェクトは、 [Recordset](recordset-object-ado.md) の 1 つの列に対応します。 [Field](value-property-ado.md) オブジェクトの **Value** プロパティを使用すると、カレント レコードのデータを設定または取得できます。プロバイダーが公開している機能によっては、 **Field** オブジェクトの一部のコレクション、メソッド、またはプロパティを使用できない場合があります。

**Field** オブジェクトのコレクション、メソッド、およびプロパティを使用すると、次の操作を実行できます。

  - [Name](name-property-ado.md) プロパティを使用して、フィールドの名前を取得できます。

  - **Value** プロパティを使用して、フィールド内のデータを表示または変更できます。 **Value** は、 **Field** オブジェクトの既定のプロパティです。

  - [Type](type-property-ado.md)、[Precision](precision-property-ado.md)、および [NumericScale](numericscale-property-ado.md) の各プロパティを使用して、フィールドの基本的な特性を取得できます。

  - [DefinedSize](definedsize-property-ado.md) プロパティを使用して、フィールドの宣言されたサイズを取得できます。

  - [ActualSize](actualsize-property-ado.md) プロパティを使用して、特定のフィールドに含まれるデータの実際のサイズを取得できます。

  - [Attributes](attributes-property-ado.md) プロパティおよび [Properties](properties-collection-ado.md) コレクションを使用して、特定のフィールドについてサポートされている機能の種類を確認できます。

  - [AppendChunk](appendchunk-method-ado.md) メソッドおよび [GetChunk](getchunk-method-ado.md) メソッドを使用して、長いバイナリ データまたは長い文字データを含むフィールドの値を操作できます。

  - プロバイダーがバッチ更新をサポートしている場合は、[OriginalValue](originalvalue-property-ado.md) プロパティおよび [UnderlyingValue](underlyingvalue-property-ado.md) プロパティを使用して、バッチ更新中に発生するフィールドの値の不一致を解決できます。

メタデータ プロパティのすべて (**Name**、**Type**、**DefinedSize**、**Precision**、および **NumericScale**) は、**Field** オブジェクトの **Recordset** を開く前に使用可能になります。この時点でこれらのプロパティを設定すると、フォームを動的に作成する際に便利です。

