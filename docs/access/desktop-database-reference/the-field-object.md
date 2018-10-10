---
title: フィールド オブジェクト (デスクトップ データベース参照のアクセス)
TOCTitle: The Field Object
ms:assetid: 55531e04-d74f-6394-df64-1660e5d572ca
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249284(v=office.15)
ms:contentKeyID: 48544926
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 760e4cd3ebc3192ee63a790009398f2bc1e6d1c7
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476895"
---
# <a name="field-object"></a><span data-ttu-id="68fa5-102">Field オブジェクト</span><span class="sxs-lookup"><span data-stu-id="68fa5-102">Field Object</span></span>


<span data-ttu-id="68fa5-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="68fa5-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="68fa5-p101">各 **Field** オブジェクトは、通常、データベース テーブル内の列に対応しています。ただし、 **Field** では、チャプターと呼ばれる他の **Recordset** へのポインターを表すこともできます。チャプター列などの例外については、このガイドの後半で説明します。</span><span class="sxs-lookup"><span data-stu-id="68fa5-p101">Each **Field** object usually corresponds to a column in a database table. However, a **Field** can also represent a pointer to another **Recordset**, called a chapter. Exceptions, such as chapter columns, will be covered later in this guide.</span></span>

<span data-ttu-id="68fa5-p102">**Field** オブジェクトの **Value** プロパティを使用すると、カレント レコードのデータを設定または返すことができます。プロバイダーが公開している機能によっては、 **Field** オブジェクトの一部のコレクション、メソッド、またはプロパティを使用できない場合があります。</span><span class="sxs-lookup"><span data-stu-id="68fa5-p102">Use the **Value** property of **Field** objects to set or return data for the current record. Depending on the functionality the provider exposes, some collections, methods, or properties of a **Field** object may not be available.</span></span>

<span data-ttu-id="68fa5-109">**Field** オブジェクトのコレクション、メソッド、およびプロパティを使用すると、次の操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="68fa5-109">With the collections, methods, and properties of a **Field** object, you can do the following:</span></span>

  - <span data-ttu-id="68fa5-110">**Name** プロパティを使用して、フィールドの名前を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="68fa5-110">Return the name of a field by using the **Name** property.</span></span>

  - <span data-ttu-id="68fa5-p103">**Value** プロパティを使用して、フィールド内のデータを表示または変更できます。 **Value** は、 **Field** オブジェクトの既定のプロパティです。</span><span class="sxs-lookup"><span data-stu-id="68fa5-p103">View or change the data in the field by using the **Value** property. **Value** is the default property of the **Field** object.</span></span>

  - <span data-ttu-id="68fa5-113">**Type** 、 **Precision** 、および **NumericScale** の各プロパティを使用して、フィールドの基本的な特性を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="68fa5-113">Return the basic characteristics of a field by using the **Type**, **Precision**, and **NumericScale** properties.</span></span>

  - <span data-ttu-id="68fa5-114">**DefinedSize** プロパティを使用して、フィールドの宣言されたサイズを返すことができます。</span><span class="sxs-lookup"><span data-stu-id="68fa5-114">Return the declared size of a field by using the **DefinedSize** property.</span></span>

  - <span data-ttu-id="68fa5-115">**ActualSize** プロパティを使用して、特定のフィールドに含まれるデータの実際のサイズを返すことができます。</span><span class="sxs-lookup"><span data-stu-id="68fa5-115">Return the actual size of the data in a given field by using the **ActualSize** property.</span></span>

  - <span data-ttu-id="68fa5-116">**Attributes** プロパティおよび **Properties** コレクションを使用して、特定のフィールドについてサポートされている機能の種類を確認できます。</span><span class="sxs-lookup"><span data-stu-id="68fa5-116">Determine what types of functionality are supported for a given field by using the **Attributes** property and **Properties** collection.</span></span>

  - <span data-ttu-id="68fa5-117">**AppendChunk** メソッドおよび **GetChunk** メソッドを使用して、長いバイナリ データまたは長い文字データを含むフィールドの値を操作できます。</span><span class="sxs-lookup"><span data-stu-id="68fa5-117">Manipulate the values of fields containing long binary or long character data by using the **AppendChunk** and **GetChunk** methods.</span></span>

<span data-ttu-id="68fa5-118">プロバイダーがバッチ更新をサポートしている場合は、 **OriginalValue** プロパティおよび **UnderlyingValue** プロパティを使用して、バッチ更新中に発生するフィールドの値の不一致を解決できます。</span><span class="sxs-lookup"><span data-stu-id="68fa5-118">Resolve discrepancies in field values during batch updating by using the **OriginalValue** and **UnderlyingValue** properties, if the provider supports batch updates.</span></span>

## <a name="describing-a-field"></a><span data-ttu-id="68fa5-119">フィールドに関する情報を記述する</span><span class="sxs-lookup"><span data-stu-id="68fa5-119">Describing a Field</span></span>

<span data-ttu-id="68fa5-p104">以降のトピックでは、[Field](field-object-ado.md) オブジェクト自体に関する情報、つまりフィールドのメタデータを表す **Field** オブジェクトのプロパティについて説明します。この情報を使用すると、 **Recordset** のスキーマについて多くのことを確認できます。これらのプロパティには、 **Type** 、 **DefinedSize** と **ActualSize** 、 **Name** 、 **NumericScale** と **Precision** などがあります。</span><span class="sxs-lookup"><span data-stu-id="68fa5-p104">The topics that follow will discuss properties of the [Field](field-object-ado.md) object that represent information that describes the **Field** object itself — that is, metadata about the field. This information can be used to determine much about the schema of the **Recordset**. These properties include **Type**, **DefinedSize** and **ActualSize**, **Name**, and **NumericScale** and **Precision**.</span></span>

## <a name="discovering-the-data-type"></a><span data-ttu-id="68fa5-123">データ型を確認する</span><span class="sxs-lookup"><span data-stu-id="68fa5-123">Discovering the Data Type</span></span>

<span data-ttu-id="68fa5-124">**Type**プロパティは、フィールドのデータ型を示します。</span><span class="sxs-lookup"><span data-stu-id="68fa5-124">The **Type** property indicates the data type of the field.</span></span> <span data-ttu-id="68fa5-125">ADO でサポートされているデータ型の列挙定数については、 *ADO プログラマーズ リファレンス*に[格納](datatypeenum.md)してください。</span><span class="sxs-lookup"><span data-stu-id="68fa5-125">The data type enumerated constants that are supported by ADO are described in [DataTypeEnum](datatypeenum.md) in the *ADO Programmer's Reference*.</span></span>

<span data-ttu-id="68fa5-p106">**adNumeric** などの浮動小数点型については、より多くの情報を取得できます。 **NumericScale** プロパティは、 **Field** の値を表現するために使用する小数部の桁数を示します。 **Precision** プロパティは、 **Field** の値を表現するために使用する最大桁数を指定します。</span><span class="sxs-lookup"><span data-stu-id="68fa5-p106">For floating point numeric types such **adNumeric**, you can obtain more information. The **NumericScale** property indicates how many digits to the right of the decimal point will be used to represent values for the **Field**. The **Precision** property specifies the maximum number of digits used to represent values for the **Field**.</span></span>

## <a name="determining-field-size"></a><span data-ttu-id="68fa5-129">フィールドのサイズを確認する</span><span class="sxs-lookup"><span data-stu-id="68fa5-129">Determining Field Size</span></span>

<span data-ttu-id="68fa5-130">**DefinedSize** プロパティを使用すると、 **Field** オブジェクトのデータ容量を確認できます。</span><span class="sxs-lookup"><span data-stu-id="68fa5-130">Use the **DefinedSize** property to determine the data capacity of a **Field** object.</span></span>

<span data-ttu-id="68fa5-p107">**ActualSize** プロパティを使用すると、 **Field** オブジェクトの値の実際の長さを返すことができます。 **ActualSize** プロパティは、すべてのフィールドについて読み取り専用です。ADO によって **Field** オブジェクトの値の長さが特定できない場合、 **ActualSize** プロパティは **adUnknown** を返します。</span><span class="sxs-lookup"><span data-stu-id="68fa5-p107">Use the **ActualSize** property to return the actual length of a **Field** object's value. For all fields, the **ActualSize** property is read-only. If ADO cannot determine the length of the **Field** object's value, the **ActualSize** property returns **adUnknown**.</span></span>

<span data-ttu-id="68fa5-p108">**DefinedSize** プロパティと **ActualSize** プロパティの目的は異なります。たとえば、宣言された型が **adVarChar** で、 **DefinedSize** プロパティの値が 50 である **Field** オブジェクトに、文字が 1 つだけ含まれているとします。この場合、返される **ActualSize** プロパティの値は、この 1 文字のバイト単位の長さとなります。</span><span class="sxs-lookup"><span data-stu-id="68fa5-p108">The **DefinedSize** and **ActualSize** properties have different purposes. For example, consider a **Field** object with a declared type of **adVarChar** and a **DefinedSize** property value of 50, containing a single character. The **ActualSize** property value it returns is the length in bytes of the single character.</span></span>

## <a name="determining-field-contents"></a><span data-ttu-id="68fa5-137">フィールドの内容を確認する</span><span class="sxs-lookup"><span data-stu-id="68fa5-137">Determining Field Contents</span></span>

<span data-ttu-id="68fa5-p109">データ ソースから取得された列の識別子は、 **Field** の **Name** プロパティで表されます。 **Field** オブジェクトの **Value** プロパティは、フィールドの実際の値を返したり、設定したりするために使用します。これは既定のプロパティです。</span><span class="sxs-lookup"><span data-stu-id="68fa5-p109">The identifier of the column from the data source is represented by the **Name** property of the **Field**. The **Value** property of the **Field** object returns or sets the actual data content of the field. This is the default property.</span></span>

<span data-ttu-id="68fa5-p110">フィールドの値を変更するには、 **Value** プロパティを適切な型の新しい値に設定します。フィールドの内容を変更するためには、使用しているカーソルが更新をサポートしている必要があります。バッチ モードでは、この時点でデータベースの検証が行われないため、 **UpdateBatch** を呼び出すときにエラーがないことを確認する必要があります。一部のプロバイダーは、ADO **Field** オブジェクトの **UnderlyingValue** プロパティと **OriginalValue** プロパティをサポートしており、バッチ更新を実行しようとしたときに発生する競合の解決に役立ちます。そのような競合の解決方法の詳細については、「 [4 章: データを編集する](chapter-4-editing-data.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="68fa5-p110">To change the data in a field, set the **Value** property equal to a new value of the correct type. Your cursor type must support updates to change the contents of a field. Database validation is not done here in batch mode, so you will need to check for errors when you call **UpdateBatch** in such a case. Some providers also support the ADO **Field** object's **UnderlyingValue** and **OriginalValue** properties to assist you with resolving conflicts when you attempt to perform batch updates. For details about how to resolve such conflicts, see [Chapter 4: Editing Data](chapter-4-editing-data.md).</span></span>


> [!NOTE]
> <P><span data-ttu-id="68fa5-p111">[!メモ] 新しい <STRONG>Field</STRONG> を <STRONG>Recordset</STRONG> に追加する場合は、 <STRONG>Recordset Field</STRONG> の値を設定できません。新しい <STRONG>Field</STRONG> は、閉じている <STRONG>Recordset</STRONG> に追加できます。追加した後に <STRONG>Recordset</STRONG> を開いて、これらの新しい <STRONG>Field</STRONG> に値を割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="68fa5-p111"><STRONG>Recordset Field</STRONG> values cannot be set when appending new <STRONG>Fields</STRONG> to a <STRONG>Recordset</STRONG>. Rather, new <STRONG>Fields</STRONG> can be appended to a closed <STRONG>Recordset</STRONG>. Then the <STRONG>Recordset</STRONG> must be opened, and only then can values be assigned to these <STRONG>Fields</STRONG>.</span></span></P>



## <a name="getting-more-field-information"></a><span data-ttu-id="68fa5-149">フィールドに関する詳細情報を取得する</span><span class="sxs-lookup"><span data-stu-id="68fa5-149">Getting More Field Information</span></span>

<span data-ttu-id="68fa5-p112">ADO オブジェクトには、組み込みのプロパティと動的プロパティという 2 種類のプロパティがあります。これまでは、 **Field** オブジェクトの組み込みのプロパティについてのみ説明してきました。</span><span class="sxs-lookup"><span data-stu-id="68fa5-p112">ADO objects have two types of properties: built-in and dynamic. To this point, only the built-in properties of the **Field** object have been discussed.</span></span>

<span data-ttu-id="68fa5-152">組み込みのプロパティは、これらのプロパティは、ADO に実装されていると、構文を使用して、すべての新しいオブジェクトにすぐに利用可能です。</span><span class="sxs-lookup"><span data-stu-id="68fa5-152">Built-in properties are those properties implemented in ADO and immediately available to any new object, using the syntax.</span></span> <span data-ttu-id="68fa5-153">これらのプロパティは、オブジェクトの **Properties** コレクションに **Property** オブジェクトとして格納されません。</span><span class="sxs-lookup"><span data-stu-id="68fa5-153">They do not appear as **Property** objects in an object's **Properties** collection.</span></span>

<span data-ttu-id="68fa5-154">動的プロパティは、基になるデータ プロバイダーによって定義され、該当する ADO オブジェクトの **Properties** コレクションに含まれます。</span><span class="sxs-lookup"><span data-stu-id="68fa5-154">Dynamic properties are defined by the underlying data provider, and appear in the **Properties** collection for the appropriate ADO object.</span></span> <span data-ttu-id="68fa5-155">たとえば、プロバイダー固有のプロパティには、 **Recordset** オブジェクトがトランザクションや更新をサポートしているかどうかを示すものがあります。</span><span class="sxs-lookup"><span data-stu-id="68fa5-155">For example, a property specific to the provider may indicate if a **Recordset** object supports transactions or updating.</span></span> <span data-ttu-id="68fa5-156">これらの追加のプロパティは、その **Recordset** オブジェクトの **Properties** コレクションに、 **Property** オブジェクトとして格納されます。</span><span class="sxs-lookup"><span data-stu-id="68fa5-156">These additional properties will appear as **Property** objects in that **Recordset** object's **Properties** collection.</span></span> <span data-ttu-id="68fa5-157">動的プロパティは、MyObject.Properties(0) の構文を使用して、このコレクションを通じてのみ参照できるか、または MyObject.Properties("Name")。</span><span class="sxs-lookup"><span data-stu-id="68fa5-157">Dynamic properties can be referenced only through the collection, using the syntax MyObject.Properties(0) or or MyObject.Properties("Name") .</span></span>

<span data-ttu-id="68fa5-158">どちらの種類のプロパティも削除できません。</span><span class="sxs-lookup"><span data-stu-id="68fa5-158">You cannot delete either kind of property.</span></span>

<span data-ttu-id="68fa5-159">動的プロパティである **Property** オブジェクトには、それ自体に次の 4 つの組み込みのプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="68fa5-159">A dynamic **Property** object has four built-in properties of its own:</span></span>

  - <span data-ttu-id="68fa5-160">**Name** プロパティは、プロパティを識別する文字列です。</span><span class="sxs-lookup"><span data-stu-id="68fa5-160">The **Name** property is a string that identifies the property.</span></span>

  - <span data-ttu-id="68fa5-161">**Type** プロパティは、プロパティのデータ型を指定する整数です。</span><span class="sxs-lookup"><span data-stu-id="68fa5-161">The **Type** property is an integer that specifies the property data type.</span></span>

  - <span data-ttu-id="68fa5-p115">**Value** プロパティは、プロパティの設定を格納する変数です。 **Value** は、 **Property** オブジェクトの既定のプロパティです。</span><span class="sxs-lookup"><span data-stu-id="68fa5-p115">The **Value** property is a variant that contains the property setting. **Value** is the default property for a **Property** object.</span></span>

  - <span data-ttu-id="68fa5-164">**Attributes** プロパティは、プロバイダー固有のプロパティの特性を示すロング型 ( **Long** ) の値です。</span><span class="sxs-lookup"><span data-stu-id="68fa5-164">The **Attributes** property is a **Long** value that indicates characteristics of the property specific to the provider.</span></span>

<span data-ttu-id="68fa5-p116">**Field** オブジェクトの **Properties** コレクションには、フィールドに関する追加のメタデータが含まれます。このコレクションの内容は、プロバイダーによって異なります。この章の最初で使用したサンプルの **Recordset** の **Properties** コレクションを確認するコード例を次に示します。ここでは、まずコレクションの内容を確認します。このコードでは、 [Microsoft OLE DB Provider for SQL Server](microsoft-ole-db-provider-for-sql-server.md) を使用しているため、 **Properties** コレクションには、そのプロバイダーに関する情報が格納されています。</span><span class="sxs-lookup"><span data-stu-id="68fa5-p116">The **Properties** collection for the **Field** object contains additional metadata about the field. The contents of this collection vary depending upon the provider. The following code example examines the **Properties** collection of the sample **Recordset** introduced at the beginning of this chapter. It first looks at the contents of the collection. This code uses the [OLE DB Provider for SQL Server](microsoft-ole-db-provider-for-sql-server.md), so the **Properties** collection contains information relevant to that provider.</span></span>

```vb 
 
'BeginFieldProps 
 Dim objProp As ADODB.Property 
 
 For intLoop = 0 To (objFields.Count - 1) 
 Debug.Print objFields.Item(intLoop).Name 
 
 For Each objProp In objFields(intLoop).Properties 
 Debug.Print vbTab & objProp.Name & " = " & objProp.Value 
 Next objProp 
 Next intLoop 
'EndFieldProps 
```

## <a name="dealing-with-binary-data"></a><span data-ttu-id="68fa5-170">バイナリ データを処理する</span><span class="sxs-lookup"><span data-stu-id="68fa5-170">Dealing with Binary Data</span></span>

<span data-ttu-id="68fa5-p117">[Field](appendchunk-method-ado.md) オブジェクトの **AppendChunk** メソッドを使用すると、そのオブジェクトに長いバイナリ データまたは文字データを格納できます。システムのメモリ容量が少ない場合、 **AppendChunk** メソッドを使用して、長い値の全体ではなく一部を操作できます。</span><span class="sxs-lookup"><span data-stu-id="68fa5-p117">Use the [AppendChunk](appendchunk-method-ado.md) method on a **Field** object to fill it with long binary or character data. In situations where system memory is limited, you can use the **AppendChunk** method to manipulate long values in portions rather than in their entirety.</span></span>

<span data-ttu-id="68fa5-173">**Field** オブジェクトの **Attributes** プロパティの **adFldLong** ビットが **True** に設定されている場合は、そのフィールドに対して **AppendChunk** メソッドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="68fa5-173">If the **adFldLong** bit in the **Attributes** property of a **Field** object is set to **True**, you can use the **AppendChunk** method for that field.</span></span>

<span data-ttu-id="68fa5-p118">**Field** オブジェクトで最初に **AppendChunk** を呼び出すと、フィールドにデータが書き込まれますが、既存のデータは上書きされます。それ以降に **AppendChunk** を呼び出すと、既存のデータに追加されます。あるフィールドにデータを追加した後に、カレント レコードに含まれる他のフィールドの値を設定したり読み込んだりすると、ADO は、最初のフィールドに対するデータの追加操作が完了したものと見なします。最初のフィールドに対して再度 **AppendChunk** メソッドを呼び出すと、ADO はその呼び出しを新しい **AppendChunk** 操作として仲介し、既存のデータを上書きします。一方、最初の **Recordset** オブジェクトの複製でない他の **Recordset** オブジェクトのフィールドにアクセスしても、 **AppendChunk** 操作は中断されません。</span><span class="sxs-lookup"><span data-stu-id="68fa5-p118">The first **AppendChunk** call on a **Field** object writes data to the field, overwriting any existing data. Subsequent **AppendChunk** calls add to existing data. If you are appending data to one field and then you set or read the value of another field in the current record, ADO assumes that you are finished appending data to the first field. If you call the **AppendChunk** method on the first field again, ADO interprets the call as a new **AppendChunk** operation and overwrites the existing data. Accessing fields in other **Recordset** objects that are not clones of the first **Recordset** object will not disrupt **AppendChunk** operations.</span></span>

<span data-ttu-id="68fa5-p119">**Field** オブジェクトの **GetChunk** メソッドを使用すると、長いバイナリ データまたは文字データの一部または全体を取得できます。システムのメモリ容量が少ない場合、 **GetChunk** メソッドを使用して、長い値の全体ではなく一部を操作できます。</span><span class="sxs-lookup"><span data-stu-id="68fa5-p119">Use the **GetChunk** method on a **Field** object to retrieve part or all of its long binary or character data. In situations where system memory is limited, you can use the **GetChunk** method to manipulate long values in portions, rather than in their entirety.</span></span>

<span data-ttu-id="68fa5-p120">**GetChunk** への呼び出しによって返される値は、*variable* に格納されます。*Size* が残りのデータよりも大きい場合、**GetChunk** メソッドは、*variable* の余った部分を空白で埋めることはなく、残りのデータのみを返します。フィールドが空の場合、**GetChunk** メソッドは Null 値を返します。</span><span class="sxs-lookup"><span data-stu-id="68fa5-p120">The data that a **GetChunk** call returns is assigned to *variable*. If *Size* is greater than the remaining data, the **GetChunk** method returns only the remaining data without padding *variable* with empty spaces. If the field is empty, the **GetChunk** method returns a null value.</span></span>

<span data-ttu-id="68fa5-p121">**GetChunk** を連続して呼び出すと、直前の **GetChunk** の呼び出しで取得されたデータの直後からデータが取得されます。ただし、あるフィールドのデータを取得しているときに、カレント レコードの別のフィールドの値の設定または読み取りを行うと、ADO は、最初のフィールドからのデータ取得は終了したと見なします。最初のフィールドでもう一度 **GetChunk** メソッドを呼び出すと、ADO は、その呼び出しを新しい **GetChunk** 操作と解釈し、データの先頭から読み取りを開始します。最初の **Recordset** オブジェクトの複製を除く別の **Recordset** オブジェクトのフィールドにアクセスした場合、 **GetChunk** 操作は中断されません。</span><span class="sxs-lookup"><span data-stu-id="68fa5-p121">Each subsequent **GetChunk** call retrieves data starting from where the previous **GetChunk** call left off. However, if you are retrieving data from one field and then set or read the value of another field in the current record, ADO assumes you have finished retrieving data from the first field. If you call the **GetChunk** method on the first field again, ADO interprets the call as a new **GetChunk** operation and starts reading from the beginning of the data. Accessing fields in other **Recordset** objects that are not clones of the first **Recordset** object will not disrupt **GetChunk** operations.</span></span>

<span data-ttu-id="68fa5-188">**Field** オブジェクトの **Attributes** プロパティの **adFldLong** ビットが **True** に設定されている場合は、そのフィールドに対して **GetChunk** メソッドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="68fa5-188">If the **adFldLong** bit in the **Attributes** property of a **Field** object is set to **True**, you can use the **GetChunk** method for that field.</span></span>

<span data-ttu-id="68fa5-189">**Field** オブジェクトの **GetChunk** メソッドまたは **AppendChunk** メソッドを使用したときに、カレント レコードが存在しない場合は、エラー 3021 (カレント レコードがありません) が発生します。</span><span class="sxs-lookup"><span data-stu-id="68fa5-189">If there is no current record when you use the **GetChunk** or **AppendChunk** method on a **Field** object, error 3021 (no current record) occurs.</span></span>

<span data-ttu-id="68fa5-190">これらのメソッドを使用してバイナリ データを操作する例は、 *ADO プログラマーズ リファレンス* [AppendChunk メソッド](appendchunk-method-ado.md)と[GetChunk メソッド](getchunk-method-ado.md)の例を参照してください。</span><span class="sxs-lookup"><span data-stu-id="68fa5-190">For an example of using these methods to manipulate binary data, see the [AppendChunk Method](appendchunk-method-ado.md) and [GetChunk Method](getchunk-method-ado.md) examples in the *ADO Programmer's Reference*.</span></span>

