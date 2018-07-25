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
# <a name="dialogmsgproc"></a>DIALOGMsgProc

**適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
この手順は [fShowDialog](fshowdialog.md) が表示する Windows のネイティブ ダイアログ ボックスに関連するものです。 この手順で、ユーザーによるダイアログ ボックスのボタン、入力フィールド、またはコントロールのいずれかの操作時に発生するイベント (メッセージ) 用に Windows が呼び出すサービス ルーチンを用意します。 
  
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

