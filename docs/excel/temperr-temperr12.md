---
title: TempErr/TempErr12
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempErr
- TempErr12
keywords:
- temperr function [excel 2007],TempErr12 function [Excel 2007]
localization_priority: Normal
ms.assetid: cf8c26b2-ca2b-4dda-a02d-0ccbeac19106
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 22c0ff1b8259fc0e5ee70edb06bb3db53781ff8c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798943"
---
# <a name="temperrtemperr12"></a><span data-ttu-id="ef5d8-104">TempErr/TempErr12</span><span class="sxs-lookup"><span data-stu-id="ef5d8-104">TempErr/TempErr12</span></span>

 <span data-ttu-id="ef5d8-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="ef5d8-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="ef5d8-106">Microsoft Excel ���[�N�V�[�g�̃G���[��܂ވꎞ **XLOPER**/ **XLOPER12**��쐬����t���[�����[�N ���C�u�����֐��B</span><span class="sxs-lookup"><span data-stu-id="ef5d8-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** containing a Microsoft Excel worksheet error.</span></span> 
  
```cs
LPXLOPER TempErr(WORD err);
LPXLOPER12 TempErr12(BOOL err);
```

## <a name="parameters"></a><span data-ttu-id="ef5d8-107">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="ef5d8-107">Parameters</span></span>

 <span data-ttu-id="ef5d8-108">_err_</span><span class="sxs-lookup"><span data-stu-id="ef5d8-108">_err_</span></span>
  
<span data-ttu-id="ef5d8-109">�ړI�̃G���[ �R�[�h�܂��̓��e�������l�Ɠ����̐��l����̕\�Ɏ����܂��B</span><span class="sxs-lookup"><span data-stu-id="ef5d8-109">The desired error code, or its literal numeric equivalent, as shown in the following table.</span></span>
  
|<span data-ttu-id="ef5d8-110">**�G���[**</span><span class="sxs-lookup"><span data-stu-id="ef5d8-110">**Error**</span></span>|<span data-ttu-id="ef5d8-111">**XLCALL.H �Œ�\`���ꂽ�G���[ �R�[�h**</span><span class="sxs-lookup"><span data-stu-id="ef5d8-111">**Error code defined in XLCALL.H**</span></span>|<span data-ttu-id="ef5d8-112">**������ 10 �i��**</span><span class="sxs-lookup"><span data-stu-id="ef5d8-112">**Decimal equivalent**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ef5d8-113">#NULL</span><span class="sxs-lookup"><span data-stu-id="ef5d8-113">#NULL</span></span>  <br/> |<span data-ttu-id="ef5d8-114">**xlerrNull**</span><span class="sxs-lookup"><span data-stu-id="ef5d8-114">**xlerrNull**</span></span> <br/> |<span data-ttu-id="ef5d8-115">0</span><span class="sxs-lookup"><span data-stu-id="ef5d8-115">0</span></span>  <br/> |
|<span data-ttu-id="ef5d8-116">#DIV/0!</span><span class="sxs-lookup"><span data-stu-id="ef5d8-116">#DIV/0!</span></span>  <br/> |<span data-ttu-id="ef5d8-117">**xlerrDiv0**</span><span class="sxs-lookup"><span data-stu-id="ef5d8-117">**xlerrDiv0**</span></span> <br/> |<span data-ttu-id="ef5d8-118">7</span><span class="sxs-lookup"><span data-stu-id="ef5d8-118">7</span></span>  <br/> |
|<span data-ttu-id="ef5d8-119">#VALUE!</span><span class="sxs-lookup"><span data-stu-id="ef5d8-119">#VALUE!</span></span>  <br/> |<span data-ttu-id="ef5d8-120">**xlerrValue**</span><span class="sxs-lookup"><span data-stu-id="ef5d8-120">**xlerrValue**</span></span> <br/> |<span data-ttu-id="ef5d8-121">15</span><span class="sxs-lookup"><span data-stu-id="ef5d8-121">15</span></span>  <br/> |
|<span data-ttu-id="ef5d8-122">#REF!</span><span class="sxs-lookup"><span data-stu-id="ef5d8-122">#REF!</span></span>  <br/> |<span data-ttu-id="ef5d8-123">**xlerrRef**</span><span class="sxs-lookup"><span data-stu-id="ef5d8-123">**xlerrRef**</span></span> <br/> |<span data-ttu-id="ef5d8-124">23</span><span class="sxs-lookup"><span data-stu-id="ef5d8-124">23</span></span>  <br/> |
|<span data-ttu-id="ef5d8-125">#NAME?</span><span class="sxs-lookup"><span data-stu-id="ef5d8-125">#NAME?</span></span>  <br/> |<span data-ttu-id="ef5d8-126">**xlerrName**</span><span class="sxs-lookup"><span data-stu-id="ef5d8-126">**xlerrName**</span></span> <br/> |<span data-ttu-id="ef5d8-127">29</span><span class="sxs-lookup"><span data-stu-id="ef5d8-127">29</span></span>  <br/> |
|<span data-ttu-id="ef5d8-128">#NUM!</span><span class="sxs-lookup"><span data-stu-id="ef5d8-128">#NUM!</span></span>  <br/> |<span data-ttu-id="ef5d8-129">**xlerrNum**</span><span class="sxs-lookup"><span data-stu-id="ef5d8-129">**xlerrNum**</span></span> <br/> |<span data-ttu-id="ef5d8-130">36</span><span class="sxs-lookup"><span data-stu-id="ef5d8-130">36</span></span>  <br/> |
|<span data-ttu-id="ef5d8-131">#N/A</span><span class="sxs-lookup"><span data-stu-id="ef5d8-131">#N/A</span></span>  <br/> |<span data-ttu-id="ef5d8-132">**xlerrNA**</span><span class="sxs-lookup"><span data-stu-id="ef5d8-132">**xlerrNA**</span></span> <br/> |<span data-ttu-id="ef5d8-133">42</span><span class="sxs-lookup"><span data-stu-id="ef5d8-133">42</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="ef5d8-134">�߂�l</span><span class="sxs-lookup"><span data-stu-id="ef5d8-134">Return value</span></span>

<span data-ttu-id="ef5d8-135">�n���ꂽ�G���[ �R�[�h��܂� **xltypeBool** ��Ԃ��܂��B</span><span class="sxs-lookup"><span data-stu-id="ef5d8-135">Returns an **xltypeBool** containing the error code passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="ef5d8-136">��</span><span class="sxs-lookup"><span data-stu-id="ef5d8-136">Example</span></span>

<span data-ttu-id="ef5d8-p101">���̗�ł́A **TempErr12** �֐���g�p���� #VALUE! �G���[�� Excel �ɕԂ��܂��B</span><span class="sxs-lookup"><span data-stu-id="ef5d8-p101">This example uses the **TempErr12** function to return a #VALUE! error to Excel.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="ef5d8-p102">[!����] �t���[�����[�N ���C�u�����֐� **TempErr12** �́A����o�b�t�@�[���烁��������蓖�Ă܂��B���̃������́A�ʏ�A�t���[�����[�N�֐� **Excel12f** ���Ăяo�����Ɖ������܂��B���̗�̊֐����A **Excel12f** ��Ăяo�����ɌJ��Ԃ��Ăяo�����ƁA������ ���[�N���������܂��B</span><span class="sxs-lookup"><span data-stu-id="ef5d8-p102">The Framework library function **TempErr12** allocates memory from an internal buffer, which is normally freed when the Framework function **Excel12f** is called. If this example function is called repeatedly without **Excel12f** being called, a memory leak occurs.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
LPXLOPER WINAPI TempErrExample(void)
{
    return TempErr12(xlerrValue);
}
```

## <a name="see-also"></a><span data-ttu-id="ef5d8-141">�֘A����</span><span class="sxs-lookup"><span data-stu-id="ef5d8-141">See also</span></span>



<span data-ttu-id="ef5d8-142">[�t���[�����[�N ���C�u�����̊֐�](functions-in-the-framework-library.md)</span><span class="sxs-lookup"><span data-stu-id="ef5d8-142">[Functions in the Framework Library](functions-in-the-framework-library.md)</span></span>

