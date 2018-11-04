---
title: AddNew メソッド (ADO)
TOCTitle: AddNew method (ADO)
ms:assetid: bae09be0-5707-4f38-9c74-0acd0f29dbac
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249899(v=office.15)
ms:contentKeyID: 48547384
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 54217fdfe40bd8fea9b94ac78f1e05d2d94daa71
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949986"
---
# <a name="addnew-method-ado"></a>AddNew メソッド (ADO)

**適用されます**Access 2013、Office 2013。

更新可能な [Recordset](recordset-object-ado.md) オブジェクトの新しいレコードを作成します。

## <a name="syntax"></a>構文

*レコード セット*です。AddNew *FieldList*、*値*

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*recordset* |**Recordset** オブジェクトです。|
|*FieldList* |省略可能です。新しいレコード内の単一フィールドの名前であるか、複数フィールドの名前または順序の配列です。|
|*Values* |省略可能です。 1 つの値、または新しいレコードのフィールドの値の配列。 *Fieldlist*が配列の場合は、*値*配列と同じ数のメンバーにもする必要があります。それ以外の場合、エラーが発生します。 また、一方の配列におけるフィールド名の順序と、もう一方の配列におけるフィールド値の順序は、一致している必要があります。|

## <a name="remarks"></a>解説

**AddNew** メソッドは、新しいレコードの作成と初期化に使用します。現在の [Recordset](supports-method-ado.md) オブジェクトにレコードを追加できるかどうかを確認するには、 **Supports** メソッドに [adAddNew](cursoroptionenum.md) ( **CursorOptionEnum** 値) を指定して使用します。

**AddNew** メソッドを呼び出した後は、新しいレコードがカレント レコードになり、 [Update](update-method-ado.md) メソッドを呼び出した後もカレント レコードのままになります。新しいレコードは **Recordset** の最後に追加されるので、Update に続いて **MoveNext** を呼び出すと、 **Recordset** の末尾を超えて移動し、 **EOF** が True になります。 **Recordset** オブジェクトがブックマークをサポートしていない場合は、別のレコードに移動すると、新しいレコードにアクセスできなくなることがあります。カーソルの種類によっては、新規レコードにアクセスするために、 [Requery](requery-method-ado.md) メソッドを呼び出すことが必要になる場合があります。

カレント レコードの編集中または新規レコードの追加中に **AddNew** メソッドを呼び出すと、ADO は **Update** メソッドを呼び出してすべての変更を保存した後、新しいレコードを作成します。

**AddNew**メソッドの動作は、**レコード セット**オブジェクトと、 *Fieldlist*と*値*の引数を渡すかどうかの更新モードに依存します。

*イミディ エイト更新モード*(のプロバイダーに変更を書き込みます基底のデータ ソース**の更新**メソッドを呼び出すと)、 **adEditAdd** ( [EditMode](editmode-property-ado.md)プロパティを設定する引数を指定しないで**AddNew**メソッドを呼び出す[EditModeEnum](editmodeenum.md)値)。 プロバイダーは、ローカルでのフィールド値の変更をキャッシュします。 **Update**メソッドを呼び出してデータベースに新しいレコードを転記し、 **EditMode**プロパティが**adEditNone** ( **EditModeEnum**値) にリセットします。 ADO が ( **Update**呼び出し必要はありません)、データベースに新しいレコードをすぐに投稿、 *Fieldlist*と*値*の引数を渡す場合**EditMode**プロパティの値には、(**adEditNone**) は変更されません。

*バッチ更新モード*(をプロバイダー複数の変更をキャッシュし、 [UpdateBatch](updatebatch-method-ado.md)メソッドを呼び出した場合にのみ、基になるデータ ソースに書き込みます)、 **EditMode**を設定する引数を指定しないで**AddNew**メソッドを呼び出す**adEditAdd**プロパティです。 プロバイダーは、ローカルでのフィールド値の変更をキャッシュします。 **UpdateBatch が呼び出されるまで、プロバイダーは基になるデータベースへの変更 post しないですが、現在の**レコード セット**に新しいレコードを追加します。 **Update**メソッドを呼び出すと、 **EditMode**プロパティが**adEditNone**にリセット**メソッドです。 ADO がプロバイダーをキャッシュに格納するために新しいレコードを送信する、 *Fieldlist*と*値*の引数を渡す場合**UpdateBatch**メソッドを呼び出して基になるデータベースに新しいレコードを転記する必要があります。

