---
title: xlfGetDef
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
keywords:
- xlfgetdef
localization_priority: Normal
ms.assetid: 68f5edbd-9040-46d3-acd5-dd51ca82f6fa
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 030c4e501e8a9eb4b6ce29d7fe0e171324b50b5c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798992"
---
# <a name="xlfgetdef"></a><span data-ttu-id="5fda1-104">xlfGetDef</span><span class="sxs-lookup"><span data-stu-id="5fda1-104">xlfGetDef</span></span>

<span data-ttu-id="5fda1-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="5fda1-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="5fda1-106">テキストで特定の領域、値、またはブック内の数式で定義されている名前を返します。</span><span class="sxs-lookup"><span data-stu-id="5fda1-106">Returns the name, as text, that is defined for a particular area, value, or formula in a workbook.</span></span> <span data-ttu-id="5fda1-107">Excel では、この値を取得する使用**xlfGetDef**の [**数式**] タブで**定義された名前**] セクションで **[名前の管理**] をクリックするときに表示される [**名前の管理**] ダイアログ ボックスの [**名前**] 列で、定義に対応する名前です。</span><span class="sxs-lookup"><span data-stu-id="5fda1-107">In Excel, this value is displayed in the **Name** column of the **Name Manager** dialog box, which is displayed when you click **Name Manager** in the **Defined Names** section on the **Formulas** tab. Use **xlfGetDef** to get the name that corresponds to a definition.</span></span> <span data-ttu-id="5fda1-108">名前の定義を取得するには、 [xlfGetName](xlfgetname.md)を使用します。</span><span class="sxs-lookup"><span data-stu-id="5fda1-108">To get the definition of a name, use [xlfGetName](xlfgetname.md).</span></span>
  
```cpp
Excel12(xlfGetDef, LPXLOPER12 pxRes, 3, LPXLOPER12 pxDefText, LPXLOPER12 pxDocumentText, LPXLOPER12 pxTypeNum);
```

## <a name="parameters"></a><span data-ttu-id="5fda1-109">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="5fda1-109">Parameters</span></span>

<span data-ttu-id="5fda1-110">_pxDefText_(**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="5fda1-110">_pxDefText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="5fda1-111">�Q�ƁA�l�A�I�u�W�F�N�g�A�����ȂǁA�Q�Ɛ�̖��O�Ƃ��Ē�\`�ł��邠�����̂�w��ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="5fda1-111">Can be anything you can define a name to refer to, including a reference, a value, an object, or a formula.</span></span>
  
<span data-ttu-id="5fda1-p102">�Q�Ƃ̏ꍇ�́A `"R3C5"` �Ȃǂ� R1C1 �X�^�C���Ŏw�肷��K�v������܂��B  _pxDefText_ ���l�܂��͐����̏ꍇ�A **[���O�̊Ǘ�]** �_�C�A���O �{�b�N�X�� **[�Q�Ɣ͈�]** ��ɕ\������铙�� (=) ��܂߂�K�v�͂���܂���B  _pxDefText_ �ɕ����̖��O�����݂���ꍇ�A **xlfGetDef** �͍ŏ��̖��O��Ԃ��܂��B  _pxDefText_ �ƈ�v���閼�O�����݂��Ȃ��ꍇ�A **xlfGetDef** ��  `#NAME?` �G���[�l��Ԃ��܂��B</span><span class="sxs-lookup"><span data-stu-id="5fda1-p102">References must be given in R1C1 style, such as  `"R3C5"`. If  _pxDefText_ is a value or formula, it is not necessary to include the equal sign that is displayed in the **Refers To** column in the **Name Manager** dialog box. If there is more than one name for  _pxDefText_, **xlfGetDef** returns the first name. If no name matches  _pxDefText_, **xlfGetDef** returns the  `#NAME?` error value.</span></span> 
  
<span data-ttu-id="5fda1-116">_pxDocumentText_(**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="5fda1-116">_pxDocumentText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="5fda1-p103">_pxDefText_ �����݂���V�[�g��w�肵�܂��B  _pxDocumentText_ ���ȗ������ƁA�A�N�e�B�u�ȃV�[�g�Ƃ��đz�肳��܂��B</span><span class="sxs-lookup"><span data-stu-id="5fda1-p103">Specifies the sheet that  _pxDefText_ is on. If  _pxDocumentText_ is omitted, it is assumed to be the active sheet.</span></span> 
  
<span data-ttu-id="5fda1-119">_pxTypeNum_(**xltypeNum**)</span><span class="sxs-lookup"><span data-stu-id="5fda1-119">_pxTypeNum_ (**xltypeNum**)</span></span>
  
<span data-ttu-id="5fda1-120">�Ԃ����O�̎�ނ�w�肷��A1 ���� 3 �͈̔͂̐��l�ł��B</span><span class="sxs-lookup"><span data-stu-id="5fda1-120">A number from 1 to 3 specifying which types of names are returned.</span></span>
  
|<span data-ttu-id="5fda1-121">**_pxTypeNum_**</span><span class="sxs-lookup"><span data-stu-id="5fda1-121">**_pxTypeNum_**</span></span>|<span data-ttu-id="5fda1-122">**�߂�l**</span><span class="sxs-lookup"><span data-stu-id="5fda1-122">**Returns**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5fda1-123">1 �܂��͏ȗ�</span><span class="sxs-lookup"><span data-stu-id="5fda1-123">1 or omitted</span></span>  <br/> |<span data-ttu-id="5fda1-124">�W�����̂݁B</span><span class="sxs-lookup"><span data-stu-id="5fda1-124">Normal names only.</span></span>  <br/> |
|<span data-ttu-id="5fda1-125">2</span><span class="sxs-lookup"><span data-stu-id="5fda1-125">2</span></span>  <br/> |<span data-ttu-id="5fda1-126">��\�����̂݁B</span><span class="sxs-lookup"><span data-stu-id="5fda1-126">Hidden names only.</span></span>  <br/> |
|<span data-ttu-id="5fda1-127">3</span><span class="sxs-lookup"><span data-stu-id="5fda1-127">3</span></span>  <br/> |<span data-ttu-id="5fda1-128">���ׂĂ̖��O�B</span><span class="sxs-lookup"><span data-stu-id="5fda1-128">All names.</span></span>  <br/> |
   
## <a name="property-valuereturn-value"></a><span data-ttu-id="5fda1-129">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="5fda1-129">Property value/Return value</span></span>

 <span data-ttu-id="5fda1-130">_pxRes_(**xltypeStr**または**xltypeErr**)</span><span class="sxs-lookup"><span data-stu-id="5fda1-130">_pxRes_ (**xltypeStr** or **xltypeErr**)</span></span>
  
<span data-ttu-id="5fda1-131">�w��̒�\`�Ɋ֘A�t�����Ă��閼�O��Ԃ��܂��B</span><span class="sxs-lookup"><span data-stu-id="5fda1-131">Returns the name associated with the specified definition.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5fda1-132">����</span><span class="sxs-lookup"><span data-stu-id="5fda1-132">Remarks</span></span>

<span data-ttu-id="5fda1-133">���̕\�ɁA����̈�����w�肵�� **xlfGetDef** ��Ăяo�����ꍇ�ɕԂ����l�̗�� 4 �����܂��B</span><span class="sxs-lookup"><span data-stu-id="5fda1-133">The following table lists four examples of the values returned by a call to **xlfGetDef** with the specified arguments.</span></span> 
  
|<span data-ttu-id="5fda1-134">**Excel �Œ�\`���ꂽ���O**</span><span class="sxs-lookup"><span data-stu-id="5fda1-134">**Name defined in Excel**</span></span>|<span data-ttu-id="5fda1-135">**_pxDefText_**</span><span class="sxs-lookup"><span data-stu-id="5fda1-135">**_pxDefText_**</span></span>|<span data-ttu-id="5fda1-136">**_pxDocumentText_**</span><span class="sxs-lookup"><span data-stu-id="5fda1-136">**_pxDocumentText_**</span></span>|<span data-ttu-id="5fda1-137">**_pxTypeNum_**</span><span class="sxs-lookup"><span data-stu-id="5fda1-137">**_pxTypeNum_**</span></span>|<span data-ttu-id="5fda1-138">**�߂�l**</span><span class="sxs-lookup"><span data-stu-id="5fda1-138">**Value Returned**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="5fda1-139">Sheet4 �̎w��͈̔͂ɂ́uSales�v�Ƃ������O���t���Ă��܂��B</span><span class="sxs-lookup"><span data-stu-id="5fda1-139">The specified range in Sheet4 is named Sales.</span></span>  <br/> |<span data-ttu-id="5fda1-140">"R2C2:R9C6"</span><span class="sxs-lookup"><span data-stu-id="5fda1-140">"R2C2:R9C6"</span></span>  <br/> |<span data-ttu-id="5fda1-141">"Sheet4"</span><span class="sxs-lookup"><span data-stu-id="5fda1-141">"Sheet4"</span></span>  <br/> |<span data-ttu-id="5fda1-142">\<�ȗ�\></span><span class="sxs-lookup"><span data-stu-id="5fda1-142">\<omitted\></span></span>  <br/> |<span data-ttu-id="5fda1-143">"Sales"</span><span class="sxs-lookup"><span data-stu-id="5fda1-143">"Sales"</span></span>  <br/> |
|<span data-ttu-id="5fda1-144">Sheet4 �̒l 100 �́A�uConstant�v�Ƃ��Ē�\`����Ă��܂��B</span><span class="sxs-lookup"><span data-stu-id="5fda1-144">The value 100 in Sheet4 is defined as Constant.</span></span>  <br/> |<span data-ttu-id="5fda1-145">"100"</span><span class="sxs-lookup"><span data-stu-id="5fda1-145">"100"</span></span>  <br/> |<span data-ttu-id="5fda1-146">"Sheet4"</span><span class="sxs-lookup"><span data-stu-id="5fda1-146">"Sheet4"</span></span>  <br/> |<span data-ttu-id="5fda1-147">\<�ȗ�\></span><span class="sxs-lookup"><span data-stu-id="5fda1-147">\<omitted\></span></span>  <br/> |<span data-ttu-id="5fda1-148">"Constant"</span><span class="sxs-lookup"><span data-stu-id="5fda1-148">"Constant"</span></span>  <br/> |
|<span data-ttu-id="5fda1-149">Sheet4 �̎w��̐����ɂ́uSumTotal�v�Ƃ������O���t���Ă��܂��B</span><span class="sxs-lookup"><span data-stu-id="5fda1-149">The specified formula in Sheet4 is named SumTotal.</span></span>  <br/> |<span data-ttu-id="5fda1-150">"SUM(R1C1:R10C1)"</span><span class="sxs-lookup"><span data-stu-id="5fda1-150">"SUM(R1C1:R10C1)"</span></span>  <br/> |<span data-ttu-id="5fda1-151">"Sheet4"</span><span class="sxs-lookup"><span data-stu-id="5fda1-151">"Sheet4"</span></span>  <br/> |<span data-ttu-id="5fda1-152">\<�ȗ�\></span><span class="sxs-lookup"><span data-stu-id="5fda1-152">\<omitted\></span></span>  <br/> |<span data-ttu-id="5fda1-153">"SumTotal"</span><span class="sxs-lookup"><span data-stu-id="5fda1-153">"SumTotal"</span></span>  <br/> |
|<span data-ttu-id="5fda1-154">�A�N�e�B�u�ȃV�[�g�̔�\�����uCounter�v�Ƃ��� 3 ����\`����Ă��܂��B</span><span class="sxs-lookup"><span data-stu-id="5fda1-154">3 is defined as the hidden name Counter on the active sheet.</span></span>  <br/> |<span data-ttu-id="5fda1-155">"3"</span><span class="sxs-lookup"><span data-stu-id="5fda1-155">"3"</span></span>  <br/> |<span data-ttu-id="5fda1-156">\<�ȗ�\></span><span class="sxs-lookup"><span data-stu-id="5fda1-156">\<omitted\></span></span>  <br/> |<span data-ttu-id="5fda1-157">2</span><span class="sxs-lookup"><span data-stu-id="5fda1-157">2</span></span>  <br/> |<span data-ttu-id="5fda1-158">"Counter"</span><span class="sxs-lookup"><span data-stu-id="5fda1-158">"Counter"</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5fda1-159">�֘A����</span><span class="sxs-lookup"><span data-stu-id="5fda1-159">See also</span></span>

- [<span data-ttu-id="5fda1-160">xlfGetName</span><span class="sxs-lookup"><span data-stu-id="5fda1-160">xlfGetName</span></span>](xlfgetname.md)
- [<span data-ttu-id="5fda1-161">�d�v�Ŗ�ɗ��� C API XLM �֐�</span><span class="sxs-lookup"><span data-stu-id="5fda1-161">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

