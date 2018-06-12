---
title: TempNum/TempNum12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempNum
- TempNum12
keywords:
- tempnum12 function [excel 2007],TempNum function [Excel 2007]
localization_priority: Normal
ms.assetid: 5b74d618-db3a-4d84-bd17-4fee7ae3b51e
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 5ebe58dba32c2cf0382bf0811713eaa0a5471dda
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798949"
---
# <a name="tempnumtempnum12"></a><span data-ttu-id="97619-104">TempNum/TempNum12</span><span class="sxs-lookup"><span data-stu-id="97619-104">TempNum/TempNum12</span></span>

 <span data-ttu-id="97619-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="97619-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="97619-106">Microsoft Excel ���[�N�V�[�g�̔ԍ���܂ވꎞ **XLOPER**/ **XLOPER12** ��쐬����t���[�����[�N ���C�u�����֐� (IEEE 8 �o�C�g�̔{���x���������_�^)�B</span><span class="sxs-lookup"><span data-stu-id="97619-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** containing a Microsoft Excel worksheet number (an IEEE 8-byte double).</span></span> 
  
```cs
LPXLOPER TempNum(double d);
LPXLOPER12 TempNum12(double d);
```

## <a name="parameters"></a><span data-ttu-id="97619-107">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="97619-107">Parameters</span></span>

 <span data-ttu-id="97619-108">_d_ (**ダブル**)</span><span class="sxs-lookup"><span data-stu-id="97619-108">_d_ (**double**)</span></span>
  
<span data-ttu-id="97619-p101">�z��l�BIEEE �K�i�̔񐳋K���͌��݃T�|�[�g����Ă��Ȃ����߁A�[���Ɋۂ߂��܂��B���̖�����ɑΉ����Ă��܂��B</span><span class="sxs-lookup"><span data-stu-id="97619-p101">The intended value. Note that IEEE sub-normal numbers are not currently supported and are rounded to zero. Negative infinity is supported.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="97619-112">�߂�l</span><span class="sxs-lookup"><span data-stu-id="97619-112">Return value</span></span>

<span data-ttu-id="97619-113">�n�����l��܂ސ��l **xltypeNum**�B�܂��́A�񐳋K�����l�ɓn���ꂽ�ꍇ�̓[����Ԃ��܂��B</span><span class="sxs-lookup"><span data-stu-id="97619-113">Returns a numeric **xltypeNum** containing the value passed in or zero if the passed in value was sub-normal.</span></span> 
  
## <a name="example"></a><span data-ttu-id="97619-114">��</span><span class="sxs-lookup"><span data-stu-id="97619-114">Example</span></span>

<span data-ttu-id="97619-115">���̗�ł́A **TempNum12** �֐���g�p���āA **xlfGetWorkspace** �Ɉ�����n���Ă��܂��B</span><span class="sxs-lookup"><span data-stu-id="97619-115">This example uses the **TempNum12** function to pass an argument to **xlfGetWorkspace**.</span></span>
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempNumExample(void)
{
   XLOPER12 xRes;
   Excel12f(xlfGetWorkspace, &xRes, 1, TempNum12(44));
   Excel12f(xlFree, 0, 1, (LPXLOPER12)&xRes);
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="97619-116">�֘A����</span><span class="sxs-lookup"><span data-stu-id="97619-116">See also</span></span>



<span data-ttu-id="97619-117">[�t���[�����[�N ���C�u�����̊֐�](functions-in-the-framework-library.md)</span><span class="sxs-lookup"><span data-stu-id="97619-117">[Functions in the Framework Library](functions-in-the-framework-library.md)</span></span>

