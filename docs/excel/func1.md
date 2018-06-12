---
title: Func1
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Func1
keywords:
- func1 function [excel 2007]
localization_priority: Normal
ms.assetid: 801b14ef-0be8-4b97-919d-a9d413705d1c
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 26439f1fb05aae2077844ce19935d9ff99e4f701
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798880"
---
# <a name="func1"></a><span data-ttu-id="730d4-104">Func1</span><span class="sxs-lookup"><span data-stu-id="730d4-104">Func1</span></span>

 <span data-ttu-id="730d4-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="730d4-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="730d4-p101">���[�U�[��\`�̃��[�N�V�[�g�֐��̗�ŁA�Ԃ����ÓI�ȕ�����l�ɂ��Đ�����܂��BGENERIC.xll ���ǂݍ��܂��ƁAGENERIC.xll �ɂ���Ă��̊֐����o�^����āA���[�N�V�[�g����Ăяo�����Ƃ��ł���悤�ɂȂ�܂��B</span><span class="sxs-lookup"><span data-stu-id="730d4-p101">Example user-defined worksheet function demonstrates the return of a static string value. When GENERIC.xll is loaded, it registers this function so that it can be called from the worksheet.</span></span>
  
```cs
LPXLOPER12 WINAPI Func1(LPXLOPER12 px);
```

## <a name="parameters"></a><span data-ttu-id="730d4-108">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="730d4-108">Parameters</span></span>

 <span data-ttu-id="730d4-109">_px_(**LPXLOPER**)</span><span class="sxs-lookup"><span data-stu-id="730d4-109">_px_ (**LPXLOPER**)</span></span>
  
<span data-ttu-id="730d4-110">���̈����͖�������AMicrosoft Excel ��g���K�[���Ċ֐���Ăяo�����߂����̖�ڂ�ʂ����܂��B</span><span class="sxs-lookup"><span data-stu-id="730d4-110">This argument is ignored, and serves only to trigger Microsoft Excel to call the function.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="730d4-111">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="730d4-111">Property value/Return value</span></span>

 <span data-ttu-id="730d4-112">**LPXLOPER12**:��ɕ����� "Func1"</span><span class="sxs-lookup"><span data-stu-id="730d4-112">**LPXLOPER12**: Always the string "Func1"</span></span>
  
### <a name="example"></a><span data-ttu-id="730d4-113">��</span><span class="sxs-lookup"><span data-stu-id="730d4-113">Example</span></span>

<span data-ttu-id="730d4-114">���̊֐��̃\�[�X �R�[�h�ɂ��ẮA `\SAMPLES\GENERIC\GENERIC.C` ��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="730d4-114">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="730d4-115">�֘A����</span><span class="sxs-lookup"><span data-stu-id="730d4-115">See also</span></span>



[<span data-ttu-id="730d4-116">�ėp DLL �̊֐�</span><span class="sxs-lookup"><span data-stu-id="730d4-116">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

