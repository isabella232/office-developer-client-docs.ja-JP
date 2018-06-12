---
title: XLOperToXLOper12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- XLOperToXLOper12
keywords:
- xlopertoxloper12 function [excel 2007]
localization_priority: Normal
ms.assetid: b2d4581b-ebf6-4eba-aa95-69a5a9ee8028
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 76c78e5a2ad62b1a3d1aa23748b10e49e07f6543
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799008"
---
# <a name="xlopertoxloper12"></a><span data-ttu-id="3c239-104">XLOperToXLOper12</span><span class="sxs-lookup"><span data-stu-id="3c239-104">XLOperToXLOper12</span></span>

<span data-ttu-id="3c239-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="3c239-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="3c239-106">�Â� **XLOPER** ����V���� **XLOPER12** �ւ̕ϊ��Ɏg�p����ϊ����[�\`���ł��B</span><span class="sxs-lookup"><span data-stu-id="3c239-106">Conversion routine used to convert from the old **XLOPER** to the new **XLOPER12**.</span></span>
  
```cs
BOOL XLOperToXLOper12(LPXLOPER pxloper, LPXLOPER12 pxloper12);
```

## <a name="parameters"></a><span data-ttu-id="3c239-107">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="3c239-107">Parameters</span></span>

<span data-ttu-id="3c239-108">_pxloper_(**LPXLOPER**)</span><span class="sxs-lookup"><span data-stu-id="3c239-108">_pxloper_ (**LPXLOPER**)</span></span>
  
<span data-ttu-id="3c239-109">�ϊ��Ώۂ̃\�[�X **XLOPER** �ւ̃|�C���^�[�B</span><span class="sxs-lookup"><span data-stu-id="3c239-109">Pointer to the source **XLOPER** to be converted.</span></span> 
  
<span data-ttu-id="3c239-110">_pxloper12_(**LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="3c239-110">_pxloper12_ (**LPXLOPER12**)</span></span>
  
<span data-ttu-id="3c239-111">�ϊ����ꂽ�l��i�[����^�[�Q�b�g **XLOPER12** �ւ̃|�C���^�[�B</span><span class="sxs-lookup"><span data-stu-id="3c239-111">Pointer to the target **XLOPER12** to contain the converted value.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="3c239-112">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="3c239-112">Property value/Return value</span></span>

<span data-ttu-id="3c239-113">�ϊ������������ꍇ�� **TRUE**�B����ȊO�̏ꍇ�� **FALSE**�B</span><span class="sxs-lookup"><span data-stu-id="3c239-113">**TRUE** if the conversion succeeded, **FALSE** otherwise.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="3c239-114">����</span><span class="sxs-lookup"><span data-stu-id="3c239-114">Remarks</span></span>

<span data-ttu-id="3c239-p101">**XLOPER** �̌^�ɉ����āA�ϊ������l�ɐV���������� �o�b�t�@�[����蓖�Ă܂��B�^�[�Q�b�g **XLOPER12** �́A���̃o�b�t�@�[��|�C���g���܂��B�ϊ��ɐ��������ꍇ�́A�R�s�[�Ɋ֘A�t����ꂽ��������Ăяo�����ŉ������K�v������܂��B **FreeXLOper12T** ��g�p���邱�Ƃ�A **free** ��g�p���Ē��ډ�����邱�Ƃ�ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="3c239-p101">Depending on the type of the **XLOPER**, this function allocates a new memory buffer for the converted values, which are pointed to in the target **XLOPER12**. The caller is responsible for freeing any memory associated with the copy if the conversion is a success; **FreeXLOper12T** can be used, or it can be done directly using **free**.</span></span>
  
<span data-ttu-id="3c239-117">�ϊ������s�����ꍇ�́A�Ăяo�����Ń�������������K�v�͂���܂���B</span><span class="sxs-lookup"><span data-stu-id="3c239-117">If the conversion fails, the caller does not need to free any memory.</span></span>
  
<span data-ttu-id="3c239-p102">��ʂɁA�C�ӂ� **XLOPER** ���� **XLOPER12** �ւ̕ϊ����\�ł��B����ɑ΂��āA **XLOPER12** ���� **XLOPER** �ւ̕ϊ��́A **XLOPER** �Ɏ��܂肫��Ȃ��قǑ傫���z���Q�ƁA�܂��͒��������� **XLOPER12** �Ɋi�[����Ă���ƁA���s���邱�Ƃ�����܂�</span><span class="sxs-lookup"><span data-stu-id="3c239-p102">In general, conversion from any **XLOPER** to an **XLOPER12** is possible. In contrast, conversion from an **XLOPER12** to an **XLOPER** can fail when the **XLOPER12** contains an array or reference that is too large or a string that is too long for the **XLOPER** to contain.</span></span> 
  
<span data-ttu-id="3c239-120">**XLOPER** �� ASCII �o�C�g������́A���P�[���Ɉˑ�������@�� **XLOPER12** �� Unicode ���C�h����������ɕϊ�����܂��B</span><span class="sxs-lookup"><span data-stu-id="3c239-120">**XLOPER** ASCII byte strings are converted to **XLOPER12** Unicode wide-character strings in a way that is locale-dependent.</span></span> 
  
### <a name="example"></a><span data-ttu-id="3c239-121">��</span><span class="sxs-lookup"><span data-stu-id="3c239-121">Example</span></span>

<span data-ttu-id="3c239-122">���̊֐��̃R�[�h�ɂ��ẮA�t�@�C��  `\SAMPLES\FRAMEWRK\FRAMEWRK.C` ��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="3c239-122">See the file  `\SAMPLES\FRAMEWRK\FRAMEWRK.C` for the code for this function.</span></span> 
  

