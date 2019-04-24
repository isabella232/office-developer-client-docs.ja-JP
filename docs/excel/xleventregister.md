---
title: xlEventRegister
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b98637d4-02e3-4dbd-8be5-6b46d32980c6
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 869122954ffe3928dfea72b8fc9fb432b9979e42
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303935"
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

成功した場合、**TRUE** (**xltypeBool**) を返します。 失敗した場合は、**FALSE** を返します。
  
## <a name="see-also"></a>関連項目



[非同期のユーザー定義関数](asynchronous-user-defined-functions.md)

