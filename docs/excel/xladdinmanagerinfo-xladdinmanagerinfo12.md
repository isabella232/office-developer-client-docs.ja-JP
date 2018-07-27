---
title: xlAddInManagerInfo/xlAddInManagerInfo12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAddInManagerInfo
keywords:
- xladdinmanagerinfo function [excel 2007]
localization_priority: Normal
ms.assetid: 63a73cd2-6479-4233-ad68-93379f940717
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e42cca809c4426ddf9a98b3b275d08490d31c8db
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798950"
---
# <a name="xladdinmanagerinfoxladdinmanagerinfo12"></a>xlAddInManagerInfo/xlAddInManagerInfo12

 **適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
アドイン マネージャーが Excel セッションで初めて呼び出されたときに、Microsoft Excel によって呼び出されます。この関数は、ご使用のアドインについての情報をアドイン マネージャーに提供するために使用されます。
  
Excel 2007 以降のバージョンでは、XLL によってエクスポートされる場合には **xlAddInManagerInfo** ではなく **xlAddInManagerInfo12** が呼び出されます。**xlAddInManagerInfo12** 関数は、**xlAddInManagerInfo** と同じように機能して、XLL の動作におけるバージョン固有の相違点を回避する必要があります。Excel では **xlAddInManagerInfo12** が **XLOPER12** データ型を返し、**xlAddInManagerInfo** は **XLOPER** データ型を返す必要があります。
  
**xlAddInManagerInfo12** 関数は Excel 2007 より前の Excel バージョンでは呼び出されません。**XLOPER12** をサポートしていないためです。
  
Excel では、XLL がこれらいずれかの関数を実装してエクスポートすることは不要です。
  
```cs
LPXLOPER WINAPI xlAddInManagerInfo(LPXLOPER pxAction);
LPXLOPER12 WINAPI xlAddInManagerInfo12(LPXLOPER12 pxAction);
```

## <a name="parameters"></a>パラメーター

 _pxAction:_ 数値 **XLOPER/XLOPER12** (**xltypeInt** または **xltypeNum**) へのポインター。
  
Excel で要求される情報です。
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

_pxAction_ が数値 1 の場合 (1 になるよう強制することもできます)、この関数を実装すると、アドインについての情報 (通常は名前。バージョン番号が含まれることもあります) が含まれる文字列が返ります。それ以外の場合、#VALUE を返します。 
  
文字列を返さない場合、Excel が戻り値を文字列に変換しようとします。
  
## <a name="remarks"></a>注釈

返される文字列が、動的に割り当てられたバッファーをポイントしている場合は、このバッファーを最終的に解放する必要があります。文字列が Excel によって割り当てられた場合、**xlbitXLFree** を設定して解放します。文字列が DLL によって割り当てられた場合には、**xlbitDLLFree** を設定して解放します。さらに、[xlAutoFree](xlautofree-xlautofree12.md) (**XLOPER** を返す場合) または **xlAutoFree12** (**XLOPER12** を返す場合) も実装しなければなりません。
  
## <a name="example"></a>例

 `\SAMPLES\GENERIC\GENERIC.C`
  
```cs
LPXLOPER12 WINAPI xlAddInManagerInfo12(LPXLOPER12 xAction)
{
    static XLOPER12 xInfo, xIntAction;
/*
** This code coerces the passed-in value to an integer. This is how the
** code determines what is being requested. If it receives a 1, it returns a
** string representing the long name. If it receives anything else, it
** returns a #VALUE! error.
*/
    Excel12f(xlCoerce, &xIntAction, 2, xAction, TempInt12(xltypeInt));
    if(xIntAction.val.w == 1) 
    {
        xInfo.xltype = xltypeStr;
        xInfo.val.str = L"\026Example Standalone DLL";
    }
    else 
    {
        xInfo.xltype = xltypeErr;
        xInfo.val.err = xlerrValue;
    }
// Word of caution - returning static XLOPERs/XLOPER12s is not thread safe
// for UDFs declared as thread safe. Use alternate memory allocation mechanisms.
    return (LPXLOPER12)&xInfo;
} 

```

## <a name="see-also"></a>関連項目



[アドイン マネージャーと XLL インターフェイス関数](add-in-manager-and-xll-interface-functions.md)

