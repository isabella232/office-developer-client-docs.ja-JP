---
title: ConvertXLRef12ToXLRef
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- ConvertXLRef12ToXLRef
keywords:
- convertxlref12toxlref function [excel 2007]
localization_priority: Normal
ms.assetid: b620ed21-73ef-489b-9c00-7be12bb41214
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 826428edb57eba9e17d601164aa8b4b797fc8929
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798770"
---
# <a name="convertxlref12toxlref"></a><span data-ttu-id="e3706-104">ConvertXLRef12ToXLRef</span><span class="sxs-lookup"><span data-stu-id="e3706-104">ConvertXLRef12ToXLRef</span></span>

<span data-ttu-id="e3706-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e3706-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="e3706-106">**XLREF12** ���� **XLREF** �ւ̕ϊ�����s���܂��B</span><span class="sxs-lookup"><span data-stu-id="e3706-106">Tries to convert an **XLREF12** into an **XLREF**.</span></span>
  
```cs
BOOL ConvertXLRefToXLRef12(LPXLREF12 pxRef12, LPXLREF pxRef);
```

## <a name="parameters"></a><span data-ttu-id="e3706-107">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="e3706-107">Parameters</span></span>

 <span data-ttu-id="e3706-108">_pxRef12_(**LPXLREF12**)</span><span class="sxs-lookup"><span data-stu-id="e3706-108">_pxRef12_ (**LPXLREF12**)</span></span>
  
<span data-ttu-id="e3706-109">�\�[�X�̎Q�ƍ\���̂ւ̃|�C���^�[�B</span><span class="sxs-lookup"><span data-stu-id="e3706-109">Pointer to the source reference structure.</span></span>
  
 <span data-ttu-id="e3706-110">_pxRef_(**LPXLREF**)</span><span class="sxs-lookup"><span data-stu-id="e3706-110">_pxRef_ (**LPXLREF**)</span></span>
  
<span data-ttu-id="e3706-111">�ϊ������l���z�u�����^�[�Q�b�g�̎Q�ƍ\���̂ւ̃|�C���^�[�B</span><span class="sxs-lookup"><span data-stu-id="e3706-111">Pointer to the target reference structure into which the converted value is to be placed.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="e3706-112">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="e3706-112">Property value/Return value</span></span>

 <span data-ttu-id="e3706-113">�ϊ������������ꍇ�� **TRUE**�B����ȊO�̏ꍇ�� **FALSE**�B</span><span class="sxs-lookup"><span data-stu-id="e3706-113">**TRUE** if the conversion succeeded, **FALSE** otherwise.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e3706-114">����</span><span class="sxs-lookup"><span data-stu-id="e3706-114">Remarks</span></span>

<span data-ttu-id="e3706-115">�w�肵���Q�Ƃ��ȑO�̃o�[�W�����ł̓T�|�[�g����Ă��Ȃ� Excel 2007 ���[�N�V�[�g�̕�����Q�Ƃ��Ă���ꍇ�A **XLREF12** ���� **XLREF** �ւ̕ϊ��͎��s���܂��B</span><span class="sxs-lookup"><span data-stu-id="e3706-115">The conversion from **XLREF12** to **XLREF** fails if the supplied reference refers to part of a Excel 2007 worksheet that is not supported in earlier versions.</span></span> 
  
## <a name="example"></a><span data-ttu-id="e3706-116">��</span><span class="sxs-lookup"><span data-stu-id="e3706-116">Example</span></span>

 `\SAMPLES\FRAMEWRK\FRAMEWRK.C`
  
```cs
BOOL ConvertXLRef12ToXLRef(LPXLREF12 pxref12, LPXLREF pxref)
{
   if (pxref12->rwLast >= pxref12->rwFirst && pxref12->colLast >= pxref12->colFirst)
   {
      if (pxref12->rwFirst >=0 && pxref12->colFirst >= 0)
      {
         if (pxref12->rwLast < rwMaxO8 && pxref12->colLast < colMaxO8)
         {
            pxref->rwFirst = (WORD)pxref12->rwFirst;
            pxref->rwLast = (WORD)pxref12->rwLast;
            pxref->colFirst = (BYTE)pxref12->colFirst;
            pxref->colLast = (BYTE)pxref12->colLast;
            return TRUE;
         }
      }
   }
   return FALSE;
}
```

## <a name="see-also"></a><span data-ttu-id="e3706-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="e3706-117">See also</span></span>



<span data-ttu-id="e3706-118">[�t���[�����[�N ���C�u�����̊֐�](functions-in-the-framework-library.md)</span><span class="sxs-lookup"><span data-stu-id="e3706-118">[Functions in the Framework Library](functions-in-the-framework-library.md)</span></span>

