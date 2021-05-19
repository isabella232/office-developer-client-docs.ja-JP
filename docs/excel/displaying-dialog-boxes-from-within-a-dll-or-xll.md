---
title: DLL または XLL ファイルの中からダイアログ ボックスを表示する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- 'xlls [excel 2007], displaying dialog boxes from,dialog boxes [Excel 2007], displaying from a DLL or XLL,DLLs [Excel 2007], displaying dialog boxes from ms.prod: office-online-server localization_priority: Normal ms.assetid: e77ac555-331d-41c8-a000-7b178959754d'
localization_priority: Normal
ms.assetid: e77ac555-331d-41c8-a000-7b178959754d
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 7b00430b047fe792afef701d210ccde06dd16216
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417869"
---
# <a name="displaying-dialog-boxes-from-within-a-dll-or-xll"></a><span data-ttu-id="a7016-104">DLL または XLL ファイルの中からダイアログ ボックスを表示する</span><span class="sxs-lookup"><span data-stu-id="a7016-104">Displaying Dialog Boxes from Within a DLL or XLL</span></span>

 <span data-ttu-id="a7016-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a7016-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="a7016-106">Windows SDK 関数 **DialogBox** などを使用して、Win32 ダイアログ ボックスを表示するには、最初に完全な 32 ビットのインスタンスと、Excel のメイン ウィンドウ ハンドルを取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a7016-106">To display a Win32 dialog box using, for example, the Windows SDK function **DialogBox**, you must first obtain the full 32-bit instance and main window handles for Excel.</span></span> <span data-ttu-id="a7016-107">詳細については、「[Excel インスタンスとメイン ウィンドウ ハンドルへのアクセス](how-to-access-excel-instance-and-main-window-handles.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a7016-107">For more information, see [Access Excel Instance and Main Window Handles](how-to-access-excel-instance-and-main-window-handles.md).</span></span> 
  
<span data-ttu-id="a7016-p102">Assuming your project contains the dialog box resource, you must take several steps to set the message-handling routine to that of the newly displayed dialog box and to restore the Excel message handling routine when the dialog box is closed. The example command [fShowDialog](fshowdialog.md) in the Generic project demonstrates the use of the Windows functions to do this correctly.</span><span class="sxs-lookup"><span data-stu-id="a7016-p102">Assuming your project contains the dialog box resource, you must take several steps to set the message-handling routine to that of the newly displayed dialog box and to restore the Excel message handling routine when the dialog box is closed. The example command [fShowDialog](fshowdialog.md) in the Generic project demonstrates the use of the Windows functions to do this correctly.</span></span> 
  
<span data-ttu-id="a7016-p103">C API を使用しても、ダイアログ ボックスを表示できます。この場合、Windows SDK 関数を使用する必要はありません。ただし、C API のダイアログ ボックスは、Windows、Visual Basic for Applications (VBA)、または Microsoft Foundation Classes (MFC) のものと比べて、機能が非常に制限されています。(たとえば、C API ダイアログ ボックスは常にモーダルです)。</span><span class="sxs-lookup"><span data-stu-id="a7016-p103">You can also display dialog boxes using the C API without having to use Windows SDK functions. However, the dialog box capabilities of the C API are very limited compared with those of Windows, Visual Basic for Applications (VBA), or the Microsoft Foundation Classes (MFC). (For example, C API dialog boxes are always modal).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a7016-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="a7016-113">See also</span></span>



[<span data-ttu-id="a7016-114">XLL を作成する</span><span class="sxs-lookup"><span data-stu-id="a7016-114">Creating XLLs</span></span>](creating-xlls.md)
  
[<span data-ttu-id="a7016-115">DLL の開発</span><span class="sxs-lookup"><span data-stu-id="a7016-115">Developing DLLs</span></span>](developing-dlls.md)
  
[<span data-ttu-id="a7016-116">Excel インスタンスとメイン ウィンドウ ハンドルへのアクセス</span><span class="sxs-lookup"><span data-stu-id="a7016-116">Access Excel Instance and Main Window Handles</span></span>](how-to-access-excel-instance-and-main-window-handles.md)
  
[<span data-ttu-id="a7016-117">DLL または XLL からのみ呼び出し可能な C API 関数</span><span class="sxs-lookup"><span data-stu-id="a7016-117">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

