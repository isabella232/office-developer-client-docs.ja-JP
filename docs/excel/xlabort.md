---
title: xlAbort
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAbort
keywords:
- xlabort function [excel 2007]
localization_priority: Normal
ms.assetid: 0fe71454-6b00-464b-8abf-afb209d57754
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 08ab69252520e76a5631c5e32a3970d2d95b1ff4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436658"
---
# <a name="xlabort"></a>xlAbort

 **適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
システム内の他のタスクにプロセッサを生成し、ユーザーが **Esc** を押してマクロを取り消したかどうかを確認します。ブックの再計算中にユーザーが **Esc** が押した場合は、この関数を呼び出すことによってワークシート関数内で検出することもできます。 
  
```cs
Excel12(xlAbort, LPXLOPER12 pxRes, 1, LPXLOPER12 pxRetain);
```

## <a name="parameters"></a>パラメーター

 _pxRetain_ (**xltypeBool**)
  
(Optional). If **FALSE**, this function checks for the break condition and clears any pending break. This enables the user to continue despite the break condition. If this argument is omitted or is **TRUE**, the function checks for a user abort without clearing it.
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

ユーザーが **Esc** を押した場合は、**TRUE** (**xltypeBool**) が返されます。
  
## <a name="remarks"></a>注釈

### 

#### <a name="frequent-calls-may-be-needed"></a>頻繁な呼び出しが必要な場合

時間のかかる関数やコマンドでは、この関数を頻繁に呼び出して、プロセッサをシステム内の他のタスクに生成する必要があります。
  
#### <a name="avoid-sensitive-language"></a>微妙な表現を避ける

ユーザー インターフェイスでは "Abort" という用語を使用しないようにします。代わりに "Cancel"、"Halt"、"Break"、"Stop" の使用を検討してください。
  
## <a name="example"></a>例

次のコードは、1 分が経過するまで、またはユーザーが **Esc** を押すまで、シート上でアクティブなセルを繰り返し移動し、**xlAbort** 関数を呼び出します。これによりプロセッサが生成され、共同でのマルチタスキングが容易になります。 
  
 `\SAMPLES\GENERIC\GENERIC.C`
  
```cs
int WINAPI fDance(void)
{
   DWORD dtickStart;
   XLOPER12 xAbort, xConfirm;
   int boolSheet;
   int col=0;
   XCHAR rgch[32];
//
// Check what kind of sheet is active. If it is a worksheet or macro
// sheet, this function will move the selection in a loop to show
// activity. In any case, it will update the status bar with a countdown.
//
// Call xlSheetId; if that fails the current sheet is not a macro sheet or
// worksheet. Next, get the time at which to start. Then start a while
// loop that will run for one minute. During the while loop, check if the
// user has pressed ESC. If true, confirm the abort. If the abort is
// confirmed, clear the message bar and return; if the abort is not
// confirmed, clear the abort state and continue. After checking for an
// abort, move the active cell if on a worksheet or macro. Then
// update the status bar with the time remaining.
//
// This block uses TempActiveCell12(), which creates a temporary XLOPER12.
// The XLOPER12 contains a reference to a single cell on the active sheet.
// This function is part of the framework library.
//
   boolSheet = (Excel12f(xlSheetId, 0, 0) == xlretSuccess);
   dtickStart = GetTickCount();
   while (GetTickCount() < dtickStart + 60000L)
   {
      Excel12f(xlAbort, &xAbort, 0);
      if (xAbort.val.xbool)
      {
         Excel12f(xlcAlert, &xConfirm, 2,
           TempStr12(L"Are you sure you want to cancel this operation?"),
              TempNum12(1));
         if (xConfirm.val.xbool)
         {
            Excel12f(xlcMessage, 0, 1, TempBool12(0));
            return 1;
         }
         else
         {
            Excel12f(xlAbort, 0, 1, TempBool12(0));
         }
      }
      if (boolSheet)
      {
         Excel12f(xlcSelect, 0, 1,
            TempActiveCell12(0,(BYTE)col));
         col = (col + 1) & 3;
      }
      wsprintfW(rgch,L"0:%lu",
         (60000 + dtickStart - GetTickCount()) / 1000L);
      Excel12f(xlcMessage, 0, 2, TempBool12(1), TempStr12(rgch));
   }
   Excel12f(xlcMessage, 0, 1, TempBool12(0));
   return 1;
}
```

## <a name="see-also"></a>関連項目



[DLL または XLL からのみ呼び出し可能な C API 関数](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

