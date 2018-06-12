---
title: FuncFib
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- FuncFib
keywords:
- funcfib function [excel 2007]
localization_priority: Normal
ms.assetid: 6a719f04-b2d1-4f87-a227-be561cbd3e49
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 8d1c97ea57e968aaedffca6b37ded3d875e87413
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798878"
---
# <a name="funcfib"></a><span data-ttu-id="becb5-104">FuncFib</span><span class="sxs-lookup"><span data-stu-id="becb5-104">FuncFib</span></span>

 <span data-ttu-id="becb5-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="becb5-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="becb5-p101">N 番目のフィボナッチ数を計算するユーザー定義ワークシート関数の例です。GENERIC.xll が読み込まれるときに、ワークシートから呼び出すことができるように、この関数を登録します。</span><span class="sxs-lookup"><span data-stu-id="becb5-p101">Example user-defined worksheet function that computes the Nth Fibonacci number. When GENERIC.xll is loaded, it registers this function so that it can be called from the worksheet.</span></span>
  
```cs
LPXLOPER12 WINAPI FuncFib (LPXLOPER12 pxN);
```

## <a name="parameters"></a><span data-ttu-id="becb5-108">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="becb5-108">Parameters</span></span>

 <span data-ttu-id="becb5-109">_pxN_(**LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="becb5-109">_pxN_ (**LPXLOPER12**)</span></span>
  
<span data-ttu-id="becb5-110">N �Ԗڂ̃t�B�{�i�b�\`�����K�v�Ƃ���� N �̒l�B</span><span class="sxs-lookup"><span data-stu-id="becb5-110">The value of N for which the Nth Fibonacci number is required.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="becb5-111">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="becb5-111">Property value/Return value</span></span>

<span data-ttu-id="becb5-112">(正常終了した場合**xltypeNum LPXLOPER12**または**xltypeErr**それ以外の場合)</span><span class="sxs-lookup"><span data-stu-id="becb5-112">(**xltypeNum LPXLOPER12** if successful or **xltypeErr** otherwise)</span></span> 
  
<span data-ttu-id="becb5-113">N �Ԗڂ̃t�B�{�i�b�\`���B</span><span class="sxs-lookup"><span data-stu-id="becb5-113">The Nth Fibonacci number.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="becb5-114">����</span><span class="sxs-lookup"><span data-stu-id="becb5-114">Remarks</span></span>

<span data-ttu-id="becb5-p102">���̊֐��́A�֐��u���b�N��Œ�\`����Ă���ÓI�ϐ���߂�l **XLOPER12** �Ƃ��Ďg�p���܂��B����̓X���b�h �Z�[�t�ł͂Ȃ����߁A���̊֐��A����� **XLOPER** �܂��� **XLOPER12** ��Ԃ����߂ɂ��̐헪��g�p���邷�ׂẴ��[�N�V�[�g�֐��ɂ��ẮAExcel 2007 �ȍ~�ł̓X���b�h�Z�[�t�Ƃ��ēo�^���Ȃ��ł��������B</span><span class="sxs-lookup"><span data-stu-id="becb5-p102">The function uses a static variable defined within the function block as the return value **XLOPER12**. This is not thread safe, and so this function, and any worksheet function that uses this strategy for returning **XLOPER**s or **XLOPER12**s, should not be registered as thread safe starting in Excel 2007.</span></span>
  
### <a name="example"></a><span data-ttu-id="becb5-117">��</span><span class="sxs-lookup"><span data-stu-id="becb5-117">Example</span></span>

<span data-ttu-id="becb5-118">���̊֐��̃\�[�X �R�[�h�ɂ��ẮA `\SAMPLES\GENERIC\GENERIC.C` ��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="becb5-118">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="becb5-119">�֘A����</span><span class="sxs-lookup"><span data-stu-id="becb5-119">See also</span></span>



[<span data-ttu-id="becb5-120">�ėp DLL �̊֐�</span><span class="sxs-lookup"><span data-stu-id="becb5-120">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

