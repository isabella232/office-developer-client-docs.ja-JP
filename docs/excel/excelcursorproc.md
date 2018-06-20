---
title: ExcelCursorProc
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- ExcelCursorProc
keywords:
- excelcursorproc function [excel 2007]
localization_priority: Normal
ms.assetid: 43759617-998d-4030-a17d-c4bbe35ffaf9
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 07be8da4a07b988d5e848048a088859b58ea3a14
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798872"
---
# <a name="excelcursorproc"></a><span data-ttu-id="cfe76-104">ExcelCursorProc</span><span class="sxs-lookup"><span data-stu-id="cfe76-104">ExcelCursorProc</span></span>

 <span data-ttu-id="cfe76-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="cfe76-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="cfe76-106">Microsoft Excel のウィンドウをモーダル ダイアログ ボックスが表示されたら、カーソルは、Excel ウィンドウの上でビジー カーソルが。</span><span class="sxs-lookup"><span data-stu-id="cfe76-106">When a modal dialog box is displayed over the Microsoft Excel window, the cursor is a busy cursor over the Excel window.</span></span> <span data-ttu-id="cfe76-107">この**WndProc**トラップ WM_SETCURSOR では、Windows メッセージと、カーソルが通常の矢印に戻す変更を入力します。</span><span class="sxs-lookup"><span data-stu-id="cfe76-107">This **WndProc** traps WM_SETCURSOR type Windows messages and changes the cursor back to a normal arrow.</span></span> 
  
```cs
LRESULT CALLBACK ExcelCursorProc(HWND hwnd, UINT wMsg, WPARAM wParam, LPARAM lParam);
```

## <a name="parameters"></a><span data-ttu-id="cfe76-108">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="cfe76-108">Parameters</span></span>

 <span data-ttu-id="cfe76-109">_hWndDlg_(**HWND**)</span><span class="sxs-lookup"><span data-stu-id="cfe76-109">_hWndDlg_ (**HWND**)</span></span>
  
<span data-ttu-id="cfe76-110">�_�C�A���O �{�b�N�X�� HWND Windows �n���h����܂�ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="cfe76-110">Contains the HWND Windows handle of the dialog box.</span></span>
  
 <span data-ttu-id="cfe76-111">_メッセージ_(**UINT**)</span><span class="sxs-lookup"><span data-stu-id="cfe76-111">_message_ (**UINT**)</span></span>
  
<span data-ttu-id="cfe76-112">�������b�Z�[�W</span><span class="sxs-lookup"><span data-stu-id="cfe76-112">The message to respond to.</span></span>
  
 <span data-ttu-id="cfe76-113">_wParam_(**WPARAM**)</span><span class="sxs-lookup"><span data-stu-id="cfe76-113">_wParam_ (**WPARAM**)</span></span>
  
 <span data-ttu-id="cfe76-114">_lParam_(**LPARAM**)</span><span class="sxs-lookup"><span data-stu-id="cfe76-114">_lParam_ (**LPARAM**)</span></span>
  
<span data-ttu-id="cfe76-115">Windows ���n��������</span><span class="sxs-lookup"><span data-stu-id="cfe76-115">Arguments passed by Windows.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="cfe76-116">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="cfe76-116">Property value/Return value</span></span>

<span data-ttu-id="cfe76-117">LRESULT:���b�Z�[�W���n���h�����ꂽ�ꍇ�� 0�A����ȊO�̏ꍇ�́A����� **WndProc** ����Ԃ���錋�ʁB</span><span class="sxs-lookup"><span data-stu-id="cfe76-117">LRESULT: 0 if the message was handled, otherwise the result returned by the default **WndProc**.</span></span>
  
### <a name="example"></a><span data-ttu-id="cfe76-118">��</span><span class="sxs-lookup"><span data-stu-id="cfe76-118">Example</span></span>

<span data-ttu-id="cfe76-119">���̊֐��̃\�[�X �R�[�h�ɂ��ẮA `\SAMPLES\GENERIC\GENERIC.C` ��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="cfe76-119">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cfe76-120">�֘A����</span><span class="sxs-lookup"><span data-stu-id="cfe76-120">See also</span></span>



[<span data-ttu-id="cfe76-121">�ėp DLL �̊֐�</span><span class="sxs-lookup"><span data-stu-id="cfe76-121">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

