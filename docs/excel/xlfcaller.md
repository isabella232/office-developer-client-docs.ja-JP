---
title: xlfCaller
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfCaller
keywords:
- xlfcaller function [excel 2007]
localization_priority: Normal
ms.assetid: de4b119c-ae2e-4207-9783-8d5692a4d052
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 92d2d1877d7b315d178ef1fa36b47bd5f9f8e661
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798969"
---
# <a name="xlfcaller"></a><span data-ttu-id="fefd7-104">xlfCaller</span><span class="sxs-lookup"><span data-stu-id="fefd7-104">xlfCaller</span></span>

 <span data-ttu-id="fefd7-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="fefd7-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="fefd7-106">���ݎ��s���� DLL �R�}���h�܂��͊֐���Ăяo�����Z���A�Z���͈̔́A���j���[�̃R�}���h�A�c�[���o�[�̃c�[���A�܂��̓I�u�W�F�N�g�Ɋւ������Ԃ��܂��B</span><span class="sxs-lookup"><span data-stu-id="fefd7-106">Returns information about the cell, range of cells, command on a menu, tool on a toolbar, or object that called the DLL command or function that is currently running.</span></span>
  
|<span data-ttu-id="fefd7-107">**�Ăяo�����̃R�[�h**</span><span class="sxs-lookup"><span data-stu-id="fefd7-107">**Code called from**</span></span>|<span data-ttu-id="fefd7-108">**�߂�l**</span><span class="sxs-lookup"><span data-stu-id="fefd7-108">**Returns**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fefd7-109">DLL</span><span class="sxs-lookup"><span data-stu-id="fefd7-109">DLL</span></span>  <br/> |<span data-ttu-id="fefd7-110">�o�^ ID�B</span><span class="sxs-lookup"><span data-stu-id="fefd7-110">The Register ID.</span></span>  <br/> |
|<span data-ttu-id="fefd7-111">�P��̃Z��</span><span class="sxs-lookup"><span data-stu-id="fefd7-111">A single cell</span></span>  <br/> |<span data-ttu-id="fefd7-112">�P��Z���̎Q�ƁB</span><span class="sxs-lookup"><span data-stu-id="fefd7-112">A single-cell reference.</span></span>  <br/> |
|<span data-ttu-id="fefd7-113">�����Z���̔z�񐔎�</span><span class="sxs-lookup"><span data-stu-id="fefd7-113">A multi-cell array formula</span></span>  <br/> |<span data-ttu-id="fefd7-114">�����Z���̎Q�ƁB</span><span class="sxs-lookup"><span data-stu-id="fefd7-114">A multi-cell reference.</span></span>  <br/> |
|<span data-ttu-id="fefd7-115">����t�������ݒ莮</span><span class="sxs-lookup"><span data-stu-id="fefd7-115">A conditional formatting expression</span></span>  <br/> |<span data-ttu-id="fefd7-116">�����ݒ�̏�����K�p����Ă���Z���ւ̎Q�ƁB</span><span class="sxs-lookup"><span data-stu-id="fefd7-116">A reference to the cell to which the formatting condition is applied.</span></span>  <br/> |
|<span data-ttu-id="fefd7-117">���j���[</span><span class="sxs-lookup"><span data-stu-id="fefd7-117">A menu</span></span>  <br/> | <span data-ttu-id="fefd7-118">4 �̗v�f�̒P��s�z��</span><span class="sxs-lookup"><span data-stu-id="fefd7-118">A four-element single-row array:</span></span>  <br/>  <span data-ttu-id="fefd7-119">�o�[�� ID�B</span><span class="sxs-lookup"><span data-stu-id="fefd7-119">The bar ID.</span></span>  <br/>  <span data-ttu-id="fefd7-120">���j���[�̈ʒu�B</span><span class="sxs-lookup"><span data-stu-id="fefd7-120">The menu position.</span></span>  <br/>  <span data-ttu-id="fefd7-121">�T�u���j���[�̈ʒu�B</span><span class="sxs-lookup"><span data-stu-id="fefd7-121">The submenu position.</span></span>  <br/>  <span data-ttu-id="fefd7-122">�R�}���h�̈ʒu�B</span><span class="sxs-lookup"><span data-stu-id="fefd7-122">The command position.</span></span>  <br/> |
|<span data-ttu-id="fefd7-123">�c�[���o�[</span><span class="sxs-lookup"><span data-stu-id="fefd7-123">A toolbar</span></span>  <br/> | <span data-ttu-id="fefd7-124">2 �̗v�f�̒P��s�z��</span><span class="sxs-lookup"><span data-stu-id="fefd7-124">A two-element single-row array:</span></span>  <br/>  <span data-ttu-id="fefd7-125">�g�ݍ��݃c�[���o�[�̏ꍇ�̓c�[���o�[�ԍ��A�J�X�^�� �c�[���o�[�̏ꍇ�̓c�[���o�[���B</span><span class="sxs-lookup"><span data-stu-id="fefd7-125">The toolbar number for built-in toolbars or the toolbar name for custom toolbars.</span></span>  <br/>  <span data-ttu-id="fefd7-126">�c�[���o�[��̈ʒu�B</span><span class="sxs-lookup"><span data-stu-id="fefd7-126">The position on the toolbar.</span></span>  <br/> |
|<span data-ttu-id="fefd7-127">�O���t�B�b�N �I�u�W�F�N�g</span><span class="sxs-lookup"><span data-stu-id="fefd7-127">A graphic object</span></span>  <br/> |<span data-ttu-id="fefd7-128">�I�u�W�F�N�g�̎��ʎq (�I�u�W�F�N�g��)�B</span><span class="sxs-lookup"><span data-stu-id="fefd7-128">The object identifier (object name).</span></span>  <br/> |
|<span data-ttu-id="fefd7-129">xlcOnEnter�AON.ENTER�A�C�x���g �g���b�v�Ɋ֘A�t����ꂽ�R�}���h</span><span class="sxs-lookup"><span data-stu-id="fefd7-129">A command associated with an xlcOnEnter, ON.ENTER, event trap</span></span>  <br/> |<span data-ttu-id="fefd7-130">���͂���� 1 �܂��͕����̃Z���ւ̎Q�ƁB</span><span class="sxs-lookup"><span data-stu-id="fefd7-130">A reference to the cell or cells being entered.</span></span>  <br/> |
|<span data-ttu-id="fefd7-131">xlcOnDoubleclick�AON.DOUBLECLICK�A�C�x���g �g���b�v�Ɋ֘A�t����ꂽ�R�}���h</span><span class="sxs-lookup"><span data-stu-id="fefd7-131">A command associated with an xlcOnDoubleclick, ON.DOUBLECLICK, event trap.</span></span>  <br/> |<span data-ttu-id="fefd7-132">�_�u���N���b�N���ꂽ�Z�� (�K������A�N�e�B�u�ȃZ���ł͂���܂���)�B</span><span class="sxs-lookup"><span data-stu-id="fefd7-132">The cell that was double-clicked (not necessarily the active cell).</span></span>  <br/> |
|<span data-ttu-id="fefd7-133">Auto_Open�AAutoClose�AAuto_Activate �܂��� Auto_Deactivate �}�N��</span><span class="sxs-lookup"><span data-stu-id="fefd7-133">Auto_Open, AutoClose, Auto_Activate or Auto_Deactivate macro</span></span>  <br/> |<span data-ttu-id="fefd7-134">�Ăяo�����V�[�g�̖��O�B</span><span class="sxs-lookup"><span data-stu-id="fefd7-134">The name of the calling sheet.</span></span>  <br/> |
|<span data-ttu-id="fefd7-135">���̈ꗗ�ɂȂ����̃��\�b�h</span><span class="sxs-lookup"><span data-stu-id="fefd7-135">Other methods not listed</span></span>  <br/> |<span data-ttu-id="fefd7-p101">#REF!�G���[�B</span><span class="sxs-lookup"><span data-stu-id="fefd7-p101">#REF! Error.</span></span>  <br/> |
   
```cs
Excel12(xlfCaller, (LPXLOPER12) pxRes,0);
```

## <a name="property-valuereturn-value"></a><span data-ttu-id="fefd7-138">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="fefd7-138">Property value/Return value</span></span>

<span data-ttu-id="fefd7-p102">�߂�l�� **XLOPER**/ **XLOPER12** �f�[�^�^�� **xltypeRef**�A **xltypeSRef**�A **xltypeNum**�A **xltypeStr**�A **xltypeErr**�A�܂��� **xltypeMulti** �̂����ꂩ�ł��B�����̌^�̂��� 3 �͊��蓖�Ă�ꂽ��������|�C���g���Ă��邽�߁A�s�v�ɂȂ��� **xlfCaller** �̖߂�l�͕K�� [xlFree �֐�](xlfree.md)�ւ̌Ăяo���ŉ������K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="fefd7-p102">The return value is one of the following **XLOPER**/ **XLOPER12** data types: **xltypeRef**, **xltypeSRef**, **xltypeNum**, **xltypeStr**, **xltypeErr**, or **xltypeMulti**. Since three of these types point to allocated memory, the return value of **xlfCaller** should always be freed in a call to the [xlFree function](xlfree.md) when it is no longer needed.</span></span> 
  
<span data-ttu-id="fefd7-141">**XLOPERs**/ **XLOPER12s** �̏ڍׂɂ��ẮA�u [Excel �̃������Ǘ�](memory-management-in-excel.md)�v��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="fefd7-141">For more information about **XLOPERs**/ **XLOPER12s** see [Memory Management in Excel](memory-management-in-excel.md).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fefd7-142">����</span><span class="sxs-lookup"><span data-stu-id="fefd7-142">Remarks</span></span>

<span data-ttu-id="fefd7-p103">���̊֐��́ADLL/XLL ���[�N�V�[�g�֐�����Ăяo���\�ȗB��̔񃏁[�N�V�[�g�֐��ł��B���̑��� XLM ���֐��́A�R�}���h�܂��̓}�N�� �V�[�g�����̊֐�����̂݌Ăяo���ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="fefd7-p103">This function is the only non-worksheet function that can be called from a DLL/XLL worksheet function. Other XLM information functions can only be called from commands or macro-sheet equivalent functions.</span></span>
  
## <a name="example"></a><span data-ttu-id="fefd7-145">��</span><span class="sxs-lookup"><span data-stu-id="fefd7-145">Example</span></span>

 <span data-ttu-id="fefd7-p104">`\SAMPLES\EXAMPLE\EXAMPLE.C`�B���̊֐��̓R�}���h �}�N�� (xlcSelect) ��Ăяo���A�}�N�� �V�[�g����Ăяo���ꂽ�ꍇ�ɂ̂ݐ��������삵�܂��B</span><span class="sxs-lookup"><span data-stu-id="fefd7-p104">`\SAMPLES\EXAMPLE\EXAMPLE.C`. This function calls a command macro (xlcSelect) and will work correctly only when called from a macro sheet.</span></span>
  
```cs
short WINAPI CallerExample(void)
{
   XLOPER12 xRes;
   Excel12(xlfCaller, &xRes, 0);
   Excel12(xlcSelect, 0, 1, (LPXLOPER12)&xRes);
   Excel12(xlFree, 0, 1, (LPXLOPER12)&xRes);
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="fefd7-148">�֘A����</span><span class="sxs-lookup"><span data-stu-id="fefd7-148">See also</span></span>



[<span data-ttu-id="fefd7-149">�d�v�Ŗ�ɗ��� C API XLM �֐�</span><span class="sxs-lookup"><span data-stu-id="fefd7-149">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

