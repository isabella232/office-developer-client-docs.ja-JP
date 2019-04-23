---
title: AddNew メソッド (ADO)
TOCTitle: AddNew method (ADO)
ms:assetid: bae09be0-5707-4f38-9c74-0acd0f29dbac
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249899(v=office.15)
ms:contentKeyID: 48547384
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f733c574ba7927587c6fcb6305a361ca1070de0f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282514"
---
# <a name="addnew-method-ado"></a>AddNew メソッド (ADO)

**適用先:** Access 2013、Office 2013

更新可能な [Recordset](recordset-object-ado.md) オブジェクトの新しいレコードを作成します。

## <a name="syntax"></a>構文

*recordset*。AddNew *FieldList*、*値*

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*recordset* |**Recordset** オブジェクトです。|
|*FieldList* |省略可能です。 新しいレコード内の単一フィールドの名前であるか、複数フィールドの名前または順序の配列です。|
|*Values* |省略可能です。 新しいレコードのフィールドの値の1つまたは複数の配列。 *Fieldlist*が配列の場合は、*値*も同じ数のメンバーの配列である必要があります。それ以外の場合は、エラーが発生します。 また、一方の配列におけるフィールド名の順序と、もう一方の配列におけるフィールド値の順序は、一致している必要があります。|

## <a name="remarks"></a>注釈

**AddNew** メソッドは、新しいレコードの作成と初期化に使用します。現在の [Recordset](supports-method-ado.md) オブジェクトにレコードを追加できるかどうかを確認するには、 **Supports** メソッドに [adAddNew](cursoroptionenum.md) ( **CursorOptionEnum** 値) を指定して使用します。

**AddNew** メソッドを呼び出した後は、新しいレコードがカレント レコードになり、 [Update](update-method-ado.md) メソッドを呼び出した後もカレント レコードのままになります。新しいレコードは **Recordset** の最後に追加されるので、Update に続いて **MoveNext** を呼び出すと、 **Recordset** の末尾を超えて移動し、 **EOF** が True になります。 **Recordset** オブジェクトがブックマークをサポートしていない場合は、別のレコードに移動すると、新しいレコードにアクセスできなくなることがあります。カーソルの種類によっては、新規レコードにアクセスするために、 [Requery](requery-method-ado.md) メソッドを呼び出すことが必要になる場合があります。

カレント レコードの編集中または新規レコードの追加中に **AddNew** メソッドを呼び出すと、ADO は **Update** メソッドを呼び出してすべての変更を保存した後、新しいレコードを作成します。

**AddNew** メソッドの動作は、**Recordset** オブジェクトの更新モード、および *Fieldlist* 引数と *Values* 引数を渡すかどうかによって異なります。

*即時更新モード*( **update**メソッドを呼び出した後、プロバイダーが基になるデータソースに変更を書き込む場合) では、引数を指定せずに**AddNew**メソッドを呼び出すと、 [EditMode](editmode-property-ado.md)プロパティが**adEditAdd**に設定されます ([editmodeenum](editmodeenum.md)値)。 The provider caches any field value changes locally. Calling the **Update** method posts the new record to the database and resets the **EditMode** property to **adEditNone** (an **EditModeEnum** value). *Fieldlist*引数と*Values*引数を渡すと、ADO によって新しいレコードがすぐにデータベースにポストされます (**更新**呼び出しは必要ありません)。**EditMode**プロパティの値は変更されません (**adEditNone**)。

*バッチ更新モード*(プロバイダーが複数の変更をキャッシュし、 [UpdateBatch](updatebatch-method-ado.md)メソッドを呼び出したときに、基になるデータソースにその変更を書き込む場合)、引数を指定せずに**AddNew**メソッドを呼び出すと、 **EditMode**が設定されます。プロパティを**adEditAdd**にします。 The provider caches any field value changes locally. Calling the **Update** method adds the new record to the current **Recordset** and resets the **EditMode** property to **adEditNone**, but the provider does not post the changes to the underlying database until you call the **UpdateBatch** method. *Fieldlist*引数と*Values*引数を渡すと、ADO はキャッシュに格納されているプロバイダーに新しいレコードを送信します。新しいレコードを基になるデータベースにポストするには、 **UpdateBatch**メソッドを呼び出す必要があります。

