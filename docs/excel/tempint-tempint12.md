---
title: TempInt/TempInt12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempInt
- TempInt12
keywords:
- tempint12 function [excel 2007],TempInt function [Excel 2007]
localization_priority: Normal
ms.assetid: 86d690b8-caca-450d-93f7-69ca4cd1a6e0
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: eb1dd9be0c0b20e533d9cd8202f8878c43b997be
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798952"
---
# <a name="tempinttempint12"></a><span data-ttu-id="ceed7-104">TempInt/TempInt12</span><span class="sxs-lookup"><span data-stu-id="ceed7-104">TempInt/TempInt12</span></span>

 <span data-ttu-id="ceed7-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="ceed7-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="ceed7-106">������܂ވꎞ **XLOPER**/ **XLOPER12** ��쐬����t���[�����[�N ���C�u�����֐��B</span><span class="sxs-lookup"><span data-stu-id="ceed7-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** that contains an integer.</span></span> 
  
```cs
LPXLOPER TempInt(short int i);
LPXLOPER12 TempInt12(int i);
```

## <a name="parameters"></a><span data-ttu-id="ceed7-107">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="ceed7-107">Parameters</span></span>

 <span data-ttu-id="ceed7-108">_i_</span><span class="sxs-lookup"><span data-stu-id="ceed7-108">_i_</span></span>
  
<span data-ttu-id="ceed7-p101">�Ώۂ̐����l�B **XLOPER** �����́A�����t�� 16 �r�b�g���� (short int) �ł���̂ɑ΂��A **XLOPER12** �����́A�����t�� 32 �r�b�g���� ([long] int) �ł��邱�Ƃɂ����ӂ��������B</span><span class="sxs-lookup"><span data-stu-id="ceed7-p101">The intended integer value. Note that the **XLOPER** integer is a signed 16-bit integer (short int), whereas the **XLOPER12** integer is a signed 32-bit integer ([long] int).</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="ceed7-111">�߂�l</span><span class="sxs-lookup"><span data-stu-id="ceed7-111">Return value</span></span>

<span data-ttu-id="ceed7-112">�n���ꂽ�l��܂� **xltypeInt** ������Ԃ��܂��B</span><span class="sxs-lookup"><span data-stu-id="ceed7-112">Returns an **xltypeInt** integer containing the value passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="ceed7-113">��</span><span class="sxs-lookup"><span data-stu-id="ceed7-113">Example</span></span>

<span data-ttu-id="ceed7-114">���̗�ł́A **TempInt12** �֐���g�p���āA **xlfGetWorkspace** �Ɉ�����n���Ă��܂��B</span><span class="sxs-lookup"><span data-stu-id="ceed7-114">This example uses the **TempInt12** function to pass an argument to **xlfGetWorkspace**.</span></span>
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempIntExample(void)
{
    XLOPER12 xRes;
    Excel12f(xlfGetWorkspace, (LPXLOPER12)&xRes, 1, TempInt12(44));
    Excel12f(xlFree, 0, 1, (LPXLOPER12)&xRes);
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="ceed7-115">�֘A����</span><span class="sxs-lookup"><span data-stu-id="ceed7-115">See also</span></span>



<span data-ttu-id="ceed7-116">[�t���[�����[�N ���C�u�����̊֐�](functions-in-the-framework-library.md)</span><span class="sxs-lookup"><span data-stu-id="ceed7-116">[Functions in the Framework Library](functions-in-the-framework-library.md)</span></span>

