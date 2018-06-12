---
title: ConvertXLRefToXLRef12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- ConvertXLRefToXLRef12
keywords:
- convertxlreftoxlref12 function [excel 2007]
localization_priority: Normal
ms.assetid: 94580044-9497-425f-a31e-53bb4d94dc30
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: f2830633482e5329d285907b610386b708c406a4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798777"
---
# <a name="convertxlreftoxlref12"></a><span data-ttu-id="71756-104">ConvertXLRefToXLRef12</span><span class="sxs-lookup"><span data-stu-id="71756-104">ConvertXLRefToXLRef12</span></span>

<span data-ttu-id="71756-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="71756-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="71756-106">**XLREF** �� **XLREF12** �ɕϊ����悤�Ƃ��� Framework �֐��B</span><span class="sxs-lookup"><span data-stu-id="71756-106">Framework function that attempts to convert an **XLREF** into an **XLREF12**.</span></span>
  
```cs
BOOL ConvertXLRefToXLRef12(LPXLREF pxRef, LPXLREF12 pxRef12);
```

## <a name="parameters"></a><span data-ttu-id="71756-107">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="71756-107">Parameters</span></span>

 <span data-ttu-id="71756-108">_pxRef_(**LPXLREF**)</span><span class="sxs-lookup"><span data-stu-id="71756-108">_pxRef_ (**LPXLREF**)</span></span>
  
<span data-ttu-id="71756-109">�\�[�X�̎Q�ƍ\���̂ւ̃|�C���^�[�B</span><span class="sxs-lookup"><span data-stu-id="71756-109">Pointer to the source reference structure.</span></span>
  
 <span data-ttu-id="71756-110">_pxRef12_(**LPXLREF12**)</span><span class="sxs-lookup"><span data-stu-id="71756-110">_pxRef12_ (**LPXLREF12**)</span></span>
  
<span data-ttu-id="71756-111">�ϊ������l���z�u�����^�[�Q�b�g�̎Q�ƍ\���̂ւ̃|�C���^�[�B</span><span class="sxs-lookup"><span data-stu-id="71756-111">Pointer to the target reference structure into which the converted value is to be placed.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="71756-112">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="71756-112">Property value/Return value</span></span>

 <span data-ttu-id="71756-113">�ϊ������������ꍇ�� **TRUE**�B����ȊO�̏ꍇ�� **FALSE**�B</span><span class="sxs-lookup"><span data-stu-id="71756-113">**TRUE** if the conversion succeeded, **FALSE** otherwise.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="71756-114">����</span><span class="sxs-lookup"><span data-stu-id="71756-114">Remarks</span></span>

<span data-ttu-id="71756-p101">�n���ꂽ **XLREF** ���L���ȏꍇ�́A���̑���͏�ɐ�������͂��ł��B���΂ɁA�������ꂽ�Q�Ƃ��ȑO�̃o�[�W�����ŃT�|�[�g����Ă��Ȃ� Excel 2007 ���[�N�V�[�g�̈ꕔ��Q�Ƃ��Ă���ꍇ�́A **ConvertXLRef12ToXLRef** ���s�� **XLREF12** ���� [XLREF](convertxlref12toxlref.md) �ւ̕ϊ��͎��s���܂��B</span><span class="sxs-lookup"><span data-stu-id="71756-p101">Provided that the passed-in **XLREF** is valid, this operation should always be successful. In contrast, conversion the other way from **XLREF12** to **XLREF**, performed by [ConvertXLRef12ToXLRef](convertxlref12toxlref.md), fails if the supplied reference refers to part of an Excel 2007 worksheet that is not supported in earlier versions.</span></span>
  
## <a name="example"></a><span data-ttu-id="71756-117">��</span><span class="sxs-lookup"><span data-stu-id="71756-117">Example</span></span>

 `\SAMPLES\FRAMEWRK\FRAMEWRK.C`
  
```cs
BOOL ConvertXLRefToXLRef12(LPXLREF pxref, LPXLREF12 pxref12)
{
   if (pxref->rwLast >= pxref->rwFirst && pxref->colLast >= pxref->colFirst)
   {
      if (pxref->rwFirst >= 0 && pxref->colFirst >= 0)
      {
         pxref12->rwFirst = pxref->rwFirst;
         pxref12->rwLast = pxref->rwLast;
         pxref12->colFirst = pxref->colFirst;
         pxref12->colLast = pxref->colLast;
         return TRUE;
      }
   }
   return FALSE;
}
```

## <a name="see-also"></a><span data-ttu-id="71756-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="71756-118">See also</span></span>



<span data-ttu-id="71756-119">[�t���[�����[�N ���C�u�����̊֐�](functions-in-the-framework-library.md)</span><span class="sxs-lookup"><span data-stu-id="71756-119">[Functions in the Framework Library](functions-in-the-framework-library.md)</span></span>

