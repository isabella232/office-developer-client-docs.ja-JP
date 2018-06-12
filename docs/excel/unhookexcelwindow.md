---
title: UnhookExcelWindow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- UnhookExcelWindow
keywords:
- unhookexcelwindow function
localization_priority: Normal
ms.assetid: 6508cb69-0c7c-4d8c-a466-dd79eb13e316
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 7b70bf4ed0ff45921df407605baa692c7621bca4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798959"
---
# <a name="unhookexcelwindow"></a><span data-ttu-id="46126-104">UnhookExcelWindow</span><span class="sxs-lookup"><span data-stu-id="46126-104">UnhookExcelWindow</span></span>

 <span data-ttu-id="46126-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="46126-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="46126-p101">**HookExcelWindow** �ɂ���ĈȑO�ɃC���X�g�[�����ꂽ **ExcelCursorProc** ��폜���܂��B����́AMicrosoft Excel ���C�� **WndProc** �̑O�� **ExcelCursorProc** ���Ăяo�����Ƃ��Ɏ��s����܂��B</span><span class="sxs-lookup"><span data-stu-id="46126-p101">Removes the **ExcelCursorProc** that was previously installed by **HookExcelWindow**. This would have been done so that **ExcelCursorProc** was called before the Microsoft Excel main **WndProc**.</span></span>
  
```cs
extern void FAR PASCAL UnhookExcelWindow(HANDLE hWndExcel);
```

## <a name="parameters"></a><span data-ttu-id="46126-108">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="46126-108">Parameters</span></span>

 <span data-ttu-id="46126-109">_hWndExcel_(**処理**)</span><span class="sxs-lookup"><span data-stu-id="46126-109">_hWndExcel_ (**HANDLE**)</span></span>
  
<span data-ttu-id="46126-110">Excel �̃��C�� �E�B���h�E �n���h���B</span><span class="sxs-lookup"><span data-stu-id="46126-110">The Excel main Windows handle.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="46126-111">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="46126-111">Property value/Return value</span></span>

<span data-ttu-id="46126-112">���̊֐��͒l��Ԃ��܂���B</span><span class="sxs-lookup"><span data-stu-id="46126-112">The function does not return a value.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="46126-113">����</span><span class="sxs-lookup"><span data-stu-id="46126-113">Remarks</span></span>

<span data-ttu-id="46126-114">���̊֐��́A **SetWindowLong()** ��g�p���� Excel ����� **WndProc** �𕜌����A **HookExcelWindow()** �ɂ���ĕۑ����ꂽ�A�h���X�𕜌����܂��B</span><span class="sxs-lookup"><span data-stu-id="46126-114">This function restores the Excel default **WndProc** using **SetWindowLong()** to restore the address that was saved by **HookExcelWindow()**.</span></span>
  
### <a name="example"></a><span data-ttu-id="46126-115">��</span><span class="sxs-lookup"><span data-stu-id="46126-115">Example</span></span>

<span data-ttu-id="46126-116">���̊֐��̃\�[�X �R�[�h�ɂ��ẮA `\SAMPLES\GENERIC\GENERIC.C` ��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="46126-116">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="46126-117">�֘A����</span><span class="sxs-lookup"><span data-stu-id="46126-117">See also</span></span>



[<span data-ttu-id="46126-118">�ėp DLL �̊֐�</span><span class="sxs-lookup"><span data-stu-id="46126-118">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

