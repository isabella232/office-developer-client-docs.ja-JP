---
title: Excel4v/Excel12v
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Excel12v
- Excel4v
keywords:
- excel12v function [excel 2007],Excel4v function [Excel 2007]
ms.localizationpriority: medium
ms.assetid: e3e96b98-c5a7-4625-95b6-a1e2d09c6d3d
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3969fb3d9e8323b6857ea11bfed5989232287fdf
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621459"
---
# <a name="excel4vexcel12v"></a>Excel4v/Excel12v

 **適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Excel ワークシートの内部関数、マクロ シート関数やコマンド、または XLL 固有の特殊関数やコマンドを DLL、XLL、またはコード リソース内部から呼び出します。
  
Excel のすべての最新バージョンは、**Excel4v** をサポートしています。Excel 2007 以降のバージョンでは、**Excel12v** がサポートされています。 
  
�����̊֐��́AExcel �� DLL �܂��� XLL �ɐ����n���Ă���ꍇ�ɂ̂݁A�Ăяo�����Ƃ��ł��܂��B�����̊֐��́AExcel �� Visual Basic for Applications (VBA) �ւ̌Ăяo�����ĊԐړI�ɐ����n���Ă���ꍇ�ɂ�Ăяo����邱�Ƃ�����܂��B����ȊO�̎��ɁA�����̊֐���Ăяo�����Ƃ͂ł��܂���B���Ƃ��΁ADllMain �֐��ɑ΂���Ăяo���̊Ԃ�A�I�y���[�e�B���O �V�X�e���� DLL ��Ăяo���Ă���Ƃ���A�����̊֐���Ăяo�����Ƃ͂ł��܂���BDLL ���쐬�����X���b�h�����A�����̊֐���Ăяo�����Ƃ͂ł��܂���B 
  
[Excel4 と Excel12](excel4-excel12.md) 関数は、スタック上の可変長リストとしてそれらの引数を受け入れます。一方、**Excel4v** と **Excel12v** 関数は、配列としてそれらの引数を受け入れます。それ以外の点のすべてで、**Excel4** は **Excel4v** と同じように動作し、**Excel12** は **Excel12v** と同じように動作します。
  
```cs
int _cdecl Excel4v(int iFunction, LPXLOPER pxRes, int iCount, LPXLOPER rgx[]);
int _cdecl Excel12v(int iFunction, LPXLOPER12 pxRes, int iCount, LPXLOPER12 rgx[]);
```

## <a name="parameters"></a>パラメーター

 _iFunction_ (**int**)
  
呼び出すコマンド、関数、または特殊関数を示す数値。_iFunction_ の有効な値の一覧は、次の解説を参照してください。 
  
 _pxRes_ (**LPXLOPER** または **LPXLOPER12**)
  
評価された関数の結果を保持する、**XLOPER** (**Excel4v** の場合) または **XLOPER12** (**Excel12v** の場合) へのポインター。
  
 _iCount_ (**int**)
  
関数へ渡される一連の引数の数。Excel 2003 以前のバージョンでは、0 ～ 30 の任意の数です。Excel 2007 以降は、0 ～ 255 の任意の数です。
  
 _rgx_ (**LPXLOPER []** または **LPXLOPER12 []**)
  
関数への引数を含む配列です。配列内のすべての引数が **XLOPER** または **XLOPER12** の値を指すポインターである必要があります。 
  
## <a name="return-value"></a>戻り値

これらの関数は、**Excel4** および **Excel12** と同じ値を返します。
  
## <a name="remarks"></a>注釈

これらの関数は、演算子に渡された引数の数が可変の場合に役立ちます。たとえば **Excel4v** および **Excel12v** は、[xlfRegister](xlfregister-form-1.md) (引数の合計数が、登録対象の関数が取る引数の数によって決まる) を使用して関数を登録するときに役に立ちます。**Excel4v** および **Excel12v** は、**Excel4** または **Excel12** のラッパー関数を記述するときにも役立ちます。これらの場合、(通常 **Excel4** または **Excel12** に指定される) 可変引数リストを可変サイズの単一の配列の引数に変換し、**Excel4v** または **Excel12v** を使用して Excel にコールバックする必要があります。
  
### <a name="example"></a>例

コードの例については、次に示す SDK をインストールした場所にある、Excel 2010 XLL SDK の **Excel** および **Excel12f** 関数のコードを参照してください。 
  
Samples\Framewrk\Framewrk.c
  
## <a name="see-also"></a>関連項目



[Excel4/Excel12](excel4-excel12.md)

