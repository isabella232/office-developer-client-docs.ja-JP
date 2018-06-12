---
title: xlEventRegister
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b98637d4-02e3-4dbd-8be5-6b46d32980c6
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: d837d87c479f70f0184a7cf1612dea5ab8c99e6d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798975"
---
# <a name="xleventregister"></a><span data-ttu-id="5c95f-103">xlEventRegister</span><span class="sxs-lookup"><span data-stu-id="5c95f-103">xlEventRegister</span></span>

 <span data-ttu-id="5c95f-104">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="5c95f-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="5c95f-p101">�C�x���g �n���h���[�̓o�^�Ɏg�p���܂��BExcel 2010 �ɓ�������܂����B</span><span class="sxs-lookup"><span data-stu-id="5c95f-p101">Used to register an event handler. Introduced in Excel 2010.</span></span>
  
```vb
Excel12(xlEventRegister, LPXLOPER12 pxRes, 2, LPXLOPER12 pxProcedure, LPXLOPER12 pxEvent);
```

## <a name="parameters"></a><span data-ttu-id="5c95f-107">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="5c95f-107">Parameters</span></span>

 <span data-ttu-id="5c95f-108">_pxProcedure_(**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="5c95f-108">_pxProcedure_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="5c95f-109">DLL �R�[�h�Ŏ�����Ă���A�C�x���g �n���h���[�֐��̖��O�B</span><span class="sxs-lookup"><span data-stu-id="5c95f-109">The name of the event handler function as it appears in the DLL code.</span></span>
  
 <span data-ttu-id="5c95f-110">_pxEvent_(**xltypeInt**)</span><span class="sxs-lookup"><span data-stu-id="5c95f-110">_pxEvent_ (**xltypeInt**)</span></span>
  
<span data-ttu-id="5c95f-111">_pxProcedure_ �p�����[�^�[�Ŏw�肵���֐��ŏ��������C�x���g�B</span><span class="sxs-lookup"><span data-stu-id="5c95f-111">The event handled by the function designated in the  _pxProcedure_ parameter.</span></span> 
  
<span data-ttu-id="5c95f-112">Excel 2010 �ȍ~�� Excel �ł́A���̃C�x���g��T�|�[�g���Ă��܂��B</span><span class="sxs-lookup"><span data-stu-id="5c95f-112">Starting in Excel 2010, Excel supports the following events:</span></span>
  
|<span data-ttu-id="5c95f-113">**�C�x���g**</span><span class="sxs-lookup"><span data-stu-id="5c95f-113">**Event**</span></span>|<span data-ttu-id="5c95f-114">**���**</span><span class="sxs-lookup"><span data-stu-id="5c95f-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5c95f-115">**xleventCalculationEnded**</span><span class="sxs-lookup"><span data-stu-id="5c95f-115">**xleventCalculationEnded**</span></span> <br/> |<span data-ttu-id="5c95f-p102">Excel ���v�Z����������Ƃ��ɔ������܂��B�v�Z���Ɋ��蓖�Ă����\�[�X�́A���̃C�x���g�̌�ŉ���ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="5c95f-p102">Raised when Excel completes a calculation. You can free any resources allocated during the calculation after this event.</span></span>  <br/> |
|<span data-ttu-id="5c95f-118">**xleventCalculationCanceled**</span><span class="sxs-lookup"><span data-stu-id="5c95f-118">**xleventCalculationCanceled**</span></span> <br/> |<span data-ttu-id="5c95f-p103">���[�U�[���v�Z�𒆒f�����Ƃ��ɔ������܂��BXLL �́A������񓯊��̃A�N�e�B�r�e�B���~���܂��B���̃C�x���g�̒���ɁACalculationEnded �C�x���g���������܂��B</span><span class="sxs-lookup"><span data-stu-id="5c95f-p103">Raised when the user interrupts the calculation. The XLL should stop any asynchronous activities. The CalculationEnded event is raised immediately following this event.</span></span>  <br/> |
   
## <a name="property-valuereturn-value"></a><span data-ttu-id="5c95f-122">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="5c95f-122">Property value/Return value</span></span>

<span data-ttu-id="5c95f-123">成功した場合は、 **TRUE** (**xltypeBool**) を返します。</span><span class="sxs-lookup"><span data-stu-id="5c95f-123">If successful, returns **TRUE** (**xltypeBool**).</span></span> <span data-ttu-id="5c95f-124">失敗した場合は、 **FALSE**が返されます。</span><span class="sxs-lookup"><span data-stu-id="5c95f-124">If unsuccessful, returns **FALSE**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5c95f-125">�֘A����</span><span class="sxs-lookup"><span data-stu-id="5c95f-125">See also</span></span>



<span data-ttu-id="5c95f-126">[�񓯊��̃��[�U�[��\`�֐�](asynchronous-user-defined-functions.md)</span><span class="sxs-lookup"><span data-stu-id="5c95f-126">[Asynchronous User-Defined Functions](asynchronous-user-defined-functions.md)</span></span>

