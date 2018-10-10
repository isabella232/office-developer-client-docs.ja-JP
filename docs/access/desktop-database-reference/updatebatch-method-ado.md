---
title: UpdateBatch メソッド (ADO)
TOCTitle: UpdateBatch Method (ADO)
ms:assetid: 69e72a65-b637-36fd-d09f-7f81050f71ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249416(v=office.15)
ms:contentKeyID: 48545420
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 522cfe50ac160074f7199a8364326d7debd5b780
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478636"
---
# <a name="updatebatch-method-ado"></a>UpdateBatch メソッド (ADO)


**適用されます**Access 2013 |。Office 2013

保留中の一括更新をすべてディスクに書き込みます。

## <a name="syntax"></a>構文

*レコード セット*です。UpdateBatch*AffectRecords*

## <a name="parameters"></a>パラメーター

  - *AffectRecords*

  - 省略可能です。 [UpdateBatch](affectenum.md) メソッドで処理するレコードの数を示す **AffectEnum** 値を指定します。

## <a name="remarks"></a>解説

**Recordset** オブジェクトを一括更新モードで変更している場合に **UpdateBatch** メソッドを使用すると、 **Recordset** オブジェクトに加えられた変更を基になるデータベースに転送できます。

**Recordset** オブジェクトが一括更新をサポートしている場合は、 **UpdateBatch** メソッドを呼び出すまでの間、1 つまたは複数のレコードへの複数の変更をローカルにキャッシュしておくことができます。カレント レコードの編集中、または新しいレコードの追加中に **UpdateBatch** メソッドを呼び出すと、ADO によって自動的に [Update](update-method-ado.md) メソッドが呼び出されてカレント レコードへの保留中の変更が保存されてから、変更内容がまとめてプロバイダーに転送されます。一括更新は、キーセットまたは静的カーソルのみで使用してください。


> [!NOTE]
> <P>[!メモ] パラメーターの値として <STRONG>adAffectGroup</STRONG> を指定すると、現在の <STRONG>Recordset</STRONG> 内に表示可能なレコードがなかった場合 (一致するレコードのないフィルターがかかっているなど) にはエラーが発生します。</P>



基になるデータとの競合が原因で一部またはすべてのレコードの変更の転送に失敗した場合 (たとえば、レコードが他のユーザーによって既に削除されていた場合)、プロバイダーから [Errors](errors-collection-ado.md) コレクションに警告が返され、実行時エラーが発生します。[Filter](filter-property-ado.md) プロパティ (**adFilterAffectedRecords**) と [Status](status-property-ado-recordset.md) プロパティを使用すると、競合のあるレコードを突き止めることができます。

保留になっているすべての一括更新を取り消すには、[CancelBatch](cancelbatch-method-ado.md) メソッドを使用します。

動的プロパティの [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) と [Update Resync](update-resync-property-dynamic-ado.md) が設定されていて、 **Recordset** が複数のテーブルに対して JOIN 操作を実行した結果になっている場合は、 **UpdateBatch** メソッドの実行の後に、 [Update Resync](resync-method-ado.md) プロパティの設定に応じて暗黙的に **Resync** メソッドが実行されます。

個々の一括更新がデータ ソースに対して実行される順序は、必ずしもそれらがローカル **Recordset** に実行された順序と同じになるわけではありません。更新の順序は、プロバイダーに依存します。挿入または更新に対する外部キー制約など、相互に関連のある更新をコーディングする場合は、このことを考慮してください。

