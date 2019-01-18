---
title: Visual C++ ADO プログラミング
TOCTitle: Visual C++ ADO programming
ms:assetid: 117c4fad-8c11-5e3a-ea0c-18811e87475f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248878(v=office.15)
ms:contentKeyID: 48543319
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2a890b4906fb9f207f12ff17ef0d3ccf1a97a44d
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721291"
---
# <a name="visual-c-ado-programming"></a><span data-ttu-id="e823b-102">Visual C++ ADO プログラミング</span><span class="sxs-lookup"><span data-stu-id="e823b-102">Visual C++ ADO programming</span></span>

<span data-ttu-id="e823b-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="e823b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e823b-104">「ADO API リファレンス」では、Microsoft Visual Basic に似た構文を使用して ADO アプリケーション プログラミング インターフェイス (API) の機能を説明しています。</span><span class="sxs-lookup"><span data-stu-id="e823b-104">The ADO API Reference describes the functionality of the ADO application programming interface (API) using a syntax similar to Microsoft Visual Basic.</span></span> <span data-ttu-id="e823b-105">対象がすべてのユーザーは、ADO プログラマは Visual Basic、Visual C++ などの多様な言語を採用して (しなくても、**\#インポート**ディレクティブ)、および Visual j (ADO/WFC クラス パッケージ) を持つ。</span><span class="sxs-lookup"><span data-stu-id="e823b-105">Though the intended audience is all users, ADO programmers employ diverse languages such as Visual Basic, Visual C++ (with and without the **\#import** directive), and Visual J++ (with the ADO/WFC class package).</span></span>

<span data-ttu-id="e823b-106">この多様性に対応するため、「[ADO を Visual C++ と共に使用する](using-ado-with-microsoft-visual-c.md)」では、「ADO API リファレンス」内の機能、パラメーター、例外的な動作などの共通の説明にリンクしている Visual C++ 言語固有の構文が用意されています。</span><span class="sxs-lookup"><span data-stu-id="e823b-106">To accommodate this diversity, the [ADO for Visual C++ Syntax Indexes](using-ado-with-microsoft-visual-c.md) provide Visual C++ language-specific syntax with links to common descriptions of functionality, parameters, exceptional behaviors, and so on, in the API Reference.</span></span>

<span data-ttu-id="e823b-p102">ADO は COM (コンポーネント オブジェクト モデル) インターフェイスで実装されています。プログラマにとって、COM の操作は言語によって簡単である場合とそうでない場合があります。たとえば、Visual Basic のプログラマの場合は COM のほとんどの処理が暗黙的に実行されますが、Visual C++ プログラマの場合はそれらの処理を自分で行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="e823b-p102">ADO is implemented with COM (Component Object Model) interfaces. However, it is easier for programmers to work with COM in certain programming languages than others. For example, nearly all the details of using COM are handled implicitly for Visual Basic programmers, whereas Visual C++ programmers must attend to those details themselves.</span></span>

<span data-ttu-id="e823b-110">次のセクションの概要を C および C++ のプログラマが ADO を使用して、**\#インポート**ディレクティブです。</span><span class="sxs-lookup"><span data-stu-id="e823b-110">The following sections summarize details for C and C++ programmers using ADO and the **\#import** directive.</span></span> <span data-ttu-id="e823b-111">COM (**バリアント**、 **BSTR**、および**safearray 型**)、およびエラー処理に固有のデータ型に重点を置いています (\_com\_エラー)。</span><span class="sxs-lookup"><span data-stu-id="e823b-111">It focuses on data types specific to COM (**Variant**, **BSTR**, and **SafeArray**), and error handling (\_com\_error).</span></span>

## <a name="using-the-import-compiler-directive"></a><span data-ttu-id="e823b-112">使用して、\#コンパイラ ディレクティブのインポート</span><span class="sxs-lookup"><span data-stu-id="e823b-112">Using the \#import compiler directive</span></span>

<span data-ttu-id="e823b-113">**\#インポート**Visual C++ コンパイラ ディレクティブは、ADO のメソッドとプロパティの使用を簡略化します。</span><span class="sxs-lookup"><span data-stu-id="e823b-113">The **\#import** Visual C++ compiler directive simplifies working with the ADO methods and properties.</span></span> <span data-ttu-id="e823b-114">このディレクティブは、タイプ ライブラリを含んでいる ADO .dll (Msado15.dll) などのファイルの名前を取得し、typedef 宣言、インターフェイスのスマート ポインター、および列挙定数を含むヘッダー ファイルを生成します。</span><span class="sxs-lookup"><span data-stu-id="e823b-114">The directive takes the name of a file containing a type library, such as the ADO .dll (Msado15.dll), and generates header files containing typedef declarations, smart pointers for interfaces, and enumerated constants.</span></span> <span data-ttu-id="e823b-115">各インターフェイスはクラス内にカプセル化またはラップされます。</span><span class="sxs-lookup"><span data-stu-id="e823b-115">Each interface is encapsulated, or wrapped, in a class.</span></span>

<span data-ttu-id="e823b-p105">クラス内の操作 (メソッドまたはプロパティの呼び出し) ごとに、操作を直接呼び出す宣言 ("raw" 形式の操作) と、raw 操作を呼び出して、操作の実行が失敗したときに COM エラーをスローする宣言があります。プロパティの操作の場合は、通常、その操作に対して Visual Basic に似た構文を持つ代替構文を作成するコンパイラ ディレクティブがあります。</span><span class="sxs-lookup"><span data-stu-id="e823b-p105">For each operation within a class (that is, a method or property call), there is a declaration to call the operation directly (that is, the "raw" form of the operation), and a declaration to call the raw operation and throw a COM error if the operation fails to execute successfully. If the operation is a property, there is usually a compiler directive that creates an alternative syntax for the operation that has syntax like Visual Basic.</span></span>

<span data-ttu-id="e823b-118">プロパティの値を取得する操作は、フォームの名前を持つ \**を取得します。 プロパティ*。</span><span class="sxs-lookup"><span data-stu-id="e823b-118">Operations that retrieve the value of a property have names of the form, \**Get\*\*\*Property*.</span></span> <span data-ttu-id="e823b-119">プロパティの値を設定する操作は、フォームの名前を持つ \**配置。 プロパティ*。</span><span class="sxs-lookup"><span data-stu-id="e823b-119">Operations that set the value of a property have names of the form, \**Put\*\*\*Property*.</span></span> <span data-ttu-id="e823b-120">ADO オブジェクトへのポインターを持つプロパティの値を設定する操作は、フォームの名前を持つ \**PutRef。 プロパティ*。</span><span class="sxs-lookup"><span data-stu-id="e823b-120">Operations that set the value of a property with a pointer to an ADO object have names of the form, \**PutRef\*\*\*Property*.</span></span>

<span data-ttu-id="e823b-121">プロパティを取得または設定するには、次の形式の呼び出しを行います。</span><span class="sxs-lookup"><span data-stu-id="e823b-121">You can get or set a property with calls of these forms:</span></span>

```vb 
 
variable = objectPtr->GetProperty(); // get property value 
objectPtr->PutProperty(value); // set property value 
objectPtr->PutRefProperty(&value); // set property with object pointer 
```

## <a name="using-property-directives"></a><span data-ttu-id="e823b-122">プロパティ ディレクティブの使用</span><span class="sxs-lookup"><span data-stu-id="e823b-122">Using property directives</span></span>

<span data-ttu-id="e823b-123">\*\* \_ \_Declspec(property...)\*\* コンパイラ ディレクティブは、マイクロソフト固有の C 言語拡張機能が別の構文を使用してプロパティとして使用される関数を宣言します。</span><span class="sxs-lookup"><span data-stu-id="e823b-123">The **\_\_declspec(property...)** compiler directive is a Microsoft-specific C language extension that declares a function used as a property to have an alternative syntax.</span></span> <span data-ttu-id="e823b-124">これにより、Visual Basic に似た方法でプロパティの値を設定または取得できるようになります。</span><span class="sxs-lookup"><span data-stu-id="e823b-124">As a result, you can set or get values of a property in a way similar to Visual Basic.</span></span> <span data-ttu-id="e823b-125">たとえば、次のようにしてプロパティを設定または取得できます。</span><span class="sxs-lookup"><span data-stu-id="e823b-125">For example, you can set and get a property this way:</span></span>

```vb 
 
objectPtr->property = value; // set property value 
variable = objectPtr->property; // get property value 
```

<span data-ttu-id="e823b-126">コーディングが不要な点に注意してください。</span><span class="sxs-lookup"><span data-stu-id="e823b-126">Notice you do not have to code:</span></span>

```vb 
 
objectPtr->PutProperty(value); // set property value 
variable = objectPtr->GetProperty; // get property value 
```

<span data-ttu-id="e823b-127">適切なコンパイラが生成されます **Get。-\*、**配置\*\*の、または \**PutRef。 プロパティ*の呼び出しでは、宣言されたどのような代替の構文と、プロパティがされているかどうかに基づいて読み取りや書き込みをします。</span><span class="sxs-lookup"><span data-stu-id="e823b-127">The compiler will generate the appropriate \**Get\*\*\*-*, **Put**-, or \**PutRef\*\*\*Property* call based on what alternative syntax is declared and whether the property is being read or written.</span></span>

<span data-ttu-id="e823b-128">\*\* \_ \_Declspec(property...)\*\* コンパイラ ディレクティブには、**取得**、**配置**、または関数の別の構文を\*\*\*\*取得**し、** のみを宣言できます。</span><span class="sxs-lookup"><span data-stu-id="e823b-128">The **\_\_declspec(property...)** compiler directive can only declare **get**, **put**, or **get** and **put** alternative syntax for a function.</span></span> <span data-ttu-id="e823b-129">読み取り専用操作では **get** 宣言だけを、書き込み専用操作では **put** 宣言だけを、読み取りおよび書き込み操作では **get** 宣言と **put** 宣言の両方を組み込みます。</span><span class="sxs-lookup"><span data-stu-id="e823b-129">Read-only operations only have a **get** declaration; write-only operations only have a **put** declaration; operations that are both read and write have both **get** and **put** declarations.</span></span>

<span data-ttu-id="e823b-130">2 つの宣言は、このディレクティブで実行できます。ただし、各プロパティがプロパティの 3 つの関数を必要があります: **を取得します。 プロパティ\*、**配置。 プロパティ\*、および \**PutRef。 プロパティ*。</span><span class="sxs-lookup"><span data-stu-id="e823b-130">Only two declarations are possible with this directive; however, each property may have three property functions: \**Get\*\*\*Property*, \**Put\*\*\*Property*, and \**PutRef\*\*\*Property*.</span></span> <span data-ttu-id="e823b-131">その場合、代替構文があるのは 2 つの形式のプロパティだけです。</span><span class="sxs-lookup"><span data-stu-id="e823b-131">In that case, only two forms of the property have the alternative syntax.</span></span>

<span data-ttu-id="e823b-132">代替の構文を使用して**Command**オブジェクトの**ActiveConnection**プロパティを宣言するたとえば、\**を取得します。 ActiveConnection*と \**PutRef。 ActiveConnection*。</span><span class="sxs-lookup"><span data-stu-id="e823b-132">For example, the **Command** object **ActiveConnection** property is declared with an alternative syntax for \**Get\*\*\*ActiveConnection* and \**PutRef\*\*\*ActiveConnection*.</span></span> <span data-ttu-id="e823b-133">**PutRef**での構文をお勧めため実際には、通常このプロパティで開いている**接続**オブジェクト (つまり、**接続**オブジェクト ポインター) を配置します。</span><span class="sxs-lookup"><span data-stu-id="e823b-133">The **PutRef**- syntax is a good choice because in practice, you will typically want to put an open **Connection** object (that is, a **Connection** object pointer) in this property.</span></span> <span data-ttu-id="e823b-134">**レコード セット**オブジェクトには、その一方で、**取得**、**配置**、および \**PutRef。 ActiveConnection*操作が別の構文ではありません。</span><span class="sxs-lookup"><span data-stu-id="e823b-134">On the other hand, the **Recordset** object has **Get**-, **Put**-, and \**PutRef\*\*\*ActiveConnection* operations, but no alternative syntax.</span></span>

## <a name="collections-the-getitem-method-and-the-item-property"></a><span data-ttu-id="e823b-135">コレクション、GetItem メソッド、および Item プロパティ</span><span class="sxs-lookup"><span data-stu-id="e823b-135">Collections, the GetItem method, and the Item property</span></span>

<span data-ttu-id="e823b-p111">ADO では、**Fields**、**Parameters**、**Properties**、**Errors** など、いくつかのコレクションが定義されています。Visual C++ では、コレクションのメンバーは **GetItem(***index***)** メソッドによって返されます。*Index* はバリアント型 (**Variant**) で、値はコレクションのメンバーの数値インデックスか、またはメンバーの名前を含む文字列です。</span><span class="sxs-lookup"><span data-stu-id="e823b-p111">ADO defines several collections, including **Fields**, **Parameters**, **Properties**, and **Errors**. In Visual C++, the **GetItem(***index***)** method returns a member of the collection. *Index* is a **Variant**, the value of which is either a numerical index of the member in the collection, or a string containing the name of the member.</span></span>

<span data-ttu-id="e823b-139">\*\* \_ \_Declspec(property...)\*\* コンパイラ ディレクティブは、 **getitem() を実行**メソッドの基本的なコレクションごとに別の構文として**Item**プロパティを宣言しています。</span><span class="sxs-lookup"><span data-stu-id="e823b-139">The **\_\_declspec(property...)** compiler directive declares the **Item** property as an alternative syntax to each collection's fundamental **GetItem()** method.</span></span> <span data-ttu-id="e823b-140">代替構文は角かっこを使用し、配列参照に似ています。</span><span class="sxs-lookup"><span data-stu-id="e823b-140">The alternative syntax uses square brackets and looks similar to an array reference.</span></span> <span data-ttu-id="e823b-141">一般に、次のような 2 つの形式になります。</span><span class="sxs-lookup"><span data-stu-id="e823b-141">In general, the two forms look like the following:</span></span>

```vb
    collectionPtr->GetItem(index); 
    collectionPtr->Item[index]; 
```

<span data-ttu-id="e823b-142">たとえば、 ***rs***、 **pubs**データベースの**authors**テーブルから派生したという名前**のレコード セット**オブジェクトのフィールドに値を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="e823b-142">For example, assign a value to a field of a **Recordset** object, named ***rs***, derived from the **authors** table of the **pubs** database.</span></span> <span data-ttu-id="e823b-143">**Item()** プロパティを使用して、 **Recordset**オブジェクトの**Fields**コレクションの 3 番目の**フィールド**にアクセスするのには (コレクションのインデックスは 0 から; 3 番目のフィールドの名前は前提としています***au\_fname***)。</span><span class="sxs-lookup"><span data-stu-id="e823b-143">Use the **Item()** property to access the third **Field** of the **Recordset** object **Fields** collection (collections are indexed from zero; assume the third field is named ***au\_fname***).</span></span> <span data-ttu-id="e823b-144">**Field** オブジェクトで **Value()** メソッドを呼び出して、文字列値を代入します。</span><span class="sxs-lookup"><span data-stu-id="e823b-144">Then call the **Value()** method on the **Field** object to assign a string value.</span></span>

<span data-ttu-id="e823b-145">これを Visual Basic で記述するには、次の 4 つの方法があります (最後の 2 つの形式は Visual Basic 固有の形式であり、他の言語には同等の形式はありません)。</span><span class="sxs-lookup"><span data-stu-id="e823b-145">This can be expressed in Visual Basic in the following four ways (the last two forms are unique to Visual Basic; other languages do not have equivalents):</span></span>

```vb 
 
rs.Fields.Item(2).Value = "value" 
rs.Fields.Item("au_fname").Value = "value" 
rs(2) = "value" 
rs!au_fname = "value" 
```

<span data-ttu-id="e823b-146">最初の 2 つの形式と同等の Visual C++ の形式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="e823b-146">The equivalent in Visual C++ to the first two forms above is:</span></span>

```cpp 
 
rs->Fields->GetItem(long(2))->PutValue("value"); 
rs->Fields->GetItem("au_fname")->PutValue("value"); 
```

<span data-ttu-id="e823b-147">\-または -( **Value**プロパティの代替構文も表示)</span><span class="sxs-lookup"><span data-stu-id="e823b-147">\-or- (the alternative syntax for the **Value** property is also shown)</span></span>

```cpp 
 
rs->Fields->Item[long(2)]->Value = "value"; 
rs->Fields->Item["au_fname"]->Value = "value"; 
```

## <a name="com-specific-data-types"></a><span data-ttu-id="e823b-148">COM 固有のデータ型</span><span class="sxs-lookup"><span data-stu-id="e823b-148">COM-specific data types</span></span>

<span data-ttu-id="e823b-p114">一般に、「ADO API リファレンス」で使われている Visual Basic のデータ型に対しては、同等のデータ型が Visual C++ にあります。たとえば、Visual Basic のバイト型 ( **Byte** ) に対する **unsigned char** 、整数型 ( **Integer** ) に対する **short** 、長整数型 ( **Long** ) に対する **long** などの標準データ型があります。各メソッドまたはプロパティのオペランドに必要な要素の詳細については、各「構文インデックス」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e823b-p114">In general, any Visual Basic data type you find in the ADO API Reference has a Visual C++ equivalent. These include standard data types such as **unsigned char** for a Visual Basic **Byte**, **short** for **Integer**, and **long** for **Long**. Look in the Syntax Indexes to see exactly what is required for the operands of a given method or property.</span></span>

<span data-ttu-id="e823b-152">この規則が当てはまらないのは、COM 固有のデータ型であるバリアント型 ( **Variant** )、 **BSTR** 型、および **SafeArray** 型です。</span><span class="sxs-lookup"><span data-stu-id="e823b-152">The exceptions to this rule are the data types specific to COM: **Variant**, **BSTR**, and **SafeArray**.</span></span>

### <a name="variant"></a><span data-ttu-id="e823b-153">バリアント型 (Variant)</span><span class="sxs-lookup"><span data-stu-id="e823b-153">Variant</span></span>

<span data-ttu-id="e823b-p115">バリアント型 ( **Variant** ) は、値メンバーとデータ型メンバーを格納する構造化データ型です。バリアント型 ( **Variant** ) には、別のバリアント型 (Variant)、BSTR、ブール型 (Boolean)、IDispatch ポインターまたは IUnknown ポインター、通貨、日付など、さまざまなデータ型を格納できます。また、COM には、データ型の変換を簡単に実行できるメソッドが用意されています。</span><span class="sxs-lookup"><span data-stu-id="e823b-p115">A **Variant** is a structured data type that contains a value member and a data type member. A **Variant** may contain a wide range of other data types including another Variant, BSTR, Boolean, IDispatch or IUnknown pointer, currency, date, and so on. COM also provides methods that make it easy to convert one data type to another.</span></span>

<span data-ttu-id="e823b-157">**\_バリアント\_t**クラスは、カプセル化し、**バリアント**データ型を管理します。</span><span class="sxs-lookup"><span data-stu-id="e823b-157">The **\_variant\_t** class encapsulates and manages the **Variant** data type.</span></span>

<span data-ttu-id="e823b-158">場合 ADO API リファレンス」でメソッドまたはプロパティのオペランドが値を受け取り、通常は、値が渡された、**\_バリアント\_t**。</span><span class="sxs-lookup"><span data-stu-id="e823b-158">When the ADO API Reference says a method or property operand takes a value, it usually means the value is passed in a **\_variant\_t**.</span></span>

<span data-ttu-id="e823b-p116">「ADO API リファレンス」のトピックの「 **パラメーター** 」セクションでオペランドがバリアント型 ( **Variant** ) であると記載されている場合は、この規則が明白に当てはまります。例外は、このドキュメントでオペランドが長整数型 ( **Long** ) やバイト型 ( **Byte** ) などの標準データ型である、または列挙型であると明示的に記載されている場合です。また、オペランドが文字列型 ( **String** ) である場合も例外です。</span><span class="sxs-lookup"><span data-stu-id="e823b-p116">This rule is explicitly true when the **Parameters** section in the topics of the ADO API Reference says an operand is a **Variant**. One exception is when the documentation explicitly says the operand takes a standard data type, such as **Long** or **Byte**, or an enumeration. Another exception is when the operand takes a **String**.</span></span>

### <a name="bstr"></a><span data-ttu-id="e823b-162">BSTR 型</span><span class="sxs-lookup"><span data-stu-id="e823b-162">BSTR</span></span>

<span data-ttu-id="e823b-p117">**BSTR** (**B**asic **STR**ing) は、文字列と文字列長を格納する構造化データ型です。COM には、**BSTR** 型を割り当て、操作、および解放するメソッドが用意されています。</span><span class="sxs-lookup"><span data-stu-id="e823b-p117">A **BSTR** (**B**asic **STR**ing) is a structured data type that contains a character string and the string's length. COM provides methods to allocate, manipulate, and free a **BSTR**.</span></span>

<span data-ttu-id="e823b-165">\*\* \_Bstr\_t\*\*クラスは、カプセル化し、 **BSTR**データ型を管理します。</span><span class="sxs-lookup"><span data-stu-id="e823b-165">The **\_bstr\_t** class encapsulates and manages the **BSTR** data type.</span></span>

<span data-ttu-id="e823b-166">「ADO API リファレンス」でメソッドまたはプロパティが**文字列**値を受け取る、ときにことを意味値の形式で、 \*\* \_bstr\_t\*\*.</span><span class="sxs-lookup"><span data-stu-id="e823b-166">When the ADO API Reference says a method or property takes a **String** value, it means the value is in the form of a **\_bstr\_t**.</span></span>

#### <a name="casting-variantt-and-bstrt-classes"></a><span data-ttu-id="e823b-167">キャスト\_バリアント\_t と\_bstr\_t クラス</span><span class="sxs-lookup"><span data-stu-id="e823b-167">Casting \_variant\_t and \_bstr\_t classes</span></span>

<span data-ttu-id="e823b-168">多くの場合、コードでは明示的にする必要はありません、**\_バリアント\_t**または**\_bstr\_t**操作への引数にします。</span><span class="sxs-lookup"><span data-stu-id="e823b-168">Often it is not necessary to explicitly code a **\_variant\_t** or **\_bstr\_t** in an argument to an operation.</span></span> <span data-ttu-id="e823b-169">場合、**\_バリアント\_t**または**\_bstr\_t**クラスには、引数のデータ型に一致するコンス トラクターは、コンパイラが生成されます、適切な**\_バリアント\_t**または**\_bstr\_t**。</span><span class="sxs-lookup"><span data-stu-id="e823b-169">If the **\_variant\_t** or **\_bstr\_t** class has a constructor that matches the data type of the argument, then the compiler will generate the appropriate **\_variant\_t** or **\_bstr\_t**.</span></span>

<span data-ttu-id="e823b-170">しかし、引数が不明確である、つまり、引数のデータ型が複数のコンストラクターに対応する場合は、正しいコンストラクターを呼び出すことができるように、引数を適切なデータ型にキャストする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e823b-170">However, if the argument is ambiguous, that is, the argument's data type matches more than one constructor, you must cast the argument with the appropriate data type to invoke the correct constructor.</span></span>

<span data-ttu-id="e823b-171">たとえば、 **Recordset::Open** メソッドの宣言を次に示します。</span><span class="sxs-lookup"><span data-stu-id="e823b-171">For example, the declaration for the **Recordset::Open** method is:</span></span>

```vb 
 
 HRESULT Open ( 
 const _variant_t & Source, 
 const _variant_t & ActiveConnection, 
 enum CursorTypeEnum CursorType, 
 enum LockTypeEnum LockType, 
 long Options ); 
```

<span data-ttu-id="e823b-172">参照は、暗黙的に**\_バリアント\_t**、接続文字列または開いている**接続**オブジェクトへのポインターとしてコードを作成することがあります。</span><span class="sxs-lookup"><span data-stu-id="e823b-172">The ActiveConnection argument takes a reference to a **\_variant\_t**, which you may code as a connection string or a pointer to an open **Connection** object.</span></span>

<span data-ttu-id="e823b-173">正しい**\_バリアント\_t**次のように文字列を渡す場合は、暗黙的に作成される"DSN = pubs; uid = sa; pwd =;"、またはようにポインター"(IDispatch \*) pConn」。</span><span class="sxs-lookup"><span data-stu-id="e823b-173">The correct **\_variant\_t** will be constructed implicitly if you pass a string such as "DSN=pubs;uid=sa;pwd=;", or a pointer such as "(IDispatch \*) pConn".</span></span>

<span data-ttu-id="e823b-174">明示的にコーディングすることがありますか、**\_バリアント\_t**のポインターを次のように含まれている"\_バリアント\_t ((IDispatch \*) pConn、true を指定)」です。</span><span class="sxs-lookup"><span data-stu-id="e823b-174">Or you may explicitly code a **\_variant\_t** containing a pointer such as "\_variant\_t((IDispatch \*) pConn, true)".</span></span> <span data-ttu-id="e823b-175">キャスト (IDispatch \*)、IUnknown インターフェイスへのポインターを取得するもう 1 つのコンス トラクターを持つあいまいさを解決します。</span><span class="sxs-lookup"><span data-stu-id="e823b-175">The cast, (IDispatch \*), resolves the ambiguity with another constructor that takes a pointer to an IUnknown interface.</span></span>

<span data-ttu-id="e823b-p120">ほとんど言及されませんが、ADO が IDispatch インターフェイスであるということは非常に重要です。ADO オブジェクトへのポインターをバリアント型 ( **Variant** ) として渡す場合は、そのポインターを IDispatch インターフェイスへのポインターとしてキャストする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e823b-p120">It is a crucial, though seldom mentioned fact, that ADO is an IDispatch interface. Whenever a pointer to an ADO object must be passed as a **Variant**, that pointer must be cast as a pointer to an IDispatch interface.</span></span>

<span data-ttu-id="e823b-178">コンス トラクターの 2 番目のブール型の引数のオプションの既定値の true を明示的にコーディングする方法も。</span><span class="sxs-lookup"><span data-stu-id="e823b-178">The last case explicitly codes the second boolean argument of the constructor with its optional, default value of true.</span></span> <span data-ttu-id="e823b-179">この引数は、**バリアント型**コンス トラクターは、ADO の呼び出しを自動的に補正、 **AddRef**() メソッドを呼び出す、**\_バリアント\_t::Release**() メソッドの ADO のメソッドまたはプロパティの呼び出しが完了するとします。</span><span class="sxs-lookup"><span data-stu-id="e823b-179">This argument causes the **Variant** constructor to call its **AddRef**() method, which compensates for ADO automatically calling the **\_variant\_t::Release**() method when the ADO method or property call completes.</span></span>

### <a name="safearray"></a><span data-ttu-id="e823b-180">SafeArray</span><span class="sxs-lookup"><span data-stu-id="e823b-180">SafeArray</span></span>

<span data-ttu-id="e823b-181">**SafeArray**は、他のデータ型の配列を含む構造化データ タイプです。</span><span class="sxs-lookup"><span data-stu-id="e823b-181">A **SafeArray** is a structured data type that contains an array of other data types.</span></span> <span data-ttu-id="e823b-182">**SafeArray**は各配列の次元、およびそれらの範囲内の配列要素へのアクセス制限の範囲に関する情報が含まれているために、*安全*と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="e823b-182">A **SafeArray** is called *safe* because it contains information about the bounds of each array dimension, and limits access to array elements within those bounds.</span></span>

<span data-ttu-id="e823b-183">「ADO API リファレンス」で、メソッドまたはプロパティが配列を取得する、または配列を返すと記載されている場合は、メソッドまたはプロパティが、C/C++ のネイティブ配列ではなく **SafeArray** 型を取得するまたは返すことを意味します。</span><span class="sxs-lookup"><span data-stu-id="e823b-183">When the ADO API Reference says a method or property takes or returns an array, it means the method or property takes or returns a **SafeArray**, not a native C/C++ array.</span></span>

<span data-ttu-id="e823b-p123">たとえば、 **Connection** オブジェクトの **OpenSchema** メソッドの 2 番目のパラメーターには、バリアント型 ( **Variant** ) の値の配列が必要です。これらのバリアント型 ( **Variant** ) の値は **SafeArray** 型の要素として渡される必要があり、その **SafeArray** 型は別のバリアント型 ( **Variant** ) の値として設定される必要があります。 **OpenSchema** の 2 番目の引数として渡されるのは、この別のバリアント型 ( **Variant** ) です。</span><span class="sxs-lookup"><span data-stu-id="e823b-p123">For example, the second parameter of the **Connection** object **OpenSchema** method requires an array of **Variant** values. Those **Variant** values must be passed as elements of a **SafeArray**, and that **SafeArray** must be set as the value of another **Variant**. It is that other **Variant** that is passed as the second argument of **OpenSchema**.</span></span>

<span data-ttu-id="e823b-187">さらに別の例として、 **Find** メソッドの最初の引数がバリアント型 ( **Variant** ) で、その値が 1 次元の **SafeArray** 型である場合、 **AddNew** の最初と 2 番目のオプションの引数はそれぞれ 1 次元の **SafeArray** 型で、 **GetRows** メソッドの戻り値は、値が 2 次元の **SafeArray** 型であるバリアント型 ( **Variant** ) です。</span><span class="sxs-lookup"><span data-stu-id="e823b-187">As further examples, the first argument of the **Find** method is a **Variant** whose value is a one-dimensional **SafeArray**; each of the optional first and second arguments of **AddNew** is a one-dimensional **SafeArray**; and the return value of the **GetRows** method is a **Variant** whose value is a two-dimensional **SafeArray**.</span></span>

## <a name="missing-and-default-parameters"></a><span data-ttu-id="e823b-188">不足していると、既定のパラメーター</span><span class="sxs-lookup"><span data-stu-id="e823b-188">Missing and default parameters</span></span>

<span data-ttu-id="e823b-p124">Visual Basic では、メソッドのパラメーターを省略できます。たとえば、 **Recordset** オブジェクトの **Open** メソッドには 5 つのパラメーターがありますが、中間のパラメーターを省略して、後続のパラメーターをそのまま使用できます。省略可能なオペランドのデータ型に応じて、既定の **BSTR** 型またはバリアント型 ( **Variant** ) が代用されます。</span><span class="sxs-lookup"><span data-stu-id="e823b-p124">Visual Basic allows missing parameters in methods. For example, the **Recordset** object **Open** method has five parameters, but you can skip intermediate parameters and leave off trailing parameters. A default **BSTR** or **Variant** will be substituted depending on the data type of the missing operand.</span></span>

<span data-ttu-id="e823b-192">C/C++ では、すべてのオペランドを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e823b-192">In C/C++, all operands must be specified.</span></span> <span data-ttu-id="e823b-193">不足しているパラメーターを指定する場合は、データ型の文字列は、指定、 \*\* \_bstr\_t\*\*は、null 文字列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e823b-193">If you want to specify a missing parameter whose data type is a string, specify a **\_bstr\_t** containing a null string.</span></span> <span data-ttu-id="e823b-194">不足しているパラメーターを指定する場合は、データ型の**バリアント型**は、指定、**\_バリアント\_t**変位の値を持つ\_E\_PARAMNOTFOUND と vt 型\_エラーです。</span><span class="sxs-lookup"><span data-stu-id="e823b-194">If you want to specify a missing parameter whose data type is a **Variant**, specify a **\_variant\_t** with a value of DISP\_E\_PARAMNOTFOUND and a type of VT\_ERROR.</span></span> <span data-ttu-id="e823b-195">または、相当するものを指定**\_バリアント\_t**定数、 **vtMissing**が提供する、**\#インポート**ディレクティブです。</span><span class="sxs-lookup"><span data-stu-id="e823b-195">Alternatively, specify the equivalent **\_variant\_t** constant, **vtMissing**, which is supplied by the **\#import** directive.</span></span>

<span data-ttu-id="e823b-p126">**vtMissing** の一般的な使用方法の例外として、3 つのメソッドがあります。それは、 **Connection** オブジェクトおよび **Command** オブジェクトの **Execute** メソッドと、 **Recordset** オブジェクトの **NextRecordset** メソッドです。次に、これらのメソッドを示します。</span><span class="sxs-lookup"><span data-stu-id="e823b-p126">Three methods are exceptions to the typical use of **vtMissing**. These are the **Execute** methods of the **Connection** and **Command** objects, and the **NextRecordset** method of the **Recordset** object. The following are their signatures:</span></span>

```vb 
 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthcnnexecute_HV10294345.xml( _bstr_t CommandText, VARIANT * RecordsAffected, 
 long Options ); // Connection 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthcmdexecute_HV10294344.xml( VARIANT * RecordsAffected, VARIANT * Parameters, 
 long Options ); // Command 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthnextrec_HV10294541.xml( VARIANT * RecordsAffected ); // Recordset 
```

<span data-ttu-id="e823b-p127">*RecordsAffected* パラメーターと *Parameters* パラメーターは、1 つのバリアント型 (**Variant**) へのポインターです。*Parameters* は、実行されるコマンドを変更する 1 つのパラメーターまたはパラメーターの配列を格納するバリアント型 (**Variant**) のアドレスを指定する入力パラメーターです。*RecordsAffected* は、メソッドによって影響を受ける行数を返すバリアント型 (**Variant**) のアドレスを指定する出力パラメーターです。</span><span class="sxs-lookup"><span data-stu-id="e823b-p127">The parameters, *RecordsAffected* and *Parameters*, are pointers to a **Variant**. *Parameters* is an input parameter which specifies the address of a **Variant** containing a single parameter, or array of parameters, that will modify the command being executed. *RecordsAffected* is an output parameter that specifies the address of a **Variant**, where the number of rows affected by the method is returned.</span></span>

<span data-ttu-id="e823b-202">**コマンド**オブジェクトの**Execute**メソッドで*パラメーター*を設定するか、パラメーターが指定されていないことを示す\&vtMissing (推奨)、または null のポインターを (つまり、 **NULL**またはゼロ (0))。</span><span class="sxs-lookup"><span data-stu-id="e823b-202">In the **Command** object **Execute** method, indicate that no parameters are specified by setting *Parameters* to either \&vtMissing (which is recommended) or to the null pointer (that is, **NULL** or zero (0)).</span></span> <span data-ttu-id="e823b-203">*パラメーター*は、null ポインターに設定されているメソッドは、 **vtMissing**のと同じでは内部的に、操作が完了します。</span><span class="sxs-lookup"><span data-stu-id="e823b-203">If *Parameters* is set to the null pointer, the method internally substitutes the equivalent of **vtMissing**, and then completes the operation.</span></span>

<span data-ttu-id="e823b-204">すべてのメソッドでことの影響を受けるレコードの数を返すべきでない*RecordsAffected*を null ポインターに設定することでを指定します。</span><span class="sxs-lookup"><span data-stu-id="e823b-204">In all the methods, indicate that the number of records affected should not be returned by setting *RecordsAffected* to the null pointer.</span></span> <span data-ttu-id="e823b-205">この場合、Null ポインターは省略されたパラメーターではなく、影響を受けるレコードの数を破棄するようにというメソッドへの指示です。</span><span class="sxs-lookup"><span data-stu-id="e823b-205">In this case, the null pointer is not so much a missing parameter as an indication that the method should discard the number of records affected.</span></span>

<span data-ttu-id="e823b-206">したがって、これらの 3 つのメソッドの場合、次のようなコーディングもできます。</span><span class="sxs-lookup"><span data-stu-id="e823b-206">Thus, for these three methods, it is valid to code something such as:</span></span>

```vb 
 
pConnection->Execute("commandText", NULL, adCmdText); 
pCommand->Execute(NULL, NULL, adCmdText); 
pRecordset->NextRecordset(NULL); 
```

## <a name="error-handling"></a><span data-ttu-id="e823b-207">エラー処理</span><span class="sxs-lookup"><span data-stu-id="e823b-207">Error handling</span></span>

<span data-ttu-id="e823b-208">COM では、ほとんどの操作は、関数が正常に完了したかどうかを示す HRESULT リターン コードを返します。</span><span class="sxs-lookup"><span data-stu-id="e823b-208">In COM, most operations return an HRESULT return code that indicates whether a function completed successfully.</span></span> <span data-ttu-id="e823b-209">**\#インポート**ディレクティブは、各「生」のメソッドまたはプロパティをラッパー コードを生成し、返された HRESULT を確認します。</span><span class="sxs-lookup"><span data-stu-id="e823b-209">The **\#import** directive generates wrapper code around each "raw" method or property and checks the returned HRESULT.</span></span> <span data-ttu-id="e823b-210">ラッパー コードが呼び出すことによって COM エラーをスローする HRESULT は、エラーを示している場合\_com\_問題\_の errorex() には、引数としてコードが返されます。</span><span class="sxs-lookup"><span data-stu-id="e823b-210">If the HRESULT indicates failure, the wrapper code throws a COM error by calling \_com\_issue\_errorex() with the HRESULT return code as an argument.</span></span> <span data-ttu-id="e823b-211">**実行してください**COM エラー オブジェクトをキャッチできます-**catch**ブロック。</span><span class="sxs-lookup"><span data-stu-id="e823b-211">COM error objects can be caught in a **try**-**catch** block.</span></span> <span data-ttu-id="e823b-212">(効率のためへの参照をキャッチ、 \*\* \_com\_エラー\*\*オブジェクト)。</span><span class="sxs-lookup"><span data-stu-id="e823b-212">(For efficiency's sake, catch a reference to a **\_com\_error** object.)</span></span>

<span data-ttu-id="e823b-p131">これらは ADO エラーであり、ADO 操作の失敗によって生成されます。基になるプロバイダーから返されるエラーは、 **Connection** オブジェクトの **Errors** コレクションに **Error** オブジェクトとして表示されます。</span><span class="sxs-lookup"><span data-stu-id="e823b-p131">Remember, these are ADO errors: they result from the ADO operation failing. Errors returned by the underlying provider appear as **Error** objects in the **Connection** object **Errors** collection.</span></span>

<span data-ttu-id="e823b-215">**\#インポート**ディレクティブによって作成のみエラー処理ルーチンでメソッドおよびプロパティは、ADO .dll で宣言されているのです。</span><span class="sxs-lookup"><span data-stu-id="e823b-215">The **\#import** directive creates only error handling routines for methods and properties declared in the ADO .dll.</span></span> <span data-ttu-id="e823b-216">ただし、自分でエラー確認マクロやインライン関数を記述すると、同じエラー処理機構を利用できます。</span><span class="sxs-lookup"><span data-stu-id="e823b-216">However, you can take advantage of this same error handling mechanism by writing your own error checking macro or inline function.</span></span> <span data-ttu-id="e823b-217">例については、「 [ADO 用の Visual C++ Extensions](visual-c-extensions-for-ado.md)」または、以下に説明するコードを参照してください。</span><span class="sxs-lookup"><span data-stu-id="e823b-217">See the topic, [Visual C++ Extensions](visual-c-extensions-for-ado.md), or the code in the following sections for examples.</span></span>

## <a name="visual-c-equivalents-of-visual-basic-conventions"></a><span data-ttu-id="e823b-218">Visual C++ に対応する Visual Basic の規則の</span><span class="sxs-lookup"><span data-stu-id="e823b-218">Visual C++ equivalents of Visual Basic conventions</span></span>

<span data-ttu-id="e823b-219">Visual Basic および、それと同等の Visual C++ でコーディングされた ADO ドキュメントにおけるいくつかの規則の概要を次に示します。</span><span class="sxs-lookup"><span data-stu-id="e823b-219">The following is a summary of several conventions in the ADO documentation, coded in Visual Basic, as well as their equivalents in Visual C++.</span></span>

### <a name="declaring-an-ado-object"></a><span data-ttu-id="e823b-220">ADO オブジェクトの宣言</span><span class="sxs-lookup"><span data-stu-id="e823b-220">Declaring an ADO object</span></span>

<span data-ttu-id="e823b-221">Visual Basic では、ADO オブジェクト変数 (この場合は **Recordset** オブジェクトの変数) を次のように宣言します。</span><span class="sxs-lookup"><span data-stu-id="e823b-221">In Visual Basic, an ADO object variable (in this case for a **Recordset** object) is declared as follows:</span></span>

```vb 
 
Dim rst As ADODB.Recordset 
```

<span data-ttu-id="e823b-222">句は"ADODB。レコード セット"は、レジストリで定義されている**レコード セット**オブジェクトの ProgID です。</span><span class="sxs-lookup"><span data-stu-id="e823b-222">The clause, "ADODB.Recordset", is the ProgID of the **Recordset** object as defined in the Registry.</span></span> <span data-ttu-id="e823b-223">**Record** オブジェクトの新しいインスタンスは、次のように宣言します。</span><span class="sxs-lookup"><span data-stu-id="e823b-223">A new instance of a **Record** object is declared as follows:</span></span>

```vb 
 
Dim rst As New ADODB.Recordset 
```

<span data-ttu-id="e823b-224">\-または -</span><span class="sxs-lookup"><span data-stu-id="e823b-224">\-or-</span></span>

```vb 
 
Dim rst As ADODB.Recordset 
Set rst = New ADODB.Recordset 
```

<span data-ttu-id="e823b-225">Visual C++ で、**\#インポート**ディレクティブは、すべての ADO オブジェクトのスマート ポインターの型宣言を生成します。</span><span class="sxs-lookup"><span data-stu-id="e823b-225">In Visual C++, the **\#import** directive generates smart pointer-type declarations for all the ADO objects.</span></span> <span data-ttu-id="e823b-226">ポイントする変数などの**\_レコード セット**型のオブジェクトは、 \*\* \_RecordsetPtr\*\*が次のように宣言されているとします。</span><span class="sxs-lookup"><span data-stu-id="e823b-226">For example, a variable that points to a **\_Recordset** object is of type **\_RecordsetPtr**, and is declared as follows:</span></span>

```cpp 
 
_RecordsetPtr rs; 
```

<span data-ttu-id="e823b-227">新しいインスタンスを指す変数、**\_レコード セット**オブジェクトは次のように宣言します。</span><span class="sxs-lookup"><span data-stu-id="e823b-227">A variable that points to a new instance of a **\_Recordset** object is declared as follows:</span></span>

```cpp 
 
_RecordsetPtr rs("ADODB.Recordset"); 
```

<span data-ttu-id="e823b-228">\-または -</span><span class="sxs-lookup"><span data-stu-id="e823b-228">\-or-</span></span>

```cpp 
 
_RecordsetPtr rs; 
rs.CreateInstance("ADODB.Recordset"); 
```

<span data-ttu-id="e823b-229">\-または -</span><span class="sxs-lookup"><span data-stu-id="e823b-229">\-or-</span></span>

```cpp 
 
_RecordsetPtr rs; 
rs.CreateInstance(__uuidof(_Recordset)); 
```

<span data-ttu-id="e823b-230">**CreateInstance** メソッドの呼び出し後に、この変数を次のように使用できます。</span><span class="sxs-lookup"><span data-stu-id="e823b-230">After the **CreateInstance** method is called, the variable can be used as follows:</span></span>

```cpp 
 
rs->Open(...); 
```

<span data-ttu-id="e823b-231">1 つのケースでいることを確認、"です。"演算子は、変数が (rs クラスのインスタンスであるかのように使用。CreateInstance) と別のケースで、"-\>"演算子は、変数がインターフェイスへのポインターであるかのように使用 (rs -\>オープン)。</span><span class="sxs-lookup"><span data-stu-id="e823b-231">Notice that in one case, the "." operator is used as if the variable were an instance of a class (rs.CreateInstance), and in another case, the "-\>" operator is used as if the variable were a pointer to an interface (rs-\>Open).</span></span>

<span data-ttu-id="e823b-232">2 つの方法の 1 つの変数を使用できます、"-\>"インターフェイスへのポインターのように動作するクラスのインスタンスを許可する演算子をオーバー ロードします。</span><span class="sxs-lookup"><span data-stu-id="e823b-232">One variable can be used in two ways because the "-\>" operator is overloaded to allow an instance of a class to behave like a pointer to an interface.</span></span> <span data-ttu-id="e823b-233">インスタンス変数のプライベート クラス メンバーへのポインターを含む、**\_レコード セット**インタ フェースです。"-\>"演算子がそのポインターを返します。返されたポインターのメンバーにアクセスして、**\_レコード セット**オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="e823b-233">A private class member of the instance variable contains a pointer to the **\_Recordset** interface; the "-\>" operator returns that pointer; and the returned pointer accesses the members of the **\_Recordset** object.</span></span>

### <a name="coding-a-missing-parameter"></a><span data-ttu-id="e823b-234">欠落しているパラメーターのコーディング</span><span class="sxs-lookup"><span data-stu-id="e823b-234">Coding a missing parameter</span></span>

#### <a name="string"></a><span data-ttu-id="e823b-235">String</span><span class="sxs-lookup"><span data-stu-id="e823b-235">String</span></span>

<span data-ttu-id="e823b-236">Visual Basic で省略可能な文字列型 ( **String** ) のオペランドをコーディングする場合は、単純にそのオペランドを省略します。</span><span class="sxs-lookup"><span data-stu-id="e823b-236">When you need to code a missing **String** operand in Visual Basic, you merely omit the operand.</span></span> <span data-ttu-id="e823b-237">Visual C++ では、そのオペランドを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e823b-237">You must specify the operand in Visual C++.</span></span> <span data-ttu-id="e823b-238">コードは**\_bstr\_t**の値として空の文字列を持ちます。</span><span class="sxs-lookup"><span data-stu-id="e823b-238">Code a **\_bstr\_t** that has an empty string as a value.</span></span>

```cpp 
 
_bstr_t strMissing(L""); 
```

#### <a name="variant"></a><span data-ttu-id="e823b-239">バリアント型</span><span class="sxs-lookup"><span data-stu-id="e823b-239">Variant</span></span>

<span data-ttu-id="e823b-240">Visual Basic で省略可能なバリアント型 ( **Variant** ) のオペランドをコーディングする場合は、単純にそのオペランドを省略します。</span><span class="sxs-lookup"><span data-stu-id="e823b-240">When you need to code a missing **Variant** operand in Visual Basic, you merely omit the operand.</span></span> <span data-ttu-id="e823b-241">Visual C++ では、そのオペランドを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e823b-241">You must specify all operands in Visual C++.</span></span> <span data-ttu-id="e823b-242">コードで不足している**バリアント型**パラメーター、**\_バリアント\_t**変位、特別な値に設定\_E\_PARAMNOTFOUND、および、型の VT\_エラーです。</span><span class="sxs-lookup"><span data-stu-id="e823b-242">Code a missing **Variant** parameter with a **\_variant\_t** set to the special value, DISP\_E\_PARAMNOTFOUND, and type, VT\_ERROR.</span></span> <span data-ttu-id="e823b-243">**VtMissing**同等であるの代わりに、指定によって定義済みの定数が指定された、**\#インポート**ディレクティブです。</span><span class="sxs-lookup"><span data-stu-id="e823b-243">Alternatively, specify **vtMissing**, which is an equivalent pre-defined constant supplied by the **\#import** directive.</span></span>

```cpp 
 
_variant_t vtMissingYours(DISP_E_PARAMNOTFOUND, VT_ERROR); 
```

<span data-ttu-id="e823b-244">\-またはを使用して-</span><span class="sxs-lookup"><span data-stu-id="e823b-244">\-or use -</span></span>

```cpp 
 
...vtMissing...; 
```

### <a name="declaring-a-variant"></a><span data-ttu-id="e823b-245">バリアント型を宣言します。</span><span class="sxs-lookup"><span data-stu-id="e823b-245">Declaring a variant</span></span>

<span data-ttu-id="e823b-246">Visual Basic では、バリアント型 ( **Variant** ) は次のように **Dim** ステートメントで宣言します。</span><span class="sxs-lookup"><span data-stu-id="e823b-246">In Visual Basic, a **Variant** is declared with the **Dim** statement as follows:</span></span>

```vb 
 
Dim VariableName As Variant 
```

<span data-ttu-id="e823b-247">Visual C++ の型として変数を宣言**\_バリアント\_t**。</span><span class="sxs-lookup"><span data-stu-id="e823b-247">In Visual C++, declare a variable as type **\_variant\_t**.</span></span> <span data-ttu-id="e823b-248">いくつかの回路図**\_バリアント\_t**の宣言を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="e823b-248">A few schematic **\_variant\_t** declarations are shown below.</span></span>

> [!NOTE]
> <span data-ttu-id="e823b-p139">[!メモ] これらの宣言では、プログラムでコーディングする内容の概要のみを示しています。詳細については、後の例や Visual C++ のドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="e823b-p139">These declarations merely give a rough idea of what you would code in your own program. For more information, see the examples below, and the Visual C++ documentation.</span></span>

```cpp 
 
_variant_t VariableName(value); 
_variant_t VariableName((data type cast) value); 
_variant_t VariableName(value, VT_DATATYPE); 
_variant_t VariableName(interface * value, bool fAddRef = true); 
```

### <a name="using-arrays-of-variants"></a><span data-ttu-id="e823b-251">バリアントの配列を使用します。</span><span class="sxs-lookup"><span data-stu-id="e823b-251">Using arrays of variants</span></span>

<span data-ttu-id="e823b-252">Visual Basic では、バリアント型 ( **Variant** ) の配列は **Dim** ステートメントを使用するか、または **Array** 関数を使用してコーディングできます。次にコード例を示します。</span><span class="sxs-lookup"><span data-stu-id="e823b-252">In Visual Basic, arrays of **Variants** can be coded with the **Dim** statement, or you may use the **Array** function, as demonstrated in the following example code:</span></span>

```vb 
 
Public Sub ArrayOfVariants 
Dim cn As ADODB.Connection 
Dim rs As ADODB.Recordset 
Dim fld As ADODB.Field 
 
cn.Open "DSN=pubs", "sa", "" 
rs = cn.OpenSchema(adSchemaColumns, _ 
 Array(Empty, Empty, "authors", Empty)) 
For Each fld in rs.Fields 
 Debug.Print "Name = "; fld.Name 
Next fld 
rs.Close 
cn.Close 
End Sub 
```

<span data-ttu-id="e823b-253">Visual C++ の例を次に使用される**SafeArray**を使用する、**\_バリアント\_t**。</span><span class="sxs-lookup"><span data-stu-id="e823b-253">The following Visual C++ example demonstrates using a **SafeArray** used with a **\_variant\_t**.</span></span>

> [!NOTE]
> <span data-ttu-id="e823b-254">[!メモ] 次の注意事項は、コード例のコメント部分に対応しています。</span><span class="sxs-lookup"><span data-stu-id="e823b-254">The following notes correspond to commented sections in the code example.</span></span>

1. <span data-ttu-id="e823b-255">既存のエラー処理機構を利用するために、もう一度、TESTHR() インライン関数を定義します。</span><span class="sxs-lookup"><span data-stu-id="e823b-255">Once again, the TESTHR() inline function is defined to take advantage of the existing error-handling mechanism.</span></span>

2. <span data-ttu-id="e823b-p140">必要なのは 1 次元配列のみであるため、汎用の **SAFEARRAYBOUND** 宣言と **SafeArrayCreate** 関数の代わりに **SafeArrayCreateVector** 関数を使用できます。次に、 **SafeArrayCreate** を使用した場合のコードを示します。</span><span class="sxs-lookup"><span data-stu-id="e823b-p140">You only need a one-dimensional array, so you can use **SafeArrayCreateVector**, instead of the general purpose **SAFEARRAYBOUND** declaration and **SafeArrayCreate** function. The following is what that code would look like using **SafeArrayCreate**:</span></span>
    
   ```cpp 
     
     SAFEARRAYBOUND sabound[1]; 
     sabound[0].lLbound = 0; 
     sabound[0].cElements = 4; 
     pSa = SafeArrayCreate(VT_VARIANT, 1, sabound); 
   ```

3. <span data-ttu-id="e823b-258">列挙定数**adSchemaColumns**、によって識別されるスキーマは、次の 4 つの制約列に関連付けられている: テーブル\_カタログ、テーブル\_スキーマ、テーブル\_名、および列\_名です。</span><span class="sxs-lookup"><span data-stu-id="e823b-258">The schema identified by the enumerated constant, **adSchemaColumns**, is associated with four constraint columns: TABLE\_CATALOG, TABLE\_SCHEMA, TABLE\_NAME, and COLUMN\_NAME.</span></span> <span data-ttu-id="e823b-259">したがって、4 つの要素を持つバリアント型 ( **Variant** ) の値の配列が作成されます。</span><span class="sxs-lookup"><span data-stu-id="e823b-259">Therefore, an array of **Variant** values with four elements is created.</span></span> <span data-ttu-id="e823b-260">3 番目の列では、テーブルに対応する制約値にし、\_の名前が指定されています。</span><span class="sxs-lookup"><span data-stu-id="e823b-260">Then a constraint value that corresponds to the third column, TABLE\_NAME, is specified.</span></span> <span data-ttu-id="e823b-261">返される **Recordset** はいくつかの列で構成され、そのサブセットは制約列です。</span><span class="sxs-lookup"><span data-stu-id="e823b-261">The **Recordset** that is returned consists of several columns, a subset of which is the constraint columns.</span></span> <span data-ttu-id="e823b-262">返される各行に対する制約列の値は、対応する制約値と同じである必要があります。</span><span class="sxs-lookup"><span data-stu-id="e823b-262">The values of the constraint columns for each returned row must be the same as the corresponding constraint values.</span></span>

4. <span data-ttu-id="e823b-263">ご存知の**Safearray**を見て驚かれるかもしれません**SafeArrayDestroy**() が終了する前に呼び出されません。</span><span class="sxs-lookup"><span data-stu-id="e823b-263">Those familiar with **SafeArrays** may be surprised that **SafeArrayDestroy**() is not called before the exit.</span></span> <span data-ttu-id="e823b-264">実際、 **SafeArrayDestroy**() を呼び出してここで例外が発生実行時。</span><span class="sxs-lookup"><span data-stu-id="e823b-264">In fact, calling **SafeArrayDestroy**() in this case will cause a run-time exception.</span></span> <span data-ttu-id="e823b-265">理由は、vtCriteria のデストラクターが**VariantClear**() を呼び出すことと、**\_バリアント\_t** **SafeArray**を開放するには、スコープ外に出る。</span><span class="sxs-lookup"><span data-stu-id="e823b-265">The reason is that the destructor for vtCriteria will call **VariantClear**() when the **\_variant\_t** goes out of scope, which will free the **SafeArray**.</span></span> <span data-ttu-id="e823b-266">**SafeArrayDestroy**を呼び出すことを手動でオフにすることがなく、**\_バリアント\_t**、デストラクターが無効な**SafeArray**ポインターをオフにしようとしていますが発生します。</span><span class="sxs-lookup"><span data-stu-id="e823b-266">Calling **SafeArrayDestroy**, without manually clearing the **\_variant\_t**, would cause the destructor to try to clear an invalid **SafeArray** pointer.</span></span> <span data-ttu-id="e823b-267">**SafeArrayDestroy** を呼び出した場合、コードは次のようになります。</span><span class="sxs-lookup"><span data-stu-id="e823b-267">If **SafeArrayDestroy** were called, the code would look like this:</span></span>
    
   ```cpp 
     
     TESTHR(SafeArrayDestroy(pSa)); 
     vtCriteria.vt = VT_EMPTY; 
     vtCriteria.parray = NULL; 
   ```
    
   <span data-ttu-id="e823b-268">ただし、ことができるようにした方が簡単、**\_バリアント\_t** **SafeArray**を管理します。</span><span class="sxs-lookup"><span data-stu-id="e823b-268">However, it is much simpler to let the **\_variant\_t** manage the **SafeArray**.</span></span>


```cpp 
 
    #import "c:\Program Files\Common Files\System\ADO\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
    #include <stdio.h> 
    
    // Note 1 
    inline void TESTHR( HRESULT _hr ) 
    { if FAILED(_hr) _com_issue_error(_hr); } 
    
    void main(void) 
    { 
    CoInitialize(NULL); 
    try 
    { 
    _RecordsetPtr pRs("ADODB.Recordset"); 
    _ConnectionPtr pCn("ADODB.Connection"); 
    _variant_t vtTableName("authors"), 
    vtCriteria; 
    long ix[1]; 
    SAFEARRAY *pSa = NULL; 
    
    pCn->Open("DSN=pubs;User ID=MyUserId;pwd=MyPassword;Provider=MSDASQL;", "", "", 
    adConnectUnspecified); 
    // Note 2, Note 3 
    pSa = SafeArrayCreateVector(VT_VARIANT, 1, 4); 
    if (!pSa) _com_issue_error(E_OUTOFMEMORY); 
    
    // Specify TABLE_NAME in the third array element (index of 2). 
    
    ix[0] = 2; 
    TESTHR(SafeArrayPutElement(pSa, ix, &vtTableName)); 
    
    // There is no Variant constructor for a SafeArray, so manually set the 
    // type (SafeArray of Variant) and value (pointer to a SafeArray). 
    
    vtCriteria.vt = VT_ARRAY | VT_VARIANT; 
    vtCriteria.parray = pSa; 
    
    pRs = pCn->OpenSchema(adSchemaColumns, vtCriteria, vtMissing); 
    
    long limit = pRs->GetFields()->Count; 
    for (long x = 0; x < limit; x++) 
    printf("%d: %s\n", x+1, 
    ((char*) pRs->GetFields()->Item[x]->Name)); 
    // Note 4 
    pRs->Close(); 
    pCn->Close(); 
    } 
    catch (_com_error &e) 
    { 
    printf("Error:\n"); 
    printf("Code = %08lx\n", e.Error()); 
    printf("Code meaning = %s\n", (char*) e.ErrorMessage()); 
    printf("Source = %s\n", (char*) e.Source()); 
    printf("Description = %s\n", (char*) e.Description()); 
    } 
    CoUninitialize(); 
    } 
```

### <a name="using-property-getputputref"></a><span data-ttu-id="e823b-269">プロパティ取得、構造体、PutRef Put を使用します。</span><span class="sxs-lookup"><span data-stu-id="e823b-269">Using property Get/Put/PutRef</span></span>

<span data-ttu-id="e823b-270">Visual Basic では、プロパティが取得、割り当て、または参照を割り当てられるかどうかによって、プロパティの名前が修飾されることはありません。</span><span class="sxs-lookup"><span data-stu-id="e823b-270">In Visual Basic, the name of a property is not qualified by whether it is retrieved, assigned, or assigned a reference.</span></span>

```vb
    Public Sub GetPutPutRef 
    Dim rs As New ADODB.Recordset 
    Dim cn As New ADODB.Connection 
    Dim sz as Integer 
    cn.Open "Provider=sqloledb;Data Source=yourserver;" & _ 
     "Initial Catalog=pubs;Integrated Security=SSPI;" 
    rs.PageSize = 10 
    sz = rs.PageSize 
    rs.ActiveConnection = cn 
    rs.Open "authors",,adOpenStatic 
    ' ... 
    rs.Close 
    cn.Close 
    End Sub
```

<span data-ttu-id="e823b-271">この Visual C++ の例は、**取得**/**に**/\**PutRef。 プロパティ*。</span><span class="sxs-lookup"><span data-stu-id="e823b-271">This Visual C++ example demonstrates the **Get**/**Put**/\**PutRef\*\*\*Property*.</span></span>

> [!NOTE]
> <span data-ttu-id="e823b-272">[!メモ] 次の注意事項は、コード例のコメント部分に対応しています。</span><span class="sxs-lookup"><span data-stu-id="e823b-272">The following notes correspond to commented sections in the code example.</span></span>

1. <span data-ttu-id="e823b-273">不足している文字列の引数の 2 つのフォームを使用して、次の使用例: 明示的な定数**strMissing**と一時領域を作成するコンパイラを使用する文字列**\_bstr\_t**の**Open**メソッドのスコープが存在します。</span><span class="sxs-lookup"><span data-stu-id="e823b-273">This example uses two forms of a missing string argument: an explicit constant, **strMissing**, and a string that the compiler will use to create a temporary **\_bstr\_t** that will exist for the scope of the **Open** method.</span></span>

2. <span data-ttu-id="e823b-274">Rs のオペランドをキャストする必要はありません\>に PutRefActiveConnection(cn) (IDispatch \*) のオペランドの型が既にあるため (IDispatch \*)。</span><span class="sxs-lookup"><span data-stu-id="e823b-274">It isn't necessary to cast the operand of rs-\>PutRefActiveConnection(cn) to (IDispatch \*) because the type of the operand is already (IDispatch \*).</span></span>
    
   ```cpp 
     
    #import "c:\Program Files\Common Files\System\ADO\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
    #include <stdio.h> 
     
    void main(void) 
    { 
     CoInitialize(NULL); 
     try 
     { 
     _ConnectionPtr cn("ADODB.Connection"); 
     _RecordsetPtr rs("ADODB.Recordset"); 
     _bstr_t strMissing(L""); 
     long oldPgSz = 0, 
     newPgSz = 5; 
     
    // Note 1 
     cn->Open("Provider=sqloledb;Data Source=MyServer;" 
     "Initial Catalog=pubs;Integrated Security=SSPI;", 
     strMissing, "", 
     adConnectUnspecified); 
     
     oldPgSz = rs->GetPageSize(); 
     // -or- 
     oldPgSz = rs->PageSize; 
     
     rs->PutPageSize(newPgSz); 
     // -or- 
     rs->PageSize = newPgSz; 
     
    // Note 2 
     rs->PutRefActiveConnection( cn ); 
     rs->Open("authors", vtMissing, adOpenStatic, adLockReadOnly, 
     adCmdTable); 
     printf("Original pagesize = %d, new pagesize = %d\n", oldPgSz, 
     rs->GetPageSize()); 
     rs->Close(); 
     cn->Close(); 
     } 
     catch (_com_error &e) 
     { 
     printf("Description = %s\n", (char*) e.Description()); 
     } 
     ::CoUninitialize(); 
    } 
   ```

### <a name="using-getitemx-and-itemx"></a><span data-ttu-id="e823b-275">GetItem(x) とアイテムを使用して\[x\]</span><span class="sxs-lookup"><span data-stu-id="e823b-275">Using GetItem(x) and Item\[x\]</span></span>

<span data-ttu-id="e823b-276">この Visual Basic の例では、**Item**() の標準構文と代替構文を示します。</span><span class="sxs-lookup"><span data-stu-id="e823b-276">This Visual Basic example demonstrates the standard and alternative syntax for **Item**().</span></span>

```vb 
 
Public Sub GetItemItem 
Dim rs As New ADODB.Recordset 
Dim name as String 
rs = rs.Open "authors", "DSN=pubs;", adOpenDynamic, _ 
 adLockBatchOptimistic, adTable 
name = rs(0) 
' -or- 
name = rs.Fields.Item(0) 
rs(0) = "Test" 
rs.UpdateBatch 
' Restore name 
rs(0) = name 
rs.UpdateBatch 
rs.Close 
End Sub 
```

<span data-ttu-id="e823b-277">この Visual C++ の例は、 **Item** を示します。</span><span class="sxs-lookup"><span data-stu-id="e823b-277">This Visual C++ example demonstrates **Item**.</span></span>

> [!NOTE]
> <span data-ttu-id="e823b-278">[!メモ] 次の注意事項は、コード例のコメント部分に対応しています。</span><span class="sxs-lookup"><span data-stu-id="e823b-278">The following note corresponds to commented sections in the code example.</span></span>

1. <span data-ttu-id="e823b-279">コレクションに **Item** を使用してアクセスした場合、適切なコンストラクターが呼び出されるように、インデックス **2** が **long** にキャストされる必要があります。</span><span class="sxs-lookup"><span data-stu-id="e823b-279">When the collection is accessed with **Item**, the index, **2**, must be cast to **long** so an appropriate constructor will be invoked.</span></span>
    
   ```cpp 
     
    #import "c:\Program Files\Common Files\System\ADO\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
    #include <stdio.h> 
     
    void main(void) 
    { 
     CoInitialize(NULL); 
     try { 
     _RecordsetPtr rs("ADODB.Recordset"); 
     _variant_t vtFirstName; 
     
     rs->Open("authors", 
     "Provider=sqloledb;Data Source=MyServer;" 
     "Initial Catalog=pubs;Integrated Security=SSPI;", 
     adOpenStatic, adLockOptimistic, adCmdTable); 
     rs->MoveFirst(); 
     
    // Note 1. Get a field. 
     vtFirstName = rs->Fields->GetItem((long)2)->GetValue(); 
     // -or- 
     vtFirstName = rs->Fields->Item[(long)2]->Value; 
     
     printf( "First name = '%s'\n", (char*) ((_bstr_t) vtFirstName)); 
     
     rs->Fields->GetItem((long)2)->Value = L"TEST"; 
     rs->Update(vtMissing, vtMissing); 
     
     // Restore name 
     rs->Fields->GetItem((long)2)->PutValue(vtFirstName); 
     // -or- 
     rs->Fields->GetItem((long)2)->Value = vtFirstName; 
     rs->Update(vtMissing, vtMissing); 
     rs->Close(); 
     } 
     catch (_com_error &e) 
     { 
     printf("Description = '%s'\n", (char*) e.Description()); 
     } 
     ::CoUninitialize(); 
    } 
   ```

### <a name="casting-ado-object-pointers-with-idispatch-"></a><span data-ttu-id="e823b-280">(IDispatch \*) による ADO オブジェクト ポインターのキャスト</span><span class="sxs-lookup"><span data-stu-id="e823b-280">Casting ADO object pointers with (IDispatch \*)</span></span>

<span data-ttu-id="e823b-281">次の Visual C++ の例では、(IDispatch \*) を使用した ADO オブジェクト ポイントのキャストを示します。</span><span class="sxs-lookup"><span data-stu-id="e823b-281">The following Visual C++ example demonstrates using (IDispatch \*) to cast ADO object pointers.</span></span>

> [!NOTE]
> <span data-ttu-id="e823b-282">[!メモ] 次の注意事項は、コード例のコメント部分に対応しています。</span><span class="sxs-lookup"><span data-stu-id="e823b-282">The following notes correspond to commented sections in the code example.</span></span>

1. <span data-ttu-id="e823b-283">明示的にコーディングされたバリアント型 ( **Variant** ) で、開いている **Connection** オブジェクトを指定します。</span><span class="sxs-lookup"><span data-stu-id="e823b-283">Specify an open **Connection** object in an explicitly coded **Variant**.</span></span> <span data-ttu-id="e823b-284">キャスト (IDispatch \*)、適切なコンス トラクターが呼び出されるようにします。</span><span class="sxs-lookup"><span data-stu-id="e823b-284">Cast it with (IDispatch \*) so the correct constructor will be invoked.</span></span> <span data-ttu-id="e823b-285">また、2 番目を明示的に設定**\_バリアント\_t**パラメーター、既定値**は true**、 **Recordset::Open**操作が終了したときに、オブジェクトの参照カウントが正しくありますので。</span><span class="sxs-lookup"><span data-stu-id="e823b-285">Also, explicitly set the second **\_variant\_t** parameter to the default value of **true**, so the object reference count will be correct when the **Recordset::Open** operation ends.</span></span>

2. <span data-ttu-id="e823b-286">式 (\_bstr\_t)、キャストではありませんが、**\_バリアント\_t**を抽出するための演算子、 \*\* \_bstr\_t\*\* **値**によって返される**バリアント型**の文字列。</span><span class="sxs-lookup"><span data-stu-id="e823b-286">The expression, (\_bstr\_t), is not a cast, but a **\_variant\_t** operator that extracts a **\_bstr\_t** string from the **Variant** returned by **Value**.</span></span> <span data-ttu-id="e823b-287">式 (char\*)、キャストではありませんが、 \*\* \_bstr\_t**にカプセル化された文字列へのポインターを抽出するための演算子、 \*\* \_bstr\_t**オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="e823b-287">The expression, (char\*), is not a cast, but a **\_bstr\_t** operator that extracts a pointer to the encapsulated string in a **\_bstr\_t** object.</span></span> <span data-ttu-id="e823b-288">コードのこのセクションでは、いくつかの便利な動作を示します**\_バリアント\_t**と**\_bstr\_t**演算子です。</span><span class="sxs-lookup"><span data-stu-id="e823b-288">This section of code demonstrates some of the useful behaviors of **\_variant\_t** and **\_bstr\_t** operators.</span></span>
    
   ```cpp 
     
    #import "c:\Program Files\Common Files\System\ADO\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
     
    #include <stdio.h> 
     
    void main(void) 
    { 
     CoInitialize(NULL); 
     try 
     { 
     _ConnectionPtr pConn("ADODB.Connection"); 
     _RecordsetPtr pRst("ADODB.Recordset"); 
     
     pConn->Open("Provider=sqloledb;Data Source=MyServer;" 
     "Initial Catalog=pubs;Integrated Security=SSPI;", 
     "", "", adConnectUnspecified); 
    // Note 1. 
     pRst->Open( 
     "authors", 
     _variant_t((IDispatch *) pConn, true), 
     adOpenStatic, 
     adLockReadOnly, 
     adCmdTable); 
     pRst->MoveLast(); 
    // Note 2. 
     printf("Last name is '%s %s'\n", 
     (char*) ((_bstr_t) pRst->GetFields()->GetItem("au_fname")->GetValue()), 
     (char*) ((_bstr_t) pRst->Fields->Item["au_lname"]->Value)); 
     
     pRst->Close(); 
     pConn->Close(); 
     } 
     catch (_com_error &e) 
     { 
     printf("Description = '%s'\n", (char*) e.Description()); 
     } 
    ::CoUninitialize(); 
    } 
   ```

