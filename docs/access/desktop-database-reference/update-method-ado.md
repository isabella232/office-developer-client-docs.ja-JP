---
title: Update メソッド (ADO)
TOCTitle: Update Method (ADO)
ms:assetid: fc88cab6-c379-bb4f-530c-da08107924e0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250294(v=office.15)
ms:contentKeyID: 48548893
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 772602b31f83d2255c9fdf1b08fa41541f5fc4da
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884108"
---
# <a name="update-method-ado"></a>Update メソッド (ADO)


**適用されます**Access 2013、Office 2013。

[Recordset](recordset-object-ado.md) オブジェクトのカレント行、または [Record](fields-collection-ado.md) オブジェクトの [Fields](record-object-ado.md) コレクションに加えた変更を保存します。

## <a name="syntax"></a>構文

*レコード セット*です。*フィールド*、*値*を更新します。

*レコード*です。 *フィールド*です。更新

## <a name="parameters"></a>パラメーター

  - *Fields*

  - 省略可能です。変更する単一のフィールドの名前を表すバリアント型 ( **Variant** ) の値、または複数のフィールドの名前か順序を表すバリアント型 ( **Variant** ) の配列を指定します。

  - *Values*

  - 省略可能です。新しいレコードでの単一のフィールドの値を表すバリアント型 ( **Variant** ) の値、または複数のフィールドの値を表すバリアント型 ( **Variant** ) の配列を指定します。

## <a name="remarks"></a>解説

**Recordset**

**Update** メソッドを使用すると、 **AddNew** メソッドを呼び出したか、または既存レコードのいずれかのフィールドの値を変更した時点以降に [Recordset](addnew-method-ado.md) オブジェクトのカレント レコードに加えた変更がすべて保存されます。 **Recordset** オブジェクトが更新をサポートしている必要があります。

フィールドの値を設定するには、次のいずれかを行います。

  - [Field](field-object-ado.md) オブジェクトの [Value](value-property-ado.md) プロパティに値を代入してから、 **Update** メソッドを呼び出します。

  - フィールド名と値を **Update** 呼び出しで引数として渡します。

  - フィールド名の配列と値の配列を **Update** 呼び出しで渡します。

フィールドと値の配列を使用する場合は、両方の配列の要素の数を同じにする必要があります。また、フィールド名の順序がフィールドの値の順序と一致している必要があります。フィールドと値の数と順序が一致していないと、エラーが発生します。

**Recordset** オブジェクトが一括更新をサポートしている場合は、1 つまたは複数のレコードへの複数の変更をローカルにキャッシュしてから、 [UpdateBatch](updatebatch-method-ado.md) メソッドを呼び出すことができます。カレント レコードの編集中、または新しいレコードの追加中に **UpdateBatch** メソッドを呼び出すと、ADO によって自動的に **Update** メソッドが呼び出されてカレント レコードへの保留中の変更が保存されてから、変更内容がまとめてプロバイダーに転送されます。

**Update** メソッドを呼び出すより前に追加中または編集中のレコードから移動すると、ADO によって自動的に **Update** が呼び出されて変更内容が保存されます。カレント レコードに加えた変更を取り消す場合や、新しく追加したレコードを破棄する場合は、 [CancelUpdate](cancelupdate-method-ado.md) メソッドを呼び出す必要があります。

カレント レコードは、 **Update** メソッドを呼び出した後もカレントのままです。

**Record**

**Update** メソッドは、 [Record](fields-collection-ado.md) オブジェクトの **Fields** コレクションへのフィールドの追加、削除、および更新を完了させます。

たとえば、 **Delete** メソッドで削除されたフィールドは、直ちに削除のマークが付けられますが、コレクション内には残されます。これらのフィールドをプロバイダーのコレクションから実際に削除するには、 **Update** メソッドを呼び出す必要があります。

