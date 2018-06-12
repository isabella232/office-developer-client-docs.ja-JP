---
title: xlAddInManagerInfo/xlAddInManagerInfo12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAddInManagerInfo
keywords:
- xladdinmanagerinfo function [excel 2007]
localization_priority: Normal
ms.assetid: 63a73cd2-6479-4233-ad68-93379f940717
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: e42cca809c4426ddf9a98b3b275d08490d31c8db
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798950"
---
# <a name="xladdinmanagerinfoxladdinmanagerinfo12"></a><span data-ttu-id="3b2bb-104">xlAddInManagerInfo/xlAddInManagerInfo12</span><span class="sxs-lookup"><span data-stu-id="3b2bb-104">xlAddInManagerInfo/xlAddInManagerInfo12</span></span>

 <span data-ttu-id="3b2bb-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="3b2bb-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="3b2bb-p101">�A�h�C�� �}�l�[�W���[�� Excel �Z�b�V�����ŏ��߂ČĂяo���ꂽ�Ƃ��ɁAMicrosoft Excel �ɂ���ČĂяo����܂��B���̊֐��́A���g�p�̃A�h�C���ɂ��Ă̏���A�h�C�� �}�l�[�W���[�ɒ񋟂��邽�߂Ɏg�p����܂��B</span><span class="sxs-lookup"><span data-stu-id="3b2bb-p101">Called by Microsoft Excel when the Add-in Manager is invoked for the first time in an Excel session. This function is used to provide the Add-In Manager with information about your add-in.</span></span>
  
<span data-ttu-id="3b2bb-p102">Excel 2007 �ȍ~�̃o�[�W�����ł́AXLL �ɂ���ăG�N�X�|�[�g�����ꍇ�ɂ� **xlAddInManagerInfo** �ł͂Ȃ� **xlAddInManagerInfo12** ���Ăяo����܂��B **xlAddInManagerInfo12** �֐��́A **xlAddInManagerInfo** �Ɠ����悤�ɋ@�\���āAXLL �̓���ɂ�����o�[�W�����ŗL�̑���_�������K�v������܂��BExcel �ł́A **xlAddInManagerInfo12** �� **XLOPER12** �f�[�^�^��Ԃ��A **xlAddInManagerInfo** �� **XLOPER** �f�[�^�^��Ԃ��K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="3b2bb-p102">Excel 2007 and later versions call **xlAddInManagerInfo12** in preference to **xlAddInManagerInfo** if exported by the XLL. The **xlAddInManagerInfo12** function should work in the same way as **xlAddInManagerInfo** to avoid version-specific differences in the behavior of the XLL. Excel expects **xlAddInManagerInfo12** to return an **XLOPER12** data type, whereas **xlAddInManagerInfo** should return an **XLOPER**.</span></span>
  
<span data-ttu-id="3b2bb-111">**xlAddInManagerInfo12** �֐��� Excel 2007 ���O�� Excel �o�[�W�����ł͌Ăяo����܂���B **XLOPER12** ��T�|�[�g���Ă��Ȃ����߂ł��B</span><span class="sxs-lookup"><span data-stu-id="3b2bb-111">The **xlAddInManagerInfo12** function is not called by versions of Excel earlier than Excel 2007, as these do not support the **XLOPER12**.</span></span>
  
<span data-ttu-id="3b2bb-112">Excel �ł́AXLL ������炢���ꂩ�̊֐���������ăG�N�X�|�[�g���邱�Ƃ͕s�v�ł��B</span><span class="sxs-lookup"><span data-stu-id="3b2bb-112">Excel does not require an XLL to implement and export either of these functions.</span></span>
  
```cs
LPXLOPER WINAPI xlAddInManagerInfo(LPXLOPER pxAction);
LPXLOPER12 WINAPI xlAddInManagerInfo12(LPXLOPER12 pxAction);
```

## <a name="parameters"></a><span data-ttu-id="3b2bb-113">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="3b2bb-113">Parameters</span></span>

 <span data-ttu-id="3b2bb-114">_pxAction:_ 数値**XLOPER または XLOPER12** (**xltypeInt**または**xltypeNum**) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="3b2bb-114">_pxAction:_ A pointer to a numeric **XLOPER/XLOPER12** (**xltypeInt** or **xltypeNum**).</span></span>
  
<span data-ttu-id="3b2bb-115">Excel �ŗv���������ł��B</span><span class="sxs-lookup"><span data-stu-id="3b2bb-115">The information that Excel is asking for.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="3b2bb-116">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="3b2bb-116">Property value/Return value</span></span>

<span data-ttu-id="3b2bb-p103">_pxAction_ �����l 1 �̏ꍇ (1 �ɂȂ�悤�������邱�Ƃ�ł��܂�)�A���̊֐����������ƁA�A�h�C���ɂ��Ă̏�� (�ʏ�͖��O�B�o�[�W�����ԍ����܂܂�邱�Ƃ����܂�) ���܂܂�镶���񂪕Ԃ�܂��B����ȊO�̏ꍇ�A#VALUE ��Ԃ��܂��B</span><span class="sxs-lookup"><span data-stu-id="3b2bb-p103">If  _pxAction_ is, or can be coerced to, the number 1, then your implementation of this function should return a string containing some information about the add-in, typically its name and perhaps a version number. Otherwise it should return #VALUE!.</span></span> 
  
<span data-ttu-id="3b2bb-119">�������Ԃ��Ȃ��ꍇ�AExcel ���߂�l�𕶎���ɕϊ����悤�Ƃ��܂��B</span><span class="sxs-lookup"><span data-stu-id="3b2bb-119">If you do not return a string, Excel tries to convert the returned value to a string.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3b2bb-120">����</span><span class="sxs-lookup"><span data-stu-id="3b2bb-120">Remarks</span></span>

<span data-ttu-id="3b2bb-p104">�Ԃ���镶���񂪁A���I�Ɋ��蓖�Ă�ꂽ�o�b�t�@�[��|�C���g���Ă���ꍇ�́A���̃o�b�t�@�[��ŏI�I�ɉ������K�v������܂��B������ Excel �ɂ���Ċ��蓖�Ă�ꂽ�ꍇ�A **xlbitXLFree** ��ݒ肵�ĉ�����܂��B������ DLL �ɂ���Ċ��蓖�Ă�ꂽ�ꍇ�ɂ́A **xlbitDLLFree** ��ݒ肵�ĉ�����܂��B����ɁA [xlAutoFree](xlautofree-xlautofree12.md) ( **XLOPER** ��Ԃ��ꍇ) �܂��� **xlAutoFree12** ( **XLOPER12** ��Ԃ��ꍇ) ��������Ȃ���΂Ȃ�܂���B</span><span class="sxs-lookup"><span data-stu-id="3b2bb-p104">If the returned string points to dynamically allocated buffer, you must make sure that this buffer is eventually freed. If the string was allocated by Excel, you do this by setting **xlbitXLFree**. If the string was allocated by the DLL, you do this by setting **xlbitDLLFree**, and you must also implement in [xlAutoFree](xlautofree-xlautofree12.md) (if you are returning an **XLOPER**) or **xlAutoFree12** (if you are returning an **XLOPER12**).</span></span>
  
## <a name="example"></a><span data-ttu-id="3b2bb-124">��</span><span class="sxs-lookup"><span data-stu-id="3b2bb-124">Example</span></span>

 `\SAMPLES\GENERIC\GENERIC.C`
  
```cs
LPXLOPER12 WINAPI xlAddInManagerInfo12(LPXLOPER12 xAction)
{
    static XLOPER12 xInfo, xIntAction;
/*
** This code coerces the passed-in value to an integer. This is how the
** code determines what is being requested. If it receives a 1, it returns a
** string representing the long name. If it receives anything else, it
** returns a #VALUE! error.
*/
    Excel12f(xlCoerce, &xIntAction, 2, xAction, TempInt12(xltypeInt));
    if(xIntAction.val.w == 1) 
    {
        xInfo.xltype = xltypeStr;
        xInfo.val.str = L"\026Example Standalone DLL";
    }
    else 
    {
        xInfo.xltype = xltypeErr;
        xInfo.val.err = xlerrValue;
    }
// Word of caution - returning static XLOPERs/XLOPER12s is not thread safe
// for UDFs declared as thread safe. Use alternate memory allocation mechanisms.
    return (LPXLOPER12)&xInfo;
} 

```

## <a name="see-also"></a><span data-ttu-id="3b2bb-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="3b2bb-125">See also</span></span>



<span data-ttu-id="3b2bb-126">[�A�h�C�� �}�l�[�W���[�� XLL �C���^�[�t�F�C�X�֐�](add-in-manager-and-xll-interface-functions.md)</span><span class="sxs-lookup"><span data-stu-id="3b2bb-126">[Add-in Manager and XLL Interface Functions](add-in-manager-and-xll-interface-functions.md)</span></span>

