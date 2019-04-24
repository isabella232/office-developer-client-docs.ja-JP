---
title: unique Table、unique Schema、unique Catalog 動的プロパティ (ADO)
TOCTitle: Unique Table, Unique Schema, Unique Catalog dynamic properties (ADO)
ms:assetid: e6374782-755b-322b-21de-6d6a386dcd98
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250169(v=office.15)
ms:contentKeyID: 48548374
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5f4bf93afc200edd88e89cf5d4e90435c2476942
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32313749"
---
# <a name="unique-table-unique-schema-unique-catalog-dynamic-properties-ado"></a>unique Table、unique Schema、unique Catalog 動的プロパティ (ADO)


**適用先:** Access 2013、Office 2013

複数のベース テーブルに対する JOIN 操作で形成された [Recordset](recordset-object-ado.md) 中の、特定のベース テーブルに対する変更を細かく制御します。

  - **Unique Table** は、更新、挿入、および削除の操作ができるベース テーブルの名前を指定します。

  - **Unique schema**は、*スキーマ*、またはテーブルの所有者の名前を指定します。

  - **Unique catalog**は、*カタログ*、またはテーブルを含むデータベースの名前を指定します。

## <a name="settings-and-return-values"></a>設定値と戻り値

テーブル、スキーマ、またはカタログの名前である文字列型 (**String**) の値を設定または取得します。

## <a name="remarks"></a>注釈

対象となるベース テーブルは、一意なカタログ名、スキーマ名、およびテーブル名で識別します。 **Unique Table** プロパティが設定されている場合、 **Unique Schema** プロパティまたは **Unique Catalog** プロパティの値がベース テーブルを検索するために使用されます。 **Unique Table** プロパティを設定する前に **Unique Schema** プロパティと **Unique Catalog** プロパティのどちらかまたは両方を設定するのが本来の順序ですが、必ずしもそうする必要はありません。

**Unique Table** の主キーは、 **Recordset** 全体の主キーとして扱われます。これは、主キーを必要とするすべてのメソッドで使用されるキーです。

**Unique Table** が設定されている場合、 [Delete](delete-method-ado-recordset.md) メソッドは、指定されたテーブルだけに反映されます。 [AddNew](addnew-method-ado.md) メソッド、 [Resync](resync-method-ado.md) メソッド、 [Update](update-method-ado.md) メソッド、および [UpdateBatch](updatebatch-method-ado.md) メソッドは、 **Recordset** の基になるベース テーブルに反映されます。

カスタム再同期を実行するには、あらかじめ **Unique Table** を指定する必要があります。 **Unique Table** が指定されていないと、 [Resync Command](resync-command-property-dynamic-ado.md) プロパティは反映されません。

一意のベース テーブルが見つからないと、実行時エラーになります。

**CursorLocation** プロパティを [adUseClient](properties-collection-ado.md) に設定すると、これらの動的プロパティは、すべてその [Recordset](cursorlocation-property-ado.md) オブジェクトの **Properties** コレクションに追加されます。

