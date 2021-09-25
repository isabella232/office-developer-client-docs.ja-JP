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
ms.localizationpriority: medium
ms.assetid: 9a538e83-ba34-4806-bb8c-7cda3beb6b66
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f93be01679460833d9555cc747ff72d9b1d5b6fa
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625967"
---
# <a name="dialogmsgproc"></a>DIALOGMsgProc

**適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
This procedure is associated with the native Windows dialog box that [fShowDialog](fshowdialog.md) displays. It provides the service routines called by Windows for the events (messages) that occur when the user operates one of the dialog box's buttons, entry fields, or controls. 
  
```cs
BOOL CALLBACK DIALOGMsgProc(HWND hWndDlg, UINT message, WPARAM wParam, LPARAM lParam);
```

## <a name="parameters"></a>パラメーター

 _hWndDlg_ (**HWND**)
  
ダイアログ ボックスの HWND Windows ハンドルを含んでいます。
  
 _message_ (**UINT**)
  
応答メッセージ
  
 _wParam_ (**WPARAM**)
  
 _lParam_ (**LPARAM**)
  
Windows より渡される引数
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

 メッセージが処理された場合は **TRUE**、そうでない場合は **FALSE**。 
  
### <a name="example"></a>例

この関数のソース コードについては、`\SAMPLES\GENERIC\GENERIC.C` を参照してください。 
  
## <a name="see-also"></a>関連項目



[汎用 DLL の関数](functions-in-the-generic-dll.md)

