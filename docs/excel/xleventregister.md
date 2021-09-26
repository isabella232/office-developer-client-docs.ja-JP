---
title: xlEventRegister
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: b98637d4-02e3-4dbd-8be5-6b46d32980c6
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: c5236a2859b69a45481b4eedd587b923dbe0776e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59631490"
---
# <a name="xleventregister"></a>xlEventRegister

 **適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
Excel 2010 で導入されたイベント ハンドラーの登録に使用します。
  
```vb
Excel12(xlEventRegister, LPXLOPER12 pxRes, 2, LPXLOPER12 pxProcedure, LPXLOPER12 pxEvent);
```

## <a name="parameters"></a>パラメーター

 _pxProcedure_ (**xltypeStr**)
  
DLL コードで示されている、イベント ハンドラー関数の名前。
  
 _pxEvent_ (**xltypeInt**)
  
_pxProcedure_ パラメーターで指定した関数によって処理されるイベント。 
  
Excel 2010 以降の Excel では、次のイベントをサポートしています。
  
|**イベント**|**説明**|
|:-----|:-----|
|**xleventCalculationEnded** <br/> |Excel が計算を完了したときに発生します。計算中に割り当てたリソースは、このイベントの後で解放できます。  <br/> |
|**xleventCalculationCanceled** <br/> |ユーザーが計算を中断すると発生します。XLL はすべての非同期アクティビティを停止します。このイベントの直後に、CalculationEnded イベントが発生します。  <br/> |
   
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

成功した場合、pxRes (**xltypeInt**) の値は 0 >されます。 成功しなかった場合、pxRes ==0。
  
## <a name="see-also"></a>関連項目



[非同期のユーザー定義関数](asynchronous-user-defined-functions.md)

