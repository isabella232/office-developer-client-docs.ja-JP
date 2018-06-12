---
title: xlAutoRemove
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoRemove
keywords:
- xlautoremove function [excel 2007]
localization_priority: Normal
ms.assetid: fff0de4d-605d-49e6-a5be-a000410c09d8
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 6e5daac21a6d89472a7d84a25e9aeaea56db1ae1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798974"
---
# <a name="xlautoremove"></a><span data-ttu-id="47159-104">xlAutoRemove</span><span class="sxs-lookup"><span data-stu-id="47159-104">xlAutoRemove</span></span>

 <span data-ttu-id="47159-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="47159-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="47159-p101">���[�U�[�� Excel �Z�b�V�������ɃA�h�C�� �}�l�[�W���[��g�p���� XLL �𖳌��ɂ��邽�тɁAMicrosoft Excel �ɂ���ČĂяo����܂��B�A�h�C�����C���X�g�[������Ă����Ԃ� Excel �Z�b�V����������I���A�܂��ُ͈�I������ƁA���̊֐��͌Ăяo����܂���B</span><span class="sxs-lookup"><span data-stu-id="47159-p101">Called by Microsoft Excel whenever the user deactivates the XLL during an Excel session by using the Add-In Manager. This function is not called when an Excel session closes, normally or abnormally, with the add-in installed.</span></span>
  
<span data-ttu-id="47159-108">���Ƃ��΂��̊֐���g�p���āA�A�h�C���������ɂȂ��Ă��邱�Ƃ���[�U�[�ɒʒm����J�X�^�� �_�C�A���O �{�b�N�X��\��������A���W�X�g���̓ǂݎ��Ə������݂�s�����肷�邱�Ƃ��ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="47159-108">This function can be used to display a custom dialog box telling the user that the add-in has been deactivated, or to read from or write to the registry, for example.</span></span>
  
<span data-ttu-id="47159-109">Excel �ł́A�����̊֐��̎����ƃG�N�X�|�[�g�� XLL �͕K�v����܂���B</span><span class="sxs-lookup"><span data-stu-id="47159-109">Excel does not require an XLL to implement and export this function.</span></span> 
  
```cs
int WINAPI xlAutoRemove(void);
```

## <a name="parameters"></a><span data-ttu-id="47159-110">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="47159-110">Parameters</span></span>

<span data-ttu-id="47159-111">���̊֐��Ɉ����͂���܂���B</span><span class="sxs-lookup"><span data-stu-id="47159-111">This function takes no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="47159-112">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="47159-112">Property value/Return value</span></span>

<span data-ttu-id="47159-113">この関数の実装では、1 (**int**) を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="47159-113">Your implementation of this function must return 1 (**int**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="47159-114">����</span><span class="sxs-lookup"><span data-stu-id="47159-114">Remarks</span></span>

<span data-ttu-id="47159-115">�A�h�C�� �}�l�[�W���[�ɂ���ă^�X�N���폜���ꂽ�Ƃ��� XLL �����̃^�X�N���������K�v������ꍇ�́A���̊֐���g�p���܂��B</span><span class="sxs-lookup"><span data-stu-id="47159-115">Use this function if your XLL needs to complete any task when it is removed by the Add-In Manager.</span></span>
  
## <a name="example"></a><span data-ttu-id="47159-116">��</span><span class="sxs-lookup"><span data-stu-id="47159-116">Example</span></span>

<span data-ttu-id="47159-p102">���̊֐��̎���������  `\SAMPLES\EXAMPLE\EXAMPLE.C` �t�@�C����  `\SAMPLES\GENERIC\GENERIC.C` �t�@�C����Q�Ƃ��Ă��������B���̃R�[�h�́A  `\SAMPLES\EXAMPLE\EXAMPLE.C` �ɂ���܂��B</span><span class="sxs-lookup"><span data-stu-id="47159-p102">See the files  `\SAMPLES\EXAMPLE\EXAMPLE.C` and  `\SAMPLES\GENERIC\GENERIC.C` for example implementations of this function. The following code is from  `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span></span>
  
```cs
int WINAPI xlAutoRemove(void)
{
/* Display a dialog box indicating that the XLL was successfully removed */
   Excel12f(xlcAlert, 0, 2,
      TempStr12(L"Thank you for removing Example.XLL!"),
      TempInt12(2));
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="47159-119">�֘A����</span><span class="sxs-lookup"><span data-stu-id="47159-119">See also</span></span>



[<span data-ttu-id="47159-120">xlAutoAdd</span><span class="sxs-lookup"><span data-stu-id="47159-120">xlAutoAdd</span></span>](xlautoadd.md)


<span data-ttu-id="47159-121">[�A�h�C�� �}�l�[�W���[�� XLL �C���^�[�t�F�C�X�֐�](add-in-manager-and-xll-interface-functions.md)</span><span class="sxs-lookup"><span data-stu-id="47159-121">[Add-in Manager and XLL Interface Functions](add-in-manager-and-xll-interface-functions.md)</span></span>

