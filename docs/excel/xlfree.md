---
title: xlFree
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlFree
keywords:
- xlfree function [excel 2007]
localization_priority: Normal
ms.assetid: 8ce2eef2-0138-495d-b6cb-bbb727a3cda4
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 2dd61ee5cd0e2e671cc47425689287b8a437732f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798984"
---
# <a name="xlfree"></a><span data-ttu-id="a7831-104">xlFree</span><span class="sxs-lookup"><span data-stu-id="a7831-104">xlFree</span></span>

 <span data-ttu-id="a7831-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a7831-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="a7831-p101">**Excel4**�A/ �A**Excel12**�A�܂��� [Excel12v](excel4-excel12.md) �̌Ăяo���Ŗ߂�l [XLOPER](excel4v-excel12v.md)[](excel4-excel12.md)[XLOPER12](excel4v-excel12v.md) ��쐬����Ƃ��ɁAMicrosoft Excel �����蓖�Ă������� ���\�[�X�������邽�߂Ɏg�p���܂��B **xlFree** �֐��͕⏕�������������A�|�C���^�[�� **NULL** �Ƀ��Z�b�g���܂����A **XLOPER**/ **XLOPER12**�̑��̕����͔j�����܂���B</span><span class="sxs-lookup"><span data-stu-id="a7831-p101">Used to free memory resources allocated by Microsoft Excel when creating the return value **XLOPER**/ **XLOPER12** in a call to [Excel4](excel4-excel12.md), [Excel4v](excel4v-excel12v.md), [Excel12](excel4-excel12.md), or [Excel12v](excel4v-excel12v.md). The **xlFree** function frees the auxiliary memory and resets the pointer to **NULL** but does not destroy other parts of the **XLOPER**/ **XLOPER12**.</span></span>
  
```cs
Excel4(xlFree, 0, n, LPXLOPER px_1, ..., LPXLOPER px_n);
Excel12(xlFree, 0, n, LPXLOPER12 px_1, ..., LPXLOPER12 px_n);
```

## <a name="parameters"></a><span data-ttu-id="a7831-108">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="a7831-108">Parameters</span></span>

 <span data-ttu-id="a7831-109">_px_1, ..., px_n_</span><span class="sxs-lookup"><span data-stu-id="a7831-109">_px_1, ..., px_n_</span></span>
  
<span data-ttu-id="a7831-p102">1 �ȏ�� **XLOPER**/ **XLOPER12** �������܂��BExcel 2003 �܂ł̃o�[�W�����ł́A�n����|�C���^�[�̍ő吔�� 30 �ł��BExcel 2007 �ȍ~�́A255 �ɑ�������܂����B</span><span class="sxs-lookup"><span data-stu-id="a7831-p102">One or more **XLOPER**/ **XLOPER12**s to be freed. In Excel versions up to 2003, the maximum number of pointers that can be passed is 30. Starting in Excel 2007, this is increased to 255.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="a7831-113">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="a7831-113">Property value/Return value</span></span>

<span data-ttu-id="a7831-114">���̊֐��͒l��Ԃ��܂���B</span><span class="sxs-lookup"><span data-stu-id="a7831-114">This function does not return a value.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a7831-115">����</span><span class="sxs-lookup"><span data-stu-id="a7831-115">Remarks</span></span>

<span data-ttu-id="a7831-p103">**Excel4** �܂��� **Excel4v** ����߂�l�Ƃ��Ď擾���� **XLOPER**�A����� **Excel12** �܂��� **Excel12v** ����߂�l�Ƃ��Ď擾���� **XLOPER12** �́A�^�� **xltypeStr**�A **xltypeMulti**�A�܂��� **xltypeRef** �̂����ꂩ�̏ꍇ�͂��ׂĉ������K�v������܂��B���̌^�������Ă�A���ꂪ **Excel4** �܂��� **Excel12** ����擾������̂ł������A���Ƃ����ꂪ�⏕��������g�p���Ȃ��ꍇ�ł�A��肪�����邱�Ƃ͂���܂���B</span><span class="sxs-lookup"><span data-stu-id="a7831-p103">You must free every **XLOPER** that you get as a return value from **Excel4** or **Excel4v** and every **XLOPER12** that you get as a return value from **Excel12** or **Excel12v** if they are one of the following types: **xltypeStr**, **xltypeMulti**, or **xltypeRef**. It is always safe to free other types even if they do not use auxiliary memory, as long as you got them from **Excel4** or **Excel12**.</span></span>
  
<span data-ttu-id="a7831-118">����Ώۂ� Excel �����蓖�Ă���������܂� **XLOPER**/ **XLOPER12**�ւ̃|�C���^�[�� Excel �ɖ߂��ꍇ�A **xlbitXLFree** ��ݒ肵�� Excel �Ƀ�������m���ɉ�������܂��B</span><span class="sxs-lookup"><span data-stu-id="a7831-118">Where you are returning to Excel a pointer to an **XLOPER**/ **XLOPER12** that still contains Excel-allocated memory to be freed, you must set the **xlbitXLFree** to ensure Excel releases the memory.</span></span> 
  
## <a name="example"></a><span data-ttu-id="a7831-119">��</span><span class="sxs-lookup"><span data-stu-id="a7831-119">Example</span></span>

<span data-ttu-id="a7831-p104">���̗�ł� **GET.WORKSPACE(1)** ��Ăяo���AExcel ����s���̃v���b�g�t�H�[���𕶎���Ƃ��ĕԂ��܂��B�R�[�h�͕Ԃ��ꂽ��������Ŏg�p���邽�߂Ƀo�b�t�@�[�ɃR�s�[���܂��B�R�[�h�͂��̃o�b�t�@�[���� Excel �֐��Ŏg�p���邽�߂� **XLOPER12** �ɖ߂��܂��B�Ō�ɁA�R�[�h�͌x���{�b�N�X�ɕ������\�����܂��B</span><span class="sxs-lookup"><span data-stu-id="a7831-p104">This example calls **GET.WORKSPACE(1)** to return the platform on which Excel is currently running as a string. The code copies this returned string into a buffer for later use. The code places the buffer back into the **XLOPER12** for later use with the Excel function. Finally, the code displays the string in an alert box.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlFreeExample(void)
{
   XLOPER12 xRes, xInt;
   XCHAR buffer[cchMaxStz];
   int i,len;
   // Create an XLOPER12 for the argument to Getworkspace.
   xInt.xltype = xltypeInt;
   xInt.val.w = 1;
   // Call GetWorkspace.
   Excel12f(xlfGetWorkspace, &xRes, 1, (LPXLOPER12)&xInt);
   
   // Get the length of the returned string
   len = (int)xRes.val.str[0];
   //Take into account 1st char, which contains the length
   //and the null terminator. Truncate if necessary to fit
   //buffer.
   if (len > cchMaxStz - 2)
      len = cchMaxStz - 2;
   // Copy to buffer.
   for(i = 1; i <= len; i++)
      buffer[i] = xRes.val.str[i];
   // Null terminate, Not necessary but a good idea.
   buffer[len] = '\0';
   buffer[0] = len;
   // Free the string returned from Excel.
   Excel12f(xlFree, 0, 1, &xRes);
   // Create a new string XLOPER12 for the alert.
   xRes.xltype = xltypeStr;
   xRes.val.str = buffer;
   // Show the alert.
   Excel12f(xlcAlert, 0, 1, (LPXLOPER12)&xRes);
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="a7831-124">�֘A����</span><span class="sxs-lookup"><span data-stu-id="a7831-124">See also</span></span>

- [<span data-ttu-id="a7831-125">DLL �܂��� XLL ����̂݌Ăяo���\�� C API �֐�</span><span class="sxs-lookup"><span data-stu-id="a7831-125">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

