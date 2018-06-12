---
title: HookExcelWindow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- HookExcelWindow
keywords:
- hookexcelwindow function [excel 2007]
localization_priority: Normal
ms.assetid: 13f0ae5e-9951-4e89-a245-7cf68c6f6724
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 8965cc6b1e3d24001c42744f2ee7d447aa4c79b5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798891"
---
# <a name="hookexcelwindow"></a><span data-ttu-id="1ced0-104">HookExcelWindow</span><span class="sxs-lookup"><span data-stu-id="1ced0-104">HookExcelWindow</span></span>

 <span data-ttu-id="1ced0-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="1ced0-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="1ced0-106">**ExcelCursorProc** ��C���X�g�[�����āAMicrosoft Excel �̃��C�� **WndProc** �̑O�ɌĂяo�����悤�ɂ��܂��B</span><span class="sxs-lookup"><span data-stu-id="1ced0-106">Installs **ExcelCursorProc** so that it is called before the Microsoft Excel main **WndProc**.</span></span>
  
```cs
extern void FAR PASCAL HookExcelWindow(HANDLE hWndExcel);
```

## <a name="parameters"></a><span data-ttu-id="1ced0-107">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="1ced0-107">Parameters</span></span>

 <span data-ttu-id="1ced0-108">_hWndExcel_(**処理**)</span><span class="sxs-lookup"><span data-stu-id="1ced0-108">_hWndExcel_ (**HANDLE**)</span></span>
  
<span data-ttu-id="1ced0-109">Excel �̃��C�� �E�B���h�E �n���h���B</span><span class="sxs-lookup"><span data-stu-id="1ced0-109">The Excel main Windows handle.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="1ced0-110">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="1ced0-110">Property value/Return value</span></span>

<span data-ttu-id="1ced0-111">���̊֐��͒l��Ԃ��܂���B</span><span class="sxs-lookup"><span data-stu-id="1ced0-111">The function does not return a value.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1ced0-112">����</span><span class="sxs-lookup"><span data-stu-id="1ced0-112">Remarks</span></span>

<span data-ttu-id="1ced0-p101">���̊֐��́A **GetWindowLong()** ��g�p���� Excel **WndProc** �̃A�h���X��擾���܂��B����� **WndProc** ��Ăяo���A�������邽�߂Ɏg�p�ł��邱�̒l��O���[�o���Ɋi�[���܂��B�Ō�ɁA **SetWindowLong()** ��g�p���āA���̃A�h���X�� **ExcelCursorProc** �̃A�h���X�ɒu�������܂��B</span><span class="sxs-lookup"><span data-stu-id="1ced0-p101">The function obtains the address of the Excel **WndProc** through the use of **GetWindowLong()**. It stores this value in a global that can be used to call the default **WndProc** and also to restore it. Finally, it replaces this address with the address of **ExcelCursorProc** using **SetWindowLong()**.</span></span>
  
### <a name="example"></a><span data-ttu-id="1ced0-116">��</span><span class="sxs-lookup"><span data-stu-id="1ced0-116">Example</span></span>

<span data-ttu-id="1ced0-117">���̊֐��̃\�[�X �R�[�h�ɂ��ẮA `\SAMPLES\GENERIC\GENERIC.C` ��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="1ced0-117">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1ced0-118">�֘A����</span><span class="sxs-lookup"><span data-stu-id="1ced0-118">See also</span></span>



[<span data-ttu-id="1ced0-119">�ėp DLL �̊֐�</span><span class="sxs-lookup"><span data-stu-id="1ced0-119">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

