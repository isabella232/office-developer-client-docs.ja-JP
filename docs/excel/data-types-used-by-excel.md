---
title: Excel で使用されるデータ型
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
keywords:
- 登録データ型 [excel 2007],Excel データ型,文字 [Excel 2007],数字 [Excel 2007],データ構造 [Excel 2007],データ型 [Excel 2007]
ms.assetid: 8740a8fb-ad67-4232-a49b-d78967a786c2
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: c546fc80b212301689744d3279a59733d9cc5524
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710609"
---
# <a name="data-types-used-by-excel"></a><span data-ttu-id="96984-104">Excel で使用されるデータ型</span><span class="sxs-lookup"><span data-stu-id="96984-104">Data types used by Excel</span></span>

<span data-ttu-id="96984-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="96984-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="96984-106">Mirosoft Excel は ANSI C/C++ 型と Excel 固有のデータ構造を交換します。</span><span class="sxs-lookup"><span data-stu-id="96984-106">Microsoft Excel exchanges several ANSI C/C++ types and also some Excel-specific data structures.</span></span> <span data-ttu-id="96984-107">ここでこれらを説明するのは、他のセクションのコンテキスト提供のためです。詳細については、「[xlfRegister (形式 1)](xlfregister-form-1.md)」のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="96984-107">These are mentioned here to provide a context for other sections, and they are discussed in detail in the [xlfRegister (Form 1)](xlfregister-form-1.md) topic.</span></span> 
  
## <a name="ansi-cc-types"></a><span data-ttu-id="96984-108">ANSI C /C++ 形式</span><span class="sxs-lookup"><span data-stu-id="96984-108">ANSI C/C++ types</span></span>

### <a name="numbers"></a><span data-ttu-id="96984-109">数値</span><span class="sxs-lookup"><span data-stu-id="96984-109">Numbers</span></span>

<span data-ttu-id="96984-110">すべてのバージョンの Excel：</span><span class="sxs-lookup"><span data-stu-id="96984-110">All versions of Excel:</span></span>
  
- <span data-ttu-id="96984-111">8 バイト倍精度浮動小数点型</span><span class="sxs-lookup"><span data-stu-id="96984-111">8-byte double</span></span>
    
- <span data-ttu-id="96984-112">[signed] short [int] &ndash; **Boolean** の値および整数に用いられます</span><span class="sxs-lookup"><span data-stu-id="96984-112">[signed] short [int] &ndash; used for **Boolean** values and also integers</span></span> 
    
- <span data-ttu-id="96984-113">unsigned short [int]</span><span class="sxs-lookup"><span data-stu-id="96984-113">unsigned short [int]</span></span>
    
- <span data-ttu-id="96984-114">[signed long] int</span><span class="sxs-lookup"><span data-stu-id="96984-114">[signed long] int</span></span>
    
### <a name="strings"></a><span data-ttu-id="96984-115">文字列</span><span class="sxs-lookup"><span data-stu-id="96984-115">Strings</span></span>

<span data-ttu-id="96984-116">すべてのバージョンの Excel：</span><span class="sxs-lookup"><span data-stu-id="96984-116">All versions of Excel:</span></span>
  
- <span data-ttu-id="96984-117">[signed] char \* &ndash;: 最大 255 文字のヌル終端文字列</span><span class="sxs-lookup"><span data-stu-id="96984-117">[signed] char \* &ndash; null-terminated byte strings of up to 255 characters</span></span>
    
- <span data-ttu-id="96984-118">unsigned char \* &ndash; 最大 255 文字の length-counted バイト文字列</span><span class="sxs-lookup"><span data-stu-id="96984-118">unsigned char \* &ndash; length-counted byte strings of up to 255 characters</span></span>
    
<span data-ttu-id="96984-119">Excel 2007 以降:</span><span class="sxs-lookup"><span data-stu-id="96984-119">Starting in Excel 2007:</span></span>
  
- <span data-ttu-id="96984-120">unsigned short \* &ndash; 最大 32,767 文字の Unicode 文字列で、ヌル終端文字列または length-counted 文字列のいずれかの形式</span><span class="sxs-lookup"><span data-stu-id="96984-120">unsigned short \* &ndash; Unicode strings of up to 32,767 characters, which can be null-terminated or length-counted</span></span>
    
<span data-ttu-id="96984-121">Excel のワークシート番号はすべて倍精度小数点として格納されているため、Excel でアドイン関数をこれに代わる整数型として宣言する必要はありません (むしろそうするなら小さな変換オーバーヘッドが発生します) 。</span><span class="sxs-lookup"><span data-stu-id="96984-121">All worksheet numbers in Excel are stored as doubles so that it is not necessary (and in fact introduces a small conversion overhead) to declare add-in functions as exchanging integer types with Excel.</span></span>
  
<span data-ttu-id="96984-p102">整数型を使用している場合、Excel は入力が型の範囲内に入っていることを確認します。範囲外の場合は **#NUM!** で失敗します。例外は、関数を登録して、short int で実装される **Boolean** 引数を取る場合です。この場合、0 以外の入力はすべて 1 に変換され、0 は直接渡されます。</span><span class="sxs-lookup"><span data-stu-id="96984-p102">Where you are using integer types, Excel verifies that the inputs are within the limits of the type, and they fail with **#NUM!** if outside these. The exception is when you are registering a function to take a **Boolean** argument, implemented using short int. In this case, any non-zero input is converted to 1, and zero is passed straight through.</span></span> 
  
## <a name="excel-specific-data-structures"></a><span data-ttu-id="96984-125">Excel 固有のデータ構造</span><span class="sxs-lookup"><span data-stu-id="96984-125">Excel-specific data structures</span></span>

<span data-ttu-id="96984-126">すべてのバージョンの Excel：</span><span class="sxs-lookup"><span data-stu-id="96984-126">All versions of Excel:</span></span>
  
- <span data-ttu-id="96984-127">**FP**&ndash; 2 次元の浮動小数点型配列構造で、行数は最大 65,356 行、列数は Excel のバージョンでサポートされる最大数をサポートします。</span><span class="sxs-lookup"><span data-stu-id="96984-127">**FP** &ndash; a two-dimensional floating-point array structure supporting up to 65,356 rows by the maximum number columns supported in the given version of Excel.</span></span> 
    
- <span data-ttu-id="96984-128">**XLOPER**&ndash; 複数の型のデータ構造で、ワークシートのデータ型 (エラーを含む)、整数、範囲の参照、XLM マクロ シート フロー コントロールの型、および内部バイナリ ストレージ データの型をすべて表します。 </span><span class="sxs-lookup"><span data-stu-id="96984-128">**XLOPER** &ndash; a multi-type data structure that can represent all the worksheet data types (including errors), integers, range references, XLM macro sheet flow control types, and an internal binary storage data type.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="96984-129">文字列は最大 255 文字の length-counted 文字列で表されます。</span><span class="sxs-lookup"><span data-stu-id="96984-129">Strings are represented as length-counted byte strings of up to 255 characters length.</span></span> 
  
<span data-ttu-id="96984-130">Excel 2007 以降:</span><span class="sxs-lookup"><span data-stu-id="96984-130">Starting in Excel 2007:</span></span>
  
- <span data-ttu-id="96984-131">**FP12** &ndash; 2 次元の浮動小数点型配列構造で、Excel 2007 以降のすべての行および列をサポートします。</span><span class="sxs-lookup"><span data-stu-id="96984-131">**FP12** &ndash; a two-dimensional floating-point array structure supporting all the rows and columns starting in Excel 2007.</span></span> 
    
- <span data-ttu-id="96984-132">**XLOPER12**&ndash; 複数の型のデータ構造で、ワークシートのデータ型 (エラーを含む)、整数、範囲の参照、XLM マクロ シート フロー コントロールの型、および内部バイナリ ストレージ データの型をすべて表します。</span><span class="sxs-lookup"><span data-stu-id="96984-132">**XLOPER12** &ndash; a multi-type data structure that can represent all the worksheet data types (including errors), integers, range references, XLM macro sheet flow control types, and an internal binary storage data type.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="96984-133">文字列は、最大 32,767 文字の length-counted Unicode 文字列で表されます。</span><span class="sxs-lookup"><span data-stu-id="96984-133">Strings are represented as length-counted Unicode strings of up to 32,767 characters long.</span></span> 
  
## <a name="registration-data-type-codes"></a><span data-ttu-id="96984-134">登録データ型コード</span><span class="sxs-lookup"><span data-stu-id="96984-134">Registration data type codes</span></span>

<span data-ttu-id="96984-135">XLL 関数は、C API 関数 **xlfRegister** を使用して登録されます。この関数は戻り値および引数の型をエンコードする文字列を 3 番目の引数として取ります。</span><span class="sxs-lookup"><span data-stu-id="96984-135">XLL functions are registered using the C API function **xlfRegister**, which takes as its third argument a string of letters that encode the return and argument types.</span></span> <span data-ttu-id="96984-136">この文字列には、関数が揮発性関数か、スレッド セーフか (Excel 2007 以降)、マクロ シートの同等関数か、また、引数をインプレース変更して結果を返すかどうかということを Excel に指示する情報も含まれています。</span><span class="sxs-lookup"><span data-stu-id="96984-136">This string also contains the information that tells Excel whether the function is volatile, is thread-safe (starting in Excel 2007), is macro sheet equivalent, and whether it returns its result by modifying an argument in place.</span></span>
  
<span data-ttu-id="96984-137">次の表は、「[xlfRegister (形式 1)](xlfregister-form-1.md)」のトピックで再度取り上げて、詳しく説明します。</span><span class="sxs-lookup"><span data-stu-id="96984-137">The following table is reproduced and discussed in more detail in the [xlfRegister (Form 1)](xlfregister-form-1.md) topic.</span></span> <span data-ttu-id="96984-138">ここでは、本セクションの残りのコンテキストを提供する目的で掲載しています。</span><span class="sxs-lookup"><span data-stu-id="96984-138">It is reproduced here in order to provide a context for the rest of this section.</span></span> <span data-ttu-id="96984-139">たとえば、length-counted Unicode 文字列 (Excel 2007 以降) を取る関数は、C% 引数型を取る関数と表現できます。</span><span class="sxs-lookup"><span data-stu-id="96984-139">For example, a function that takes a length-counted Unicode string (starting in Excel 2007) could be described as taking a type C% argument.</span></span> 
  
|<span data-ttu-id="96984-140">データ型</span><span class="sxs-lookup"><span data-stu-id="96984-140">Data type</span></span>|<span data-ttu-id="96984-141">値渡し</span><span class="sxs-lookup"><span data-stu-id="96984-141">Pass by value</span></span>|<span data-ttu-id="96984-142">参照渡し (ポインター)</span><span class="sxs-lookup"><span data-stu-id="96984-142">Pass by ref (pointer)</span></span>|<span data-ttu-id="96984-143">コメント</span><span class="sxs-lookup"><span data-stu-id="96984-143">Comments</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="96984-144">ブール型 (Boolean)。</span><span class="sxs-lookup"><span data-stu-id="96984-144">Boolean</span></span>  <br/> |<span data-ttu-id="96984-145">A</span><span class="sxs-lookup"><span data-stu-id="96984-145">A</span></span>  <br/> |<span data-ttu-id="96984-146">L</span><span class="sxs-lookup"><span data-stu-id="96984-146">L</span></span>  <br/> |<span data-ttu-id="96984-147">short (0 = false または 1 = true)</span><span class="sxs-lookup"><span data-stu-id="96984-147">short (0=false or 1=true)</span></span>  <br/> |
|<span data-ttu-id="96984-148">double</span><span class="sxs-lookup"><span data-stu-id="96984-148">double</span></span>  <br/> |<span data-ttu-id="96984-149">B</span><span class="sxs-lookup"><span data-stu-id="96984-149">B</span></span>  <br/> |<span data-ttu-id="96984-150">E</span><span class="sxs-lookup"><span data-stu-id="96984-150">E</span></span>  <br/> ||
|<span data-ttu-id="96984-151">char \*</span><span class="sxs-lookup"><span data-stu-id="96984-151">char \*</span></span>  <br/> ||<span data-ttu-id="96984-152">C、F</span><span class="sxs-lookup"><span data-stu-id="96984-152">C, F</span></span>  <br/> |<span data-ttu-id="96984-153">Null で終了する ASCII バイト文字列</span><span class="sxs-lookup"><span data-stu-id="96984-153">Null-terminated ASCII byte string</span></span>  <br/> |
|<span data-ttu-id="96984-154">unsigned char \*</span><span class="sxs-lookup"><span data-stu-id="96984-154">unsigned char \*</span></span>  <br/> ||<span data-ttu-id="96984-155">D、G</span><span class="sxs-lookup"><span data-stu-id="96984-155">D, G</span></span>  <br/> |<span data-ttu-id="96984-156">Length-counted ASCII バイト文字列</span><span class="sxs-lookup"><span data-stu-id="96984-156">Length -counted ASCII byte string</span></span>  <br/> |
|<span data-ttu-id="96984-157">unsigned short \*  (Excel 2007 以降)</span><span class="sxs-lookup"><span data-stu-id="96984-157">unsigned short \*  (starting in Excel 2007)</span></span>  <br/> ||<span data-ttu-id="96984-158">C%、F%</span><span class="sxs-lookup"><span data-stu-id="96984-158">C%, F%</span></span>  <br/> |<span data-ttu-id="96984-159">ヌル終端 Unicode ワイド文字文字列</span><span class="sxs-lookup"><span data-stu-id="96984-159">Null-terminated Unicode wide character string</span></span>  <br/> |
|<span data-ttu-id="96984-160">unsigned short \*  (Excel 2007 以降)</span><span class="sxs-lookup"><span data-stu-id="96984-160">unsigned short \*  (starting in Excel 2007)</span></span>  <br/> ||<span data-ttu-id="96984-161">D%、G%</span><span class="sxs-lookup"><span data-stu-id="96984-161">D%, G%</span></span>  <br/> |<span data-ttu-id="96984-162">Length-counted Unicode ワイド文字文字列</span><span class="sxs-lookup"><span data-stu-id="96984-162">Length-counted Unicode wide character string</span></span>  <br/> |
|<span data-ttu-id="96984-163">unsigned short [int]</span><span class="sxs-lookup"><span data-stu-id="96984-163">unsigned short [int]</span></span>  <br/> |<span data-ttu-id="96984-164">H</span><span class="sxs-lookup"><span data-stu-id="96984-164">H</span></span>  <br/> ||<span data-ttu-id="96984-165">WORD</span><span class="sxs-lookup"><span data-stu-id="96984-165">WORD</span></span>  <br/> |
|<span data-ttu-id="96984-166">[signed] short [int]</span><span class="sxs-lookup"><span data-stu-id="96984-166">[signed] short [int]</span></span>  <br/> |<span data-ttu-id="96984-167">I</span><span class="sxs-lookup"><span data-stu-id="96984-167">I</span></span>  <br/> |<span data-ttu-id="96984-168">M</span><span class="sxs-lookup"><span data-stu-id="96984-168">M</span></span>  <br/> |<span data-ttu-id="96984-169">16 ビット</span><span class="sxs-lookup"><span data-stu-id="96984-169">16-bit</span></span>  <br/> |
|<span data-ttu-id="96984-170">[signed long] int</span><span class="sxs-lookup"><span data-stu-id="96984-170">[signed long] int</span></span>  <br/> |<span data-ttu-id="96984-171">J</span><span class="sxs-lookup"><span data-stu-id="96984-171">J</span></span>  <br/> |<span data-ttu-id="96984-172">N</span><span class="sxs-lookup"><span data-stu-id="96984-172">N</span></span>  <br/> |<span data-ttu-id="96984-173">32 ビット</span><span class="sxs-lookup"><span data-stu-id="96984-173">32-bit</span></span>  <br/> |
|<span data-ttu-id="96984-174">配列</span><span class="sxs-lookup"><span data-stu-id="96984-174">Array</span></span>  <br/> ||<span data-ttu-id="96984-175">O</span><span class="sxs-lookup"><span data-stu-id="96984-175">O</span></span>  <br/> | <span data-ttu-id="96984-176">参照により以下の 3 つの引数として渡されます。</span><span class="sxs-lookup"><span data-stu-id="96984-176">Passed as three arguments by reference:</span></span>  <br/><span data-ttu-id="96984-177">1. short int \*rows</span><span class="sxs-lookup"><span data-stu-id="96984-177">1. short int \*rows</span></span>  <br/><span data-ttu-id="96984-178">2. short int \*columns</span><span class="sxs-lookup"><span data-stu-id="96984-178">2. short int \*columns</span></span>  <br/><span data-ttu-id="96984-179">3. double \*array</span><span class="sxs-lookup"><span data-stu-id="96984-179">3. double \*array</span></span>  <br/> |
|<span data-ttu-id="96984-180">配列</span><span class="sxs-lookup"><span data-stu-id="96984-180">Array</span></span>  <br/> <span data-ttu-id="96984-181">(Excel 2007 以降)</span><span class="sxs-lookup"><span data-stu-id="96984-181">(starting in Excel 2007)</span></span>  <br/> ||<span data-ttu-id="96984-182">O%</span><span class="sxs-lookup"><span data-stu-id="96984-182">O%</span></span>  <br/> | <span data-ttu-id="96984-183">参照により以下の 3 つの引数として渡されます。</span><span class="sxs-lookup"><span data-stu-id="96984-183">Passed as three arguments by reference:</span></span>  <br/><span data-ttu-id="96984-184">1. int \*rows</span><span class="sxs-lookup"><span data-stu-id="96984-184">1. int \*rows</span></span>  <br/><span data-ttu-id="96984-185">2. int \*columns</span><span class="sxs-lookup"><span data-stu-id="96984-185">2. int \*columns</span></span>  <br/><span data-ttu-id="96984-186">3. double \*array</span><span class="sxs-lookup"><span data-stu-id="96984-186">3. double \*array</span></span>  <br/> |
|<span data-ttu-id="96984-187">FP</span><span class="sxs-lookup"><span data-stu-id="96984-187">FP</span></span>  <br/> ||<span data-ttu-id="96984-188">K</span><span class="sxs-lookup"><span data-stu-id="96984-188">K</span></span>  <br/> |<span data-ttu-id="96984-189">浮動小数点配列構造</span><span class="sxs-lookup"><span data-stu-id="96984-189">Floating-point array structure</span></span>  <br/> |
|<span data-ttu-id="96984-190">FP12</span><span class="sxs-lookup"><span data-stu-id="96984-190">FP12</span></span>  <br/> <span data-ttu-id="96984-191">(Excel 2007 以降)</span><span class="sxs-lookup"><span data-stu-id="96984-191">(starting in Excel 2007)</span></span>  <br/> ||<span data-ttu-id="96984-192">K%</span><span class="sxs-lookup"><span data-stu-id="96984-192">K%</span></span>  <br/> |<span data-ttu-id="96984-193">大グリッド浮動小数点配列構造</span><span class="sxs-lookup"><span data-stu-id="96984-193">Large grid floating-point array structure</span></span>  <br/> |
|<span data-ttu-id="96984-194">XLOPER</span><span class="sxs-lookup"><span data-stu-id="96984-194">XLOPER</span></span>  <br/> ||<span data-ttu-id="96984-195">P</span><span class="sxs-lookup"><span data-stu-id="96984-195">P</span></span>  <br/> |<span data-ttu-id="96984-196">可変型のワークシートの値および配列</span><span class="sxs-lookup"><span data-stu-id="96984-196">Variable-type worksheet values and arrays</span></span>  <br/> |
|||<span data-ttu-id="96984-197">R</span><span class="sxs-lookup"><span data-stu-id="96984-197">R</span></span>  <br/> |<span data-ttu-id="96984-198">値、配列、および範囲の参照</span><span class="sxs-lookup"><span data-stu-id="96984-198">Values, arrays, and range references</span></span>  <br/> |
|<span data-ttu-id="96984-199">XLOPER12</span><span class="sxs-lookup"><span data-stu-id="96984-199">XLOPER12</span></span>  <br/> <span data-ttu-id="96984-200">(Excel 2007 以降)</span><span class="sxs-lookup"><span data-stu-id="96984-200">(starting in Excel 2007)</span></span>  <br/> ||<span data-ttu-id="96984-201">Q</span><span class="sxs-lookup"><span data-stu-id="96984-201">Q</span></span>  <br/> |<span data-ttu-id="96984-202">可変型のワークシートの値および配列</span><span class="sxs-lookup"><span data-stu-id="96984-202">Variable-type worksheet values and arrays</span></span>  <br/> |
|||<span data-ttu-id="96984-203">U</span><span class="sxs-lookup"><span data-stu-id="96984-203">U</span></span>  <br/> |<span data-ttu-id="96984-204">値、配列、および範囲の参照</span><span class="sxs-lookup"><span data-stu-id="96984-204">Values, arrays, and range references</span></span>  <br/> |
   
<span data-ttu-id="96984-205">**C%**、**F%**、**D%**、**G%**、**K%**、**O%**、**Q**、および **U** は Microsoft Office Excel 2007 から登場する新しい型のため、それ以前のバージョンではサポートされません。</span><span class="sxs-lookup"><span data-stu-id="96984-205">The types **C%**, **F%**, **D%**, **G%**, **K%**, **O%**, **Q**, and **U** were all new in Microsoft Office Excel 2007 and are not supported in earlier versions.</span></span> <span data-ttu-id="96984-206">文字列型 **F**、**F%**、**G**、および **G%** は、インプレース変更される引数に使用します。</span><span class="sxs-lookup"><span data-stu-id="96984-206">The string types **F**, **F%**, **G**, and **G%** are used for arguments that are modified-in-place.</span></span> <span data-ttu-id="96984-207">引数 **XLOPER** または **XLOPER12** の引数は、それぞれ **P** または **Q** の型として登録されている場合、Excel は準備段階で単一セル参照を単純数値に、複数セル参照を配列に変換します。</span><span class="sxs-lookup"><span data-stu-id="96984-207">When **XLOPER** or **XLOPER12** arguments are registered as types **P** or **Q** respectively, Excel converts single-cell references to simple values and multi-cell references to arrays when it prepares them.</span></span> 
  
<span data-ttu-id="96984-208">**P** および **Q** の型は常に逆参照されるため、**xltypeRef** または **xltypeSRef** ではなく、必ず **xltypeNum**、**xltypeStr**、**xltypeBool**、**xltypeErr**、**xltypeMulti**、**xltypeMissing** または **xltypeNil** のいずれかとして入力されます。</span><span class="sxs-lookup"><span data-stu-id="96984-208">**P** and **Q** types always arrive in your function as one of the following types: **xltypeNum**, **xltypeStr**, **xltypeBool**, **xltypeErr**, **xltypeMulti**, **xltypeMissing**, or **xltypeNil**, but not **xltypeRef** or **xltypeSRef** because these are always dereferenced.</span></span> 
  
<span data-ttu-id="96984-209">**O** の型は、スタックの 3 つの引数であり、引数が参照によって渡される Fortran Dll との互換性を確保するために導入されました。</span><span class="sxs-lookup"><span data-stu-id="96984-209">Type **O**, which is really three arguments on the stack, was introduced for compatibility with Fortran DLLs where arguments are passed by reference.</span></span> <span data-ttu-id="96984-210">インプレース変更の戻り値として引数を宣言し、結果を参照値に配置する場合以外では、値を返す目的で使用できません。</span><span class="sxs-lookup"><span data-stu-id="96984-210">It cannot be used to return a value except by declaring the argument as a modify-in-place return value and placing the results in the referenced values.</span></span> <span data-ttu-id="96984-211">**O%** の型は、Excel 2007 の **O** の型を拡張したもので、Office Excel 2003 グリッドよりも広い領域をカバーしている配列にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="96984-211">Type **O%** extends type **O** in Excel 2007 so that it can access arrays that cover areas larger than the Office Excel 2003 grid.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="96984-212">関連項目</span><span class="sxs-lookup"><span data-stu-id="96984-212">See also</span></span>

- [<span data-ttu-id="96984-213">xlfRegister (形式 1)</span><span class="sxs-lookup"><span data-stu-id="96984-213">xlfRegister (Form 1)</span></span>](xlfregister-form-1.md)
- [<span data-ttu-id="96984-214">Excel プログラミングの概念</span><span class="sxs-lookup"><span data-stu-id="96984-214">Excel Programming Concepts</span></span>](excel-programming-concepts.md)
- [<span data-ttu-id="96984-215">Excel XLL SDK API 関数リファレンス</span><span class="sxs-lookup"><span data-stu-id="96984-215">Excel XLL SDK API Function Reference</span></span>](excel-xll-sdk-api-function-reference.md)

