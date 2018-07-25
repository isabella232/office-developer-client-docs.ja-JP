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
# <a name="displaying-dialog-boxes-from-within-a-dll-or-xll"></a>DLL または XLL ファイルの中からダイアログ ボックスを表示する

 **適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
Windows SDK 関数 **DialogBox** などを使用して、Win32 ダイアログ ボックスを表示するには、最初に完全な 32 ビットのインスタンスと、Excel のメイン ウィンドウ ハンドルを取得する必要があります。 詳細については、「[Excel インスタンスとメイン ウィンドウ ハンドルへのアクセス](how-to-access-excel-instance-and-main-window-handles.md)」を参照してください。 
  
プロジェクトにダイアログ ボックスのリソースが含まれていると仮定した場合、新しく表示されるダイアログ ボックスとメッセージ処理ルーチンの設定や、ダイアログ ボックスを閉じたときの Excel メッセージ処理ルーチンの復元のために、いくつかの手順を実行する必要があります。 Generic プロジェクトのコマンド例 [fShowDialog](fshowdialog.md) では、Windows 関数を使用して、これを正しく実行しています。 
  
C API を使用しても、ダイアログ ボックスを表示できます。この場合、Windows SDK 関数を使用する必要はありません。ただし、C API のダイアログ ボックスは、Windows、Visual Basic for Applications (VBA)、または Microsoft Foundation Classes (MFC) のものと比べて、機能が非常に制限されています。(たとえば、C API ダイアログ ボックスは常にモーダルです)。
  
## <a name="see-also"></a>関連項目



[XLL を作成する](creating-xlls.md)
  
[DLL の開発](developing-dlls.md)
  
[Excel インスタンスとメイン ウィンドウ ハンドルへのアクセス](how-to-access-excel-instance-and-main-window-handles.md)
  
[DLL または XLL からのみ呼び出し可能な C API 関数](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

