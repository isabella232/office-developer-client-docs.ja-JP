---
title: Excel で DLL にアクセスする
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- DLL にアクセスする [Excel 2007]、DLL [Excel 2007]、Excel でアクセスする
localization_priority: Normal
ms.assetid: e2bfd6ea-efa3-45c1-a5b8-2ccb8650c6ab
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: bfb562b6bbe824124c6b5a691745d076720ee004
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798884"
---
# <a name="access-dlls-in-excel"></a><span data-ttu-id="f8ce3-104">Excel で DLL にアクセスする</span><span class="sxs-lookup"><span data-stu-id="f8ce3-104">How to: Access DLLs in Excel</span></span>

<span data-ttu-id="f8ce3-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f8ce3-105">Applies to: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="f8ce3-106">Microsoft Excel の DLL 関数やコマンドには、さまざまな方法でアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="f8ce3-106">You can access a DLL function or command in Microsoft Excel in several ways:</span></span>
  
- <span data-ttu-id="f8ce3-107">**Declare** ステートメントを使用して、関数またはコマンドが使用可能できるようになっている Microsoft Visual Basic for Applications (VBA) コード モジュールを通じてアクセスする。</span><span class="sxs-lookup"><span data-stu-id="f8ce3-107">Through a Microsoft Visual Basic for Applications (VBA) code module in which the function or command has been made available using a **Declare** statement.</span></span> 
    
- <span data-ttu-id="f8ce3-108">**CALL** 関数または **REGISTER** 関数を使用して、XLM マクロ シートを通じてアクセスする。</span><span class="sxs-lookup"><span data-stu-id="f8ce3-108">Through an XLM macro sheet by using the **CALL** or **REGISTER** functions.</span></span> 
    
- <span data-ttu-id="f8ce3-109">直接ワークシートから、またはユーザー インターフェイス (UI) のカスタマイズされた項目からアクセスする。</span><span class="sxs-lookup"><span data-stu-id="f8ce3-109">Directly from the worksheet or from a customized item in the user interface (UI).</span></span>
    
<span data-ttu-id="f8ce3-p101">このドキュメントでは、XLM 関数については説明しません。それ以外の 2 つの方法のうち、どちらかを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="f8ce3-p101">This documentation does not cover XLM functions. It is recommended that you use either of the other two approaches.</span></span>
  
<span data-ttu-id="f8ce3-p102">直接ワークシートから、または UI のカスタマイズされた項目からアクセスするには、最初に関数またはコマンドを Excel に登録する必要があります。コマンドと関数の登録の詳細については、「[Excel で XLL コードにアクセスする](accessing-xll-code-in-excel.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8ce3-p102">To be accessed directly from the worksheet or from a customized item in the UI, the function or command must first be registered with Excel. For information about registering commands and functions, see [Accessing XLL Code in Excel](accessing-xll-code-in-excel.md).</span></span>
  
## <a name="calling-dll-functions-and-commands-from-vba"></a><span data-ttu-id="f8ce3-114">VBA から DLL 関数およびコマンドを呼び出す</span><span class="sxs-lookup"><span data-stu-id="f8ce3-114">Calling DLL Functions and Commands from VBA</span></span>

<span data-ttu-id="f8ce3-p103">**Declare** ステートメントを使用して、VBA の DLL 関数とコマンドにアクセスすることができます。このステートメントには、コマンド用の構文と関数用の構文が 1 つずつあります。</span><span class="sxs-lookup"><span data-stu-id="f8ce3-p103">You can access DLL functions and commands in VBA by using the **Declare** statement. This statement has one syntax for commands and one for functions.</span></span> 
  
- <span data-ttu-id="f8ce3-117">**構文 1 - コマンド**</span><span class="sxs-lookup"><span data-stu-id="f8ce3-117">**Syntax 1 - commands**</span></span>
    
  ```vb
  [Public | Private] Declare Sub name Lib "libname" [Alias "aliasname"] [([arglist])]
  ```

- <span data-ttu-id="f8ce3-118">**構文 2 - 関数**</span><span class="sxs-lookup"><span data-stu-id="f8ce3-118">**Syntax 2 - functions**</span></span>
    
  ```vb
  [Public | Private] Declare Function name Lib "libname" [Alias "aliasname"] [([arglist])] [As type]
  ```

<span data-ttu-id="f8ce3-p104">オプションの **Public** キーワードおよび **Private** キーワードはインポートされた関数のスコープを示し、それぞれ Visual Basic プロジェクト全体と Visual Basic モジュールのみを指定します。名前は VBA コードで使用する名前です。この名前が DLL の名前と異なる場合は、別名 "aliasname" 指定子を使用する必要があります。また、DLL によってエクスポートされる関数の名前を付ける必要があります。DLL の序数を参照して DLL 関数にアクセスする場合は、プレフィックスが **#** の序数であるエイリアス名を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f8ce3-p104">The optional **Public** and **Private** keywords specify the scope of the imported function: the entire Visual Basic project or just the Visual Basic module, respectively. The name is the name that you want to use in the VBA code. If this differs from the name in the DLL, you must use the Alias "aliasname" specifier, and you should give the name of the function as exported by the DLL. If you want to access a DLL function by reference to a DLL ordinal number, you must provide an alias name, which is the ordinal prefixed by **#**.</span></span>
  
<span data-ttu-id="f8ce3-p105">コマンドは **void** を返す必要があります。関数は、VBA が **ByVal** と認識できる型を返す必要があります。つまり、いくつかの型 (文字列、配列、ユーザー定義型、オブジェクト) は引数をインプレースで変更することで、より簡単に返されるということです。</span><span class="sxs-lookup"><span data-stu-id="f8ce3-p105">Commands should return **void**. Functions should return types that VBA can recognize **ByVal**. This means that some types are more easily returned by modifying arguments in place: strings, arrays, user-defined types, and objects.</span></span>
  
> [!NOTE]
> <span data-ttu-id="f8ce3-p106">VBA では、Visual Basic モジュールで示された引数リストと戻り値が DLL でコード化されたものと同じであることを確認できません。間違いがあると Excel がクラッシュする可能性があるため、自身で慎重に確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f8ce3-p106">VBA cannot check that the argument list and return stated in the Visual Basic module are the same as coded in the DLL. You should check this yourself very carefully, because a mistake could cause Excel to crash.</span></span> 
  
<span data-ttu-id="f8ce3-p107">関数またはコマンドの引数が参照またはポインターによって渡されない場合、**arglist** 宣言の **ByVal** キーワードを前に付ける必要があります。C/C++ 関数がポインター引数を受け取る場合、または C++ 関数が参照引数を受け取る場合は、**ByRef** を渡す必要があります。**ByRef** キーワードは、VBA の既定値であるため、引数リストから省略できます。</span><span class="sxs-lookup"><span data-stu-id="f8ce3-p107">When the function or command's arguments are not passed by reference or pointer, they must be preceded by the **ByVal** keyword in the **arglist** declaration. When a C/C++ function takes pointer arguments, or a C++ function takes reference arguments, they should be passed **ByRef**. The keyword **ByRef** can be omitted from argument lists because it is the default in VBA.</span></span> 
  
### <a name="argument-types-in-cc-and-vba"></a><span data-ttu-id="f8ce3-131">C/C++ および VBA の引数の型</span><span class="sxs-lookup"><span data-stu-id="f8ce3-131">Argument Types in C/C++ and VBA</span></span>

<span data-ttu-id="f8ce3-132">C/C++ と VBA の引数の型の宣言を比較するときには、次の点に注意が必要です。</span><span class="sxs-lookup"><span data-stu-id="f8ce3-132">You should note the following when you compare the declarations of argument types in C/C++ and VBA.</span></span>
  
- <span data-ttu-id="f8ce3-133">VBA の **String** は、ByVal 渡しの場合はバイト文字列 BSTR 構造体へのポインターとして渡されます。**ByRef** 渡しの場合はポインターへのポインターとして渡されます。</span><span class="sxs-lookup"><span data-stu-id="f8ce3-133">A VBA **String** is passed as a pointer to a byte-string BSTR structure when passed ByVal, and as a pointer to a pointer when passed **ByRef**.</span></span>
    
- <span data-ttu-id="f8ce3-134">文字列を格納している VBA の **Variant** は、**ByVal** 渡しの場合は Unicode ワイド文字文字列 BSTR 構造体へのポインターとして渡されます。**ByRef** 渡しの場合はポインターへのポインターとして渡されます。</span><span class="sxs-lookup"><span data-stu-id="f8ce3-134">A VBA **Variant** that contains a string is passed as a pointer to a Unicode wide-character string BSTR structure when passed **ByVal**, and as a pointer to a pointer when passed **ByRef**.</span></span>
    
- <span data-ttu-id="f8ce3-135">VBA の **Integer** は、C/C++ の signed short と同等の 16 ビット型です。</span><span class="sxs-lookup"><span data-stu-id="f8ce3-135">The VBA **Integer** is a 16-bit type equivalent to a signed short in C/C++.</span></span> 
    
- <span data-ttu-id="f8ce3-136">VBA の **Long** は、C/C++ の signed int と同等の 32 ビット型です。</span><span class="sxs-lookup"><span data-stu-id="f8ce3-136">The VBA **Long** is a 32-bit type equivalent to a signed int in C/C++.</span></span> 
    
- <span data-ttu-id="f8ce3-137">VBA と C/C++ は、どちらもユーザー定義データ型の定義が可能です。それぞれ、**Type** ステートメントと **struct** ステートメントを使用します。</span><span class="sxs-lookup"><span data-stu-id="f8ce3-137">Both VBA and C/C++ allow the definition of user-defined data types, using the **Type** and **struct** statements respectively.</span></span> 
    
- <span data-ttu-id="f8ce3-138">VBA と C/C++ は、どちらも **Variant** データ型をサポートしています。C/C++ については、Windows OLE/COM ヘッダー ファイル内で VARIANT として定義されています。</span><span class="sxs-lookup"><span data-stu-id="f8ce3-138">Both VBA and C/C++ support the **Variant** data type, defined for C/C++ in the Windows OLE/COM header files as VARIANT.</span></span> 
    
- <span data-ttu-id="f8ce3-139">VBA の配列は OLE の **SafeArrays** です。C/C++ については、Windows OLE/COM ヘッダー ファイル内で **SAFEARRAY** として定義されています。</span><span class="sxs-lookup"><span data-stu-id="f8ce3-139">VBA arrays are OLE **SafeArrays**, defined for C/C++ in the Windows OLE/COM header files as **SAFEARRAY**.</span></span>
    
- <span data-ttu-id="f8ce3-140">VBA の **Currency** データ型は、**ByVal** 渡しの場合は Windows ヘッダー ファイル wtypes.h 内で定義されている **CY** 型の構造体として渡されます。**ByRef** 渡しの場合はそのポインターとして渡されます。</span><span class="sxs-lookup"><span data-stu-id="f8ce3-140">The VBA **Currency** data type is passed as a structure of type **CY**, defined in the Windows header file wtypes.h, when passed **ByVal**, and as a pointer to this when passed **ByRef**.</span></span>
    
<span data-ttu-id="f8ce3-141">VBA では、ユーザー定義データ型のデータ要素は 4 バイト境界にパッキングされます。Visual Studio では、このデータ要素が既定で 8 バイト境界にパッキングされます。</span><span class="sxs-lookup"><span data-stu-id="f8ce3-141">In VBA, data elements in user-defined data types are packed to 4-byte boundaries, whereas in Visual Studio, by default, they are packed to 8-byte boundaries. Therefore you must enclose the C/C++ structure definition in a #pragma pack(4) … #pragma pack() block to avoid elements being misaligned.</span></span> <span data-ttu-id="f8ce3-142">そのため、C/C++ 構造体の定義は `#pragma pack(4) … #pragma pack()` ブロックで囲んで要素の配置がずれないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f8ce3-142">Therefore you must enclose the C/C++ structure definition in a `#pragma pack(4) … #pragma pack()` block to avoid elements being misaligned.</span></span> 
  
<span data-ttu-id="f8ce3-143">次に、同等のユーザー タイプ定義の例を示します。</span><span class="sxs-lookup"><span data-stu-id="f8ce3-143">The following is an example of equivalent user type definitions.</span></span>
  
```vb
Type VB_User_Type
    i As Integer
    d As Double
    s As String
End Type

```

```cpp
#pragma pack(4)
struct C_user_type
{
    short iVal;
    double dVal;
    BSTR bstr; // VBA String type is a byte string
}
#pragma pack() // restore default

```

<span data-ttu-id="f8ce3-p109">VBA は、Excel がサポートするよりも多くの値の範囲をサポートすることがあります。VBA の double は IEEE に準拠していて、現時点のワークシートでは 0 に切り捨てられている非正規化数をサポートしています。VBA の ** Date ** 型は、負のシリアル化された日付を使用して、0100 年 1 月 1 日までの日付を表すことができます。Excel では、0 以上のシリアル化された日付のみが許容されます。VBA の **Currency** 型 (スケーリングされた 64 ビット整数) は、8 バイトの double ではサポートしていない精度を実現できるため、ワークシートでは一致しません。</span><span class="sxs-lookup"><span data-stu-id="f8ce3-p109">VBA supports a greater range of values in some cases than Excel supports. The VBA double is IEEE compliant, supporting subnormal numbers that are currently rounded down to zero on the worksheet. The VBA **Date** type can represent dates as early as 1-Jan-0100 using negative serialized dates. Excel only allows serialized dates greater than or equal to zero. The VBA **Currency** type—a scaled 64-bit integer—can achieve accuracy not supported in 8-byte doubles, and so is not matched in the worksheet.</span></span> 
  
<span data-ttu-id="f8ce3-149">Excel は、VBA ユーザー定義関数に、次に示す型のバリアントのみを渡します。</span><span class="sxs-lookup"><span data-stu-id="f8ce3-149">Excel only passes Variants of the following types to a VBA user-defined function.</span></span>
  
|<span data-ttu-id="f8ce3-150">**VBA データ型**</span><span class="sxs-lookup"><span data-stu-id="f8ce3-150">**VBA data type**</span></span>|<span data-ttu-id="f8ce3-151">**C/C++ バリアント型のビット フラグ**</span><span class="sxs-lookup"><span data-stu-id="f8ce3-151">**C/C++ Variant type bit flags**</span></span>|<span data-ttu-id="f8ce3-152">**説明**</span><span class="sxs-lookup"><span data-stu-id="f8ce3-152">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f8ce3-153">倍精度浮動小数点数</span><span class="sxs-lookup"><span data-stu-id="f8ce3-153">Double</span></span>  <br/> |<span data-ttu-id="f8ce3-154">**VT_R8**</span><span class="sxs-lookup"><span data-stu-id="f8ce3-154">**VT_R8**</span></span> <br/> ||
|<span data-ttu-id="f8ce3-155">ブール型</span><span class="sxs-lookup"><span data-stu-id="f8ce3-155">Boolean</span></span>  <br/> |<span data-ttu-id="f8ce3-156">**VT_BOOL**</span><span class="sxs-lookup"><span data-stu-id="f8ce3-156">**VT_BOOL**</span></span> <br/> ||
|<span data-ttu-id="f8ce3-157">日付</span><span class="sxs-lookup"><span data-stu-id="f8ce3-157">Date</span></span>  <br/> |<span data-ttu-id="f8ce3-158">**VT_DATE**</span><span class="sxs-lookup"><span data-stu-id="f8ce3-158">**VT_DATE**</span></span> <br/> ||
|<span data-ttu-id="f8ce3-159">String</span><span class="sxs-lookup"><span data-stu-id="f8ce3-159">String</span></span>  <br/> |<span data-ttu-id="f8ce3-160">**VT_BSTR**</span><span class="sxs-lookup"><span data-stu-id="f8ce3-160">**VT_BSTR**</span></span> <br/> |<span data-ttu-id="f8ce3-161">OLE Bstr バイト文字列</span><span class="sxs-lookup"><span data-stu-id="f8ce3-161">OLE Bstr byte string</span></span>  <br/> |
|<span data-ttu-id="f8ce3-162">範囲</span><span class="sxs-lookup"><span data-stu-id="f8ce3-162">Range</span></span>  <br/> |<span data-ttu-id="f8ce3-163">**VT_DISPATCH**</span><span class="sxs-lookup"><span data-stu-id="f8ce3-163">**VT_DISPATCH**</span></span> <br/> |<span data-ttu-id="f8ce3-164">範囲とセルの参照</span><span class="sxs-lookup"><span data-stu-id="f8ce3-164">Range and cell references</span></span>  <br/> |
|<span data-ttu-id="f8ce3-165">配列を含むバリアント型</span><span class="sxs-lookup"><span data-stu-id="f8ce3-165">Variant containing an array</span></span>  <br/> |<span data-ttu-id="f8ce3-166">**VT_ARRAY**</span><span class="sxs-lookup"><span data-stu-id="f8ce3-166">**VT_ARRAY**</span></span> | <span data-ttu-id="f8ce3-167">**VT_VARIANT**</span><span class="sxs-lookup"><span data-stu-id="f8ce3-167">**VT_VARIANT**</span></span> <br/> |<span data-ttu-id="f8ce3-168">リテラル配列</span><span class="sxs-lookup"><span data-stu-id="f8ce3-168">Literal arrays</span></span>  <br/> |
|<span data-ttu-id="f8ce3-169">Ccy</span><span class="sxs-lookup"><span data-stu-id="f8ce3-169">Ccy</span></span>  <br/> |<span data-ttu-id="f8ce3-170">**VT_CY**</span><span class="sxs-lookup"><span data-stu-id="f8ce3-170">**VT_CY**</span></span> <br/> |<span data-ttu-id="f8ce3-171">64 ビット整数を拡張して、小数点以下 4 桁に四捨五入した精度を許可します。</span><span class="sxs-lookup"><span data-stu-id="f8ce3-171">64-bit integer scaled to permit 4 decimal places of accuracy.</span></span>  <br/> |
|<span data-ttu-id="f8ce3-172">エラーを含むバリアント型</span><span class="sxs-lookup"><span data-stu-id="f8ce3-172">Variant containing an error</span></span>  <br/> |<span data-ttu-id="f8ce3-173">**VT_ERROR**</span><span class="sxs-lookup"><span data-stu-id="f8ce3-173">**VT_ERROR**</span></span> <br/> ||
||<span data-ttu-id="f8ce3-174">**VT_EMPTY**</span><span class="sxs-lookup"><span data-stu-id="f8ce3-174">**VT_EMPTY**</span></span> <br/> |<span data-ttu-id="f8ce3-175">空のセルまたは省略された引数</span><span class="sxs-lookup"><span data-stu-id="f8ce3-175">Empty cells or omitted arguments</span></span>  <br/> |
   
<span data-ttu-id="f8ce3-p110">**VarType** を使用して、渡された VBA バリアント型の種類を確認できます。ただし、参照を使用して呼び出されたときに範囲の値の型を返す関数を除きます。**バリアント型**が**範囲**の参照オブジェクトであるかどうかを判断するには、**IsObject** 関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="f8ce3-p110">You can check the type of a passed-in Variant in VBA using the **VarType**, except that the function returns the type of the range's values when called with references. To determine if a **Variant** is a **Range** reference object, you can use the **IsObject** function.</span></span> 
  
<span data-ttu-id="f8ce3-p111">**範囲**から VBA のバリアントの配列を含む**バリアント型**を作成するには、その **Value** プロパティを**バリアント型**に割り当てます。ソース範囲内のセルが、その時点での地域設定の標準通貨書式を使用してフォーマットされている場合、**Currency** 型の配列要素に変換されます。日付として書式化されているセルは、**Date** 型の配列要素に変換されます。文字列を含むセルは、ワイド文字の **BSTR** バリアントに変換されます。エラーを含むセルは、**VT_ERROR** 型の**バリアント** に変換されます。**True** または **False** の**ブール値**を含むセルは、**VT_BOOL** 型の**バリアント** に変換されます。</span><span class="sxs-lookup"><span data-stu-id="f8ce3-p111">You can create **Variants** that contain arrays of variants in VBA from a **Range** by assigning its **Value** property to a **Variant**. Any cells in the source range that are formatted using the standard currency format for the regional settings in force at the time are converted to array elements of type **Currency**. Any cells formatted as dates are converted to array elements of type **Date**. Cells containing strings are converted to wide-character **BSTR** Variants. Cells containing errors are converted to **Variants** of type **VT_ERROR**. Cells containing **Boolean** **True** or **False** are converted to **Variants** of type **VT_BOOL**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="f8ce3-p112">この**バリアント型**は、**True** を -1 として、**False** を 0 として格納します。日付または通貨金額として書式化されていない数値は、**VT_R8** 型のバリアントに変換されます。</span><span class="sxs-lookup"><span data-stu-id="f8ce3-p112">The **Variant** stores **True** as -1 and **False** as 0. Numbers not formatted as dates or currency amounts are converted to Variants of type **VT_R8**.</span></span> 
  
### <a name="variant-and-string-arguments"></a><span data-ttu-id="f8ce3-186">バリアント型と文字列の引数</span><span class="sxs-lookup"><span data-stu-id="f8ce3-186">Variant and String Arguments</span></span>

<span data-ttu-id="f8ce3-p113">Excel は、ワイド文字 Unicode 文字列を使用して内部で動作しています。VBA ユーザー定義関数が **String** 引数を取るように宣言されている場合、Excel は指定した文字列をロケール固有の方法でバイト文字列に変換します。関数に Unicode 文字列を渡す場合、VBA ユーザー定義関数は **String** 引数の代わりに**バリアント型**を受け入れる必要があります。その後、DLL 関数は、VBA から **バリアント** BSTR ワイド文字列を受け入れることができます。</span><span class="sxs-lookup"><span data-stu-id="f8ce3-p113">Excel works internally with wide-character Unicode strings. When a VBA user-defined function is declared as taking a **String** argument, Excel converts the supplied string to a byte-string in a locale-specific way. If you want your function to be passed a Unicode string, your VBA user-defined function should accept a **Variant** instead of a **String** argument. Your DLL function can then accept that **Variant** BSTR wide-character string from VBA.</span></span> 
  
<span data-ttu-id="f8ce3-p114">DLL から VBA に Unicode 文字列を返すには、**バリアント**文字列引数を修正する必要があります。これが機能するには、C/C++ コードで**バリアント**へのポインターを使用するよう DLL 関数を宣言し、VBA コードで引数を `ByRef varg As Variant` として宣言する必要があります。古い文字列のメモリを解放し、OLE Bstr 文字列を使用して作成された新しい文字列値は DLL でのみ機能すべきです。</span><span class="sxs-lookup"><span data-stu-id="f8ce3-p114">To return Unicode strings to VBA from a DLL, you should modify a **Variant** string argument in place. For this to work, you must declare the DLL function as taking a pointer to the **Variant** and in your C/C++ code, and declare the argument in the VBA code as  `ByRef varg As Variant`. The old string memory should be released, and the new string value created by using the OLE Bstr string functions only in the DLL.</span></span>
  
<span data-ttu-id="f8ce3-p115">DLL から VBA にバイト文字列を返すには、バイト文字列 BSTR 引数をインプレースで変更する必要があります。これが機能するには、C/C++ コードで BSTR へのポインターへのポインターを使用するよう DLL 関数を宣言し、VBA コードで引数を「**ByRef varg As String**」として宣言する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f8ce3-p115">To return a byte string to VBA from a DLL, you should modify a byte-string BSTR argument in place. For this to work, you must declare the DLL function as taking a pointer to a pointer to the BSTR and in your C/C++ code, and declare the argument in the VBA code as ' **ByRef varg As String**'.</span></span>
  
<span data-ttu-id="f8ce3-p116">このような方法で VBA から渡された文字列は、メモリ関連の問題を避けるために、OLE BSTR 文字列関数を使用してのみ処理する必要があります。たとえば、** SysFreeString** を呼び出して、渡された文字列を上書きする前にメモリを解放し、**SysAllocStringByteLen** または **SysAllocStringLen** を呼び出して、新しい文字列の領域を割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="f8ce3-p116">You should only handle strings that are passed in these ways from VBA using the OLE BSTR string functions to avoid memory-related problems. For example, you must call **SysFreeString** to free the memory before overwriting the passed in string, and **SysAllocStringByteLen** or **SysAllocStringLen** to allocate space for a new string.</span></span> 
  
<span data-ttu-id="f8ce3-p117">次の表に示すように、**CVerr** 関数を引数と共に使用すると、VBA で Excel ワークシートのエラーを**バリアント**として作成できます。ワークシートのエラーは、** VT_ERROR ** 型の**バリアント**を使用し、**ulVal** フィールドに次の値を指定して、DLL から VBA に返すこともできます。</span><span class="sxs-lookup"><span data-stu-id="f8ce3-p117">You can create Excel worksheet errors as **Variants** in VBA by using the **CVerr** function with arguments as shown in the following table. Worksheet errors can also be returned to VBA from a DLL using **Variants** of type **VT_ERROR**, and with the following values in the **ulVal** field.</span></span> 
  
|<span data-ttu-id="f8ce3-200">**エラー**</span><span class="sxs-lookup"><span data-stu-id="f8ce3-200">**Error**</span></span>|<span data-ttu-id="f8ce3-201">**バリアント型の ulVal 値**</span><span class="sxs-lookup"><span data-stu-id="f8ce3-201">**Variant ulVal value**</span></span>|<span data-ttu-id="f8ce3-202">**CVerr 引数**</span><span class="sxs-lookup"><span data-stu-id="f8ce3-202">**CVerr argument**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f8ce3-203">#NULL!</span><span class="sxs-lookup"><span data-stu-id="f8ce3-203">#NULL!</span></span>  <br/> |<span data-ttu-id="f8ce3-204">2148141008</span><span class="sxs-lookup"><span data-stu-id="f8ce3-204">2148141008</span></span>  <br/> |<span data-ttu-id="f8ce3-205">2000</span><span class="sxs-lookup"><span data-stu-id="f8ce3-205">Excel 2000</span></span>  <br/> |
|<span data-ttu-id="f8ce3-206">#DIV/0!</span><span class="sxs-lookup"><span data-stu-id="f8ce3-206">#DIV/0!</span></span>  <br/> |<span data-ttu-id="f8ce3-207">2148141015</span><span class="sxs-lookup"><span data-stu-id="f8ce3-207">2148141015</span></span>  <br/> |<span data-ttu-id="f8ce3-208">2007</span><span class="sxs-lookup"><span data-stu-id="f8ce3-208">Word 2007</span></span>  <br/> |
|<span data-ttu-id="f8ce3-209">#VALUE!</span><span class="sxs-lookup"><span data-stu-id="f8ce3-209">#VALUE!</span></span>  <br/> |<span data-ttu-id="f8ce3-210">2148141023</span><span class="sxs-lookup"><span data-stu-id="f8ce3-210">2148141023</span></span>  <br/> |<span data-ttu-id="f8ce3-211">2015</span><span class="sxs-lookup"><span data-stu-id="f8ce3-211">September 2015</span></span>  <br/> |
|<span data-ttu-id="f8ce3-212">#REF!</span><span class="sxs-lookup"><span data-stu-id="f8ce3-212">#REF!</span></span>  <br/> |<span data-ttu-id="f8ce3-213">2148141031</span><span class="sxs-lookup"><span data-stu-id="f8ce3-213">2148141031</span></span>  <br/> |<span data-ttu-id="f8ce3-214">2023</span><span class="sxs-lookup"><span data-stu-id="f8ce3-214">2023</span></span>  <br/> |
|<span data-ttu-id="f8ce3-215">#NAME?</span><span class="sxs-lookup"><span data-stu-id="f8ce3-215">#NAME?</span></span>  <br/> |<span data-ttu-id="f8ce3-216">2148141037</span><span class="sxs-lookup"><span data-stu-id="f8ce3-216">2148141037</span></span>  <br/> |<span data-ttu-id="f8ce3-217">2029</span><span class="sxs-lookup"><span data-stu-id="f8ce3-217">2029</span></span>  <br/> |
|<span data-ttu-id="f8ce3-218">#NUM!</span><span class="sxs-lookup"><span data-stu-id="f8ce3-218">#NUM!</span></span>  <br/> |<span data-ttu-id="f8ce3-219">2148141044</span><span class="sxs-lookup"><span data-stu-id="f8ce3-219">2148141044</span></span>  <br/> |<span data-ttu-id="f8ce3-220">2036</span><span class="sxs-lookup"><span data-stu-id="f8ce3-220">2036</span></span>  <br/> |
|<span data-ttu-id="f8ce3-221">#N/A</span><span class="sxs-lookup"><span data-stu-id="f8ce3-221">#N/A</span></span>  <br/> |<span data-ttu-id="f8ce3-222">2148141050</span><span class="sxs-lookup"><span data-stu-id="f8ce3-222">2148141050</span></span>  <br/> |<span data-ttu-id="f8ce3-223">2042</span><span class="sxs-lookup"><span data-stu-id="f8ce3-223">2042</span></span>  <br/> |
   
<span data-ttu-id="f8ce3-224">所定のバリアント型の **ulVal** 値は、**CVerr** 引数の値に 16 進数の x800A0000 を加えたものと同じになる点に注目してください。</span><span class="sxs-lookup"><span data-stu-id="f8ce3-224">Note that the Variant **ulVal** value given is equivalent to the **CVerr** argument value plus x800A0000 hexadecimal.</span></span> 
  
## <a name="calling-dll-functions-directly-from-the-worksheet"></a><span data-ttu-id="f8ce3-225">ワークシートから DLL 関数を直接呼び出す</span><span class="sxs-lookup"><span data-stu-id="f8ce3-225">Calling DLL Functions Directly from the Worksheet</span></span>

<span data-ttu-id="f8ce3-p118">たとえば、インターフェイスとして VBA または XLM を使用することなく、ワークシートから Win32 DLL の関数にアクセスすることはできません。また、その関数の引数と戻り値の型について事前に Excel に知らせておく必要もあります。これを行うプロセスは登録と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="f8ce3-p118">You cannot access Win32 DLL functions from the worksheet without, for example, using VBA or XLM as interfaces, or without letting Excel know about the function, its arguments, and its return type in advance. The process of doing this is called registration.</span></span>
  
<span data-ttu-id="f8ce3-228">次に示すような方法で、ワークシートから DLL の関数にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="f8ce3-228">The ways in which the functions of a DLL can be accessed in the worksheet are as follows:</span></span>
  
- <span data-ttu-id="f8ce3-229">前述したように VBA で関数を宣言して、その関数に VBA ユーザー定義関数でアクセスします。</span><span class="sxs-lookup"><span data-stu-id="f8ce3-229">Declare the function in VBA as described previously and access it via a VBA user-defined function.</span></span>
    
- <span data-ttu-id="f8ce3-230">XLM マクロ シートで CALL を使用することで DLL 関数を呼び出して、XLM ユーザー定義関数からアクセスします。</span><span class="sxs-lookup"><span data-stu-id="f8ce3-230">Call the DLL function using CALL on an XLM macro sheet, and access it via an XLM user-defined function.</span></span>
    
- <span data-ttu-id="f8ce3-231">XLM コマンドまたは VBA コマンドを使用して XLM の **REGISTER** 関数を呼び出します。これにより、関数がワークシート セルに入力されたときに、その関数を認識するために Excel が必要とする情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="f8ce3-231">Use an XLM or VBA command to call the XLM **REGISTER** function, which provides the information that Excel needs to recognize the function when it is entered into a worksheet cell.</span></span> 
    
- <span data-ttu-id="f8ce3-232">DLL を XLL に変換して、XLL を有効化するときに C API の **xlfRegister** 関数を使用して関数を登録します。</span><span class="sxs-lookup"><span data-stu-id="f8ce3-232">Turn the DLL into an XLL and register the function using the C API **xlfRegister** function when the XLL is activated.</span></span> 
    
<span data-ttu-id="f8ce3-p119">4 番目のアプローチは自己完結型であり、関数を登録するコードと関数のコードは、どちらも同じコード プロジェクトに含まれています。アドインに変更を加えても、XLM シートや VBA コード モジュールに変更を加える必要はありません。C API の機能を維持したまま適切に管理された方法でこれを行うには、DLL を XLL に変換して、その結果のアドインをアドイン マネージャーで読み込む必要があります。これにより、アドインが読み込まれると (または有効化されると)、DLL で公開してる関数を Excel から呼び出せるようになり、XLL に含まれるすべての関数を登録して、その他の DLL の初期化を実行できます。</span><span class="sxs-lookup"><span data-stu-id="f8ce3-p119">The fourth approach is self-contained: the code that registers the functions and the function code are both contained in the same code project. Making changes to the add-in does not involve making changes to an XLM sheet or to a VBA code module. To do this in a well-managed way while still staying within the capabilities of the C API, you must turn your DLL into an XLL and load the resulting add-in by using the Add-in Manager. This enables Excel to call a function that your DLL exposes when the add-in is loaded or activated, from which you can register all of the functions your XLL contains, and carry out any other DLL initialization.</span></span>
  
## <a name="calling-dll-commands-directly-from-excel"></a><span data-ttu-id="f8ce3-237">Excel から DLL コマンドを直接呼び出す</span><span class="sxs-lookup"><span data-stu-id="f8ce3-237">Calling DLL Commands Directly from Excel</span></span>

<span data-ttu-id="f8ce3-238">Win32 DLL コマンドは、VBA などのインターフェイスが存在しない場合や、事前にコマンドが登録されていない場合は、Excel のダイアログ ボックスやメニューから直接アクセスすることはできません。</span><span class="sxs-lookup"><span data-stu-id="f8ce3-238">Win32 DLL commands are not accessible directly from Excel dialog boxes and menus without there being an interface, such as VBA, or without the commands being registered in advance.</span></span>
  
<span data-ttu-id="f8ce3-239">次に示すような方法で DLL のコマンドにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="f8ce3-239">The ways in which you can access the commands of a DLL are as follows:</span></span>
  
- <span data-ttu-id="f8ce3-240">前述したように VBA でコマンドを宣言して、VBA マクロからアクセスします。</span><span class="sxs-lookup"><span data-stu-id="f8ce3-240">Declare the command in VBA as described previously and access it via a VBA macro.</span></span>
    
- <span data-ttu-id="f8ce3-241">XLM マクロ シートで **CALL** を使用することで DLL コマンドを呼び出して、XLM マクロからアクセスします。</span><span class="sxs-lookup"><span data-stu-id="f8ce3-241">Call the DLL command using **CALL** on an XLM macro sheet, and access it via an XLM macro.</span></span> 
    
- <span data-ttu-id="f8ce3-242">XLM コマンドまたは VBA コマンドを使用して XLM の **REGISTER** 関数を呼び出します。これにより、マクロ コマンドの名前を期待するダイアログ ボックスにコマンドが入力されたときに、そのコマンドを認識するために Excel が必要とする情報が提供されます。</span><span class="sxs-lookup"><span data-stu-id="f8ce3-242">Use an XLM or VBA command to call the XLM **REGISTER** function, which provides the information Excel needs to recognize the command when it is entered into a dialog box that expects the name of a macro command.</span></span> 
    
- <span data-ttu-id="f8ce3-243">DLL を XLL に変換して、C API の **xlfRegister** 関数を使用してコマンドを登録します。</span><span class="sxs-lookup"><span data-stu-id="f8ce3-243">Turn the DLL into an XLL and register the command using the C API **xlfRegister** function.</span></span> 
    
<span data-ttu-id="f8ce3-p120">DLL 関数に関して前述したように、4 番目のアプローチが最も自己完結的であり、登録のコードをコマンドのコードに近づけられます。これを行うには、DLL を XLL に変換し、その結果のアドインをアドイン マネージャーで読み込む必要があります。この方法でコマンドを登録すると、コマンドをユーザー インターフェイスの要素に加えることもできます (カスタム メニューなど)。また、特定のキーボード操作などのイベントでコマンドを呼び出すイベント トラップを設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="f8ce3-p120">As discussed earlier in the context of DLL functions, the fourth approach is the most self-contained, keeping the registration code close to the command code. To do this, you must turn your DLL into an XLL and load the resulting add-in using the Add-in Manager. Registering commands in this way also lets you attach the command to an element of the user interface, such as a custom menu, or to set up an event trap that calls the command on a given keystroke or other event.</span></span>
  
<span data-ttu-id="f8ce3-247">Exce に登録されたすべての XLL コマンドについて、Excel では、次の形式になっていると見なされます。</span><span class="sxs-lookup"><span data-stu-id="f8ce3-247">All XLL commands that are registered with Excel are assumed by Excel to be of the following form.</span></span>
  
```cpp
int WINAPI my_xll_cmd(void)
{
// Function code...
    return 1;
}
```

> [!NOTE]
> <span data-ttu-id="f8ce3-p121">Excel は戻り値を無視します。ただし、XLM マクロ シートから呼び出されたものを除きます (この場合、戻り値は **TRUE** または **FALSE** に変換されます)。そのため、コマンドが正常に実行された場合は 1 を返す必要があります。また、コマンドが失敗したり、ユーザーによって取り消されたりした場合は 0 を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="f8ce3-p121">Excel ignores the return value unless it is called from an XLM macro sheet, in which case the return value is converted to **TRUE** or **FALSE**. You should therefore return 1 if your command executed successfully, and 0 if it failed or was canceled by the user.</span></span> 
  
## <a name="dll-memory-and-multiple-dll-instances"></a><span data-ttu-id="f8ce3-250">DLL のメモリと複数の DLL インスタンス</span><span class="sxs-lookup"><span data-stu-id="f8ce3-250">DLL Memory and Multiple DLL Instances</span></span>

<span data-ttu-id="f8ce3-p122">アプリケーションが DLL を読み込むと、DLL の実行可能コードがグローバル ヒープに読み込まれ、実行できるようになり、データ構造のグローバル ヒープに領域が割り当てられます。Windows では、メモリ マッピングを使用して、これらのメモリ領域がアプリケーションのプロセス内にあるように表示し、アプリケーションがそこにアクセスできるようにします。</span><span class="sxs-lookup"><span data-stu-id="f8ce3-p122">When an application loads a DLL, the DLL's executable code is loaded into the global heap so that it can be run, and space is allocated on the global heap for its data structures. Windows uses memory mapping to make these areas of memory appear as if they are in the application's process so that the application can access them.</span></span>
  
<span data-ttu-id="f8ce3-p123">その後、2 番目のアプリケーションが DLL を読み込んでも、Windows は DLL の実行可能コードのコピーを別に作成することはありません (そのメモリは読み取り専用になっているため)。Windows は、DLL の実行可能コードのメモリを両方のアプリケーションのプロセスにマッピングします。ただし、DLL のデータ構造のプライベート コピー用に 2 番目の領域を割り当て、このコピーを 2 番目のプロセスにのみマッピングします。これにより、どちらのアプリケーションも相互の DLL データに干渉しないようにします。</span><span class="sxs-lookup"><span data-stu-id="f8ce3-p123">If a second application then loads the DLL, Windows does not make another copy of the DLL executable code, as that memory is read-only. Windows maps the DLL executable code memory to the processes of both applications. It does, however, allocate a second space for a private copy of the DLL's data structures and maps this copy to the second process only. This ensures that neither application can interfere with the DLL data of the other.</span></span>
  
<span data-ttu-id="f8ce3-p124">そのため、DLL 開発者は、静的変数やグローバル変数、データ構造体が複数のアプリケーションからアクセスされたり、同じアプリケーションの複数のインスタンスからアクセスされたりすることについて心配する必要がなくなります。すべてのアプリケーションの全インスタンスは、DLL のデータの独自のコピーを取得します。</span><span class="sxs-lookup"><span data-stu-id="f8ce3-p124">This means that DLL developers do not have to be concerned about static and global variables and data structures being accessed by more than one application, or more than one instance of the same application. Every instance of every application gets its own copy of the DLL's data.</span></span>
  
<span data-ttu-id="f8ce3-p125">DLL 開発者は、アプリケーションの同じインスタンスが、そのインスタンス専用の DLL を別のスレッドから何回も呼び出すことについて配慮する必要があります。この場合は、そのインスタンスのデータに競合が発生する可能性があります。詳細については、「[Excel のメモリ管理](memory-management-in-excel.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8ce3-p125">DLL developers do need to be concerned about the same instance of an application calling their DLL many times from different threads, because this can result in contention for that instance's data. For more information, see [Memory Management in Excel](memory-management-in-excel.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f8ce3-261">関連項目</span><span class="sxs-lookup"><span data-stu-id="f8ce3-261">See also</span></span>

- [<span data-ttu-id="f8ce3-262">DLL の開発</span><span class="sxs-lookup"><span data-stu-id="f8ce3-262">Developing DLLs</span></span>](developing-dlls.md) 
- [<span data-ttu-id="f8ce3-263">DLL または XLL から Excel に呼び出す</span><span class="sxs-lookup"><span data-stu-id="f8ce3-263">Calling into Excel from the DLL or XLL</span></span>](calling-into-excel-from-the-dll-or-xll.md)

