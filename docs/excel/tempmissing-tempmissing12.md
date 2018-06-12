---
title: TempMissing/TempMissing12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempMissing
- TempMissing12
keywords:
- tempmissing function [excel 2007],TempMissing12 function [Excel 2007]
localization_priority: Normal
ms.assetid: d9cb6afc-1fbb-45d6-88e5-84eba3af3c60
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: a6db2e1f2917ecd9361043577f4bf203b3267a5c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798953"
---
# <a name="tempmissingtempmissing12"></a><span data-ttu-id="5f3d2-104">TempMissing/TempMissing12</span><span class="sxs-lookup"><span data-stu-id="5f3d2-104">TempMissing/TempMissing12</span></span>

 <span data-ttu-id="5f3d2-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="5f3d2-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="5f3d2-106">�^�C�v **xltypeMissing** �̈ꎞ / ******XLOPER12** ��쐬����t���[�����[�N ���C�u�����֐��B</span><span class="sxs-lookup"><span data-stu-id="5f3d2-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** of type **xltypeMissing**.</span></span>
  
```cs
LPXLOPER TempMissing(void);
LPXLOPER12 TempMissing12(void);
```

## <a name="parameters"></a><span data-ttu-id="5f3d2-107">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="5f3d2-107">Parameters</span></span>

<span data-ttu-id="5f3d2-108">���̊֐��Ƀp�����[�^�[�͂���܂���B</span><span class="sxs-lookup"><span data-stu-id="5f3d2-108">This function takes no parameters.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="5f3d2-109">�߂�l</span><span class="sxs-lookup"><span data-stu-id="5f3d2-109">Return value</span></span>

<span data-ttu-id="5f3d2-110">**xltypeMissing** **XLOPER**/ **XLOPER12** �Ƀ|�C���^�[��Ԃ��܂��B</span><span class="sxs-lookup"><span data-stu-id="5f3d2-110">Returns a pointer to an **xltypeMissing** **XLOPER**/ **XLOPER12**.</span></span>
  
## <a name="example"></a><span data-ttu-id="5f3d2-111">��</span><span class="sxs-lookup"><span data-stu-id="5f3d2-111">Example</span></span>

<span data-ttu-id="5f3d2-p101">���̗�ł� **TempMissing12** ��g�p���� 3 �̕s������������ **xlcWorkspace** �Ɏw�肵�A���̌�� **Boolean** **FALSE** ��w�肵�āA���[�N�V�[�g�̃X�N���[�� �o�[�̕\�����\���ɂ��܂��B�ŏ��� 3 �̈����́A�e����󂯂Ȃ����̃��[�N�X�y�[�X�ݒ�ɑΉ����܂��B</span><span class="sxs-lookup"><span data-stu-id="5f3d2-p101">This example uses **TempMissing12** to provide three missing arguments to **xlcWorkspace** followed by a **Boolean** **FALSE** to suppress the display of worksheet scroll bars. The first three arguments correspond to other workspace settings which are unaffected.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempMissingExample(void)
{
   XLOPER12 xBool;
   xBool.xltype = xltypeBool;
   xBool.val.xbool = 0;
   Excel12f(xlcWorkspace, 0, 4, TempMissing12(), TempMissing12(),
      TempMissing12(), (LPXLOPER12)&xBool);
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="5f3d2-114">�֘A����</span><span class="sxs-lookup"><span data-stu-id="5f3d2-114">See also</span></span>



<span data-ttu-id="5f3d2-115">[�t���[�����[�N ���C�u�����̊֐�](functions-in-the-framework-library.md)</span><span class="sxs-lookup"><span data-stu-id="5f3d2-115">[Functions in the Framework Library](functions-in-the-framework-library.md)</span></span>

