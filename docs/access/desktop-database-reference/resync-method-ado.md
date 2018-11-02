---
title: Resync メソッド (ADO)
TOCTitle: Resync method (ADO)
ms:assetid: f594a200-56e6-fcf5-9b0a-900c56377f24
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250251(v=office.15)
ms:contentKeyID: 48548717
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 73633c38bb21a794bc2137554f0341f93d9f265d
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25931044"
---
# <a name="resync-method-ado"></a>Resync メソッド (ADO)


**適用されます**Access 2013、Office 2013。



現在の [Recordset](recordset-object-ado.md) オブジェクト、または [Record](fields-collection-ado.md) オブジェクトの [Fields](record-object-ado.md) コレクションのデータを、基になるデータベースのデータで更新します。

## <a name="syntax"></a>構文

*レコード セット*です。*AffectRecords*、 *ResyncValues*を再同期します。

*レコード*です。 *フィールド*です。*ResyncValues*を再同期します。

## <a name="parameters"></a>パラメーター

  - *AffectRecords*

  - 省略可能です。 [Resync](affectenum.md) メソッドで操作するレコードの数を決定する **AffectEnum** 値を指定します。既定値は **adAffectAll** です。この値は、 **Record** オブジェクトの **Fields** コレクションに対する **Resync** メソッドでは使用できません。

  - *ResyncValues*

  - 省略可能です。基になる値を上書きするかどうかを指定する [ResyncEnum](resyncenum.md) 値を指定します。既定値は **adResyncAllValues** です。

## <a name="remarks"></a>解説

**Recordset**

**Resync** メソッドは、現在の **Recordset** のレコードを基になるデータベースと再同期させる場合に使用します。このメソッドは、静的または前方専用のカーソルを使用していて、基になるデータベースの変更を確認する場合に役立ちます。

[CursorLocation](cursorlocation-property-ado.md) プロパティを **adUseClient** に設定した場合には、 **Resync** は、読み取り専用ではない **Recordset** オブジェクトに対してのみ使用できます。

[Requery](requery-method-ado.md) メソッドとは異なり、 **Resync** メソッドは、 **Recordset** オブジェクトの基になっているコマンドを再実行しません。基になるデータベースの新しいレコードを参照することはできません。

基になるデータとの競合 (たとえば、他のユーザーがレコードを削除した場合) が原因で再同期に失敗した場合、プロバイダーは [Errors](errors-collection-ado.md) コレクションに警告を返し、実行時エラーが発生します。競合しているレコードを特定するには、[Filter](filter-property-ado.md) プロパティ (**adFilterConflictingRecords**) と [Status](status-property-ado-recordset.md) プロパティを使用します。

ダイナミック プロパティ [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) および [Resync Command](resync-command-property-dynamic-ado.md) が設定されていて、 **Recordset** が複数のテーブルに対する JOIN 操作の実行結果である場合、 **Resync** メソッドは、 **Unique Table** プロパティで指定されているテーブルに対してのみ、 **Resync Command** プロパティで指定されているコマンドを実行します。

**Fields**

**Resync** メソッドは、 **Record** オブジェクトの **Fields** コレクションの値を、基になるデータ ソースと再同期させる場合に使用します。 [Count](count-property-ado.md) プロパティは、このメソッドによる影響を受けません。

*ResyncValues*を**adResyncAllValues** (既定値) に設定し、 [UnderlyingValue](underlyingvalue-property-ado.md)[値](value-property-ado.md)、およびコレクション内の[Field](field-object-ado.md)オブジェクトの[OriginalValue](originalvalue-property-ado.md)プロパティが同期されます。 *ResyncValues*は、**処理**に設定されている場合は、 **UnderlyingValue**プロパティだけが同期されます。

呼び出し時の各 **Field** オブジェクトの **Status** プロパティの値も、 **Resync** の動作に影響を与えます。 **Status** の値が **adFieldPendingUnknown** または **adFieldPendingInsert** である **Field** オブジェクトに対しては、 **Resync** は何も行いません。 **Status** の値が **adFieldPendingChange** または **adFieldPendingDelete** である場合は、 **Resync** はデータ ソースにまだ存在しているフィールドのデータ値を同期化します。

**再同期**は変更されません**フィールド**オブジェクトの**ステータス**の値**の再同期**が呼び出されたときにエラーが発生しません。 たとえば、フィールドが存在しない場合、プロバイダーは**adFieldDoesNotExist**など、 **Field**オブジェクトの適切な**ステータス**値を返します。 返された**ステータス**値は、 **Status**プロパティの値の中で論理的に組み合わせることができます。

