---
title: xlAutoAdd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoAdd
keywords:
- xlautoadd function [excel 2007]
localization_priority: Normal
ms.assetid: c69299af-a28a-44d9-be10-9c9fb92e21f2
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: ae0b4ae2d5f5fc58c3e18ffa9d79ec4128cb4639
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798956"
---
# <a name="xlautoadd"></a><span data-ttu-id="2b60e-104">xlAutoAdd</span><span class="sxs-lookup"><span data-stu-id="2b60e-104">xlAutoAdd</span></span>

 <span data-ttu-id="2b60e-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="2b60e-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="2b60e-p101">���[�U�[�� Excel �Z�b�V�������ɃA�h�C�� �}�l�[�W���[��g�p���� XLL ��L���ɂ��邽�тɁAMicrosoft Excel �ɂ���Ēǉ�����܂��BExcel ���N�����A���炩���߃C���X�g�[�����ꂽ�A�h�C����ǂݍ��ލۂɂ́A���̊֐��͌Ăяo����܂���B</span><span class="sxs-lookup"><span data-stu-id="2b60e-p101">Added by Microsoft Excel whenever the user activates the XLL during an Excel session by using the Add-In Manager. This function is not called when Excel starts up and loads a pre-installed add-in.</span></span>
  
<span data-ttu-id="2b60e-108">���Ƃ��΁A���̊֐���g�p���āA�A�h�C�����L���ɂȂ��Ă��邱�Ƃ���[�U�[�ɒʒm����J�X�^�� �_�C�A���O �{�b�N�X�̕\���A���W�X�g���̓ǂݎ��Ə������݁A���C�Z���X���̊m�F�Ȃǂ��ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="2b60e-108">This function can be used to display a custom dialog box that tells the user that the add-in has been activated, or to read from or write to the registry, or check licensing information, for example.</span></span>
  
<span data-ttu-id="2b60e-109">Excel �ł́A�����̊֐��̎����ƃG�N�X�|�[�g�� XLL �͕K�v����܂���B</span><span class="sxs-lookup"><span data-stu-id="2b60e-109">Excel does not require an XLL to implement and export this function.</span></span>
  
```cs
int WINAPI xlAutoAdd(void);
```

## <a name="parameters"></a><span data-ttu-id="2b60e-110">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="2b60e-110">Parameters</span></span>

<span data-ttu-id="2b60e-111">���̊֐��Ɉ����͂���܂���B</span><span class="sxs-lookup"><span data-stu-id="2b60e-111">This function takes no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="2b60e-112">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="2b60e-112">Property value/Return value</span></span>

<span data-ttu-id="2b60e-113">この関数の実装では、1 を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="2b60e-113">Your implementation of this function should return 1.</span></span> <span data-ttu-id="2b60e-114">(**int**) です。</span><span class="sxs-lookup"><span data-stu-id="2b60e-114">(**int**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2b60e-115">����</span><span class="sxs-lookup"><span data-stu-id="2b60e-115">Remarks</span></span>

<span data-ttu-id="2b60e-116">�A�h�C�� �}�l�[�W���[���C�ӂ̃^�X�N��ǉ�����Ƃ��ɁA���̃^�X�N�� XLL �����s����K�v������ꍇ�́A���̊֐���g�p���܂��B</span><span class="sxs-lookup"><span data-stu-id="2b60e-116">Use this function if there is anything your XLL needs to do when it is added by the Add-In Manager.</span></span>
  
## <a name="example"></a><span data-ttu-id="2b60e-117">��</span><span class="sxs-lookup"><span data-stu-id="2b60e-117">Example</span></span>

<span data-ttu-id="2b60e-p103">���̊֐��̎�����ɂ��ẮA `\SAMPLES\EXAMPLE\EXAMPLE.C` ��  `\SAMPLES\GENERIC\GENERIC.C` ��Q�Ƃ��Ă��������B���̃R�[�h�́A  `\SAMPLES\EXAMPLE\EXAMPLE.C` �ɂ���܂��B</span><span class="sxs-lookup"><span data-stu-id="2b60e-p103">See  `\SAMPLES\EXAMPLE\EXAMPLE.C` and  `\SAMPLES\GENERIC\GENERIC.C` for example implementations of this function. The following code is from  `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span></span>
  
```cs
int WINAPI xlAutoAdd(void)
{
    XCHAR szBuf[255];
    wsprintfW((LPWSTR)szBuf, L"Thank you for adding Example.XLL\n"
            L"build date %hs, time %hs",__DATE__, __TIME__);
/* Display a dialog indicating that the XLL was successfully added */
    Excel12f(xlcAlert, 0, 2, TempStr12(szBuf), TempInt12(2));
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="2b60e-120">�֘A����</span><span class="sxs-lookup"><span data-stu-id="2b60e-120">See also</span></span>



[<span data-ttu-id="2b60e-121">xlAutoRemove</span><span class="sxs-lookup"><span data-stu-id="2b60e-121">xlAutoRemove</span></span>](xlautoremove.md)


<span data-ttu-id="2b60e-122">[�A�h�C�� �}�l�[�W���[�� XLL �C���^�[�t�F�C�X�֐�](add-in-manager-and-xll-interface-functions.md)</span><span class="sxs-lookup"><span data-stu-id="2b60e-122">[Add-in Manager and XLL Interface Functions](add-in-manager-and-xll-interface-functions.md)</span></span>
