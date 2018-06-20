---
title: xlfGetName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
keywords:
- xlfgetname
localization_priority: Normal
ms.assetid: 65780435-aaa2-47af-b44f-07be7aa769ee
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 63bfc6e94950a621c2367b2d35d25e3de48b344f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798971"
---
# <a name="xlfgetname"></a><span data-ttu-id="d6487-104">xlfGetName</span><span class="sxs-lookup"><span data-stu-id="d6487-104">xlfGetName</span></span>

<span data-ttu-id="d6487-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d6487-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="d6487-106">**定義名**] セクションで [**数式**] タブの **[名前の管理**] をクリックするときに表示される [**名前の管理**] ダイアログ ボックスの**参照先**の列に表示される名前の定義を返します。定義に参照が含まれている場合、それらが r1c1 形式の参照として与えられます。</span><span class="sxs-lookup"><span data-stu-id="d6487-106">Returns the definition of a name as it appears in the **Refers to** column of the **Name Manager** dialog box, which is displayed when you click **Name Manager** in the **Defined Names** section on the **Formulas** tab. If the definition contains references, they are given as R1C1-style references.</span></span> <span data-ttu-id="d6487-107">**XlfGetName**を使用して、名前によって定義された値を確認します。</span><span class="sxs-lookup"><span data-stu-id="d6487-107">Use **xlfGetName** to check the value defined by a name.</span></span> <span data-ttu-id="d6487-108">定義に対応する名前を取得するには、 [xlfGetDef](xlfgetdef.md)を使用します。</span><span class="sxs-lookup"><span data-stu-id="d6487-108">To get the name that corresponds to a definition, use [xlfGetDef](xlfgetdef.md).</span></span>
  
```cpp
Excel12(xlfGetName, LPXLOPER12 pxRes, 2, LPXLOPER12 pxNameText, LPXLOPER12 pxInfoType);
```

## <a name="parameters"></a><span data-ttu-id="d6487-109">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="d6487-109">Parameters</span></span>

<span data-ttu-id="d6487-110">_pxNameText_(**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="d6487-110">_pxNameText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="d6487-111">名前に定義できるシートです。アクティブ ブックに定義された名前への外部参照`"!Sales"`です。特定開いているブックで、たとえば、定義された名前への外部参照、または`"[Book1]SHEET1!Sales"`。</span><span class="sxs-lookup"><span data-stu-id="d6487-111">Can be a name defined on the sheet; an external reference to a name defined on the active workbook, for example,  `"!Sales"`; or an external reference to a name defined on a particular open workbook, for example,  `"[Book1]SHEET1!Sales"`.</span></span>  <span data-ttu-id="d6487-112">_pxNameText_は、名前は非表示もできます。</span><span class="sxs-lookup"><span data-stu-id="d6487-112">_pxNameText_ can also be a hidden name.</span></span> 
  
<span data-ttu-id="d6487-113">_pxInfoType_(**xltypeBool**)</span><span class="sxs-lookup"><span data-stu-id="d6487-113">_pxInfoType_ (**xltypeBool**)</span></span>
  
<span data-ttu-id="d6487-p103">���O�ɂ��ĕԂ������̎�ނ�w�肵�܂��B **FALSE** �܂��͏ȗ�����ƁA��\*\*\*\* ����Ă���� **TRUE** ��Ԃ��A���O���u�b�N�S�̂ɑ΂��Ē�\`����Ă���� **FALSE** ��Ԃ��܂��B</span><span class="sxs-lookup"><span data-stu-id="d6487-p103">Specifies the type of information to return about the name. If **FALSE** or omitted, the definition is returned. If **TRUE**, returns **TRUE** if the name is defined for just the sheet, **FALSE** if the name is defined for the entire workbook.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="d6487-117">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="d6487-117">Property value/Return value</span></span>

<span data-ttu-id="d6487-118">_pxRes_(**xltypeStr**、 **xltypeBool**、または**xltypeErr**)</span><span class="sxs-lookup"><span data-stu-id="d6487-118">_pxRes_ (**xltypeStr**, **xltypeBool**, or **xltypeErr**)</span></span>
  
<span data-ttu-id="d6487-119">_PxInfoType_に渡される値によって、指定した名前 (**xltypeStr**) または**TRUE**または**FALSE** (**xltypeBool**) の定義を返します。</span><span class="sxs-lookup"><span data-stu-id="d6487-119">Depending on the value passed for  _pxInfoType_, returns the definition of the specified name (**xltypeStr**), or **TRUE** or **FALSE** (**xltypeBool**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d6487-120">����</span><span class="sxs-lookup"><span data-stu-id="d6487-120">Remarks</span></span>

<span data-ttu-id="d6487-p104">**[�V�[�g�̕ی�]** �**�C�A���O �{�b�N�X�� **[�V�[�g�ƃ��b�N���ꂽ�Z���̓�e��ی삷��]** �\*\*\*\*#N/A` �G���[�l��Ԃ��܂��B `#N/A\` �**�C�A���O �{�b�N�X��\������ɂ́A **[�Z�{]** �^�u�� **[�ύX]** �Z�N�V�����ɂ��� **[�V�[�g�̕ی�]** ��N���b�N���܂��B</span><span class="sxs-lookup"><span data-stu-id="d6487-p104">If the **Protect worksheet and contents of locked cells** check box has been selected in the **Protect Sheet** dialog box to protect the workbook containing the name, **xlfGetName** returns the  `#N/A` error value. To see the **Protect Sheet** dialog box, click **Protect Sheet** in the **Changes** section of the **Review** tab.</span></span> 
  
<span data-ttu-id="d6487-123">���̕\�ɁA�����  **pxNameText** ������w�肵��. _xlfGetDef_ ��Ăяo�����ꍇ�ɕԂ����l�̗�� 3 �����܂��B</span><span class="sxs-lookup"><span data-stu-id="d6487-123">The following table lists three examples of the values returned by a call to **xlfGetDef** with the specified  _pxNameText_ argument.</span></span> 
  
|<span data-ttu-id="d6487-124">**Excel �ɂ������\`**</span><span class="sxs-lookup"><span data-stu-id="d6487-124">**Definition in Excel**</span></span>|<span data-ttu-id="d6487-125">**_pxNameText_**</span><span class="sxs-lookup"><span data-stu-id="d6487-125">**_pxNameText_**</span></span>|<span data-ttu-id="d6487-126">**�߂�l**</span><span class="sxs-lookup"><span data-stu-id="d6487-126">**Value Returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d6487-127">�V�[�g�Ŗ��O [Sales] �����l 523 �Ƃ��Ē�\`����Ă��܂��B</span><span class="sxs-lookup"><span data-stu-id="d6487-127">The name Sales on a sheet is defined as the number 523.</span></span>  <br/> |<span data-ttu-id="d6487-128">"Sales"</span><span class="sxs-lookup"><span data-stu-id="d6487-128">"Sales"</span></span>  <br/> |<span data-ttu-id="d6487-129">"=523"</span><span class="sxs-lookup"><span data-stu-id="d6487-129">"=523"</span></span>  <br/> |
|<span data-ttu-id="d6487-130">�A�N�e�B�u�ȃV�[�g�Ŗ��O [Profit] ���A���� =Sales-Costs �Ƃ��Ē�\`����Ă��܂��B</span><span class="sxs-lookup"><span data-stu-id="d6487-130">The name Profit on the active sheet is defined as the formula =Sales-Costs.</span></span>  <br/> |<span data-ttu-id="d6487-131">"!Profit"</span><span class="sxs-lookup"><span data-stu-id="d6487-131">"!Profit"</span></span>  <br/> |<span data-ttu-id="d6487-132">"=Sales-Costs"</span><span class="sxs-lookup"><span data-stu-id="d6487-132">"=Sales-Costs"</span></span>  <br/> |
|<span data-ttu-id="d6487-133">�A�N�e�B�u �V�[�g�Ŗ��O [Database] ���A�͈� A1:F500 �Ƃ��Ē�\`����Ă��܂��B</span><span class="sxs-lookup"><span data-stu-id="d6487-133">The name Database on the active sheet is defined as the range A1:F500.</span></span>  <br/> |<span data-ttu-id="d6487-134">"!Database"</span><span class="sxs-lookup"><span data-stu-id="d6487-134">"!Database"</span></span>  <br/> |<span data-ttu-id="d6487-135">"=R1C1:R500C6"</span><span class="sxs-lookup"><span data-stu-id="d6487-135">"=R1C1:R500C6"</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d6487-136">�֘A����</span><span class="sxs-lookup"><span data-stu-id="d6487-136">See also</span></span>

- [<span data-ttu-id="d6487-137">xlfGetDef</span><span class="sxs-lookup"><span data-stu-id="d6487-137">xlfGetDef</span></span>](xlfgetdef.md)
- [<span data-ttu-id="d6487-138">�d�v�Ŗ�ɗ��� C API XLM �֐�</span><span class="sxs-lookup"><span data-stu-id="d6487-138">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

