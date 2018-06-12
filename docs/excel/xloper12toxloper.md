---
title: XLOper12ToXLOper
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- XLOper12ToXLOper
keywords:
- xloper12toxloper function [excel 2007]
localization_priority: Normal
ms.assetid: b46f87c4-778b-4502-be57-c3725f73a644
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 2c06102699db8810da803ecc0ddfa30375fcc125
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798993"
---
# <a name="xloper12toxloper"></a><span data-ttu-id="d1687-104">XLOper12ToXLOper</span><span class="sxs-lookup"><span data-stu-id="d1687-104">XLOper12ToXLOper</span></span>

<span data-ttu-id="d1687-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d1687-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="d1687-106">�V���� **XLOPER12** ����Â� **XLOPER** �ւ̕ϊ��Ɏg�p����ϊ����[�\`���ł��B</span><span class="sxs-lookup"><span data-stu-id="d1687-106">Conversion routine used to convert from the new **XLOPER12** to the old **XLOPER**.</span></span>
  
```cs
BOOL XLOper12ToXLOper(LPXLOPER12 pxloper12, LPXLOPER pxloper);
```

## <a name="parameters"></a><span data-ttu-id="d1687-107">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="d1687-107">Parameters</span></span>

<span data-ttu-id="d1687-108">_pxloper12_(**LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="d1687-108">_pxloper12_ (**LPXLOPER12**)</span></span>
  
<span data-ttu-id="d1687-109">�ϊ��Ώۂ̃\�[�X **XLOPER12** �ւ̃|�C���^�[�B</span><span class="sxs-lookup"><span data-stu-id="d1687-109">Pointer to the source **XLOPER12** to be converted.</span></span> 
  
<span data-ttu-id="d1687-110">_pxloper_(**LPXLOPER**)</span><span class="sxs-lookup"><span data-stu-id="d1687-110">_pxloper_ (**LPXLOPER**)</span></span>
  
<span data-ttu-id="d1687-111">�ϊ����ꂽ�l��i�[����^�[�Q�b�g **XLOPER** �ւ̃|�C���^�[�B</span><span class="sxs-lookup"><span data-stu-id="d1687-111">Pointer to the target **XLOPER** to contain the converted value.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="d1687-112">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="d1687-112">Property value/Return value</span></span>

<span data-ttu-id="d1687-113">�ϊ������������ꍇ�� **TRUE**�B����ȊO�̏ꍇ�� **FALSE**�B</span><span class="sxs-lookup"><span data-stu-id="d1687-113">**TRUE** if the conversion succeeded, **FALSE** otherwise.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d1687-114">����</span><span class="sxs-lookup"><span data-stu-id="d1687-114">Remarks</span></span>

<span data-ttu-id="d1687-p101">**XLOPER12** �̌^�ɉ����āA�ϊ������l�ɐV���������� �o�b�t�@�[����蓖�Ă܂��B�^�[�Q�b�g **XLOPER** �́A���̃o�b�t�@�[��|�C���g���܂��B�ϊ��ɐ��������ꍇ�́A�R�s�[�Ɋ֘A�t����ꂽ��������Ăяo�����ŉ������K�v������܂��B **FreeXLOperT** ��g�p���邱�Ƃ�A **free** ��g�p���Ē��ډ�����邱�Ƃ�ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="d1687-p101">Depending on the type of the **XLOPER12**, this function allocates a new memory buffer for the converted values, which are pointed to in the target **XLOPER**. The caller is responsible for freeing any memory associated with the copy if the conversion is a success; **FreeXLOperT** can be used, or it can be done directly by using **free**.</span></span>
  
<span data-ttu-id="d1687-117">�ϊ������s�����ꍇ�́A�Ăяo�����Ń�������������K�v�͂���܂���B</span><span class="sxs-lookup"><span data-stu-id="d1687-117">If the conversion fails, the caller does not need to free any memory.</span></span>
  
<span data-ttu-id="d1687-118">**XLOPER12** ���� **XLOPER** �ւ̕ϊ��́A **XLOPER** �Ɏ��܂肫��Ȃ��قǑ傫���z���Q�ƁA�܂��͒��������� **XLOPER12** �Ɋi�[����Ă���ƁA���s���邱�Ƃ�����܂�</span><span class="sxs-lookup"><span data-stu-id="d1687-118">Conversion from an **XLOPER12** to an **XLOPER** can fail when the **XLOPER12** contains an array or reference that is too large or a string that is too long for the **XLOPER** to contain.</span></span> 
  
<span data-ttu-id="d1687-119">**XLOPER12** �� Unicode ���C�h����������́A���P�[���Ɉˑ�������@�� **XLOPER** �� ASCII �o�C�g������ɕϊ�����܂��B</span><span class="sxs-lookup"><span data-stu-id="d1687-119">**XLOPER12** Unicode wide-character strings are converted to **XLOPER** ASCII byte strings in a way that is locale-dependent.</span></span> 
  
<span data-ttu-id="d1687-p102">**XLOPER12** **xltypeInt** �� 32 �r�b�g�����t�������ł��B **XLOPER** **xltypeInt** �� 16 �r�b�g�����t�������ł��B�w�肳�ꂽ **XLOPER12** ������ **XLOPER** �����̐����𒴂���ꍇ�́A���̐����� 8 �o�C�g�� double �ɕϊ�����A **xltypeNum** �^�� **XLOPER** �ŕԂ���܂��B���̏ꍇ�ɂ̂݁A���̊֐��͕ϊ����� **XLOPER** �̌^��ύX���܂��B</span><span class="sxs-lookup"><span data-stu-id="d1687-p102">The **XLOPER12** **xltypeInt** is a 32-bit signed integer, whereas the **XLOPER** **xltypeInt** is a 16-bit signed integer. When a supplied **XLOPER12** integer exceeds the limit of an **XLOPER** integer, the integer is converted to an 8-byte double and returned in an **XLOPER** of type **xltypeNum**. This is the only case in which this function changes the type of the converted **XLOPER**.</span></span>
  
### <a name="example"></a><span data-ttu-id="d1687-123">��</span><span class="sxs-lookup"><span data-stu-id="d1687-123">Example</span></span>

<span data-ttu-id="d1687-124">���̊֐��̃R�[�h�ɂ��ẮA�t�@�C��  `\SAMPLES\FRAMEWRK\FRAMEWRK.C` ��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="d1687-124">See the file  `\SAMPLES\FRAMEWRK\FRAMEWRK.C` for the code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d1687-125">�֘A����</span><span class="sxs-lookup"><span data-stu-id="d1687-125">See also</span></span>

- <span data-ttu-id="d1687-126">[�t���[�����[�N ���C�u�����̊֐�](functions-in-the-framework-library.md)</span><span class="sxs-lookup"><span data-stu-id="d1687-126">[Functions in the Framework Library](functions-in-the-framework-library.md)</span></span>

