---
title: Excel4、Excel12
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Excel12
- Excel4
keywords:
- excel4 関数 [excel 2007] Excel12 関数 [Excel 2007]
localization_priority: Normal
ms.assetid: 2404f10d-8641-4ee6-a909-1c5a26610f80
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 1c2c775cc7c5b051e4a1381df09ef29e79e2aca4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798867"
---
# <a name="excel4excel12"></a>Excel4、Excel12

 **適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
Microsoft Excel ワークシートの内部関数、マクロ シート関数やコマンド、または XLL 専用の特殊関数やコマンドを DLL、XLL、またはコード リソース内部から呼び出します。
  
すべての最新バージョンの Excel では、 **Excel4**をサポートします。 Excel 2007 以降では、 **Excel12**がサポートされています。 
  
�����̊֐��́AExcel �� DLL �܂��� XLL �ɐ����n���Ă���ꍇ�ɂ̂݁A�Ăяo�����Ƃ��ł��܂��B�����̊֐��́AExcel �� Visual Basic for Applications (VBA) �ւ̌Ăяo�����ĊԐړI�ɐ����n���Ă���ꍇ�ɂ�Ăяo����邱�Ƃ�����܂��B����ȊO�̎��ɁA�����̊֐���Ăяo�����Ƃ͂ł��܂���B���Ƃ��΁A[DllMain](http://msdn.microsoft.com/library/base.dllmain%28Office.15%29.aspx) �֐��ɑ΂���Ăяo���̊Ԃ�A�I�y���[�e�B���O �V�X�e���� DLL ��Ăяo���Ă���Ƃ���A�����̊֐���Ăяo�����Ƃ͂ł��܂���BDLL ���쐬�����X���b�h�����A�����̊֐���Ăяo�����Ƃ͂ł��܂���B 
  
**Excel4**と**Excel12**関数は、スタック上の可変長リストとして、引数を受け取るが、 [Excel4v と Excel12v](excel4v-excel12v.md)関数は、配列として引数をそのまま使用します。 その他のすべての点では、 **Excel4**の**Excel4v**と同じ動作し、 **Excel12**の**Excel12v**と同じ動作です。
  
```cs
int Excel4(int iFunction, LPXLOPER pxRes, int iCount, LPXLOPER argument1, ...);
int Excel12(int iFunction, LPXLOPER12 pxRes, int iCount, LPXLOPER12 argument1, ...);
```

## <a name="parameters"></a>�p�����[�^�[

 _iFunction_(**int**)
  
�Ăяo���R�}���h�A�֐��A�܂��͓���֐���������l�B _iFunction_ �̗L���Ȓl�̈ꗗ�́A���̉���Q�Ƃ��Ă��������B 
  
 _pxRes_(**LPXLOPER**または**LPXLOPER12**)
  
( **Excel4**) とは、 **XLOPER**を**XLOPER12** ( **Excel12**) と評価された関数の結果を保持するへのポインター。
  
 _iCount_(**int**)
  
関数に渡されるそれ以降の引数の数。 2003 までのバージョンの Excel は 0 から 30 までの任意の数になります。 Excel 2007 以降では、これは、0 255 までからの任意の数。
  
 _argument1、._(**LPXLOPER**または**LPXLOPER12**)
  
関数の省略可能な引数です。 すべての引数は、 **XLOPER**または**XLOPER12**の値へのポインターである必要があります。 
  
## <a name="return-value"></a>�߂�l

以下の整数 (**int**) の値のいずれかを返します。
  
|**値**|**リターン コード**|**説明**|
|:-----|:-----|:-----|
|0  <br/> |**xlretSuccess** <br/> |関数は正常に呼び出されます。 関数が、Excel のエラー値を返さなかったことはありません。アウトを見つけるには、型と結果の_pxRes_パラメーターの値を表示する必要があります。  <br/> |
|1  <br/> |**xlretAbort** <br/> |コマンドまたは関数が異常終了しました (内部アボート)。 これは、XLM マクロ シートで**CLOSE**を呼び出すことによって自動的に閉じる場合、または Excel がメモリが不足している場合に発生します。 Excel では、このエラーが返された場合、呼び出し元の関数は即座に終了する必要があります。 DLL は、 **xlFree**を終了する前にのみ呼び出すことが許可されます。 他のすべての c 言語の API 呼び出しは許可されていません。 ユーザーは [**ファイル**] メニューの [**上書き保存**] コマンドを使用して対話的に作業を保存できます。  <br/> |
|2  <br/> |**xlretInvXlfn** <br/> |指定された関数の数が正しくありません。Xlcall.h ヘッダー ファイルの定数を使用している場合、実行中の Excel のバージョンでサポートされていない何かを呼び出さない限り、これが起こることはありません。  <br/> |
|4  <br/> |**xlretInvCount** <br/> |無効な数の引数が入力されました。 Excel 2003 までのバージョンでは、関数が受け取ることができます引数の最大数は 30 です。 Excel 2007 以降では、最大数は、255 です。 いくつかは、引数の数が固定または最小値を必要があります。  <br/> |
|8  <br/> |**xlretInvXloper** <br/> |無効の**XLOPER**または**XLOPER12**は、関数に渡されたか、間違った型の引数が使用されました。  <br/> |
|16  <br/> |**xlretStackOvfl** <br/> |スタック オーバーフローが発生しました。 **XlStack**を使用すると、スタック上の部屋の左側の量を監視できます。 可能な場合は、ローカル (自動) の非常に大きな配列とスタック上の構造体の割り当てを回避します。静的となってください。 (スタック オーバーフローが検出されることがなく発生する可能性に注意してください)。  <br/> |
|32  <br/> |**xlretFailed** <br/> |コマンドと等価の関数が失敗しました。これは、[マクロ エラーの警告] ダイアログボックスを表示するマクロ コマンドと等価です。  <br/> |
|64  <br/> |**xlretUncalced** <br/> |現在のセルの後に再計算することになる予定ですので、まだ計算されていないセルを逆参照しようとしました。 この例では、DLL コントロールを Excel にすぐに返すか。 DLL は、 **xlFree**を終了する前にのみ呼び出すことが許可されます。 他のすべての c 言語の API 呼び出しは許可されていません。 先の詳細については関数およびできますが再計算されていない、 [Excel のコマンド、関数、および状態](excel-commands-functions-and-states.md)を表示するセルの値にアクセスできません。  <br/> |
|128  <br/> |**xlretNotThreadSafe** <br/> |ブックの再計算がマルチ スレッドで実行中に、スレッド セーフではない、あるいはスレッド セーフでない可能性がある関数を呼び出そうとしました。  <br/> Excel 2007 以降では、この値が返されると同様のスレッド セーフで XLL ワークシート関数の宣言内でのみです。  <br/> |
|256  <br/> |**xlRetInvAsynchronousContext** <br/> |非同期関数のハンドルが正しくありません。  <br/> この値は、Excel 2010 でのみ使用されます。  <br/> |
|512  <br/> |**xlRetNotClusterSafe** <br/> |クラスターでは、呼び出しはサポートされていません。  <br/> この値は、Excel 2010 でのみ使用されます。  <br/> |
   
## <a name="remarks"></a>備考

### <a name="valid-ifunction-values"></a>有効な iFunction の値

有効な**iFunction**の値は、 **xlf.** または**xlc.** Xlcall.h ヘッダー ファイルまたは特殊な関数を次のいずれかで定義されている定数のいずれかです。 
  
|||||
|:-----|:-----|:-----|:-----|
|**xlAbort** <br/> |**xlEnableXLMsgs** <br/> |**xlGetInst** <br/> |**xlSheetNm** <br/> |
|**xlCoerce** <br/> |**xlFree** <br/> |**xlGetName** <br/> |**xlStack** <br/> |
|**xlDefineBinaryName** <br/> |**xlGetBinaryName** <br/> |**xlSet** <br/> |**xlUDF** <br/> |
|**xlDisableXLMsgs** <br/> |**xlGetHwnd** <br/> |**xlSheetId** <br/> ||
   
### <a name="different-types-of-functions"></a>関数のさまざまな種類

 **Excel4**と**Excel12**関数の 3 つのクラスを区別します。 関数は、Excel が、DLL を呼び出す場合があります、3 つの状態によって分類されます。 
  
- クラス 1 は、DLL が再計算の結果としてワークシートから呼び出された場合に適用されます。  
    
- クラス 2 は、DLL が関数マクロ内部から呼び出された場合、またはタイプ テキストで番号記号 (#) を付けて登録されたワークシートから呼び出された場合に適用されます。
    
- クラス 3 では、DLL がオブジェクト、マクロ、メニューのツールバー、ショートカット キー、 **ExecuteExcel4Macro**メソッド、または**ツール/マクロ/実行**] コマンドから呼び出されたときに適用されます。 詳細については、 [Excel のコマンド、関数、および状態](excel-commands-functions-and-states.md)を参照してください。
    
次の表は、各クラスでどの関数が有効かを示しています。
  
|**クラス 1**|**クラス 2**|**クラス 3**|
|:-----|:-----|:-----|
|任意のワークシート関数  <br/> **XlSet**を除く任意の xll ファイル専用の**xl.** 関数です。  <br/> **xlfCaller** <br/> |任意のワークシート関数  <br/> **XlSet**を除くすべての**xl.** 関数です。  <br/> マクロ シート機能、 **xlfCaller**を含む値を返しますが、ワークスペースに影響する操作、または開いているブックを実行しません。  <br/> |**XlSet**と同じコマンド ・関数を含む関数、です。  <br/> |
   
### <a name="displaying-the-dialog-box-for-a-command-equivalent-function"></a>コマンドと等価の関数のダイアログ ボックスの表示

コマンドに相当する関数に、関連付けられたダイアログ ボックスがある場合は、 **iFunction**で**xlPrompt**ビットを設定できます。 つまり、あるコマンドを実行する前に適切なダイアログ ボックスが表示されます。
  
### <a name="writing-international-dlls"></a>International DLL の作成

**IFunction**に**xlIntl**ビットを設定すると、関数やコマンドが実行、インターナショナル マクロ シートから呼び出されているされた場合と同様です。 つまり、コマンドと動作を米国のバージョンの Excel では、国際 (ローカライズされた) バージョンで実行されている場合でも。
  
### <a name="xlretuncalced-or-xlretabort"></a>xlretUncalced または xlretAbort

、これらの戻り値のいずれかを受信した後、DLL する必要がありますをクリーンアップし、すぐにコントロールを Excel に返します。 これらの戻り値のいずれかを受信した後は、 **xlFree**を除いて、C API を使用して Excel にコールバックが無効になります。
  
## <a name="example"></a>例

次の例では、 **Excel12**関数を使用して、呼び出し元のセルを選択します。 
  
このコード例は、SDK がインストールされている次の場所に、Excel 2010 XLL SDK で提供されている大きな例の一部です。
  
\Samples\Example\Example.c。
  
> [!NOTE]
> この関数は、コマンド マクロ (xlcSelect) を呼び出し、それゆえに、それが XLM マクロ シートから呼び出された場合にのみ動作します。 
  
```cs
short WINAPI Excel12Example(void)
{
    XLOPER12 xRes;
    Excel12(xlfCaller, &xRes, 0);
    Excel12(xlcSelect, 0, 1, (LPXLOPER12)&xRes);
    Excel12(xlFree, 0, 1, (LPXLOPER12)&xRes);
    return 1;
}
```

## <a name="see-also"></a>関連項目



[Excel4v/Excel12v](excel4v-excel12v.md)

