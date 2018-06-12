---
title: TempBool/TempBool12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempBool
- TempBool12
keywords:
- tempbool function [excel 2007],TempBool12 function [Excel 2007]
localization_priority: Normal
ms.assetid: 0cf1fa58-416f-4692-a2e3-422473c19492
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 30874e7b918d8cd780bef60b4b02de1319f0f9ab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798946"
---
# <a name="tempbooltempbool12"></a><span data-ttu-id="ea9be-104">TempBool/TempBool12</span><span class="sxs-lookup"><span data-stu-id="ea9be-104">TempBool/TempBool12</span></span>

 <span data-ttu-id="ea9be-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="ea9be-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="ea9be-106">**Boolean** /  �� **FALSE** ��܂ވꎞ **XLOPER********XLOPER12** ��쐬����t���[�����[�N ���C�u�����֐��B</span><span class="sxs-lookup"><span data-stu-id="ea9be-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** containing **Boolean** **TRUE** or **FALSE**.</span></span>
  
```cs
LPXLOPER TempBool(int b);
LPXLOPER12 TempBool12(int b);
```

## <a name="parameters"></a><span data-ttu-id="ea9be-107">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="ea9be-107">Parameters</span></span>

 <span data-ttu-id="ea9be-108">_b_ (**int**)</span><span class="sxs-lookup"><span data-stu-id="ea9be-108">_b_ (**int**)</span></span>
  
<span data-ttu-id="ea9be-109">**FALSE** ��Ԃ��ɂ� 0 ��g�p���܂��B **TRUE** ��Ԃ��ɂ͂���ȊO�̒l��g�p���܂��B</span><span class="sxs-lookup"><span data-stu-id="ea9be-109">Use 0 to return **FALSE**; use any other value to return **TRUE**.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="ea9be-110">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="ea9be-110">Property value/Return value</span></span>

<span data-ttu-id="ea9be-111">�n���ꂽ�_���l��܂� **xltypeBool** **Boolean** ��Ԃ��܂��B</span><span class="sxs-lookup"><span data-stu-id="ea9be-111">Returns an **xltypeBool** **Boolean** containing the logical value passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="ea9be-112">��</span><span class="sxs-lookup"><span data-stu-id="ea9be-112">Example</span></span>

<span data-ttu-id="ea9be-p101">���̗�ł́A **TempBool12** �֐���g�p���ăX�e�[�^�X �o�[��������܂��B [Excel/Excel12f](excel-excel12f.md) �֐����Ăяo�����ƁA�ꎞ���������������܂��B</span><span class="sxs-lookup"><span data-stu-id="ea9be-p101">The following example uses the **TempBool12** function to clear the status bar. Temporary memory is freed when the [Excel/Excel12f](excel-excel12f.md) function is called.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short int WINAPI TempBoolExample(void)
{
    Excel12f(xlcMessage, 0, 1, TempBool12(0));
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="ea9be-115">�֘A����</span><span class="sxs-lookup"><span data-stu-id="ea9be-115">See also</span></span>



<span data-ttu-id="ea9be-116">[�t���[�����[�N ���C�u�����̊֐�](functions-in-the-framework-library.md)</span><span class="sxs-lookup"><span data-stu-id="ea9be-116">[Functions in the Framework Library](functions-in-the-framework-library.md)</span></span>

