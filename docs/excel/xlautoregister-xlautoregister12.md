---
title: xlAutoRegister/xlAutoRegister12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoRegister
keywords:
- xlautoregister function [excel 2007]
localization_priority: Normal
ms.assetid: aa4673cf-8e97-4678-b8d4-6a74426334f9
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: e6430a54b0c0ed3b6e08d3c9256cae7dcde926ab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2018
ms.locfileid: "19798961"
---
# <a name="xlautoregisterxlautoregister12"></a><span data-ttu-id="22590-104">xlAutoRegister/xlAutoRegister12</span><span class="sxs-lookup"><span data-stu-id="22590-104">xlAutoRegister/xlAutoRegister12</span></span>

 <span data-ttu-id="22590-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="22590-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="22590-p101">�o�^�Ώۂ̊֐��̖߂�l�̌^�ƈ����̌^���Ȃ���ԂŁAXLM �֐� [REGISTER](xlautoregister-xlautoregister12.md)�A�܂��� C API �̓����� **xlfRegister** �֐��ɑ΂���Ăяo�������s�����ƁA��� Excel �� [xlAutoRegister](xlfregister-form-1.md) �֐���Ăяo���܂��B�����g�p����ƁA�G�N�X�|�[�g���ꂽ�֐��ƃR�}���h�̓�����X�g�� XLL �Ō����ł���悤�ɂȂ�A����̈����Ɩ߂�l�̌^����֐���o�^�ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="22590-p101">Excel calls the [xlAutoRegister function](xlautoregister-xlautoregister12.md) whenever a call has been made to the XLM function **REGISTER**, or the C API equivalent [xlfRegister function](xlfregister-form-1.md), with the return and argument types of the function being registered missing. It allows the XLL to search its internal lists of exported functions and commands to register the function with the argument and return types specified.</span></span>
  
<span data-ttu-id="22590-108">Excel 2007 �ȍ~�ł́A **xlAutoRegister12** �֐��� XLL �ɂ���ăG�N�X�|�[�g�����ƁAExcel �� **xlAutoRegister** �֐��ɗD�悵�Ă��̊֐���Ăяo���܂��B</span><span class="sxs-lookup"><span data-stu-id="22590-108">Starting in Excel 2007, Excel calls the **xlAutoRegister12** function in preference to the **xlAutoRegister** function if it is exported by the XLL.</span></span> 
  
<span data-ttu-id="22590-109">Excel �ł́AXLL ������炢���ꂩ�̊֐���������ăG�N�X�|�[�g���邱�Ƃ͕s�v�ł��B</span><span class="sxs-lookup"><span data-stu-id="22590-109">Excel does not require an XLL to implement and export either of these functions.</span></span>
  
> [!NOTE]
> <span data-ttu-id="22590-110">[!����] **xlAutoRegister**/  **xlAutoRegister12** �������̌^�Ɩ߂�l�̌^��w�肵�Ȃ��Ŋ֐���o�^���悤�Ƃ���ƁA�ŏI�I�ɃR�[�� �X�^�b�N���I�[�o�[�t���[���AExcel ���N���b�V�����錴���ƂȂ�ċA�Ăяo���̃��[�v���������܂��B</span><span class="sxs-lookup"><span data-stu-id="22590-110">If **xlAutoRegister**/ **xlAutoRegister12** tries to register the function without supplying the argument and return types, a recursive calling loop occurs which eventually overflows the call stack and crashes Excel.</span></span> 
  
```cs
LPXLOPER12 WINAPI xlAutoRegister12(LPXLOPER12 pxName);
LPXLOPER WINAPI xlAutoRegister(LPXLOPER pxName);
```

## <a name="parameters"></a><span data-ttu-id="22590-111">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="22590-111">Parameters</span></span>

 <span data-ttu-id="22590-112">_pxName_(**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="22590-112">_pxName_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="22590-113">�o�^����� XLL �֐��̖��O�ł��B</span><span class="sxs-lookup"><span data-stu-id="22590-113">The name of the XLL function that is being registered.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="22590-114">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="22590-114">Property value/Return value</span></span>

<span data-ttu-id="22590-p102">�֐��́A _xlfRegister_ �֐���g�p���āAXLL �֐�  **pxName** �̓o�^����s�������ʂ�Ԃ��K�v������܂��B�w�肵���֐��� XLL �t�@�C���̃G�N�X�|�[�g�� 1 �łȂ��ꍇ�A�֐��� **#VALUE!** �G���[��Ԃ����AExcel �� **#VALUE!** �Ɖ�߂��� **NULL** ��Ԃ��K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="22590-p102">The function should return the result of the attempt to register the XLL function  _pxName_ using the **xlfRegister** function. If the specified function is not one of the XLL's exports, it should return the **#VALUE!** error, or **NULL** which Excel will interpret at **#VALUE!**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="22590-118">����</span><span class="sxs-lookup"><span data-stu-id="22590-118">Remarks</span></span>

<span data-ttu-id="22590-p103">**xlAutoRegister** �̎����ł́A�G�N�X�|�[�g���� XLL �t�@�C���̊֐��ƃR�}���h�̓�����X�g�ő啶�����������ʂ��錟������s���āA�n���ꂽ���O�Ƃ̈�v���������K�v������܂��B�֐��܂��̓R�}���h�����������ꍇ�A **xlAutoRegister** �� **xlfRegister** �֐���g�p���AExcel �Ɋ֐��̖߂�l�̌^�ƈ����̌^�A����ъ֐��Ɋւ��邻�̑��̕K�v����w�����镶�����w�肵�āA�o�^����s����K�v������܂��B����́A **xlfRegister** �ɑ΂���Ăяo�����Ԃ��ꂽ�ꍇ�ɂ�AExcel �ɕԂ��K�v������܂��B�֐�������ɓo�^���ꂽ�ꍇ�A **xlfRegister** �͊֐��̓o�^ ID ��܂� **xltypeNum** �l��Ԃ��܂��B</span><span class="sxs-lookup"><span data-stu-id="22590-p103">Your implementation of **xlAutoRegister** should perform a case-insensitive search through your XLL's internal lists of the functions and commands it exports looking for a match with the passed-in name. If the function or command is found, **xlAutoRegister** should attempt to register it, using the **xlfRegister** function, making sure to provide the string that tells Excel the return and argument types of the function, as well as any other required information about the function. It should then return to Excel whatever the call to **xlfRegister** returned. If the function was registered successfully, **xlfRegister** returns an **xltypeNum** value containing the Register ID of the function.</span></span> 
  
### <a name="example"></a><span data-ttu-id="22590-123">��</span><span class="sxs-lookup"><span data-stu-id="22590-123">Example</span></span>

<span data-ttu-id="22590-124">���̊֐��̎�����ɂ��ẮA�t�@�C��  `SAMPLES\EXAMPLE\EXAMPLE.C` ��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="22590-124">See the file  `SAMPLES\EXAMPLE\EXAMPLE.C` for an example implementation of this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="22590-125">�֘A����</span><span class="sxs-lookup"><span data-stu-id="22590-125">See also</span></span>



[<span data-ttu-id="22590-126">REGISTER</span><span class="sxs-lookup"><span data-stu-id="22590-126">REGISTER</span></span>](xlfregister-form-1.md)
  
[<span data-ttu-id="22590-127">UNREGISTER</span><span class="sxs-lookup"><span data-stu-id="22590-127">UNREGISTER</span></span>](xlfunregister-form-1.md)

