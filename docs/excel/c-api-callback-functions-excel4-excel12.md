---
title: C API �R�[���o�b�N�֐� Excel4�AExcel12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- functions [excel 2007], c api callback
localization_priority: Normal
ms.assetid: 0f3ae86d-329a-4177-a65b-6288c248297e
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 5fe5eb7486f12d75ce7e42ad57141480ec735c54
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434432"
---
# <a name="c-api-callback-functions-excel4-excel12"></a><span data-ttu-id="64cfc-104">C API コールバック関数 Excel4、Excel12</span><span class="sxs-lookup"><span data-stu-id="64cfc-104">C API Callback Functions Excel4, Excel12</span></span>

<span data-ttu-id="64cfc-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="64cfc-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="64cfc-p101">**Excel4** 関数と **Excel12** 関数は、DLL による内部 Microsoft Excel ワークシート関数、マクロ シート関数またはコマンド、XLL 専用の特殊な関数またはコマンドの呼び出しを可能にするために提供されています。**Excel4** 関数は、Excel の最近のすべてのバージョンでサポートされています。**Excel12** 関数は、Excel 2007 以降でサポートされています。両方の関数は 2 つのフォームで提供されます。</span><span class="sxs-lookup"><span data-stu-id="64cfc-p101">The **Excel4** and **Excel12** functions are provided to enable DLLs to call an internal Microsoft Excel worksheet function, macro sheet function or command, or XLL-only special function or command. All recent versions of Excel support the **Excel4** function. Starting in Excel 2007 the **Excel12** function is supported. Both functions are provided in two forms:</span></span> 
  
- <span data-ttu-id="64cfc-110">可変長引数リスト フォーム (**Excel4/Excel12**)</span><span class="sxs-lookup"><span data-stu-id="64cfc-110">A variable-length argument list form (**Excel4/Excel12**)</span></span>
    
- <span data-ttu-id="64cfc-111">引数の配列フォーム (**Excel4v/Excel12v**)</span><span class="sxs-lookup"><span data-stu-id="64cfc-111">An array-of-arguments form (**Excel4v/Excel12v**)</span></span>
    
<span data-ttu-id="64cfc-p102">Except for the way in which arguments are passed to these callbacks, the two forms are functionally equivalent. The basic concepts for both forms are fully described in [Excel4/Excel12](excel4-excel12.md). [Excel4v/Excel12v](excel4v-excel12v.md) covers other issues about this form.</span><span class="sxs-lookup"><span data-stu-id="64cfc-p102">Except for the way in which arguments are passed to these callbacks, the two forms are functionally equivalent. The basic concepts for both forms are fully described in [Excel4/Excel12](excel4-excel12.md). [Excel4v/Excel12v](excel4v-excel12v.md) covers other issues about this form.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="64cfc-115">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="64cfc-115">In this section</span></span>

[<span data-ttu-id="64cfc-116">Excel4/Excel12</span><span class="sxs-lookup"><span data-stu-id="64cfc-116">Excel4/Excel12</span></span>](excel4-excel12.md)
  
[<span data-ttu-id="64cfc-117">Excel4v/Excel12v</span><span class="sxs-lookup"><span data-stu-id="64cfc-117">Excel4v/Excel12v</span></span>](excel4v-excel12v.md)
  

