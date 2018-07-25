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
ms.openlocfilehash: afb21125bc54a2607a997c7b2f7c73ef2f528f28
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798782"
---
# <a name="displaying-dialog-boxes-from-within-a-dll-or-xll"></a><span data-ttu-id="df78d-104">DLL または XLL ファイルの中からダイアログ ボックスを表示する</span><span class="sxs-lookup"><span data-stu-id="df78d-104">Displaying Dialog Boxes from Within a DLL or XLL</span></span>

 <span data-ttu-id="df78d-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="df78d-105">Applies to: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="df78d-106">Windows SDK 関数 **DialogBox** などを使用して、Win32 ダイアログ ボックスを表示するには、最初に完全な 32 ビットのインスタンスと、Excel のメイン ウィンドウ ハンドルを取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="df78d-106">To display a Win32 dialog box using, for example, the Windows SDK function **DialogBox**, you must first obtain the full 32-bit instance and main window handles for Excel. For more information, see How to: Access Excel Instance and Main Window Handles.</span></span> <span data-ttu-id="df78d-107">詳細については、「[Excel インスタンスとメイン ウィンドウ ハンドルへのアクセス](how-to-access-excel-instance-and-main-window-handles.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="df78d-107">For more information, see [Access Excel Instance and Main Window Handles](how-to-access-excel-instance-and-main-window-handles.md).</span></span> 
  
<span data-ttu-id="df78d-108">プロジェクトにダイアログ ボックスのリソースが含まれていると仮定した場合、新しく表示されるダイアログ ボックスとメッセージ処理ルーチンの設定や、ダイアログ ボックスを閉じたときの Excel メッセージ処理ルーチンの復元のために、いくつかの手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="df78d-108">Assuming your project contains the dialog box resource, you must take several steps to set the message-handling routine to that of the newly displayed dialog box and to restore the Excel message handling routine when the dialog box is closed. The example command fShowDialog in the Generic project demonstrates the use of the Windows functions to do this correctly.</span></span> <span data-ttu-id="df78d-109">Generic プロジェクトのコマンド例 [fShowDialog](fshowdialog.md) では、Windows 関数を使用して、これを正しく実行しています。</span><span class="sxs-lookup"><span data-stu-id="df78d-109">The example command [fShowDialog](fshowdialog.md) in the Generic project demonstrates the use of the Windows functions to do this correctly.</span></span> 
  
<span data-ttu-id="df78d-p103">C API を使用しても、ダイアログ ボックスを表示できます。この場合、Windows SDK 関数を使用する必要はありません。ただし、C API のダイアログ ボックスは、Windows、Visual Basic for Applications (VBA)、または Microsoft Foundation Classes (MFC) のものと比べて、機能が非常に制限されています。(たとえば、C API ダイアログ ボックスは常にモーダルです)。</span><span class="sxs-lookup"><span data-stu-id="df78d-p103">You can also display dialog boxes using the C API without having to use Windows SDK functions. However, the dialog box capabilities of the C API are very limited compared with those of Windows, Visual Basic for Applications (VBA), or the Microsoft Foundation Classes (MFC). (For example, C API dialog boxes are always modal).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="df78d-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="df78d-113">See also</span></span>



[<span data-ttu-id="df78d-114">XLL を作成する</span><span class="sxs-lookup"><span data-stu-id="df78d-114">Creating XLLs</span></span>](creating-xlls.md)
  
[<span data-ttu-id="df78d-115">DLL の開発</span><span class="sxs-lookup"><span data-stu-id="df78d-115">Developing DLLs</span></span>](developing-dlls.md)
  
[<span data-ttu-id="df78d-116">Excel インスタンスとメイン ウィンドウ ハンドルへのアクセス</span><span class="sxs-lookup"><span data-stu-id="df78d-116">How to: Access Excel Instance and Main Window Handles</span></span>](how-to-access-excel-instance-and-main-window-handles.md)
  
[<span data-ttu-id="df78d-117">DLL または XLL からのみ呼び出し可能な C API 関数</span><span class="sxs-lookup"><span data-stu-id="df78d-117">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

