---
title: fDance
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fDance
keywords:
- fdance function [excel 2007]
localization_priority: Normal
ms.assetid: 8c2f2d83-b7aa-456e-b473-a54897bc35ae
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: b7a2fbdf723d06dcf9b02789178d7d12d0515884
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798883"
---
# <a name="fdance"></a><span data-ttu-id="67c48-104">fDance</span><span class="sxs-lookup"><span data-stu-id="67c48-104">fDance</span></span>

 <span data-ttu-id="67c48-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="67c48-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="67c48-p101">���[�U�[�� ** [ESC] ** ������܂ŁA��ƒ��̃��[�N�V�[�g�̑I��Z����ύX���郆�[�U�[��**** ���j���[ [Generic] ��쐬���܂��B</span><span class="sxs-lookup"><span data-stu-id="67c48-p101">Example user-defined command that changes the selected cells on the active worksheet around until the user presses **ESC**. When GENERIC.xll is loaded, it creates a user-defined menu, Generic, through which this command is accessed.</span></span>
  
```cs
int WINAPI fDance(void);
```

## <a name="parameters"></a><span data-ttu-id="67c48-108">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="67c48-108">Parameters</span></span>

<span data-ttu-id="67c48-109">���̊֐��ɂ̓p�����[�^�[�͂���܂���B</span><span class="sxs-lookup"><span data-stu-id="67c48-109">The function takes no parameters.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="67c48-110">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="67c48-110">Property value/Return value</span></span>

<span data-ttu-id="67c48-111">���̊֐��́A��� 1 ��Ԃ��܂��B</span><span class="sxs-lookup"><span data-stu-id="67c48-111">The function always returns 1.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="67c48-112">����</span><span class="sxs-lookup"><span data-stu-id="67c48-112">Remarks</span></span>

<span data-ttu-id="67c48-p102">����͎��Ԃ̂����鑀��̈��ł��B�֐� [xlAbort](xlabort.md) ��Ăяo�����Ƃ����܂��B����� (�����I�}���\`�^�X�L���O��x������) �v���Z�b�T�𐶐����A���[�U�[�� **[Esc]** ������đ��������������ǂ�����m�F���܂��B�{�^���������ꂽ�ꍇ�́A���[�U�[�����~�����L�����Z���ł���悤�ɂ��܂��B</span><span class="sxs-lookup"><span data-stu-id="67c48-p102">This is an example of a lengthy operation. It calls the function [xlAbort](xlabort.md) occasionally. This yields the processor (helping with cooperative multitasking), and checks whether the user has pressed **ESC** to cancel the operation. If so, it offers the user a chance to cancel the abort.</span></span> 
  
### <a name="example"></a><span data-ttu-id="67c48-117">��</span><span class="sxs-lookup"><span data-stu-id="67c48-117">Example</span></span>

<span data-ttu-id="67c48-118">���̊֐��̃\�[�X �R�[�h�ɂ��ẮA `\SAMPLES\GENERIC\GENERIC.C` ��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="67c48-118">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="67c48-119">�֘A����</span><span class="sxs-lookup"><span data-stu-id="67c48-119">See also</span></span>



[<span data-ttu-id="67c48-120">�ėp DLL �̊֐�</span><span class="sxs-lookup"><span data-stu-id="67c48-120">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

