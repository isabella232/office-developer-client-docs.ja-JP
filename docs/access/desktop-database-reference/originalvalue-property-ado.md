---
title: OriginalValue プロパティ (ADO)
TOCTitle: OriginalValue property (ADO)
ms:assetid: 02ffc728-4692-d439-e2a6-2f02cca53a71
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248798(v=office.15)
ms:contentKeyID: 48542974
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0724320e1aaa1e7bfd3ceab8cf54afd5921c7425
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700424"
---
# <a name="originalvalue-property-ado"></a>OriginalValue プロパティ (ADO)

**適用されます**Access 2013、Office 2013。

変更が行われる前のレコードに存在していた [Field](field-object-ado.md) の値を示します。

## <a name="return-value"></a>戻り値

変更前のフィールドの値を表すバリアント型 ( **Variant** ) の値を返します。

## <a name="remarks"></a>解説

現在のレコードからフィールドの元の値を返すには、 **OriginalValue** プロパティを使用します。

*イミディ エイト更新モード*(でプロバイダーに変更を書き込みます、基になるデータ ソース[の更新](update-method-ado.md)メソッドを呼び出した後)、 **OriginalValue**プロパティは、変更する前に存在していたフィールドの値を返します (以後、最後の**Update**メソッドの呼び出し)。 これは、 [Value](value-property-ado.md)プロパティを置換するのには、 [CancelUpdate](cancelupdate-method-ado.md)メソッドを使用するのと同じ値です。

*バッチ更新モード*(をプロバイダー複数の変更をキャッシュし、 [UpdateBatch](updatebatch-method-ado.md)メソッドを呼び出した場合にのみ、基になるデータ ソースに書き込みます)、 **OriginalValue**プロパティは、いずれかの前に存在していたフィールドの値を返します(つまり、最後の**UpdateBatch**メソッドを呼び出す) ために変更します。 これは、 **Value**プロパティを置換するのには、 [CancelBatch](cancelbatch-method-ado.md)メソッドを使用するのと同じ値です。 [UnderlyingValue](underlyingvalue-property-ado.md)プロパティを使用してこのプロパティを使用する場合は、バッチ更新で発生した競合を解決できます。

## <a name="record"></a>Record

[Record](record-object-ado.md) オブジェクトの場合、 **Update** を呼び出す前に追加されたフィールドの [OriginalValue](update-method-ado.md) プロパティは空になります。

