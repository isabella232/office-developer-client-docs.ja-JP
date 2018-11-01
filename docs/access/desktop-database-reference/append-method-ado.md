---
title: Append メソッド (ADO)
TOCTitle: Append Method (ADO)
ms:assetid: cca133af-2b95-877d-0488-0d99631623f2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250014(v=office.15)
ms:contentKeyID: 48547742
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e564edccf35822b94c84a931ffff5d3092875e4a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879383"
---
# <a name="append-method-ado"></a>Append メソッド (ADO)


**適用されます**Access 2013、Office 2013。



コレクションにオブジェクトを追加します。コレクションが [Fields](fields-collection-ado.md) である場合は、コレクションに追加する前に、新しい [Field](field-object-ado.md) オブジェクトを作成できます。

## <a name="syntax"></a>構文

*コレクション*です。*オブジェクト*を追加します。

*フィールド*です。*名前*、*種類*、 *DefinedSize*、 *Attrib* *FieldValue*を追加します。

## <a name="parameters"></a>パラメーター

  - *collection*

  - コレクション オブジェクトです。

  - *fields*

  - **Fields** コレクションです。

  - *object*

  - 追加するオブジェクトを表すオブジェクト変数です。

  - *Name*

  - 新しい **Field** オブジェクトの名前を含む文字列型 (**String**) の値です。*fields* に含まれる他のオブジェクトとは異なる名前にする必要があります。

  - *Type*

  - 新しいフィールドのデータ型を指定する [DataTypeEnum](datatypeenum.md) の値です。既定値は **adEmpty** です。 **adIDispatch** 、 **adIUnknown** 、 **adVariant** の各データ型は ADO ではサポートされていないので、 **Recordset** に新しいフィールドを追加するときに、これらのデータ型を使用することはできません。

  - *DefinedSize*

  - 省略可能です。新しいフィールドの定義されたサイズを文字数またはバイト数で表す長整数型 (**Long**) の値です。このパラメーターの既定値は、*Type* によって決まります。DefinedSize が 255 バイトより大きいフィールドは、可変長列として扱われます (既定の *DefinedSize* は指定されません)。

  - *Attrib*

  - 省略可能です。新しいフィールドの属性を指定する [FieldAttributeEnum](fieldattributeenum.md) 値です。既定値は **adFldDefault** です。値を指定しないと、*Type* に基づく属性が設定されます。

  - *FieldValue*

  - 省略可能です。新しいフィールドの値を表すバリアント型 ( **Variant** ) の値です。値を指定しないと、フィールドは Null 値で追加されます。

## <a name="remarks"></a>解説

**Parameters コレクション**

[Parameters](type-property-ado.md) コレクションに追加する前に、 [Parameter](parameter-object-ado.md) オブジェクトの **Type** プロパティを設定する必要があります。可変長データ型を選択する場合は、 [Size](size-property-ado.md) プロパティを 0 より大きい値に設定する必要もあります。

パラメーターを記述することで、ストアド プロシージャまたはパラメーター化されたクエリの使用時に、プロバイダーの呼び出しを最小限に抑えて、パフォーマンスを向上させることができます。ただし、そのためには、呼び出すストアド プロシージャまたはパラメーター化されたクエリに関連するパラメーターのプロパティを把握している必要があります。

[CreateParameter](createparameter-method-ado.md) メソッドを使用して適切なプロパティ設定を備えた **Parameter** オブジェクトを作成し、 **Append** メソッドを使用してオブジェクトを [Parameters](parameters-collection-ado.md) コレクションに追加します。これにより、プロバイダーを呼び出してパラメーター情報を取得しなくても、パラメーターの値を設定したり返したりすることができます。パラメーター情報を提供しないプロバイダーに書き込む場合にパラメーターを使うには、このメソッドを使用して手動で **Parameters** コレクションを設定する必要があります。

**Fields コレクション**

*FieldValue*パラメーターは、**レコード セット**オブジェクトではなく、 [Record](record-object-ado.md)オブジェクトに**Field**オブジェクトを追加する場合にのみ有効です。 **Record** オブジェクトは、フィールドの追加と値の設定を同時に行うことができます。 **Recordset** オブジェクトの場合は、 **Recordset** を閉じた状態でフィールドを作成し、その後、 **Recordset** を開いてフィールドに値を設定する必要があります。


> [!NOTE]
> **Record** オブジェクトの **Fields** コレクションに新しい **Field** オブジェクトを追加した場合は、 [Value](value-property-ado.md) プロパティを最初に設定してから、他の **Field** プロパティを指定する必要があります。まず、 **Value** プロパティに特定の値を割り当て、 [Fields](update-method-ado.md) コレクションで **Update** を呼び出します。その後は、 [Type](type-property-ado.md) や [Attributes](attributes-property-ado.md) などの他のプロパティにアクセスできます。


データ型 (**DataTypeEnum**) が **adArray**、**adChapter**、**adEmpty**、**adPropVariant**、および **adUserDefined** である **Field** オブジェクトは、**Fields** コレクションに追加できません。追加しようとするとエラーが発生します。また、データ型 **adIDispatch**、**adIUnknown**、および **adIVariant** は、ADO ではサポートされていません。これらのデータ型の場合、追加時にエラーは発生しませんが、使用すると、メモリ リークなどの予期しない結果になる可能性があります。

**Recordset**

[CursorLocation](cursorlocation-property-ado.md) プロパティを設定しないで **Append** メソッドを呼び出した場合、 **Recordset** オブジェクトの **Open** メソッドを呼び出すと、 [CursorLocation](cursorlocationenum.md) が自動的に [adUseClient](recordset-object-ado.md) ( [CursorLocationEnum](open-method-ado-recordset.md) 値) に設定されます。

開いている **Recordset** の **Fields** コレクションで、または **ActiveConnection** プロパティが設定されている **Recordset** で [Append](activeconnection-property-ado.md) メソッドを呼び出すと、実行時エラーが発生します。フィールドを追加できるのは、開かれておらず、まだデータ ソースに接続されていない **Recordset** に対してだけです。通常、これは、 **Recordset** オブジェクトが、 [CreateRecordset](createrecordset-method-rds.md) メソッドで作成されている場合、またはオブジェクト変数に割り当てられている場合です。

**Record**

開いている **Record** の **Fields** コレクションで **Append** メソッドを呼び出した場合は、実行時エラーは発生しません。 **Record** オブジェクトの **Fields** コレクションに、新しいフィールドが追加されます。 **Record** が **Recordset** から派生している場合は、 **Recordset** オブジェクトの **Fields** コレクションに新しいフィールドは追加されません。

コレクションに既に存在しているフィールドの場合と同じように、フィールド オブジェクトに値を代入することで、存在しないフィールドを作成して **Fields** コレクションに追加できます。代入により **Field** オブジェクトの自動的な作成と追加が始まり、その後で代入が完了します。

**Field** を **Record** オブジェクトの **Fields** コレクションに追加した後は、 **Fields** コレクションの **Update** メソッドを呼び出して、変更を保存します。

