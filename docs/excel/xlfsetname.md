---
title: xlfSetName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfSetName
keywords:
- xlfsetname function [excel 2007]
localization_priority: Normal
ms.assetid: ea7fd713-7c1b-4648-a609-3334f595c61a
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 48ce927f6bcb328a90779948a660cf9d0b460205
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798972"
---
# <a name="xlfsetname"></a><span data-ttu-id="7c036-104">xlfSetName</span><span class="sxs-lookup"><span data-stu-id="7c036-104">xlfSetName</span></span>

<span data-ttu-id="7c036-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="7c036-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="7c036-106">DLL �Ɋ֘A�t�����Ă����\`�ς݂̖��O��쐬����э폜���邽�߂Ɏg�p���܂��B</span><span class="sxs-lookup"><span data-stu-id="7c036-106">Used to create and delete defined names associated with the DLL.</span></span>
  
```cs
Excel12(xlfSetName, LPXLOPER12 pxRes, 2, LPXLOPER12 pxNameText, LPXLOPER12 pxNameDefinition);
```

## <a name="parameters"></a><span data-ttu-id="7c036-107">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="7c036-107">Parameters</span></span>

<span data-ttu-id="7c036-108">_pxNameText_(**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="7c036-108">_pxNameText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="7c036-109">���O�͈̔́B���̖��O�́A�L���Ȗ��O�Ɋւ��� Microsoft Excel �̒ʏ�̐����ɏ�������K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="7c036-109">The name of the range, which should conform to the usual limitations in Microsoft Excel on valid names.</span></span>
  
<span data-ttu-id="7c036-110">_pxNameDefinition_(**xltypeStr**、 **xltypeNum**、 **xltypeBool**、 **xltypeErr**、 **xltypeMulti**、 **xltypeSRef**、 **xltypeRef**、または**xltypeInt**)</span><span class="sxs-lookup"><span data-stu-id="7c036-110">_pxNameDefinition_ (**xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeMulti**, **xltypeSRef**, **xltypeRef**, or **xltypeInt**)</span></span>
  
<span data-ttu-id="7c036-111">(省略可能)。</span><span class="sxs-lookup"><span data-stu-id="7c036-111">(Optional).</span></span> <span data-ttu-id="7c036-112">値、値、セル、またはセルの範囲のセットは、その_pxNameText_として定義されます。</span><span class="sxs-lookup"><span data-stu-id="7c036-112">The value, set of values, cell, or range of cells that  _pxNameText_ is defined as.</span></span> <span data-ttu-id="7c036-113">省略すると、名前が削除されます。</span><span class="sxs-lookup"><span data-stu-id="7c036-113">If omitted, the name is deleted.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="7c036-114">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="7c036-114">Property value/Return value</span></span>

<span data-ttu-id="7c036-115">_pxRes_(**xltypeBool**または**xltypeErr**)</span><span class="sxs-lookup"><span data-stu-id="7c036-115">_pxRes_ (**xltypeBool** or **xltypeErr**)</span></span>
  
<span data-ttu-id="7c036-p102">���삪���������ꍇ�� TRUE�A���O���쐬�܂��͍폜�ł��Ȃ��ꍇ�� FALSE�B1 �܂��͕����̈����������̏ꍇ�� #VALUE! ��Ԃ��܂��B</span><span class="sxs-lookup"><span data-stu-id="7c036-p102">TRUE if the operation succeeded or FALSE if the name could not be created or deleted. Returns #VALUE! if one or more of the arguments was invalid.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7c036-119">����</span><span class="sxs-lookup"><span data-stu-id="7c036-119">Remarks</span></span>

<span data-ttu-id="7c036-p103">**xlfRegister** �ƗL����  _pxFunctionText_ ������g�p���Ċ֐��܂��̓R�}���h��o�^����ꍇ�AExcel ��DLL ���\�[�X�Ɋ֘A�t����ꂽ����쐬���܂��BDLL ���A�����[�h�����ƁA���̂悤�Ȗ��O�� [xlfSetName �֐�](xlfsetname.md)��g�p���č폜����K�v������܂��B�������A���̑���� Excel �̊��m�̖�肪�����Ŏ��s���܂��B�ڍׂɂ��ẮA�u[Excel �A�h�C�� (XLL) �J���ɂ�������m�̖��](known-issues-in-excel-xll-development.md)�v��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="7c036-p103">When a function or command is registered using **xlfRegister** with a valid  _pxFunctionText_ argument, Excel creates a name associated with the DLL resource. When your DLL is being unloaded, such names should be deleted using the [xlfSetName function](xlfsetname.md). However, due to a known issue in Excel, this deletion operation fails. For more information, see [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
### <a name="example"></a><span data-ttu-id="7c036-124">��</span><span class="sxs-lookup"><span data-stu-id="7c036-124">Example</span></span>

<span data-ttu-id="7c036-125">**** �� `\SAMPLES\GENERIC\GENERIC.C` �֐��ɂ��ẮA�R�[�h��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="7c036-125">See the code for the **xlAutoClose** function in  `\SAMPLES\GENERIC\GENERIC.C`.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7c036-126">�֘A����</span><span class="sxs-lookup"><span data-stu-id="7c036-126">See also</span></span>

- [<span data-ttu-id="7c036-127">�d�v�Ŗ�ɗ��� C API XLM �֐�</span><span class="sxs-lookup"><span data-stu-id="7c036-127">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

