---
title: xlfUnregister (�`�� 2)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfUnregister (Form 2)
keywords:
- xlfunregister [excel 2007]
localization_priority: Normal
ms.assetid: 39c6eba7-ba41-4e7b-9a28-2b662378ff5a
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: e0154e380b65b8c57e7e96a98ef131e26b49e203
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798996"
---
# <a name="xlfunregister-form-2"></a><span data-ttu-id="bc5b0-104">xlfUnregister (�\`�� 2)</span><span class="sxs-lookup"><span data-stu-id="bc5b0-104">xlfUnregister (Form 2)</span></span>

<span data-ttu-id="bc5b0-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="bc5b0-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="bc5b0-p101">Microsoft Excel �ɂ���Ă��ꎩ�̂��Ăяo����� DLL �� XLL �R�}���h����Ăяo�����Ƃ��ł��܂��B����́A **UNREGISTER** �� Excel XLM �}�N�� �V�[�g����Ăяo���̂Ɠ����ł��B</span><span class="sxs-lookup"><span data-stu-id="bc5b0-p101">Can be called from a DLL or XLL command that has itself been called by Microsoft Excel. This is equivalent to calling **UNREGISTER** from an Excel XLM macro sheet.</span></span> 
  
<span data-ttu-id="bc5b0-108">**xlfUnregister** �́A2 �̌\`���ŌĂяo�����Ƃ��ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="bc5b0-108">**xlfUnregister** can be called in two forms:</span></span> 
  
- <span data-ttu-id="bc5b0-109">�\`�� 1:�X�̃R�}���h��֐��̓o�^�������܂��B</span><span class="sxs-lookup"><span data-stu-id="bc5b0-109">Form 1: Unregisters an individual command or function.</span></span>
    
- <span data-ttu-id="bc5b0-110">�\`�� 2:XLL �̃A�����[�h�Ɣ�A�N�e�B�x�[�g����s���܂��B</span><span class="sxs-lookup"><span data-stu-id="bc5b0-110">Form 2: Unloads and deactivates an XLL.</span></span>
    
<span data-ttu-id="bc5b0-p102">�\`�� 2 �ŌĂяo�����ƁA���̊֐��� DLL ��R�[�h ���\�[�X�̊��S�ȃA�����[�h��������܂��B�ʂ̃}�N���Ō��ݎg���Ă��Ă�ADLL ��̂��ׂĂ̊֐��̓o�^�������܂��B�֐��̎g�p�ɂ��čl������܂���B���̊֐��� **xlAutoClose** ��Ăяo���Ă���ADLL ��̂��ׂĂ̊֐��̓o�^�������܂��B</span><span class="sxs-lookup"><span data-stu-id="bc5b0-p102">Called in Form 2, this function forces a DLL or code resource to be unloaded completely. It unregisters all of the functions in a DLL, even if they are currently in use by another macro, no matter what the use count. This function calls **xlAutoClose**, and then unregisters all the functions in the DLL.</span></span>
  
```cs
Excel12(xlfUnregister, LPXLOPER12 pxRes, 1, LPXLOPER12 pxModuleText);
```

## <a name="parameters"></a><span data-ttu-id="bc5b0-114">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="bc5b0-114">Parameters</span></span>

<span data-ttu-id="bc5b0-115">_pxModuleText_(**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="bc5b0-115">_pxModuleText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="bc5b0-116">DLL �̖��O�B</span><span class="sxs-lookup"><span data-stu-id="bc5b0-116">The name of the DLL.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="bc5b0-117">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="bc5b0-117">Property value/Return value</span></span>

<span data-ttu-id="bc5b0-118">成功した場合は、 **TRUE** (**xltypeBool**) を返します。</span><span class="sxs-lookup"><span data-stu-id="bc5b0-118">If successful, returns **TRUE** (**xltypeBool**).</span></span> <span data-ttu-id="bc5b0-119">失敗した場合は、 **FALSE**が返されます。</span><span class="sxs-lookup"><span data-stu-id="bc5b0-119">If unsuccessful, returns **FALSE**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bc5b0-120">����</span><span class="sxs-lookup"><span data-stu-id="bc5b0-120">Remarks</span></span>

> [!NOTE] 
> <span data-ttu-id="bc5b0-121">呼び出さないで関数の形式はこの[xlAutoClose](xlautoclose.md)の実装から 1 つの単純な関数呼び出しを使用して、DLL のリソースのすべての登録を解除しようとしてください。</span><span class="sxs-lookup"><span data-stu-id="bc5b0-121">Do not call this form of the function from your implementation of the [xlAutoClose](xlautoclose.md) in an attempt to unregister all of the DLL's resources with one simple function call.</span></span> <span data-ttu-id="bc5b0-122">これ**xlAutoClose**とスタック オーバーフローの再帰的な呼び出しにつながります。</span><span class="sxs-lookup"><span data-stu-id="bc5b0-122">This leads to recursive calling of **xlAutoClose** and a stack overflow.</span></span> 
  
### <a name="remember-to-delete-names"></a><span data-ttu-id="bc5b0-123">名前を削除することを忘れないでください。</span><span class="sxs-lookup"><span data-stu-id="bc5b0-123">Remember to delete names</span></span>

<span data-ttu-id="bc5b0-p105">_pxFunctionText_ ������ **xlfRegister** �Ɏw�肷��ꍇ�́ADLL �̊֐��ƃR�}���h�̓o�^���ɁA���ꂼ��ɂ��� 2 �ڂ̈�����ȗ����� **xlfSetName** ��Ăяo���A�֐����֐��E�B�U�[�h�ɕ\������Ȃ��悤�ɖ��O�𖾎��I�ɍ폜����K�v������܂��B�ڂ����́u [Excel �A�h�C�� (XLL) �J���ɂ�������m�̖��](known-issues-in-excel-xll-development.md)�v��������������B</span><span class="sxs-lookup"><span data-stu-id="bc5b0-p105">If you specified the  _pxFunctionText_ argument to **xlfRegister**, when registering the DLL's functions and commands, you must explicitly delete the names by calling **xlfSetName** for each one, omitting the second argument so that the function no longer appears in the Function Wizard. For more information, see [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="bc5b0-126">�֘A����</span><span class="sxs-lookup"><span data-stu-id="bc5b0-126">See also</span></span>

- [<span data-ttu-id="bc5b0-127">xlfRegister (�\`�� 1)</span><span class="sxs-lookup"><span data-stu-id="bc5b0-127">xlfRegister (Form 1)</span></span>](xlfregister-form-1.md)
- [<span data-ttu-id="bc5b0-128">xlfRegisterId</span><span class="sxs-lookup"><span data-stu-id="bc5b0-128">xlfRegisterId</span></span>](xlfregisterid.md)
- [<span data-ttu-id="bc5b0-129">xlfUnregister (�\`�� 1)</span><span class="sxs-lookup"><span data-stu-id="bc5b0-129">xlfUnregister (Form 1)</span></span>](xlfunregister-form-1.md)
- [<span data-ttu-id="bc5b0-130">�d�v�Ŗ�ɗ��� C API XLM �֐�</span><span class="sxs-lookup"><span data-stu-id="bc5b0-130">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

