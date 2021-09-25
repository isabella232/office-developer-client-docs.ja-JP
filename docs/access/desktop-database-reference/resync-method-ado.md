---
title: Resync メソッド (ADO)
TOCTitle: Resync method (ADO)
ms:assetid: f594a200-56e6-fcf5-9b0a-900c56377f24
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250251(v=office.15)
ms:contentKeyID: 48548717
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 292a7e5f769ceae7948fcd5f05e2296a2f8270e6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59562280"
---
# <a name="resync-method-ado"></a>Resync メソッド (ADO)

**適用先:** Access 2013、Office 2013

現在の [Recordset](recordset-object-ado.md) オブジェクト、または [Record](record-object-ado.md) オブジェクトの [Fields](fields-collection-ado.md) コレクションのデータを、基になるデータベースのデータで更新します。

## <a name="syntax"></a>構文

*Recordset*.再同期 *AffectRecords*、 *ResyncValues*

*Record*. *フィールド*。Resync *ResyncValues*

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*AffectRecords* |省略可能です。 [Resync](affectenum.md) メソッドで操作するレコードの数を決定する **AffectEnum** 値を指定します。既定値は **adAffectAll** です。この値は、 **Record** オブジェクトの **Fields** コレクションに対する **Resync** メソッドでは使用できません。|
|*ResyncValues* |省略可能です。基になる値を上書きするかどうかを指定する [ResyncEnum](resyncenum.md) 値を指定します。既定値は **adResyncAllValues** です。|

## <a name="remarks"></a>注釈

### <a name="recordset"></a>Recordset

**Resync** メソッドは、現在の **Recordset** のレコードを基になるデータベースと再同期させる場合に使用します。このメソッドは、静的または前方専用のカーソルを使用していて、基になるデータベースの変更を確認する場合に役立ちます。

[CursorLocation](cursorlocation-property-ado.md) プロパティを **adUseClient** に設定した場合には、 **Resync** は、読み取り専用ではない **Recordset** オブジェクトに対してのみ使用できます。

[Requery](requery-method-ado.md) メソッドとは異なり、 **Resync** メソッドは、 **Recordset** オブジェクトの基になっているコマンドを再実行しません。基になるデータベースの新しいレコードを参照することはできません。

基になるデータとの競合 (たとえば、他のユーザーがレコードを削除した場合) が原因で再同期に失敗した場合、プロバイダーは [Errors](errors-collection-ado.md) コレクションに警告を返し、実行時エラーが発生します。競合しているレコードを特定するには、[Filter](filter-property-ado.md) プロパティ (**adFilterConflictingRecords**) と [Status](status-property-ado-recordset.md) プロパティを使用します。

ダイナミック プロパティ [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) および [Resync Command](resync-command-property-dynamic-ado.md) が設定されていて、 **Recordset** が複数のテーブルに対する JOIN 操作の実行結果である場合、 **Resync** メソッドは、 **Unique Table** プロパティで指定されているテーブルに対してのみ、 **Resync Command** プロパティで指定されているコマンドを実行します。

### <a name="fields"></a>フィールド

**Resync** メソッドは、**Record** オブジェクトの **Fields** コレクションの値を、基になるデータ ソースと再同期させる場合に使用します。[Count](count-property-ado.md) プロパティは、このメソッドによる影響を受けません。

*ResyncValues* を **adResyncAllValues** (既定値) に設定すると、コレクションに含まれる [Field](field-object-ado.md) オブジェクトのプロパティ [UnderlyingValue](underlyingvalue-property-ado.md)、[Value](value-property-ado.md)、および [OriginalValue](originalvalue-property-ado.md) が同期化されます。*ResyncValues* を **adResyncUnderlyingValues** に設定すると、**UnderlyingValue** プロパティだけが同期化されます。

呼び出し時の各 **Field** オブジェクトの **Status** プロパティの値も、 **Resync** の動作に影響を与えます。 **Status** の値が **adFieldPendingUnknown** または **adFieldPendingInsert** である **Field** オブジェクトに対しては、 **Resync** は何も行いません。 **Status** の値が **adFieldPendingChange** または **adFieldPendingDelete** である場合は、 **Resync** はデータ ソースにまだ存在しているフィールドのデータ値を同期化します。

**Resync** will not modify **Status** values of **Field** objects unless an error occurs when **Resync** is called. For example, if the field no longer exists, the provider will return an appropriate **Status** value for the **Field** object, such as **adFieldDoesNotExist**. Returned **Status** values may be logically combined within the value of the **Status** property.

