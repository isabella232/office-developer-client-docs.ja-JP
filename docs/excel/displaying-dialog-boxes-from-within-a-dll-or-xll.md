---
title: DLL または XLL ファイルの中からダイアログ ボックスを表示する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- 'xlls [excel 2007], displaying dialog boxes from,dialog boxes [Excel 2007], displaying from a DLL or XLL,DLLs [Excel 2007], displaying dialog boxes from ms.prod: office-online-server localization_priority: Normal ms.assetid: e77ac555-331d-41c8-a000-7b178959754d'
ms.localizationpriority: medium
ms.assetid: e77ac555-331d-41c8-a000-7b178959754d
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a01cd39c81d88655f7e8c3c865292d657eee2c57
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576703"
---
# <a name="displaying-dialog-boxes-from-within-a-dll-or-xll"></a>DLL または XLL ファイルの中からダイアログ ボックスを表示する

 **適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
Windows SDK 関数 **DialogBox** などを使用して、Win32 ダイアログ ボックスを表示するには、最初に完全な 32 ビットのインスタンスと、Excel のメイン ウィンドウ ハンドルを取得する必要があります。 詳細については、「[Excel インスタンスとメイン ウィンドウ ハンドルへのアクセス](how-to-access-excel-instance-and-main-window-handles.md)」を参照してください。 
  
Assuming your project contains the dialog box resource, you must take several steps to set the message-handling routine to that of the newly displayed dialog box and to restore the Excel message handling routine when the dialog box is closed. The example command [fShowDialog](fshowdialog.md) in the Generic project demonstrates the use of the Windows functions to do this correctly. 
  
C API を使用しても、ダイアログ ボックスを表示できます。この場合、Windows SDK 関数を使用する必要はありません。ただし、C API のダイアログ ボックスは、Windows、Visual Basic for Applications (VBA)、または Microsoft Foundation Classes (MFC) のものと比べて、機能が非常に制限されています。(たとえば、C API ダイアログ ボックスは常にモーダルです)。
  
## <a name="see-also"></a>関連項目



[XLL を作成する](creating-xlls.md)
  
[DLL の開発](developing-dlls.md)
  
[Excel インスタンスとメイン ウィンドウ ハンドルへのアクセス](how-to-access-excel-instance-and-main-window-handles.md)
  
[DLL または XLL からのみ呼び出し可能な C API 関数](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

