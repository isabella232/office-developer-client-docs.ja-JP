---
title: debugPrintf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- debugPrintf
keywords:
- debugprintf function [excel 2007]
localization_priority: Normal
ms.assetid: 9ad541f6-0b35-4f50-926a-8940e3f8033a
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 25669cfc705e797b80be0fab590d809e8f1e3b5c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798769"
---
# <a name="debugprintf"></a><span data-ttu-id="1fca1-104">debugPrintf</span><span class="sxs-lookup"><span data-stu-id="1fca1-104">debugPrintf</span></span>

<span data-ttu-id="1fca1-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="1fca1-105">Applies to: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="1fca1-p101">null で終わるバイト文字列を、Windows SDK 関数 **OutputDebugStringA** を使用してアクティブなデバッガーに書き込むフレームワーク ライブラリ関数。アプリケーションにデバッガーがない場合は、システムのデバッガーに文字列が表示されます。アプリケーションにデバッガーがなく、システムのデバッガーがアクティブでない場合、**debugPrintf** は何の動作も行いません。</span><span class="sxs-lookup"><span data-stu-id="1fca1-p101">Framework library function that writes a null-terminated byte-string to the active debugger via the Windows SDK function **OutputDebugStringA**. If the application has no debugger, the system debugger displays the string. If the application has no debugger and the system debugger is not active, **debugPrintf** does nothing.</span></span> 
  
<span data-ttu-id="1fca1-109">この関数は値を返しません。</span><span class="sxs-lookup"><span data-stu-id="1fca1-109">This function does not return a value.</span></span>
  
```cs
void WINAPI debugPrintf(LPSTR lpFormat, arguments);
```

## <a name="parameters"></a><span data-ttu-id="1fca1-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="1fca1-110">Parameters</span></span>

 <span data-ttu-id="1fca1-111">_lpFormat (LPSTR)_</span><span class="sxs-lookup"><span data-stu-id="1fca1-111">_lpFormat (LPSTR)_</span></span>
  
<span data-ttu-id="1fca1-112">形式文字列。**sprintf** 関数とともに用いられる文字列の構文とルールに従います。</span><span class="sxs-lookup"><span data-stu-id="1fca1-112">The format string, which follows the syntax and rules for that used with the **sprintf** function.</span></span> 
  
 <span data-ttu-id="1fca1-113">_arguments_</span><span class="sxs-lookup"><span data-stu-id="1fca1-113">_arguments_</span></span>
  
<span data-ttu-id="1fca1-114">形式文字列に一致する 0 個以上の引数。</span><span class="sxs-lookup"><span data-stu-id="1fca1-114">Zero or more arguments to match the format string.</span></span>
  
## <a name="example"></a><span data-ttu-id="1fca1-115">例</span><span class="sxs-lookup"><span data-stu-id="1fca1-115">Example</span></span>

<span data-ttu-id="1fca1-p102">この関数は、関数にコントロールが渡されたことを示す文字列を印刷します。コンパイルする前に _DEBUG フラグを定義する必要があります。未定義のままでは、この関数は何の動作も行いません。</span><span class="sxs-lookup"><span data-stu-id="1fca1-p102">This function prints a string to show that control was passed to it. The _DEBUG flag must be defined before compiling or else this function does nothing.</span></span>
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI debugPrintfExample(void)
{
#ifdef _DEBUG
   debugPrintf("Made it!\r");
#endif
   return 1;
}

```

## <a name="see-also"></a><span data-ttu-id="1fca1-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="1fca1-118">See also</span></span>



[<span data-ttu-id="1fca1-119">フレームワーク ライブラリの関数</span><span class="sxs-lookup"><span data-stu-id="1fca1-119">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

