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
ms.openlocfilehash: 3a69d192babbcf0419850e203f51d8cfd81cdef6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798773"
---
# <a name="dialogmsgproc"></a><span data-ttu-id="2da89-104">DIALOGMsgProc</span><span class="sxs-lookup"><span data-stu-id="2da89-104">DIALOGMsgProc</span></span>

<span data-ttu-id="2da89-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="2da89-105">Applies to: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="2da89-106">この手順は [fShowDialog](fshowdialog.md) が表示する Windows のネイティブ ダイアログ ボックスに関連するものです。</span><span class="sxs-lookup"><span data-stu-id="2da89-106">This procedure is associated with the native Windows dialog box that [fShowDialog](fshowdialog.md) displays.</span></span> <span data-ttu-id="2da89-107">この手順で、ユーザーによるダイアログ ボックスのボタン、入力フィールド、またはコントロールのいずれかの操作時に発生するイベント (メッセージ) 用に Windows が呼び出すサービス ルーチンを用意します。</span><span class="sxs-lookup"><span data-stu-id="2da89-107">This procedure is associated with the native Windows dialog box that fShowDialog displays. It provides the service routines called by Windows for the events (messages) that occur when the user operates one of the dialog box's buttons, entry fields, or controls.</span></span> 
  
```cs
BOOL CALLBACK DIALOGMsgProc(HWND hWndDlg, UINT message, WPARAM wParam, LPARAM lParam);
```

## <a name="parameters"></a><span data-ttu-id="2da89-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2da89-108">Parameters</span></span>

 <span data-ttu-id="2da89-109">_hWndDlg_ (**HWND**)</span><span class="sxs-lookup"><span data-stu-id="2da89-109">_hWndDlg_ (**HWND**)</span></span>
  
<span data-ttu-id="2da89-110">ダイアログ ボックスの HWND Windows ハンドルを含んでいます。</span><span class="sxs-lookup"><span data-stu-id="2da89-110">Contains the HWND Windows handle of the dialog box.</span></span>
  
 <span data-ttu-id="2da89-111">_message_ (**UINT**)</span><span class="sxs-lookup"><span data-stu-id="2da89-111">_message_ (**UINT**)</span></span>
  
<span data-ttu-id="2da89-112">応答メッセージ</span><span class="sxs-lookup"><span data-stu-id="2da89-112">The message to respond to.</span></span>
  
 <span data-ttu-id="2da89-113">_wParam_ (**WPARAM**)</span><span class="sxs-lookup"><span data-stu-id="2da89-113">_wParam_ (**WPARAM**)</span></span>
  
 <span data-ttu-id="2da89-114">_lParam_ (**LPARAM**)</span><span class="sxs-lookup"><span data-stu-id="2da89-114">_lParam_ (**LPARAM**)</span></span>
  
<span data-ttu-id="2da89-115">Windows より渡される引数</span><span class="sxs-lookup"><span data-stu-id="2da89-115">Arguments passed by Windows.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="2da89-116">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="2da89-116">Property Value/Return Value</span></span>

 <span data-ttu-id="2da89-117">メッセージが処理された場合は **TRUE**、そうでない場合は **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="2da89-117">**TRUE** if message processed, **FALSE** if not.</span></span> 
  
### <a name="example"></a><span data-ttu-id="2da89-118">例</span><span class="sxs-lookup"><span data-stu-id="2da89-118">Example</span></span>

<span data-ttu-id="2da89-119">この関数のソース コードについては、`\SAMPLES\GENERIC\GENERIC.C` を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2da89-119">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2da89-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="2da89-120">See also</span></span>



[<span data-ttu-id="2da89-121">汎用 DLL の関数</span><span class="sxs-lookup"><span data-stu-id="2da89-121">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

