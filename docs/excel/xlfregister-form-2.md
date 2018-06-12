---
title: xlfRegister (�`�� 2)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfRegister
keywords:
- xlfregister function [excel 2007]
localization_priority: Normal
ms.assetid: 3ebbd775-f3d2-4ba7-8835-a5b38ad2267a
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: a535018e2b644966d183ba9ae862ce83670c9231
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798973"
---
# <a name="xlfregister-form-2"></a><span data-ttu-id="1abca-104">xlfRegister (�\`�� 2)</span><span class="sxs-lookup"><span data-stu-id="1abca-104">xlfRegister (Form 2)</span></span>

 <span data-ttu-id="1abca-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="1abca-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="1abca-p101">Microsoft Excel ���璼�ڌĂяo���悤�ɁA DLL �R�}���h�� XLL �R�}���h��g���ČĂяo�����Ƃ��ł��܂��B����́A **REGISTER** �� Excel XLM �}�N�� �V�[�g����Ăяo���̂Ɠ����ł��B</span><span class="sxs-lookup"><span data-stu-id="1abca-p101">Can be called from a DLL or XLL command that has itself been called by Microsoft Excel. This is equivalent to calling **REGISTER** from an Excel XLM macro sheet.</span></span> 
  
<span data-ttu-id="1abca-108">���� **xlfRegister** �֐��́A����2 �̌\`���ŌĂяo�����Ƃ��ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="1abca-108">The **xlfRegister** function can be called in two forms:</span></span> 
  
- <span data-ttu-id="1abca-109">[xlfRegister (�\`�� 1)](xlfregister-form-1.md):�R�}���h��֐���X�ɓo�^���܂��B</span><span class="sxs-lookup"><span data-stu-id="1abca-109">[xlfRegister (Form 1)](xlfregister-form-1.md): Registers an individual command or function.</span></span>
    
- <span data-ttu-id="1abca-110">xlfRegister (�\`�� 2):XLL ��ǂݍ���ŃA�N�e�B�u�����܂��B</span><span class="sxs-lookup"><span data-stu-id="1abca-110">xlfRegister (Form 2): Loads and activates an XLL.</span></span>
    
<span data-ttu-id="1abca-111">���̊֐���\`�� 2 �ŌĂяo�����ꍇ�́A[xlAutoOpen](xlautoopen.md) �v���V�[�W����܂� XLL �̓ǂݍ��݂ƃA�N�e�B�u���̂ݍs���܂��B</span><span class="sxs-lookup"><span data-stu-id="1abca-111">Called in Form 2, this function can only be used to load and activate an XLL containing an [xlAutoOpen](xlautoopen.md) procedure.</span></span> 
  
```cs
Excel12(xlfRegister, LPXLOPER12 pxRes, 1, LPXLOPER12 pxModuleText);
```

## <a name="parameters"></a><span data-ttu-id="1abca-112">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="1abca-112">Parameters</span></span>

 <span data-ttu-id="1abca-113">_pxModuleText_(**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="1abca-113">_pxModuleText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="1abca-114">�ǂݍ��݂ƃA�N�e�B�u����s�� DLL ���B</span><span class="sxs-lookup"><span data-stu-id="1abca-114">The name of the DLL to be loaded and activated.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="1abca-115">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="1abca-115">Property value/Return value</span></span>

<span data-ttu-id="1abca-116">成功した場合、この DLL (**xltypeStr**) の名前を返します。</span><span class="sxs-lookup"><span data-stu-id="1abca-116">If successful, this returns the name of the DLL (**xltypeStr**).</span></span> <span data-ttu-id="1abca-117">それ以外の場合、#VALUE を返します。</span><span class="sxs-lookup"><span data-stu-id="1abca-117">Otherwise it returns a #VALUE!</span></span> <span data-ttu-id="1abca-118">エラーです。</span><span class="sxs-lookup"><span data-stu-id="1abca-118">error.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1abca-119">�֘A����</span><span class="sxs-lookup"><span data-stu-id="1abca-119">See also</span></span>



[<span data-ttu-id="1abca-120">�d�v�Ŗ�ɗ��� C API XLM �֐�</span><span class="sxs-lookup"><span data-stu-id="1abca-120">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

