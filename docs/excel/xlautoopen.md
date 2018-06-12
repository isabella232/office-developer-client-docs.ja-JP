---
title: xlAutoOpen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoOpen
keywords:
- xlautoopen function [excel 2007]
localization_priority: Normal
ms.assetid: 748cecb6-61d0-496b-a1a4-a73d22eb29e2
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: bf64841cbd75e25443abe5cfc7d3d7419757e245
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798957"
---
# <a name="xlautoopen"></a><span data-ttu-id="a1215-104">xlAutoOpen</span><span class="sxs-lookup"><span data-stu-id="a1215-104">xlAutoOpen</span></span>

 <span data-ttu-id="a1215-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a1215-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="a1215-p101">���ׂĂ̗L���� XLL �ɂ���Ď�������уG�N�X�|�[�g�����K�v������R�[���o�b�N�֐��BXLL �֐��ƃR�}���h�̓o�^�A�f�[�^�\���̏������A���[�U�[ �C���^�[�t�F�C�X�̃J�X�^�}�C�Y�Ȃǂ�s���ꍇ�ɂ́A **xlAutoOpen** ��g�p���邱�Ƃ�����߂��܂��B</span><span class="sxs-lookup"><span data-stu-id="a1215-p101">Callback function that must be implemented and exported by every valid XLL. The **xlAutoOpen** function is the recommended place from where to register XLL functions and commands, initialize data structures, customize the user interface, and so on.</span></span> 
  
```cs
int WINAPI xlAutoOpen(void);
```

## <a name="parameters"></a><span data-ttu-id="a1215-108">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="a1215-108">Parameters</span></span>

<span data-ttu-id="a1215-109">���̊֐��Ɉ����͂���܂���B</span><span class="sxs-lookup"><span data-stu-id="a1215-109">This function takes no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="a1215-110">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="a1215-110">Property value/Return value</span></span>

<span data-ttu-id="a1215-111">この関数の実装では、1 (**int**) を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="a1215-111">Your implementation of this function must return 1 (**int**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a1215-112">����</span><span class="sxs-lookup"><span data-stu-id="a1215-112">Remarks</span></span>

<span data-ttu-id="a1215-p102">XLL ���A�N�e�B�u�ɂȂ邽�тɁAMicrosoft Excel �� **xlAutoOpen** ��Ăяo���܂��B�ȉ��̏󋵂ŁAXLL �̓A�N�e�B�u�ɂȂ�܂��B</span><span class="sxs-lookup"><span data-stu-id="a1215-p102">Microsoft Excel calls **xlAutoOpen** whenever the XLL is activated. The XLL is activated in the following situations:</span></span> 
  
- <span data-ttu-id="a1215-115">����I�������O��� Excel �Z�b�V�����ŃA�N�e�B�u�ł������ꍇ�AExcel �Z�b�V�����̊J�n���B</span><span class="sxs-lookup"><span data-stu-id="a1215-115">At the start of an Excel session if it was active in the last Excel session that ended normally.</span></span>
    
- <span data-ttu-id="a1215-116">Excel �Z�b�V�������ɓǂݍ��܂ꂽ�ꍇ�B</span><span class="sxs-lookup"><span data-stu-id="a1215-116">If loaded during an Excel session.</span></span>
    
- <span data-ttu-id="a1215-117">XLL �͈ȉ��̂������̕��@�œǂݍ��ނ��Ƃ��ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="a1215-117">An XLL can be loaded in several ways:</span></span>
    
- <span data-ttu-id="a1215-118">**[�t�@�C��]** ���j���[�� **[�J��]** ��I����� (Excel �̃o�[�W������ XLL �ǂݍ��݂̂��̕��@��T�|�[�g���Ă���ꍇ)�B</span><span class="sxs-lookup"><span data-stu-id="a1215-118">By choosing **Open** on the **File** menu (where the version of Excel supports this method of loading XLLs).</span></span> 
    
- <span data-ttu-id="a1215-119">�A�h�C�� �}�l�[�W���[��g�p����B</span><span class="sxs-lookup"><span data-stu-id="a1215-119">Using the Add-In Manager.</span></span>
    
- <span data-ttu-id="a1215-120">���� DLL �̖��O��B��̈����Ƃ��� [xlfRegister](xlfregister-form-1.md) ��Ăяo���ʂ� XLL ����B</span><span class="sxs-lookup"><span data-stu-id="a1215-120">From another XLL that calls [xlfRegister](xlfregister-form-1.md) with the name of this DLL as the only argument.</span></span> 
    
- <span data-ttu-id="a1215-121">���� DLL �̖��O��B��̈����Ƃ��� [REGISTER](xlfregister-form-1.md) ��Ăяo�� XLM �}�N�� �V�[�g����B</span><span class="sxs-lookup"><span data-stu-id="a1215-121">From an XLM macro sheet that calls [REGISTER](xlfregister-form-1.md) with the name of this DLL as the only argument.</span></span> 
    
- <span data-ttu-id="a1215-122">�A�h�C�����AExcel �Z�b�V�������ɔ�A�N�e�B�u�ɂ���Ă���ēx�A�N�e�B�u�ɂ����ꍇ�A���̊֐��͍ăA�N�e�B�u���̂Ƃ��ɌĂяo����܂��B</span><span class="sxs-lookup"><span data-stu-id="a1215-122">If the add-in is deactivated and reactivated during an Excel session, this function is called on reactivation.</span></span>
    
### <a name="example"></a><span data-ttu-id="a1215-123">��</span><span class="sxs-lookup"><span data-stu-id="a1215-123">Example</span></span>

<span data-ttu-id="a1215-124">���̊֐��̎�����ɂ��ẮA `SAMPLES\EXAMPLE\EXAMPLE.C` �t�@�C����  `SAMPLES\GENERIC\GENERIC.C` �t�@�C����������������B</span><span class="sxs-lookup"><span data-stu-id="a1215-124">See the files  `SAMPLES\EXAMPLE\EXAMPLE.C` and  `SAMPLES\GENERIC\GENERIC.C`, and for example implementations of this function.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a1215-125">�֘A����</span><span class="sxs-lookup"><span data-stu-id="a1215-125">See also</span></span>



[<span data-ttu-id="a1215-126">xlAutoClose</span><span class="sxs-lookup"><span data-stu-id="a1215-126">xlAutoClose</span></span>](xlautoclose.md)
  
[<span data-ttu-id="a1215-127">xlAutoRegister/xlAutoRegister12</span><span class="sxs-lookup"><span data-stu-id="a1215-127">xlAutoRegister/xlAutoRegister12</span></span>](xlautoregister-xlautoregister12.md)


<span data-ttu-id="a1215-128">[�A�h�C�� �}�l�[�W���[�� XLL �C���^�[�t�F�C�X�֐�](add-in-manager-and-xll-interface-functions.md)</span><span class="sxs-lookup"><span data-stu-id="a1215-128">[Add-in Manager and XLL Interface Functions](add-in-manager-and-xll-interface-functions.md)</span></span>

