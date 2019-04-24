---
title: xlfRegister (�`�� 2)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfRegister
keywords:
- xlfregister function [excel 2007]
localization_priority: Normal
ms.assetid: 3ebbd775-f3d2-4ba7-8835-a5b38ad2267a
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 66af741456ab763ef346a8777429f0ae1be77c11
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310123"
---
# <a name="xlfregister-form-2"></a><span data-ttu-id="33567-104">xlfRegister (形式 2)</span><span class="sxs-lookup"><span data-stu-id="33567-104">xlfRegister (Form 2)</span></span>

 <span data-ttu-id="33567-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="33567-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="33567-p101">Microsoft Excel から呼び出された DLL コマンドまたは XLL コマンドから呼び出すことができます。これは、Excel XLM マクロ シートからの **REGISTER** の呼び出しと同等です。</span><span class="sxs-lookup"><span data-stu-id="33567-p101">Can be called from a DLL or XLL command that has itself been called by Microsoft Excel. This is equivalent to calling **REGISTER** from an Excel XLM macro sheet.</span></span> 
  
<span data-ttu-id="33567-108">**xlfRegister** 関数は、次の 2 つの形式で呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="33567-108">The **xlfRegister** function can be called in two forms:</span></span> 
  
- <span data-ttu-id="33567-109">[xlfRegister (形式 1)](xlfregister-form-1.md): コマンドや関数を個々に登録します。</span><span class="sxs-lookup"><span data-stu-id="33567-109">[xlfRegister (Form 1)](xlfregister-form-1.md): Registers an individual command or function.</span></span>
    
- <span data-ttu-id="33567-110">xlfRegister (形式 2): XLL を読み込んでアクティブ化します。</span><span class="sxs-lookup"><span data-stu-id="33567-110">xlfRegister (Form 2): Loads and activates an XLL.</span></span>
    
<span data-ttu-id="33567-111">この関数を形式 2 で呼び出した場合は、[xlAutoOpen](xlautoopen.md) プロシージャを含む XLL の読み込みとアクティブ化のみ行います。</span><span class="sxs-lookup"><span data-stu-id="33567-111">Called in Form 2, this function can only be used to load and activate an XLL containing an [xlAutoOpen](xlautoopen.md) procedure.</span></span> 
  
```cs
Excel12(xlfRegister, LPXLOPER12 pxRes, 1, LPXLOPER12 pxModuleText);
```

## <a name="parameters"></a><span data-ttu-id="33567-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="33567-112">Parameters</span></span>

 <span data-ttu-id="33567-113">_pxModuleText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="33567-113">_pxModuleText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="33567-114">読み込みとアクティブ化を行う DLL 名。</span><span class="sxs-lookup"><span data-stu-id="33567-114">The name of the DLL to be loaded and activated.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="33567-115">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="33567-115">Property value/Return value</span></span>

<span data-ttu-id="33567-116">成功すると、DLL 名 (**xltypeStr**) を返します。</span><span class="sxs-lookup"><span data-stu-id="33567-116">If successful, this returns the name of the DLL (**xltypeStr**).</span></span> <span data-ttu-id="33567-117">それ以外の場合は、#VALUE! </span><span class="sxs-lookup"><span data-stu-id="33567-117">Otherwise it returns a #VALUE!</span></span> <span data-ttu-id="33567-118">エラーを返します。</span><span class="sxs-lookup"><span data-stu-id="33567-118">error.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="33567-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="33567-119">See also</span></span>



[<span data-ttu-id="33567-120">重要で役に立つ C API XLM 関数</span><span class="sxs-lookup"><span data-stu-id="33567-120">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

