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
# <a name="append-method-ado"></a><span data-ttu-id="ecf5a-102">Append メソッド (ADO)</span><span class="sxs-lookup"><span data-stu-id="ecf5a-102">Append Method (ADO)</span></span>


<span data-ttu-id="ecf5a-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="ecf5a-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="ecf5a-p101">コレクションにオブジェクトを追加します。コレクションが [Fields](fields-collection-ado.md) である場合は、コレクションに追加する前に、新しい [Field](field-object-ado.md) オブジェクトを作成できます。</span><span class="sxs-lookup"><span data-stu-id="ecf5a-p101">Appends an object to a collection. If the collection is [Fields](fields-collection-ado.md), a new [Field](field-object-ado.md) object may be created before it is appended to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="ecf5a-106">構文</span><span class="sxs-lookup"><span data-stu-id="ecf5a-106">Syntax</span></span>

<span data-ttu-id="ecf5a-107">*コレクション*です。*オブジェクト*を追加します。</span><span class="sxs-lookup"><span data-stu-id="ecf5a-107">*collection*.Append *object*</span></span>

<span data-ttu-id="ecf5a-108">*フィールド*です。*名前*、*種類*、 *DefinedSize*、 *Attrib* *FieldValue*を追加します。</span><span class="sxs-lookup"><span data-stu-id="ecf5a-108">*fields*.Append *Name*, *Type*, *DefinedSize*, *Attrib*, *FieldValue*</span></span>

## <a name="parameters"></a><span data-ttu-id="ecf5a-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ecf5a-109">Parameters</span></span>

  - <span data-ttu-id="ecf5a-110">*collection*</span><span class="sxs-lookup"><span data-stu-id="ecf5a-110">*collection*</span></span>

  - <span data-ttu-id="ecf5a-111">コレクション オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="ecf5a-111">A collection object.</span></span>

  - <span data-ttu-id="ecf5a-112">*fields*</span><span class="sxs-lookup"><span data-stu-id="ecf5a-112">*fields*</span></span>

  - <span data-ttu-id="ecf5a-113">**Fields** コレクションです。</span><span class="sxs-lookup"><span data-stu-id="ecf5a-113">A **Fields** collection.</span></span>

  - <span data-ttu-id="ecf5a-114">*object*</span><span class="sxs-lookup"><span data-stu-id="ecf5a-114">*object*</span></span>

  - <span data-ttu-id="ecf5a-115">追加するオブジェクトを表すオブジェクト変数です。</span><span class="sxs-lookup"><span data-stu-id="ecf5a-115">An object variable that represents the object to be appended.</span></span>

  - <span data-ttu-id="ecf5a-116">*Name*</span><span class="sxs-lookup"><span data-stu-id="ecf5a-116">*Name*</span></span>

  - <span data-ttu-id="ecf5a-117">新しい **Field** オブジェクトの名前を含む文字列型 (**String**) の値です。*fields* に含まれる他のオブジェクトとは異なる名前にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ecf5a-117">A **String** value that contains the name of the new **Field** object, and must not be the same name as any other object in *fields*.</span></span>

  - <span data-ttu-id="ecf5a-118">*Type*</span><span class="sxs-lookup"><span data-stu-id="ecf5a-118">*Type*</span></span>

  - <span data-ttu-id="ecf5a-p102">新しいフィールドのデータ型を指定する [DataTypeEnum](datatypeenum.md) の値です。既定値は **adEmpty** です。 **adIDispatch** 、 **adIUnknown** 、 **adVariant** の各データ型は ADO ではサポートされていないので、 **Recordset** に新しいフィールドを追加するときに、これらのデータ型を使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="ecf5a-p102">A [DataTypeEnum](datatypeenum.md) value, whose default value is **adEmpty**, that specifies the data type of the new field. The following data types are not supported by ADO, and should not be used when appending new fields to a **Recordset**: **adIDispatch**, **adIUnknown**, **adVariant**.</span></span>

  - <span data-ttu-id="ecf5a-121">*DefinedSize*</span><span class="sxs-lookup"><span data-stu-id="ecf5a-121">*DefinedSize*</span></span>

  - <span data-ttu-id="ecf5a-p103">省略可能です。新しいフィールドの定義されたサイズを文字数またはバイト数で表す長整数型 (**Long**) の値です。このパラメーターの既定値は、*Type* によって決まります。DefinedSize が 255 バイトより大きいフィールドは、可変長列として扱われます (既定の *DefinedSize* は指定されません)。</span><span class="sxs-lookup"><span data-stu-id="ecf5a-p103">Optional. A **Long** value that represents the defined size, in characters or bytes, of the new field. The default value for this parameter is derived from *Type*. Fields with a DefinedSize greater than 255 bytes, and treated as variable length columns. (The default *DefinedSize* is unspecified.)</span></span>

  - <span data-ttu-id="ecf5a-127">*Attrib*</span><span class="sxs-lookup"><span data-stu-id="ecf5a-127">*Attrib*</span></span>

  - <span data-ttu-id="ecf5a-p104">省略可能です。新しいフィールドの属性を指定する [FieldAttributeEnum](fieldattributeenum.md) 値です。既定値は **adFldDefault** です。値を指定しないと、*Type* に基づく属性が設定されます。</span><span class="sxs-lookup"><span data-stu-id="ecf5a-p104">Optional. A [FieldAttributeEnum](fieldattributeenum.md) value, whose default value is **adFldDefault**, that specifies attributes for the new field. If this value is not specified, the field will contain attributes derived from *Type*.</span></span>

  - <span data-ttu-id="ecf5a-131">*FieldValue*</span><span class="sxs-lookup"><span data-stu-id="ecf5a-131">*FieldValue*</span></span>

  - <span data-ttu-id="ecf5a-p105">省略可能です。新しいフィールドの値を表すバリアント型 ( **Variant** ) の値です。値を指定しないと、フィールドは Null 値で追加されます。</span><span class="sxs-lookup"><span data-stu-id="ecf5a-p105">Optional. A **Variant** that represents the value for the new field. If not specified, then the field is appended with a null value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ecf5a-135">解説</span><span class="sxs-lookup"><span data-stu-id="ecf5a-135">Remarks</span></span>

<span data-ttu-id="ecf5a-136">**Parameters コレクション**</span><span class="sxs-lookup"><span data-stu-id="ecf5a-136">**Parameters Collection**</span></span>

<span data-ttu-id="ecf5a-p106">[Parameters](type-property-ado.md) コレクションに追加する前に、 [Parameter](parameter-object-ado.md) オブジェクトの **Type** プロパティを設定する必要があります。可変長データ型を選択する場合は、 [Size](size-property-ado.md) プロパティを 0 より大きい値に設定する必要もあります。</span><span class="sxs-lookup"><span data-stu-id="ecf5a-p106">You must set the [Type](type-property-ado.md) property of a [Parameter](parameter-object-ado.md) object before appending it to the **Parameters** collection. If you select a variable-length data type, you must also set the [Size](size-property-ado.md) property to a value greater than zero.</span></span>

<span data-ttu-id="ecf5a-p107">パラメーターを記述することで、ストアド プロシージャまたはパラメーター化されたクエリの使用時に、プロバイダーの呼び出しを最小限に抑えて、パフォーマンスを向上させることができます。ただし、そのためには、呼び出すストアド プロシージャまたはパラメーター化されたクエリに関連するパラメーターのプロパティを把握している必要があります。</span><span class="sxs-lookup"><span data-stu-id="ecf5a-p107">Describing parameters yourself minimizes calls to the provider and consequently improves performance when using stored procedures or parameterized queries. However, you must know the properties of the parameters associated with the stored procedure or parameterized query that you want to call.</span></span>

<span data-ttu-id="ecf5a-p108">[CreateParameter](createparameter-method-ado.md) メソッドを使用して適切なプロパティ設定を備えた **Parameter** オブジェクトを作成し、 **Append** メソッドを使用してオブジェクトを [Parameters](parameters-collection-ado.md) コレクションに追加します。これにより、プロバイダーを呼び出してパラメーター情報を取得しなくても、パラメーターの値を設定したり返したりすることができます。パラメーター情報を提供しないプロバイダーに書き込む場合にパラメーターを使うには、このメソッドを使用して手動で **Parameters** コレクションを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ecf5a-p108">Use the [CreateParameter](createparameter-method-ado.md) method to create **Parameter** objects with the appropriate property settings and use the **Append** method to add them to the [Parameters](parameters-collection-ado.md) collection. This lets you set and return parameter values without having to call the provider for the parameter information. If you are writing to a provider that does not supply parameter information, you must use this method to manually populate the **Parameters** collection in order to use parameters at all.</span></span>

<span data-ttu-id="ecf5a-144">**Fields コレクション**</span><span class="sxs-lookup"><span data-stu-id="ecf5a-144">**Fields Collection**</span></span>

<span data-ttu-id="ecf5a-145">*FieldValue*パラメーターは、**レコード セット**オブジェクトではなく、 [Record](record-object-ado.md)オブジェクトに**Field**オブジェクトを追加する場合にのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="ecf5a-145">The *FieldValue* parameter is only valid when adding a **Field** object to a [Record](record-object-ado.md) object, not to a **Recordset** object.</span></span> <span data-ttu-id="ecf5a-146">**Record** オブジェクトは、フィールドの追加と値の設定を同時に行うことができます。</span><span class="sxs-lookup"><span data-stu-id="ecf5a-146">With a **Record** object, you may append fields and provide values at the same time.</span></span> <span data-ttu-id="ecf5a-147">**Recordset** オブジェクトの場合は、 **Recordset** を閉じた状態でフィールドを作成し、その後、 **Recordset** を開いてフィールドに値を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ecf5a-147">With a **Recordset** object, you must create fields while the **Recordset** is closed, then open the **Recordset** and assign values to the fields.</span></span>


> [!NOTE]
> <span data-ttu-id="ecf5a-p110">**Record** オブジェクトの **Fields** コレクションに新しい **Field** オブジェクトを追加した場合は、 [Value](value-property-ado.md) プロパティを最初に設定してから、他の **Field** プロパティを指定する必要があります。まず、 **Value** プロパティに特定の値を割り当て、 [Fields](update-method-ado.md) コレクションで **Update** を呼び出します。その後は、 [Type](type-property-ado.md) や [Attributes](attributes-property-ado.md) などの他のプロパティにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="ecf5a-p110">For new **Field** objects that have been appended to the **Fields** collection of a **Record** object, the [Value](value-property-ado.md) property must be set before any other **Field** properties can be specified. First, a specific value for the **Value** property must have been assigned and [Update](update-method-ado.md) on the **Fields** collection called. Then, other properties such as [Type](type-property-ado.md) or [Attributes](attributes-property-ado.md) can be accessed.</span></span>


<span data-ttu-id="ecf5a-p111">データ型 (**DataTypeEnum**) が **adArray**、**adChapter**、**adEmpty**、**adPropVariant**、および **adUserDefined** である **Field** オブジェクトは、**Fields** コレクションに追加できません。追加しようとするとエラーが発生します。また、データ型 **adIDispatch**、**adIUnknown**、および **adIVariant** は、ADO ではサポートされていません。これらのデータ型の場合、追加時にエラーは発生しませんが、使用すると、メモリ リークなどの予期しない結果になる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ecf5a-p111">**Field** objects of the following data types (**DataTypeEnum**) cannot be appended to the **Fields** collection and will cause an error to occur: **adArray**, **adChapter**, **adEmpty**, **adPropVariant**, and **adUserDefined**. Also, the following data types are not supported by ADO: **adIDispatch**, **adIUnknown**, and **adIVariant**. For these types, no error will occur when appended, but usage can produce unpredictable results including memory leaks.</span></span>

<span data-ttu-id="ecf5a-154">**Recordset**</span><span class="sxs-lookup"><span data-stu-id="ecf5a-154">**Recordset**</span></span>

<span data-ttu-id="ecf5a-155">[CursorLocation](cursorlocation-property-ado.md) プロパティを設定しないで **Append** メソッドを呼び出した場合、 **Recordset** オブジェクトの **Open** メソッドを呼び出すと、 [CursorLocation](cursorlocationenum.md) が自動的に [adUseClient](recordset-object-ado.md) ( [CursorLocationEnum](open-method-ado-recordset.md) 値) に設定されます。</span><span class="sxs-lookup"><span data-stu-id="ecf5a-155">If you do not set the [CursorLocation](cursorlocation-property-ado.md) property before calling the **Append** method, **CursorLocation** will be set to **adUseClient** (a [CursorLocationEnum](cursorlocationenum.md) value) automatically when the [Recordset](recordset-object-ado.md) object's [Open](open-method-ado-recordset.md) method is called.</span></span>

<span data-ttu-id="ecf5a-p112">開いている **Recordset** の **Fields** コレクションで、または **ActiveConnection** プロパティが設定されている **Recordset** で [Append](activeconnection-property-ado.md) メソッドを呼び出すと、実行時エラーが発生します。フィールドを追加できるのは、開かれておらず、まだデータ ソースに接続されていない **Recordset** に対してだけです。通常、これは、 **Recordset** オブジェクトが、 [CreateRecordset](createrecordset-method-rds.md) メソッドで作成されている場合、またはオブジェクト変数に割り当てられている場合です。</span><span class="sxs-lookup"><span data-stu-id="ecf5a-p112">A run-time error will occur if the **Append** method is called on the **Fields** collection of an open **Recordset**, or on a **Recordset** where the [ActiveConnection](activeconnection-property-ado.md) property has been set. You can only append fields to a **Recordset** that is not open and has not yet been connected to a data source. This is typically the case when a **Recordset** object is fabricated with the [CreateRecordset](createrecordset-method-rds.md) method or assigned to an object variable.</span></span>

<span data-ttu-id="ecf5a-159">**Record**</span><span class="sxs-lookup"><span data-stu-id="ecf5a-159">**Record**</span></span>

<span data-ttu-id="ecf5a-p113">開いている **Record** の **Fields** コレクションで **Append** メソッドを呼び出した場合は、実行時エラーは発生しません。 **Record** オブジェクトの **Fields** コレクションに、新しいフィールドが追加されます。 **Record** が **Recordset** から派生している場合は、 **Recordset** オブジェクトの **Fields** コレクションに新しいフィールドは追加されません。</span><span class="sxs-lookup"><span data-stu-id="ecf5a-p113">A run-time error will not occur if the **Append** method is called on the **Fields** collection of an open **Record**. The new field will be added to the **Record** object's **Fields** collection. If the **Record** was derived from a **Recordset**, then the new field will not appear in the **Recordset** object's **Fields** collection.</span></span>

<span data-ttu-id="ecf5a-p114">コレクションに既に存在しているフィールドの場合と同じように、フィールド オブジェクトに値を代入することで、存在しないフィールドを作成して **Fields** コレクションに追加できます。代入により **Field** オブジェクトの自動的な作成と追加が始まり、その後で代入が完了します。</span><span class="sxs-lookup"><span data-stu-id="ecf5a-p114">A non-existent field can be created and appended to the **Fields** collection by assigning a value to the field object as if it already existed in the collection. The assignment will trigger the automatic creation and appending of the **Field** object, then the assignment will be completed.</span></span>

<span data-ttu-id="ecf5a-165">**Field** を **Record** オブジェクトの **Fields** コレクションに追加した後は、 **Fields** コレクションの **Update** メソッドを呼び出して、変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="ecf5a-165">After appending a **Field** to a **Record** object's **Fields** collection, call the **Update** method of the **Fields** collection to save the change.</span></span>

