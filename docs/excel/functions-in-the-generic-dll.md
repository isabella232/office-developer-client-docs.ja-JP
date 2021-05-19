---
title: 汎用 DLL の関数
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- generic dll [excel 2007], functions,functions [Excel 2007], Generic DLL
localization_priority: Normal
ms.assetid: 80ce2247-d69d-45b0-b5e2-4ff0d7078a2c
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3064e1a09ad8850e121da678f3702a6236574599
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420599"
---
# <a name="functions-in-the-generic-dll"></a>汎用 DLL の関数

 **適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
サンプル DLL GENERIC.xll をコンパイルするために必要な Microsoft Visual Studio プロジェクト ファイルとソース コード ファイルは、`\EXAMPLES\GENERIC\` フォルダーに格納されています。このプロジェクトをテンプレートとして使用して独自の Microsoft Excel XLL を作成できます。このプロジェクトのソース コードには、Excel C API の多くの機能が示されています。 
  
GENERIC.xll を読み込むと、次の 4 つのコマンドがある **[Generic]** メニューが作成されます。 
  
- **Dialog** - [Microsoft Excel] ダイアログ ボックスを表示します。 
    
- **Dance** - **ESC** を押すまで選択範囲を移動します。 
    
- **Native Dialog** - [Windows] ダイアログ ボックスを表示します。 
    
- **Exit** - GENERIC.xll をアンロードし、**[Generic]** メニューを削除します。 
    
GENERIC.xll には、ワークシート関数 Func1、FuncSum、および FuncFib も用意されています。GENERIC.xll を読み込むと常に、これらの関数を使用できるようになります。GENERIC.xll は、アドイン マネージャーを使用して読み込むことができます。最後の Excel セッションが正常に終了した時点でアクティブになっていた場合は、その次のセッションでも読み込まれます。
  
このプロジェクトでは、フレームワーク ライブラリ (FRMWRK32.lib) を使用します。
  
## <a name="in-this-section"></a>このセクションの内容

[DIALOGMsgProc](dialogmsgproc.md)
  
[ExcelCursorProc](excelcursorproc.md)
  
[HookExcelWindow](hookexcelwindow.md)
  
[UnhookExcelWindow](unhookexcelwindow.md)
  
[fShowDialog](fshowdialog.md)
  
[fDance](fdance.md)
  
[fDialog/fDialog12](fdialog-fdialog12.md)
  
[fExit](fexit.md)
  
[Func1](func1.md)
  
[FuncSum](funcsum.md)
  
[FuncFib](funcfib.md)
  
## <a name="see-also"></a>関連項目



[フレームワーク ライブラリの関数](functions-in-the-framework-library.md)

