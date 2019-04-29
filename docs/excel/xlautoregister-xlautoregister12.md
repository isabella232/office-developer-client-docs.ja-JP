---
title: xlAutoRegister/xlAutoRegister12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoRegister
keywords:
- xlautoregister function [excel 2007]
localization_priority: Normal
ms.assetid: aa4673cf-8e97-4678-b8d4-6a74426334f9
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f043558f3f642001e9ba11ee5b18a2721c3dddfb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421166"
---
# <a name="xlautoregisterxlautoregister12"></a><span data-ttu-id="cf1a1-104">xlAutoRegister/xlAutoRegister12</span><span class="sxs-lookup"><span data-stu-id="cf1a1-104">xlAutoRegister/xlAutoRegister12</span></span>

 <span data-ttu-id="cf1a1-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="cf1a1-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="cf1a1-p101">登録対象の関数の戻り値の型と引数の型がない状態で、XLM 関数 **REGISTER**、または C API の同等の [xlfRegister 関数](xlfregister-form-1.md)に対する呼び出しが実行されると、常に Excel は [xlAutoRegister 関数](xlautoregister-xlautoregister12.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="cf1a1-p101">Excel calls the [xlAutoRegister function](xlautoregister-xlautoregister12.md) whenever a call has been made to the XLM function **REGISTER**, or the C API equivalent [xlfRegister function](xlfregister-form-1.md), with the return and argument types of the function being registered missing. It allows the XLL to search its internal lists of exported functions and commands to register the function with the argument and return types specified.</span></span>
  
<span data-ttu-id="cf1a1-108">Excel 2007 以降では、**xlAutoRegister12** 関数が XLL によってエクスポートされている場合、Excel はこの関数を **xlAutoRegister** 関数よりも優先して呼び出します。</span><span class="sxs-lookup"><span data-stu-id="cf1a1-108">Starting in Excel 2007, Excel calls the **xlAutoRegister12** function in preference to the **xlAutoRegister** function if it is exported by the XLL.</span></span> 
  
<span data-ttu-id="cf1a1-109">Excel では、XLL がこれらいずれかの関数を実装してエクスポートすることは不要です。</span><span class="sxs-lookup"><span data-stu-id="cf1a1-109">Excel does not require an XLL to implement and export either of these functions.</span></span>
  
> [!NOTE]
> <span data-ttu-id="cf1a1-110">**xlAutoRegister**/ **xlAutoRegister12** が引数の型と戻り値の型を指定しないで関数を登録しようとすると、最終的にコール スタックがオーバーフローし、Excel がクラッシュする原因となる再帰呼び出しのループが発生します。</span><span class="sxs-lookup"><span data-stu-id="cf1a1-110">If **xlAutoRegister**/ **xlAutoRegister12** tries to register the function without supplying the argument and return types, a recursive calling loop occurs which eventually overflows the call stack and crashes Excel.</span></span> 
  
```cs
LPXLOPER12 WINAPI xlAutoRegister12(LPXLOPER12 pxName);
LPXLOPER WINAPI xlAutoRegister(LPXLOPER pxName);
```

## <a name="parameters"></a><span data-ttu-id="cf1a1-111">パラメーター</span><span class="sxs-lookup"><span data-stu-id="cf1a1-111">Parameters</span></span>

 <span data-ttu-id="cf1a1-112">_pxName_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="cf1a1-112">_pxName_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="cf1a1-113">登録される XLL 関数の名前です。</span><span class="sxs-lookup"><span data-stu-id="cf1a1-113">The name of the XLL function that is being registered.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="cf1a1-114">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="cf1a1-114">Property value/Return value</span></span>

<span data-ttu-id="cf1a1-p102">この関数は、**xlfRegister** 関数を使用して XLL 関数 _pxName_ を登録を試行した結果を返します。指定した関数が XLL ファイルのエクスポートの 1 つでない場合、関数は **#VALUE!** エラーを返すか、Excel が **#VALUE!** と解釈する **NULL** を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="cf1a1-p102">The function should return the result of the attempt to register the XLL function  _pxName_ using the **xlfRegister** function. If the specified function is not one of the XLL's exports, it should return the **#VALUE!** error, or **NULL** which Excel will interpret at **#VALUE!**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cf1a1-118">注釈</span><span class="sxs-lookup"><span data-stu-id="cf1a1-118">Remarks</span></span>

<span data-ttu-id="cf1a1-p103">**xlAutoRegister** の実装では、エクスポートする XLL ファイルの関数とコマンドの内部リストで大文字小文字を区別する検索を実行して、渡された名前との一致を検索する必要があります。関数またはコマンドが見つかった場合、**xlAutoRegister** は **xlfRegister** 関数を使用し、Excel に関数の戻り値の型と引数の型、および関数に関するその他の必要情報を指示する文字列を指定して、登録を試行する必要があります。これは、**xlfRegister** に対する呼び出しが返された場合にも、Excel に返す必要があります。関数が正常に登録された場合、**xlfRegister** は関数の登録 ID を含む **xltypeNum** 値を返します。</span><span class="sxs-lookup"><span data-stu-id="cf1a1-p103">Your implementation of **xlAutoRegister** should perform a case-insensitive search through your XLL's internal lists of the functions and commands it exports looking for a match with the passed-in name. If the function or command is found, **xlAutoRegister** should attempt to register it, using the **xlfRegister** function, making sure to provide the string that tells Excel the return and argument types of the function, as well as any other required information about the function. It should then return to Excel whatever the call to **xlfRegister** returned. If the function was registered successfully, **xlfRegister** returns an **xltypeNum** value containing the Register ID of the function.</span></span> 
  
### <a name="example"></a><span data-ttu-id="cf1a1-123">例</span><span class="sxs-lookup"><span data-stu-id="cf1a1-123">Example</span></span>

<span data-ttu-id="cf1a1-124">この関数の実装例については、ファイル `SAMPLES\EXAMPLE\EXAMPLE.C` を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cf1a1-124">See the file  `SAMPLES\EXAMPLE\EXAMPLE.C` for an example implementation of this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cf1a1-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="cf1a1-125">See also</span></span>



[<span data-ttu-id="cf1a1-126">REGISTER</span><span class="sxs-lookup"><span data-stu-id="cf1a1-126">REGISTER</span></span>](xlfregister-form-1.md)
  
[<span data-ttu-id="cf1a1-127">UNREGISTER</span><span class="sxs-lookup"><span data-stu-id="cf1a1-127">UNREGISTER</span></span>](xlfunregister-form-1.md)

