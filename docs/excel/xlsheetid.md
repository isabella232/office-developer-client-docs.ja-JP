---
title: xlSheetId
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSheetId
keywords:
- xlsheetid function [excel 2007]
localization_priority: Normal
ms.assetid: cb32059c-b899-49cf-8028-ff828998ab75
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: e4e184d4e456ffe26292fe31b1b41463834216f9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798989"
---
# <a name="xlsheetid"></a><span data-ttu-id="77d27-104">xlSheetId</span><span class="sxs-lookup"><span data-stu-id="77d27-104">xlSheetId</span></span>

<span data-ttu-id="77d27-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="77d27-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="77d27-106">�O���Q�Ƃ�쐬���邽�߂ɁA���O�t���̃V�[�g�̃V�[�g ID ��������܂��B</span><span class="sxs-lookup"><span data-stu-id="77d27-106">Finds the sheet ID of a named sheet in order to construct external references.</span></span>
  
```cs
Excel12(xlSheetId, LPXLOPER12 pxRes, 1, LPXLOPER12 pxSheetName);
```

## <a name="parameters"></a><span data-ttu-id="77d27-107">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="77d27-107">Parameters</span></span>

<span data-ttu-id="77d27-108">_pxSheetName_(**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="77d27-108">_pxSheetName_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="77d27-109">(省略可能)。</span><span class="sxs-lookup"><span data-stu-id="77d27-109">(Optional).</span></span> <span data-ttu-id="77d27-110">詳細を確認するブックとシートの名前です。</span><span class="sxs-lookup"><span data-stu-id="77d27-110">The name of the book and sheet you want to find out about.</span></span> <span data-ttu-id="77d27-111">省略した場合、 **xlSheetId**関数は、(前面) のアクティブ シートのシート ID を返します。</span><span class="sxs-lookup"><span data-stu-id="77d27-111">If omitted, the **xlSheetId** function returns the sheet ID of the active (front) sheet.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="77d27-112">�߂�l</span><span class="sxs-lookup"><span data-stu-id="77d27-112">Return value</span></span>

<span data-ttu-id="77d27-113">_pxRes-\>val.mref.idSheet_ �̃V�[�g ID ��Ԃ��܂��B</span><span class="sxs-lookup"><span data-stu-id="77d27-113">Returns the sheet ID in  _pxRes-\>val.mref.idSheet_.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="77d27-114"> _pxRes-\>val.mref.lpmref_ �z��|�C���^�[�́A���̌Ăяo���̌�� NULL �ɐݒ肳��邽�߁A **xlFree** ��Ăяo���āA���̃^�C�v�ɒʏ�܂܂�Ă��郁������������K�v�͂���܂��� (����͊��S�Ɉ��S�ł����K�v����܂���)�B</span><span class="sxs-lookup"><span data-stu-id="77d27-114">The  _pxRes-\>val.mref.lpmref_ array pointer is set to NULL after this call so that there is no need to call **xlFree** to release the memory that this type normally contains, although it is completely safe to do so.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="77d27-115">����</span><span class="sxs-lookup"><span data-stu-id="77d27-115">Remarks</span></span>

<span data-ttu-id="77d27-p102">�w�肳�ꂽ�V�[�g��܂ރu�b�N�́A���̊֐���g�p���邽�߂ɊJ���Ă���K�v������܂��BDLL ����J���Ă��Ȃ��u�b�N�ւ̎Q�Ƃ�쐬������@�͂���܂���B **xlSheetId** ��g�p�����Q�Ƃ̍쐬�̏ڍׂɂ��ẮA�u [Excel �̃������Ǘ�](memory-management-in-excel.md)�v�� **xltypeRef** �쐬�̗��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="77d27-p102">The workbook containing the specified sheet must be open to use this function. There is no way to construct a reference to an unopened workbook from a DLL. For more information about using **xlSheetId** to construct references, see [Memory Management in Excel](memory-management-in-excel.md) for examples of **xltypeRef** construction.</span></span> 
  
## <a name="example"></a><span data-ttu-id="77d27-119">��</span><span class="sxs-lookup"><span data-stu-id="77d27-119">Example</span></span>

 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlSheetIdExample(void)
{       
   XLOPER12 xSheetName, xRes;
   xSheetName.xltype = xltypeStr;
   xSheetName.val.str = L"\022[BOOK1.XLSX]Sheet1";
   Excel12(xlSheetId, &xRes, 1, (LPXLOPER12)&xSheetName);
   Excel12f(xlcAlert, 0, 1, TempNum12(xRes.val.mref.idSheet));
   Excel12(xlFree, 0, 1, (LPXLOPER12)&xRes);
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="77d27-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="77d27-120">See also</span></span>

- [<span data-ttu-id="77d27-121">xlSheetNm</span><span class="sxs-lookup"><span data-stu-id="77d27-121">xlSheetNm</span></span>](xlsheetnm.md)
- [<span data-ttu-id="77d27-122">DLL �܂��� XLL ����̂݌Ăяo���\�� C API �֐�</span><span class="sxs-lookup"><span data-stu-id="77d27-122">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

