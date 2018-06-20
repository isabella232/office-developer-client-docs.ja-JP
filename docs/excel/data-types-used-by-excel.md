---
title: Excel で使用されるデータ型
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
keywords:
- 登録データ タイプが [excel 2007]、Excel のデータ型、文字列 [Excel 2007]、[Excel 2007] の数値、データ構造 [Excel 2007]、[Excel 2007] のデータ型
localization_priority: Normal
ms.assetid: 8740a8fb-ad67-4232-a49b-d78967a786c2
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: b32a9beb2f77c12e6b6f2c445672c717a2546386
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798779"
---
# <a name="data-types-used-by-excel"></a><span data-ttu-id="ab2f6-104">Excel で使用されるデータ型</span><span class="sxs-lookup"><span data-stu-id="ab2f6-104">Data types used by Excel</span></span>

<span data-ttu-id="ab2f6-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="ab2f6-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="ab2f6-106">Microsoft Excel では、いくつかの ANSI C および C++ の型ともいくつか Excel に固有のデータ構造体を交換します。</span><span class="sxs-lookup"><span data-stu-id="ab2f6-106">Microsoft Excel exchanges several ANSI C/C++ types and also some Excel-specific data structures.</span></span> <span data-ttu-id="ab2f6-107">他のセクションでは、コンテキストを提供するここではこれらとは、 [xlfRegister (フォーム 1)](xlfregister-form-1.md)のトピックで詳しく説明します。</span><span class="sxs-lookup"><span data-stu-id="ab2f6-107">These are mentioned here to provide a context for other sections, and they are discussed in detail in the [xlfRegister (Form 1)](xlfregister-form-1.md) topic.</span></span> 
  
## <a name="ansi-cc-types"></a><span data-ttu-id="ab2f6-108">ANSI C と C++ の型</span><span class="sxs-lookup"><span data-stu-id="ab2f6-108">ANSI C/C++ types</span></span>

### <a name="numbers"></a><span data-ttu-id="ab2f6-109">数字</span><span class="sxs-lookup"><span data-stu-id="ab2f6-109">Numbers</span></span>

<span data-ttu-id="ab2f6-110">すべてのバージョンの Excel：</span><span class="sxs-lookup"><span data-stu-id="ab2f6-110">All versions of Excel:</span></span>
  
- <span data-ttu-id="ab2f6-111">8 バイト倍精度浮動小数点型</span><span class="sxs-lookup"><span data-stu-id="ab2f6-111">8-byte double</span></span>
    
- <span data-ttu-id="ab2f6-112">[int] の [署名] 短い&ndash;の整数および**ブール**値の使用</span><span class="sxs-lookup"><span data-stu-id="ab2f6-112">[signed] short [int] &ndash; used for **Boolean** values and also integers</span></span> 
    
- <span data-ttu-id="ab2f6-113">unsigned short [int]</span><span class="sxs-lookup"><span data-stu-id="ab2f6-113">unsigned short [int]</span></span>
    
- <span data-ttu-id="ab2f6-114">[signed long] int</span><span class="sxs-lookup"><span data-stu-id="ab2f6-114">[signed long] int</span></span>
    
### <a name="strings"></a><span data-ttu-id="ab2f6-115">文字列</span><span class="sxs-lookup"><span data-stu-id="ab2f6-115">Strings</span></span>

<span data-ttu-id="ab2f6-116">すべてのバージョンの Excel：</span><span class="sxs-lookup"><span data-stu-id="ab2f6-116">All versions of Excel:</span></span>
  
- <span data-ttu-id="ab2f6-117">[署名] char \* &ndash;を 255 文字以内の文字列を null で終わるバイト</span><span class="sxs-lookup"><span data-stu-id="ab2f6-117">[signed] char \* &ndash; null-terminated byte strings of up to 255 characters</span></span>
    
- <span data-ttu-id="ab2f6-118">char 型の符号なし\*&ndash;を 255 文字以内の文字列をバイトの長さのカウント</span><span class="sxs-lookup"><span data-stu-id="ab2f6-118">unsigned char \* &ndash; length-counted byte strings of up to 255 characters</span></span>
    
<span data-ttu-id="ab2f6-119">Excel 2007 で開始します。</span><span class="sxs-lookup"><span data-stu-id="ab2f6-119">Starting in Excel 2007:</span></span>
  
- <span data-ttu-id="ab2f6-120">符号なしの短い\* &ndash; 、null で終わるか、長さのカウントは、最大 32,767 文字の Unicode 文字列</span><span class="sxs-lookup"><span data-stu-id="ab2f6-120">unsigned short \* &ndash; Unicode strings of up to 32,767 characters, which can be null-terminated or length-counted</span></span>
    
<span data-ttu-id="ab2f6-121">Excel のワークシート番号はすべて倍精度小数点として格納されているため、Excel でアドイン関数をこれに代わる整数型として宣言する必要はありません (むしろそうするなら小さな変換オーバーヘッドが発生します) 。</span><span class="sxs-lookup"><span data-stu-id="ab2f6-121">All worksheet numbers in Excel are stored as doubles so that it is not necessary (and in fact introduces a small conversion overhead) to declare add-in functions as exchanging integer types with Excel.</span></span>
  
<span data-ttu-id="ab2f6-122">整数型を使用している場合 Excel ことを確認、型の範囲内では、入力に失敗した **#NUM!**</span><span class="sxs-lookup"><span data-stu-id="ab2f6-122">Where you are using integer types, Excel verifies that the inputs are within the limits of the type, and they fail with **#NUM!**</span></span> <span data-ttu-id="ab2f6-123">これら以外の場合。</span><span class="sxs-lookup"><span data-stu-id="ab2f6-123">if outside these.</span></span> <span data-ttu-id="ab2f6-124">短い整数を使用して実装、**ブール型**の引数を使用する関数を登録する場合は例外です。この例では、0 以外の任意の入力が 1 に変換し、0 を渡すとストレート。</span><span class="sxs-lookup"><span data-stu-id="ab2f6-124">The exception is when you are registering a function to take a **Boolean** argument, implemented using short int. In this case, any non-zero input is converted to 1, and zero is passed straight through.</span></span> 
  
## <a name="excel-specific-data-structures"></a><span data-ttu-id="ab2f6-125">Excel に固有のデータ構造体</span><span class="sxs-lookup"><span data-stu-id="ab2f6-125">Excel-specific data structures</span></span>

<span data-ttu-id="ab2f6-126">すべてのバージョンの Excel：</span><span class="sxs-lookup"><span data-stu-id="ab2f6-126">All versions of Excel:</span></span>
  
- <span data-ttu-id="ab2f6-127">**FP**&ndash;浮動小数点数の 2 次元の配列構造体の特定のバージョンの Excel でサポートされている最大の番号の列で最大 65,356 の行をサポートします。</span><span class="sxs-lookup"><span data-stu-id="ab2f6-127">**FP** &ndash; a two-dimensional floating-point array structure supporting up to 65,356 rows by the maximum number columns supported in the given version of Excel.</span></span> 
    
- <span data-ttu-id="ab2f6-128">**XLOPER**&ndash; (エラーを含む) すべてのワークシートのデータ型、整数、範囲の参照、XLM マクロ シート フロー コントロールの種類、および内部バイナリ ストレージのデータ型を表すことができます複数の種類のデータ構造体です。</span><span class="sxs-lookup"><span data-stu-id="ab2f6-128">**XLOPER** &ndash; a multi-type data structure that can represent all the worksheet data types (including errors), integers, range references, XLM macro sheet flow control types, and an internal binary storage data type.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="ab2f6-129">文字列は最大 255 文字の length-counted 文字列で表されます。</span><span class="sxs-lookup"><span data-stu-id="ab2f6-129">Strings are represented as length-counted byte strings of up to 255 characters length.</span></span> 
  
<span data-ttu-id="ab2f6-130">Excel 2007 で開始します。</span><span class="sxs-lookup"><span data-stu-id="ab2f6-130">Starting in Excel 2007:</span></span>
  
- <span data-ttu-id="ab2f6-131">**FP12**&ndash;浮動小数点数の 2 次元の配列構造体のすべての行と列が Excel 2007 の起動をサポートします。</span><span class="sxs-lookup"><span data-stu-id="ab2f6-131">**FP12** &ndash; a two-dimensional floating-point array structure supporting all the rows and columns starting in Excel 2007.</span></span> 
    
- <span data-ttu-id="ab2f6-132">**XLOPER12**&ndash; (エラーを含む) すべてのワークシートのデータ型、整数、範囲の参照、XLM マクロ シート フロー コントロールの種類、および内部バイナリ ストレージのデータ型を表すことができます複数の種類のデータ構造体です。</span><span class="sxs-lookup"><span data-stu-id="ab2f6-132">**XLOPER12** &ndash; a multi-type data structure that can represent all the worksheet data types (including errors), integers, range references, XLM macro sheet flow control types, and an internal binary storage data type.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="ab2f6-133">文字列は、最大 32,767 文字の length-counted Unicode 文字列で表されます。</span><span class="sxs-lookup"><span data-stu-id="ab2f6-133">Strings are represented as length-counted Unicode strings of up to 32,767 characters long.</span></span> 
  
## <a name="registration-data-type-codes"></a><span data-ttu-id="ab2f6-134">登録データは、コードを入力します。</span><span class="sxs-lookup"><span data-stu-id="ab2f6-134">Registration data type codes</span></span>

<span data-ttu-id="ab2f6-135">XLL 関数は、戻り値と引数の型をエンコードする文字の文字列を 3 番目の引数として受け取り、C API 関数**xlfRegister**を使用して登録されます。</span><span class="sxs-lookup"><span data-stu-id="ab2f6-135">XLL functions are registered using the C API function **xlfRegister**, which takes as its third argument a string of letters that encode the return and argument types.</span></span> <span data-ttu-id="ab2f6-136">この文字列には、関数は揮発性かどうかを Excel に通知はスレッド セーフである (Excel 2007 で開始)、マクロ シートに対応する情報も含まれていて、かどうか、その結果を返します場所引数を変更することによってします。</span><span class="sxs-lookup"><span data-stu-id="ab2f6-136">This string also contains the information that tells Excel whether the function is volatile, is thread-safe (starting in Excel 2007), is macro sheet equivalent, and whether it returns its result by modifying an argument in place.</span></span>
  
<span data-ttu-id="ab2f6-137">次の表は再現し、 [xlfRegister (フォーム 1)](xlfregister-form-1.md)のトピックで詳しく説明します。</span><span class="sxs-lookup"><span data-stu-id="ab2f6-137">The following table is reproduced and discussed in more detail in the [xlfRegister (Form 1)](xlfregister-form-1.md) topic.</span></span> <span data-ttu-id="ab2f6-138">このセクションの残りのコンテキストを提供するためにここでは再現されます。</span><span class="sxs-lookup"><span data-stu-id="ab2f6-138">It is reproduced here in order to provide a context for the rest of this section.</span></span> <span data-ttu-id="ab2f6-139">たとえば、型 C % 引数を受け取るよう (Excel 2007 で始まる) の長さのカウントの Unicode 文字列を受け取る関数を記述する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ab2f6-139">For example, a function that takes a length-counted Unicode string (starting in Excel 2007) could be described as taking a type C% argument.</span></span> 
  
|<span data-ttu-id="ab2f6-140">データ型</span><span class="sxs-lookup"><span data-stu-id="ab2f6-140">Data type</span></span>|<span data-ttu-id="ab2f6-141">値渡し</span><span class="sxs-lookup"><span data-stu-id="ab2f6-141">Pass by value</span></span>|<span data-ttu-id="ab2f6-142">参照渡し (ポインター)</span><span class="sxs-lookup"><span data-stu-id="ab2f6-142">Pass by ref (pointer)</span></span>|<span data-ttu-id="ab2f6-143">コメント</span><span class="sxs-lookup"><span data-stu-id="ab2f6-143">Comments</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ab2f6-144">ブール型 (Boolean)。</span><span class="sxs-lookup"><span data-stu-id="ab2f6-144">Boolean</span></span>  <br/> |<span data-ttu-id="ab2f6-145">A</span><span class="sxs-lookup"><span data-stu-id="ab2f6-145">A</span></span>  <br/> |<span data-ttu-id="ab2f6-146">L</span><span class="sxs-lookup"><span data-stu-id="ab2f6-146">L</span></span>  <br/> |<span data-ttu-id="ab2f6-147">short (0 = false または 1 = true)</span><span class="sxs-lookup"><span data-stu-id="ab2f6-147">short (0=false or 1=true)</span></span>  <br/> |
|<span data-ttu-id="ab2f6-148">double</span><span class="sxs-lookup"><span data-stu-id="ab2f6-148">double</span></span>  <br/> |<span data-ttu-id="ab2f6-149">B</span><span class="sxs-lookup"><span data-stu-id="ab2f6-149">B</span></span>  <br/> |<span data-ttu-id="ab2f6-150">E</span><span class="sxs-lookup"><span data-stu-id="ab2f6-150">E</span></span>  <br/> ||
|<span data-ttu-id="ab2f6-151">char\*</span><span class="sxs-lookup"><span data-stu-id="ab2f6-151">char \*</span></span>  <br/> ||<span data-ttu-id="ab2f6-152">C、F</span><span class="sxs-lookup"><span data-stu-id="ab2f6-152">C, F</span></span>  <br/> |<span data-ttu-id="ab2f6-153">Null で終了する ASCII バイト文字列</span><span class="sxs-lookup"><span data-stu-id="ab2f6-153">Null-terminated ASCII byte string</span></span>  <br/> |
|<span data-ttu-id="ab2f6-154">符号なし char 型\*</span><span class="sxs-lookup"><span data-stu-id="ab2f6-154">unsigned char \*</span></span>  <br/> ||<span data-ttu-id="ab2f6-155">D、G</span><span class="sxs-lookup"><span data-stu-id="ab2f6-155">D, G</span></span>  <br/> |<span data-ttu-id="ab2f6-156">長さのバイトの ASCII 文字列をカウント</span><span class="sxs-lookup"><span data-stu-id="ab2f6-156">Length -counted ASCII byte string</span></span>  <br/> |
|<span data-ttu-id="ab2f6-157">符号なしの短い\*(Excel 2007 で開始)</span><span class="sxs-lookup"><span data-stu-id="ab2f6-157">unsigned short \*  (starting in Excel 2007)</span></span>  <br/> ||<span data-ttu-id="ab2f6-158">C%、F%</span><span class="sxs-lookup"><span data-stu-id="ab2f6-158">C%, F%</span></span>  <br/> |<span data-ttu-id="ab2f6-159">Unicode ワイド文字の null で終わる文字列</span><span class="sxs-lookup"><span data-stu-id="ab2f6-159">Null-terminated Unicode wide character string</span></span>  <br/> |
|<span data-ttu-id="ab2f6-160">符号なしの短い\*(Excel 2007 で開始)</span><span class="sxs-lookup"><span data-stu-id="ab2f6-160">unsigned short \*  (starting in Excel 2007)</span></span>  <br/> ||<span data-ttu-id="ab2f6-161">D%、G%</span><span class="sxs-lookup"><span data-stu-id="ab2f6-161">D%, G%</span></span>  <br/> |<span data-ttu-id="ab2f6-162">Unicode ワイド文字文字列の長さのカウント</span><span class="sxs-lookup"><span data-stu-id="ab2f6-162">Length-counted Unicode wide character string</span></span>  <br/> |
|<span data-ttu-id="ab2f6-163">unsigned short [int]</span><span class="sxs-lookup"><span data-stu-id="ab2f6-163">unsigned short [int]</span></span>  <br/> |<span data-ttu-id="ab2f6-164">H</span><span class="sxs-lookup"><span data-stu-id="ab2f6-164">H</span></span>  <br/> ||<span data-ttu-id="ab2f6-165">WORD</span><span class="sxs-lookup"><span data-stu-id="ab2f6-165">WORD</span></span>  <br/> |
|<span data-ttu-id="ab2f6-166">[signed] short [int]</span><span class="sxs-lookup"><span data-stu-id="ab2f6-166">[signed] short [int]</span></span>  <br/> |<span data-ttu-id="ab2f6-167">I</span><span class="sxs-lookup"><span data-stu-id="ab2f6-167">I</span></span>  <br/> |<span data-ttu-id="ab2f6-168">M</span><span class="sxs-lookup"><span data-stu-id="ab2f6-168">M</span></span>  <br/> |<span data-ttu-id="ab2f6-169">16 ビット</span><span class="sxs-lookup"><span data-stu-id="ab2f6-169">16-bit</span></span>  <br/> |
|<span data-ttu-id="ab2f6-170">[signed long] int</span><span class="sxs-lookup"><span data-stu-id="ab2f6-170">[signed long] int</span></span>  <br/> |<span data-ttu-id="ab2f6-171">J</span><span class="sxs-lookup"><span data-stu-id="ab2f6-171">J</span></span>  <br/> |<span data-ttu-id="ab2f6-172">N</span><span class="sxs-lookup"><span data-stu-id="ab2f6-172">N</span></span>  <br/> |<span data-ttu-id="ab2f6-173">32 ビット</span><span class="sxs-lookup"><span data-stu-id="ab2f6-173">32-bit</span></span>  <br/> |
|<span data-ttu-id="ab2f6-174">配列</span><span class="sxs-lookup"><span data-stu-id="ab2f6-174">Array</span></span>  <br/> ||<span data-ttu-id="ab2f6-175">O</span><span class="sxs-lookup"><span data-stu-id="ab2f6-175">O</span></span>  <br/> | <span data-ttu-id="ab2f6-176">参照により以下の 3 つの引数として渡されます。</span><span class="sxs-lookup"><span data-stu-id="ab2f6-176">Passed as three arguments by reference:</span></span>  <br/><span data-ttu-id="ab2f6-177">1. 短い int\*行</span><span class="sxs-lookup"><span data-stu-id="ab2f6-177">1. short int \*rows</span></span>  <br/><span data-ttu-id="ab2f6-178">2. 短い int\*列</span><span class="sxs-lookup"><span data-stu-id="ab2f6-178">2. short int \*columns</span></span>  <br/><span data-ttu-id="ab2f6-179">3 倍\*配列</span><span class="sxs-lookup"><span data-stu-id="ab2f6-179">3. double \*array</span></span>  <br/> |
|<span data-ttu-id="ab2f6-180">配列</span><span class="sxs-lookup"><span data-stu-id="ab2f6-180">Array</span></span>  <br/> <span data-ttu-id="ab2f6-181">(Excel 2007 で開始)</span><span class="sxs-lookup"><span data-stu-id="ab2f6-181">(starting in Excel 2007)</span></span>  <br/> ||<span data-ttu-id="ab2f6-182">O%</span><span class="sxs-lookup"><span data-stu-id="ab2f6-182">O%</span></span>  <br/> | <span data-ttu-id="ab2f6-183">参照により以下の 3 つの引数として渡されます。</span><span class="sxs-lookup"><span data-stu-id="ab2f6-183">Passed as three arguments by reference:</span></span>  <br/><span data-ttu-id="ab2f6-184">1. int\*行</span><span class="sxs-lookup"><span data-stu-id="ab2f6-184">1. int \*rows</span></span>  <br/><span data-ttu-id="ab2f6-185">2. int\*列</span><span class="sxs-lookup"><span data-stu-id="ab2f6-185">2. int \*columns</span></span>  <br/><span data-ttu-id="ab2f6-186">3 倍\*配列</span><span class="sxs-lookup"><span data-stu-id="ab2f6-186">3. double \*array</span></span>  <br/> |
|<span data-ttu-id="ab2f6-187">FP</span><span class="sxs-lookup"><span data-stu-id="ab2f6-187">FP</span></span>  <br/> ||<span data-ttu-id="ab2f6-188">K</span><span class="sxs-lookup"><span data-stu-id="ab2f6-188">K</span></span>  <br/> |<span data-ttu-id="ab2f6-189">浮動小数点配列構造</span><span class="sxs-lookup"><span data-stu-id="ab2f6-189">Floating-point array structure</span></span>  <br/> |
|<span data-ttu-id="ab2f6-190">FP12</span><span class="sxs-lookup"><span data-stu-id="ab2f6-190">FP12</span></span>  <br/> <span data-ttu-id="ab2f6-191">(Excel 2007 で開始)</span><span class="sxs-lookup"><span data-stu-id="ab2f6-191">(starting in Excel 2007)</span></span>  <br/> ||<span data-ttu-id="ab2f6-192">K%</span><span class="sxs-lookup"><span data-stu-id="ab2f6-192">K%</span></span>  <br/> |<span data-ttu-id="ab2f6-193">浮動小数点配列構造体の大規模なグリッド</span><span class="sxs-lookup"><span data-stu-id="ab2f6-193">Large grid floating-point array structure</span></span>  <br/> |
|<span data-ttu-id="ab2f6-194">XLOPER</span><span class="sxs-lookup"><span data-stu-id="ab2f6-194">XLOPER</span></span>  <br/> ||<span data-ttu-id="ab2f6-195">P</span><span class="sxs-lookup"><span data-stu-id="ab2f6-195">P</span></span>  <br/> |<span data-ttu-id="ab2f6-196">可変型のワークシートの値および配列</span><span class="sxs-lookup"><span data-stu-id="ab2f6-196">Variable-type worksheet values and arrays</span></span>  <br/> |
|||<span data-ttu-id="ab2f6-197">R</span><span class="sxs-lookup"><span data-stu-id="ab2f6-197">R</span></span>  <br/> |<span data-ttu-id="ab2f6-198">値、配列、および範囲の参照</span><span class="sxs-lookup"><span data-stu-id="ab2f6-198">Values, arrays, and range references</span></span>  <br/> |
|<span data-ttu-id="ab2f6-199">XLOPER12</span><span class="sxs-lookup"><span data-stu-id="ab2f6-199">XLOPER12</span></span>  <br/> <span data-ttu-id="ab2f6-200">(Excel 2007 で開始)</span><span class="sxs-lookup"><span data-stu-id="ab2f6-200">(starting in Excel 2007)</span></span>  <br/> ||<span data-ttu-id="ab2f6-201">Q</span><span class="sxs-lookup"><span data-stu-id="ab2f6-201">Q</span></span>  <br/> |<span data-ttu-id="ab2f6-202">可変型のワークシートの値および配列</span><span class="sxs-lookup"><span data-stu-id="ab2f6-202">Variable-type worksheet values and arrays</span></span>  <br/> |
|||<span data-ttu-id="ab2f6-203">U</span><span class="sxs-lookup"><span data-stu-id="ab2f6-203">U</span></span>  <br/> |<span data-ttu-id="ab2f6-204">値、配列、および範囲の参照</span><span class="sxs-lookup"><span data-stu-id="ab2f6-204">Values, arrays, and range references</span></span>  <br/> |
   
<span data-ttu-id="ab2f6-205">**C %** **F %** **D %** **G %** **K %** **O %** **Q**、 **U**がすべての Microsoft Office Excel 2007 で新しいとは種類は、以前のバージョンでサポートされています。</span><span class="sxs-lookup"><span data-stu-id="ab2f6-205">The types **C%**, **F%**, **D%**, **G%**, **K%**, **O%**, **Q**, and **U** were all new in Microsoft Office Excel 2007 and are not supported in earlier versions.</span></span> <span data-ttu-id="ab2f6-206">**F** **F %** **G**、および**G の %** は、文字列型は、引数には、場所の変更に使用されます。</span><span class="sxs-lookup"><span data-stu-id="ab2f6-206">The string types **F**, **F%**, **G**, and **G%** are used for arguments that are modified-in-place.</span></span> <span data-ttu-id="ab2f6-207">**XLOPER**または**XLOPER12**の引数はそれぞれ**P**または**Q**の種類として登録されている、Excel は準備をするときに単純な値を 1 つのセル参照とアレイへの複数のセル参照を変換します。</span><span class="sxs-lookup"><span data-stu-id="ab2f6-207">When **XLOPER** or **XLOPER12** arguments are registered as types **P** or **Q** respectively, Excel converts single-cell references to simple values and multi-cell references to arrays when it prepares them.</span></span> 
  
<span data-ttu-id="ab2f6-208">**P**と**Q**の種類は常に、関数に次の種類の 1 つとして到着した: **xltypeNum**、 **xltypeStr**、 **xltypeBool**、 **xltypeErr**、 **xltypeMulti**、 **xltypeMissing**、 **xltypeNil**、または、**xltypeRef**または**xltypeSRef**ではないため、これらを常に逆参照します。</span><span class="sxs-lookup"><span data-stu-id="ab2f6-208">**P** and **Q** types always arrive in your function as one of the following types: **xltypeNum**, **xltypeStr**, **xltypeBool**, **xltypeErr**, **xltypeMulti**, **xltypeMissing**, or **xltypeNil**, but not **xltypeRef** or **xltypeSRef** because these are always dereferenced.</span></span> 
  
<span data-ttu-id="ab2f6-209">引数が参照によって渡される Fortran Dll との互換性のために本当にスタック上の 3 つの引数には、 **O**の種類が導入されました。</span><span class="sxs-lookup"><span data-stu-id="ab2f6-209">Type **O**, which is really three arguments on the stack, was introduced for compatibility with Fortran DLLs where arguments are passed by reference.</span></span> <span data-ttu-id="ab2f6-210">変更・ イン ・ プレースの戻り値として引数を宣言して、参照されている値に結果を配置することによって以外の値を取得するには使用できません。</span><span class="sxs-lookup"><span data-stu-id="ab2f6-210">It cannot be used to return a value except by declaring the argument as a modify-in-place return value and placing the results in the referenced values.</span></span> <span data-ttu-id="ab2f6-211">型 **%o%** は、Office Excel 2003 グリッドよりも大きい領域をカバーしているアレイにアクセスできるように、Excel 2007 では**O**型を拡張します。</span><span class="sxs-lookup"><span data-stu-id="ab2f6-211">Type **O%** extends type **O** in Excel 2007 so that it can access arrays that cover areas larger than the Office Excel 2003 grid.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ab2f6-212">関連項目</span><span class="sxs-lookup"><span data-stu-id="ab2f6-212">See also</span></span>

- [<span data-ttu-id="ab2f6-213">xlfRegister (�\`�� 1)</span><span class="sxs-lookup"><span data-stu-id="ab2f6-213">xlfRegister (Form 1)</span></span>](xlfregister-form-1.md)
- [<span data-ttu-id="ab2f6-214">Excel �v���O���~���O�̊T�O</span><span class="sxs-lookup"><span data-stu-id="ab2f6-214">Excel Programming Concepts</span></span>](excel-programming-concepts.md)
- [<span data-ttu-id="ab2f6-215">Excel XLL SDK API �֐����t�@�����X</span><span class="sxs-lookup"><span data-stu-id="ab2f6-215">Excel XLL SDK API Function Reference</span></span>](excel-xll-sdk-api-function-reference.md)

