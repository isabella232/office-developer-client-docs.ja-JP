---
title: xlSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSet
keywords:
- xlset function [excel 2007]
localization_priority: Normal
ms.assetid: 121e6212-0692-4430-97be-4792b53719bf
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 63f50e441f5d851677f36754a17bcd6403705239
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799001"
---
# <a name="xlset"></a><span data-ttu-id="3b9db-104">xlSet</span><span class="sxs-lookup"><span data-stu-id="3b9db-104">xlSet</span></span>

<span data-ttu-id="3b9db-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="3b9db-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="3b9db-p101">�萔�l��Z����͈͂ɂ��΂₭�z�u���܂��B�ڂ����́A�u[Excel �A�h�C�� (XLL) �J���ɂ�������m�̖��](known-issues-in-excel-xll-development.md)�v�́uxlSet �Ɣz�񐔎���܂ރu�b�N�v��������������B</span><span class="sxs-lookup"><span data-stu-id="3b9db-p101">Puts constant values into cells or ranges very quickly. For more information, see "xlSet and Workbooks with Array Formulas" in [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
```cs
Excel12(xlSet, LPXLOPER12 pxRes, 2, LPXLOPER12 pxReference, LPXLOPER pxValue);
```

## <a name="parameters"></a><span data-ttu-id="3b9db-108">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="3b9db-108">Parameters</span></span>

<span data-ttu-id="3b9db-109">_pxReference_(**xltypeRef**または**xltypeSRef**)</span><span class="sxs-lookup"><span data-stu-id="3b9db-109">_pxReference_ (**xltypeRef** or **xltypeSRef**)</span></span>
  
<span data-ttu-id="3b9db-110">目的セルまたはセルを記述する四角形の参照です。</span><span class="sxs-lookup"><span data-stu-id="3b9db-110">A rectangular reference describing the target cell or cells.</span></span> <span data-ttu-id="3b9db-111">参照が、隣接するセルを記述する必要があります**xltypeRef**で`val.mref.lpmref->count`を 1 に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3b9db-111">The reference must describe adjacent cells, so that in an **xltypeRef** `val.mref.lpmref->count` must be set to 1.</span></span> 
  
<span data-ttu-id="3b9db-112">_pxValue_</span><span class="sxs-lookup"><span data-stu-id="3b9db-112">_pxValue_</span></span>
  
<span data-ttu-id="3b9db-p103">�Z���ɔz�u�����l�ł��B�ڂ����́A�u���v�Z�N�V������������������B</span><span class="sxs-lookup"><span data-stu-id="3b9db-p103">The value or values to be placed into the cell or cells. For more information, see the "Remarks" section.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3b9db-115">����</span><span class="sxs-lookup"><span data-stu-id="3b9db-115">Remarks</span></span>

### <a name="pxvalue-argument"></a><span data-ttu-id="3b9db-116">pxValue 引数</span><span class="sxs-lookup"><span data-stu-id="3b9db-116">pxValue argument</span></span>

<span data-ttu-id="3b9db-117">_pxValue_は、値または配列の場合か。</span><span class="sxs-lookup"><span data-stu-id="3b9db-117">_pxValue_ can either be a value or an array.</span></span> <span data-ttu-id="3b9db-118">値の場合は、全体の目的の範囲にその値が格納されます。</span><span class="sxs-lookup"><span data-stu-id="3b9db-118">If it is a value, the entire destination range is filled with that value.</span></span> <span data-ttu-id="3b9db-119">配列 (**xltypeMulti**) である場合、配列の要素は、四角形内の対応する場所に配置されます。</span><span class="sxs-lookup"><span data-stu-id="3b9db-119">If it is an array (**xltypeMulti**), the elements of the array are put into the corresponding locations in the rectangle.</span></span>
  
<span data-ttu-id="3b9db-120">2 番目の引数の横方向の配列を使用する場合、重複していますダウン全体の四角形を塗りつぶす。</span><span class="sxs-lookup"><span data-stu-id="3b9db-120">If you use a horizontal array for the second argument, it is duplicated down to fill the entire rectangle.</span></span> <span data-ttu-id="3b9db-121">縦方向の配列を使用する場合は、四角形全体を入力するには、右、重複しています。</span><span class="sxs-lookup"><span data-stu-id="3b9db-121">If you use a vertical array, it is duplicated right to fill the entire rectangle.</span></span> <span data-ttu-id="3b9db-122">四角形の配列を使用すると、四角形の範囲内に配置するのには小さすぎますが、その範囲に **#N/A**s が埋め込まれます。</span><span class="sxs-lookup"><span data-stu-id="3b9db-122">If you use a rectangular array, and it is too small for the rectangular range you want to put it in, that range is padded with **#N/A**s.</span></span>
  
<span data-ttu-id="3b9db-123">�Ώ۔͈͂��\�[�X�z�����������ꍇ�́A�Ώ۔͈͂̋��E�܂Œl���R�s�[����A�]���ȃf�[�^�͖�������܂��B</span><span class="sxs-lookup"><span data-stu-id="3b9db-123">If the target range is smaller than the source array, the values are copied in up to the limits of the target range and the extra data are ignored.</span></span>
  
<span data-ttu-id="3b9db-p106">�w��̒����**** �S�̂��������ɂ́A2 �Ԗڂ̈�����ȗ����܂��B</span><span class="sxs-lookup"><span data-stu-id="3b9db-p106">To clear an element of the destination rectangle, use an **xltypeNil** type array element in the source array. To clear the entire destination rectangle, omit the second argument.</span></span> 
  
### <a name="restrictions"></a><span data-ttu-id="3b9db-126">����</span><span class="sxs-lookup"><span data-stu-id="3b9db-126">Restrictions</span></span>

<span data-ttu-id="3b9db-p107">**xlSet** ����ɖ߂����Ƃ͂ł��܂���B�܂��A�ȑO�͎g�p�\�������A���ɖ߂�����Ɋւ����񂪔j������܂��B</span><span class="sxs-lookup"><span data-stu-id="3b9db-p107">**xlSet** cannot be undone. In addition, it destroys any undo information that may have been available before.</span></span> 
  
<span data-ttu-id="3b9db-129">**xlSet** �ł́A�Z���ɒ萔�݂̂�z�u�ł��A�����͔z�u�ł��܂���B</span><span class="sxs-lookup"><span data-stu-id="3b9db-129">**xlSet** can put only constants, not formulas, into cells.</span></span> 
  
<span data-ttu-id="3b9db-130">**xlSet** �́A�N���X 3 �R�}���h�Ɠ����̊֐��Ƃ��ē��삵�܂��B�܂�ADLL ���I�u�W�F�N�g�A�}�N���A���j���[�A�c�[���o�[�A�V���[�g�J�b�g �L�[�A **[�}�N��]** �_�C�A���O �{�b�N�X�� **[���s]** �{�^�� (Excel 2007 �Ŏn�܂郊�{���� **[�\��]** �^�u�A����шȑO�̃o�[�W�����ł� **[�c�[��]** ���j���[����A�N�Z�X�ł��܂�) ����Ăяo���ꂽ�ꍇ�ɂ̂� DLL �Ŏg�p�ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="3b9db-130">**xlSet** behaves as a Class 3 command-equivalent function; that is, it is available only inside a DLL when the DLL is called from an object, macro, menu, toolbar, shortcut key, or the **Run** button in the **Macro** dialog box (accessed from **View** tab on the ribbon starting in Excel 2007, and the **Tools** menu in earlier versions).</span></span> 
  
## <a name="example"></a><span data-ttu-id="3b9db-131">��</span><span class="sxs-lookup"><span data-stu-id="3b9db-131">Example</span></span>

<span data-ttu-id="3b9db-p108">���̗�ł́A�}�N������n���ꂽ�l�� B205:B206 �ɓ��͂���܂��B���̃R�}���h�֐��̗�ɂ͈������K�v�ł���A **Application.Run** ���\�b�h��g�p���āAXLM �}�N�� �V�[�g�� VBA ���W���[������Ăяo�����ꍇ�ɂ̂ݓ��삵�܂��B</span><span class="sxs-lookup"><span data-stu-id="3b9db-p108">The following example fills B205:B206 with the value that was passed in from a macro. This command function example requires an argument, and so will only work if called from an XLM macro sheet, or from a VBA module using the **Application.Run** method.</span></span> 
  
`\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlSetExample(short int iVal)
{
   XLOPER12 xRef, xValue;
   xRef.xltype = xltypeSRef;
   xRef.val.sref.count = 1;
   xRef.val.sref.ref.rwFirst = 204;
   xRef.val.sref.ref.rwLast = 205;
   xRef.val.sref.ref.colFirst = 1;
   xRef.val.sref.ref.colLast = 1;
   xValue.xltype = xltypeInt;
   xValue.val.w = iVal;
   Excel12(xlSet, 0, 2, (LPXLOPER12)&xRef, (LPXLOPER12)&xValue);
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="3b9db-134">�֘A����</span><span class="sxs-lookup"><span data-stu-id="3b9db-134">See also</span></span>

- [<span data-ttu-id="3b9db-135">xlCoerce</span><span class="sxs-lookup"><span data-stu-id="3b9db-135">xlCoerce</span></span>](xlcoerce.md)
- [<span data-ttu-id="3b9db-136">DLL �܂��� XLL ����̂݌Ăяo���\�� C API �֐�</span><span class="sxs-lookup"><span data-stu-id="3b9db-136">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

