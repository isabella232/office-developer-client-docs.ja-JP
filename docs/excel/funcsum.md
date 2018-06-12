---
title: FuncSum
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- FuncSum
keywords:
- funcsum function [excel 2007]
localization_priority: Normal
ms.assetid: 934192ef-8a89-4dbb-bd37-01e92ba24256
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 0b991cf5cdae90522abc9512193ee556e4c6e6e1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798886"
---
# <a name="funcsum"></a><span data-ttu-id="58fbe-104">FuncSum</span><span class="sxs-lookup"><span data-stu-id="58fbe-104">FuncSum</span></span>

 <span data-ttu-id="58fbe-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="58fbe-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="58fbe-p101">1 ���� 29 �̈��������āA���̍��v��v�Z���郆�[�U�[��\`���[�N�V�[�g�֐��̗�B�e�����Ɏw��ł���̂́A1 �̐����A�͈́A�܂��͔z��ł��BGENERIC.xll ���ǂݍ��܂��ƁAGENERIC.xll �ɂ���Ă��̊֐����o�^����āA���[�N�V�[�g����Ăяo�����Ƃ��ł���悤�ɂȂ�܂��B</span><span class="sxs-lookup"><span data-stu-id="58fbe-p101">Example user-defined worksheet function that takes 1 to 29 arguments and computes their sum. Each argument can be a single number, a range, or an array. When GENERIC.xll is loaded, it registers this function so that it can be called from the worksheet.</span></span> 
  
```cs
LPXLOPER12 WINAPI FuncSum(LPXLOPER12 px1, LPXLOPER12 px2, LPXLOPER12 px3,LPXLOPER12 px4, LPXLOPER12 px5, LPXLOPER12 px6, LPXLOPER12 px7,LPXLOPER12 px8, LPXLOPER12 px9, LPXLOPER12 px10, LPXLOPER12 px11,LPXLOPER12 px12, LPXLOPER12 px13, LPXLOPER12 px14, LPXLOPER12 px15,LPXLOPER12 px16, LPXLOPER12 px17, LPXLOPER12 px18, LPXLOPER12 px19,LPXLOPER12 px20, LPXLOPER12 px21, LPXLOPER12 px22, LPXLOPER12 px23,LPXLOPER12 px24, LPXLOPER12 px25, LPXLOPER12 px26, LPXLOPER12 px27,LPXLOPER12 px28, LPXLOPER12 px29);
```

## <a name="parameters"></a><span data-ttu-id="58fbe-109">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="58fbe-109">Parameters</span></span>

 <span data-ttu-id="58fbe-110">_px1 px29_(**LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="58fbe-110">_px1-px29_ (**LPXLOPER12**)</span></span>
  
<span data-ttu-id="58fbe-p102">**XLOPER12** �����ւ̃|�C���^�[�B�֐��́A�C�ӂ̓��͂̌^��󂯓���܂����A�����A�����̃��e�����z��A����ѐ����܂��͋󔒃Z���݂̂��܂܂�Ă���͈͂�Ώۂɍ쓮����悤�R�[�f�B���O����Ă��܂��B29 �����̈��������������ƁA�c��̈����� **xltypeMissing** �Ƃ��ċ�������܂��B</span><span class="sxs-lookup"><span data-stu-id="58fbe-p102">Pointers to **XLOPER12** arguments. The function accepts any kind of input type but is coded only to operate on numbers, literal arrays of numbers, and ranges containing only numbers or blank cells. If fewer than 29 arguments are supplied, the remaining arguments are supplied as **xltypeMissing**.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="58fbe-114">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="58fbe-114">Property value/Return value</span></span>

<span data-ttu-id="58fbe-115">**LPXLOPER12 xltypeNum** ( **xltypeErr**)</span><span class="sxs-lookup"><span data-stu-id="58fbe-115">(**LPXLOPER12 xltypeNum** or **xltypeErr**)</span></span>
  
<span data-ttu-id="58fbe-p103">�������ꂽ�������X�g�A�͈͓�̃Z���A�z���̗v�f�ɁA�����ȊO�̕��������݂���ꍇ�́A�����̍��v�A���邢�� #VALUE!�B</span><span class="sxs-lookup"><span data-stu-id="58fbe-p103">The sum of the arguments or #VALUE! if there are non-numerics in the supplied argument list or in a cell in a range or element in an array.</span></span>
  
### <a name="example"></a><span data-ttu-id="58fbe-118">��</span><span class="sxs-lookup"><span data-stu-id="58fbe-118">Example</span></span>

<span data-ttu-id="58fbe-119">���̊֐��̃\�[�X �R�[�h�ɂ��ẮA `\SAMPLES\GENERIC\GENERIC.C` ��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="58fbe-119">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="58fbe-120">�֘A����</span><span class="sxs-lookup"><span data-stu-id="58fbe-120">See also</span></span>



[<span data-ttu-id="58fbe-121">�ėp DLL �̊֐�</span><span class="sxs-lookup"><span data-stu-id="58fbe-121">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

