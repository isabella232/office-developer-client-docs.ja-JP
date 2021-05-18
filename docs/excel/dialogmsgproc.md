---
title: DIALOGMsgProc
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- DIALOGMsgProc
keywords:
- dialogmsgproc function [excel 2007]
localization_priority: Normal
ms.assetid: 9a538e83-ba34-4806-bb8c-7cda3beb6b66
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 1de1b73f5672067f07518ef3367d77349395a1c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406515"
---
# <a name="dialogmsgproc"></a><span data-ttu-id="6eba1-104">DIALOGMsgProc</span><span class="sxs-lookup"><span data-stu-id="6eba1-104">DIALOGMsgProc</span></span>

<span data-ttu-id="6eba1-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="6eba1-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="6eba1-p101">This procedure is associated with the native Windows dialog box that [fShowDialog](fshowdialog.md) displays. It provides the service routines called by Windows for the events (messages) that occur when the user operates one of the dialog box's buttons, entry fields, or controls.</span><span class="sxs-lookup"><span data-stu-id="6eba1-p101">This procedure is associated with the native Windows dialog box that [fShowDialog](fshowdialog.md) displays. It provides the service routines called by Windows for the events (messages) that occur when the user operates one of the dialog box's buttons, entry fields, or controls.</span></span> 
  
```cs
BOOL CALLBACK DIALOGMsgProc(HWND hWndDlg, UINT message, WPARAM wParam, LPARAM lParam);
```

## <a name="parameters"></a><span data-ttu-id="6eba1-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6eba1-108">Parameters</span></span>

 <span data-ttu-id="6eba1-109">_hWndDlg_ (**HWND**)</span><span class="sxs-lookup"><span data-stu-id="6eba1-109">_hWndDlg_ (**HWND**)</span></span>
  
<span data-ttu-id="6eba1-110">ダイアログ ボックスの HWND Windows ハンドルを含んでいます。</span><span class="sxs-lookup"><span data-stu-id="6eba1-110">Contains the HWND Windows handle of the dialog box.</span></span>
  
 <span data-ttu-id="6eba1-111">_message_ (**UINT**)</span><span class="sxs-lookup"><span data-stu-id="6eba1-111">_message_ (**UINT**)</span></span>
  
<span data-ttu-id="6eba1-112">応答メッセージ</span><span class="sxs-lookup"><span data-stu-id="6eba1-112">The message to respond to.</span></span>
  
 <span data-ttu-id="6eba1-113">_wParam_ (**WPARAM**)</span><span class="sxs-lookup"><span data-stu-id="6eba1-113">_wParam_ (**WPARAM**)</span></span>
  
 <span data-ttu-id="6eba1-114">_lParam_ (**LPARAM**)</span><span class="sxs-lookup"><span data-stu-id="6eba1-114">_lParam_ (**LPARAM**)</span></span>
  
<span data-ttu-id="6eba1-115">Windows より渡される引数</span><span class="sxs-lookup"><span data-stu-id="6eba1-115">Arguments passed by Windows.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="6eba1-116">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="6eba1-116">Property value/Return value</span></span>

 <span data-ttu-id="6eba1-117">メッセージが処理された場合は **TRUE**、そうでない場合は **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="6eba1-117">**TRUE** if message processed, **FALSE** if not.</span></span> 
  
### <a name="example"></a><span data-ttu-id="6eba1-118">例</span><span class="sxs-lookup"><span data-stu-id="6eba1-118">Example</span></span>

<span data-ttu-id="6eba1-119">この関数のソース コードについては、`\SAMPLES\GENERIC\GENERIC.C` を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6eba1-119">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6eba1-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="6eba1-120">See also</span></span>



[<span data-ttu-id="6eba1-121">汎用 DLL の関数</span><span class="sxs-lookup"><span data-stu-id="6eba1-121">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

