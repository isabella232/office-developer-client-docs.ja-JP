---
title: AddNew メソッド (ADO)
TOCTitle: AddNew method (ADO)
ms:assetid: bae09be0-5707-4f38-9c74-0acd0f29dbac
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249899(v=office.15)
ms:contentKeyID: 48547384
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 57c174e073313500331a310bab2e0284c1bf4c83
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590073"
---
# <a name="addnew-method-ado"></a>AddNew メソッド (ADO)

**適用先**: Access 2013、Office 2013

更新可能な [Recordset](recordset-object-ado.md) オブジェクトの新しいレコードを作成します。

## <a name="syntax"></a>構文

*recordset*.AddNew *FieldList*, *Values*

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*recordset* |**Recordset** オブジェクトです。|
|*FieldList* |省略可能です。新しいレコード内の単一フィールドの名前であるか、複数フィールドの名前または順序の配列です。|
|*Values* |省略可能です。 1 つの値、または新しいレコード内のフィールドの値の配列。 *Fieldlist が配列* の場合 *、Values* は同じ数のメンバーを持つ配列である必要があります。それ以外の場合は、エラーが発生します。 また、一方の配列におけるフィールド名の順序と、もう一方の配列におけるフィールド値の順序は、一致している必要があります。|

## <a name="remarks"></a>注釈

**AddNew** メソッドは、新しいレコードの作成と初期化に使用します。現在の [Recordset](supports-method-ado.md) オブジェクトにレコードを追加できるかどうかを確認するには、 **Supports** メソッドに [adAddNew](cursoroptionenum.md) ( **CursorOptionEnum** 値) を指定して使用します。

**AddNew** メソッドを呼び出した後は、新しいレコードがカレント レコードになり、 [Update](update-method-ado.md) メソッドを呼び出した後もカレント レコードのままになります。新しいレコードは **Recordset** の最後に追加されるので、Update に続いて **MoveNext** を呼び出すと、 **Recordset** の末尾を超えて移動し、 **EOF** が True になります。 **Recordset** オブジェクトがブックマークをサポートしていない場合は、別のレコードに移動すると、新しいレコードにアクセスできなくなることがあります。カーソルの種類によっては、新規レコードにアクセスするために、 [Requery](requery-method-ado.md) メソッドを呼び出すことが必要になる場合があります。

カレント レコードの編集中または新規レコードの追加中に **AddNew** メソッドを呼び出すと、ADO は **Update** メソッドを呼び出してすべての変更を保存した後、新しいレコードを作成します。

**AddNew** メソッドの動作は、**Recordset** オブジェクトの更新モード、および *Fieldlist* 引数と *Values* 引数を渡すかどうかによって異なります。

即時 *更新* モード (Update メソッドを呼び出した後にプロバイダーが基になるデータソースに変更を書き込む) では、引数を指定せずに **AddNew** メソッドを呼び出して [、EditMode](editmode-property-ado.md)プロパティを **adEditAdd** [(EditModeEnum](editmodeenum.md)値) に設定します。 The provider caches any field value changes locally. Calling the **Update** method posts the new record to the database and resets the **EditMode** property to **adEditNone** (an **EditModeEnum** value). *Fieldlist* 引数と *Values* 引数を渡した場合、ADO は新しいレコードをすぐにデータベースにポストします (**更新** 呼び出しは必要ありません)。**EditMode プロパティの** 値は変更されません **(adEditNone)。**

バッチ *更新* モード (プロバイダーが複数の変更をキャッシュし [、UpdateBatch](updatebatch-method-ado.md) メソッドを呼び出す場合にのみ基になるデータ ソースに書き込む) では、引数なしで **AddNew** メソッドを呼び出して **EditMode** プロパティを **adEditAdd** に設定します。 The provider caches any field value changes locally. Calling the **Update** method adds the new record to the current **Recordset** and resets the **EditMode** property to **adEditNone**, but the provider does not post the changes to the underlying database until you call the **UpdateBatch** method. *引数 Fieldlist* と *Values* を渡した場合、ADO はキャッシュに格納するために新しいレコードをプロバイダーに送信します。新しいレコードを基 **になるデータベースに投稿するには、UpdateBatch** メソッドを呼び出す必要があります。

