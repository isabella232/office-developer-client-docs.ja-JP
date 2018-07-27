---
title: Excel/Excel12f
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Excel12f
keywords:
- excel function [excel 2007],Excel12f function [Excel 2007]
localization_priority: Normal
ms.assetid: 4e6a9ccc-988d-42a9-8874-01f2ee29b835
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 56034984852713496465c3d1f79a9989fc47df1c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798809"
---
# <a name="excelexcel12f"></a>Excel/Excel12f

 **適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
フレームワーク ライブラリ関数。 **Excel** は [Excel4](excel4-excel12.md) 関数のラッパーです。 **Excel12f** は [Excel12](excel4-excel12.md) 関数のラッパーです。 引数がいずれも 0 になっていないことをそれぞれ確認します。0 の場合は一時的な **XLOPER** や **XLOPER12** が作成できなかったことを表します。 エラーが発生すると、それぞれデバッグ メッセージが出力されます。 出力が終わると、一時的な **XLOPER** や **XLOPER12** 用に作成された一時メモリはすべて解放されます。
  
 **Excel12f**から Excel 2007 C API ライブラリ以降の DLL からのみ呼び出すことができます。さらに、Excel 2007 以降で起動したときのみ動作し、それ以外は **xlretFailed** で失敗します。 
  
```cs
int Excel(int iFunction, LPXLOPER pxRes, int iCount, 
LPXLOPER argument1, ...);
int Excel12f(int iFunction, LPXLOPER12 pxRes, int iCount, 
LPXLOPER12 argument1, ...);
```

## <a name="parameters"></a>パラメーター

 _iFunction_ (**int**)
  
呼び出すコマンドまたは関数を示す数値。詳細については、「[Excel4/Excel12](excel4-excel12.md)」を参照してください。
  
 _pxRes_
  
評価された関数の結果のポインター。結果に示されるメモリはすべて、Excel によって割り当てられ、不要になったら [xlFree](xlfree.md) を呼び出して解放するか、または Excel に戻す場合は **xlbitXLFree** を設定して解放します。 
  
 _iCount_ (**int**)
  
関数に渡される引数の数。Excel 2007 以降、引数の数は 255 に制限されています。それ以前のバージョンでは引数の数は 30 に制限されています。
  
 _argument1, ..._
  
省略可能な、関数の引数。すべての引数は、**Excel** の場合は **XLOPER** へのポインター、**Excel12f** の場合は **XLOPER12** へのポインターにする必要があります。
  
## <a name="return-value"></a>戻り値

どちらの関数も、**Excel4**、**Excel4v**、**Excel12**、**Excel12v** と同様のエラー コードや成功コードを返します。 これらのコードの詳細については、「[Excel4/Excel12](excel4-excel12.md)」を参照してください。 さらに、パラメーターに対する NULL ポインターが検出された場合、これらのフレームワーク関数は、C API を呼び出さずに、**xlretFailed** を返します。 
  
## <a name="example"></a>例

この例では、不正な引数を **Excel12f** 関数に渡して、デバッガーにメッセージを送信しています。 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI Excel12fExample(void)
{
    Excel12f(xlcDisplay, 0, 1, 0);
    return 1;
}
```

## <a name="see-also"></a>関連項目



[Excel4/Excel12](excel4-excel12.md)


[フレームワーク ライブラリの関数](functions-in-the-framework-library.md)

