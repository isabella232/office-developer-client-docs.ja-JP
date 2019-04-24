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
- excel4 関数 [excel 2007]、Excel12 関数 [Excel 2007]
localization_priority: Normal
ms.assetid: 2404f10d-8641-4ee6-a909-1c5a26610f80
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 7c3af5f380ae4144890b1f7b486a61a05c19de74
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304110"
---
# <a name="excel4excel12"></a>Excel4、Excel12

**適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Excel ワークシートの内部関数、マクロ シート関数やコマンド、または XLL 専用の特殊関数やコマンドを DLL、XLL、またはコード リソース内部から呼び出します。
  
Excel のすべての最新バージョンは、**Excel4** をサポートしています。 Excel 2007 以降では、**Excel12** がサポートされています。 
  
これらの関数は、Excel が DLL または XLL に制御を渡している場合にのみ、呼び出すことができます。これらの関数は、Excel が Visual Basic for Applications (VBA) への呼び出しを介して間接的に制御を渡したときにも呼び出せます。たとえば、[DllMain](https://docs.microsoft.com/windows/desktop/dlls/dllmain) 関数に対する呼び出しの間も、オペレーティング システムが DLL を呼び出しているときも、これらの関数を呼び出すことはできません。DLL が作成したスレッドからも、これらの関数を呼び出すことはできません。 
  
[Excel4v と Excel12v](excel4v-excel12v.md) 関数は、配列としてそれらの引数を受け入れます。一方、**Excel4** と **Excel12** 関数は、スタック上の可変長リストとしてそれらの引数を受け入れます。それ以外の点のすべてで、**Excel4** は **Excel4v** と同じように動作し、**Excel12** は **Excel12v** と同じように動作します。
  
```cs
int Excel4(int iFunction, LPXLOPER pxRes, int iCount, LPXLOPER argument1, ...);
int Excel12(int iFunction, LPXLOPER12 pxRes, int iCount, LPXLOPER12 argument1, ...);
```

## <a name="parameters"></a>パラメーター

 _iFunction_ (**int**)
  
呼び出すコマンド、関数、または特殊関数を示す数値。_iFunction_ の有効な値の一覧は、次の解説を参照してください。 
  
 _pxRes_ (**LPXLOPER** または **LPXLOPER12**)
  
評価された関数の結果を保持する、**XLOPER** (**Excel4** の場合) または **XLOPER12** (**Excel12** の場合) へのポインター。
  
 _iCount_ (**int**)
  
関数へ渡される後続の引数の数。 Excel 2003 までのバージョンでは、0 から 30 までの任意の数です。 Excel 2007 以降は、0 から 255 までの任意の数です。
  
 _argument1, ..._ (**LPXLOPER** または **LPXLOPER12**)
  
省略可能な、関数への引数。すべての引数が **XLOPER** または **XLOPER12** の値へのポインターである必要があります。 
  
## <a name="return-value"></a>戻り値

次の整数値 (**int**) の 1 つを返します。
  
|**値**|**リターン コード**|**説明**|
|:-----|:-----|:-----|
|.0  <br/> |**xlretSuccess** <br/> |関数は正常に呼び出されました。 これは、この関数が Excel のエラー値を返さなかったという意味ではありません。それを判断するには、結果の _pxRes_ パラメーターの種類と値を調べる必要があります。  <br/> |
|1-d  <br/> |**xlretAbort** <br/> |コマンドまたは関数が異常終了しました (内部アボート)。これは、XLM マクロ シートが **CLOSE** を呼び出すことによってそれ自体を閉じた場合、またはExcel がメモリ不足になる場合に起こります。Excel がこのエラーを返す場合、呼び出し元の関数は即座に終了する必要があります。DLL が **xlFree** を呼び出すことが許可されるのは、終了前のみです。C API に対するそれ以外のすべての呼び出しは許可されません。ユーザーは、**[ファイル]** メニューの **[保存]** コマンドを使用して、対話形式で任意の作業を保存できます。<br/> |
|pbm-2  <br/> |**xlretInvXlfn** <br/> |指定された関数の数が正しくありません。Xlcall.h ヘッダー ファイルの定数を使用している場合、実行中の Excel のバージョンでサポートされていない何かを呼び出さない限り、これが起こることはありません。  <br/> |
|2/4  <br/> |**xlretInvCount** <br/> |入力された引数の数が正しくありません。 Excel 2003 までのバージョンでは、すべての関数の引数の最大数は 30 です。 Excel 2007 以降では、最大数は 255 です。 引数の数が固定されている場合もありますし、最小値が必要な場合もあります。  <br/> |
|~  <br/> |**xlretInvXloper** <br/> |関数に渡された **XLOPER** または **XLOPER12** が正しくないか、使用された引数の種類が間違っています。  <br/> |
|16  <br/> |**xlretStackOvfl** <br/> |スタック オーバーフローが発生しました。**xlStack** を使用して、スタックの残容量を監視します。大規模なローカル (自動) の配列や構造をスタック上で割り当てることを避け、可能な場合にはそれらを静的にします。(スタック オーバーフローが、検出されることなく発生する場合があることにご注意ください。)<br/> |
|32  <br/> |**xlretFailed** <br/> |コマンドと等価の関数が失敗しました。これは、[マクロ エラーの警告] ダイアログボックスを表示するマクロ コマンドと等価です。  <br/> |
|64  <br/> |**xlretUncalced** <br/> |現在のセルの後に再計算するようスケジュールされているために、まだ計算されていないセルを逆参照しようとしました。この場合、DLL は制御を即時に Excel に戻す必要があります。DLL が **xlFree** を呼び出すのが許可されるのは、終了する前のみです。C API に対するそれ以外のすべての呼び出しは許可されません。再計算されていないセルの値にアクセスできる関数とできない関数についての詳細は、「[Excel のコマンド、関数、および状態](excel-commands-functions-and-states.md)」を参照してください。<br/> |
|128  <br/> |**xlretNotThreadSafe** <br/> |ブックの再計算がマルチ スレッドで実行中に、スレッド セーフではない、あるいはスレッド セーフでない可能性がある関数を呼び出そうとしました。  <br/> Excel 2007 以降、この値が返されるようになり、XLL ワークシート関数内でのみ、スレッド セーフとして宣言されます。  <br/> |
|256  <br/> |**xlRetInvAsynchronousContext** <br/> |非同期関数のハンドルが無効です。  <br/> この値は、Excel 2010 でのみ使用されます。  <br/> |
|512  <br/> |**xlRetNotClusterSafe** <br/> |クラスターでは、呼び出しはサポートされていません。  <br/> この値は、Excel 2010 でのみ使用されます。  <br/> |
   
## <a name="remarks"></a>備考

### <a name="valid-ifunction-values"></a>有効な iFunction の値

有効な **iFunction** の値は、Xlcall.h ヘッダー ファイルまたは次の特殊関数のいずれかで定義される、任意の **xlf...** または **xlc...** 定数です。 
  
|||||
|:-----|:-----|:-----|:-----|
|**xlAbort** <br/> |**xlEnableXLMsgs** <br/> |**xlGetInst** <br/> |**xlSheetNm** <br/> |
|**xlCoerce** <br/> |**xlFree** <br/> |**xlGetName** <br/> |**xlStack** <br/> |
|**xlDefineBinaryName** <br/> |**xlGetBinaryName** <br/> |**xlSet** <br/> |**xlUDF** <br/> |
|**xlDisableXLMsgs** <br/> |**xlGetHwnd** <br/> |**xlSheetId** <br/> ||
   
### <a name="different-types-of-functions"></a>関数のさまざまな種類

 **Excel4** と **Excel12** は、関数の 3 つのクラスを識別します。関数は、Excel が DLL を呼び出す際の 3 種類の状態に基づいて分類されます。 
  
- クラス 1 は、DLL が再計算の結果としてワークシートから呼び出された場合に適用されます。 
    
- クラス 2 は、DLL が関数マクロ内部から呼び出された場合、またはタイプ テキストで番号記号 (#) を付けて登録されたワークシートから呼び出された場合に適用されます。
    
- クラス 3は、DLL が、オブジェクト、マクロ、メニュー、ツールバー、ショートカット キー、**ExecuteExcel4Macro** メソッドから呼び出された場合に適用されます。また、**ツール、マクロ、実行**の各コマンドから呼び出された場合にも適用されます。詳細は、「[Excel のコマンド、関数、および状態](excel-commands-functions-and-states.md)」を参照してください。
    
次の表は、各クラスでどの関数が有効かを示しています。
  
|**Class 1**|**Class 2**|**Class 3**|
|:-----|:-----|:-----|
|任意のワークシート関数  <br/> **xlSet** を除く、任意の XLL 専用の **xl...** 関数。  <br/> **xlfCaller** <br/> |任意のワークシート関数  <br/> **xlSet** を除く、任意の **xl...** 関数。  <br/> ワークスペースまたは開いているどのブックにも影響する操作を実行せずに値を返す、マクロ シート関数 (**xlfCaller** を含む)。  <br/> |任意の関数 (**xlSet** を含む) およびコマンド等価関数。  <br/> |
   
### <a name="displaying-the-dialog-box-for-a-command-equivalent-function"></a>コマンドと等価の関数のダイアログ ボックスの表示

コマンドと等価の関数がダイアログ ボックスと関連付けられている場合、**iFunction** の **xlPrompt** ビットを設定できます。これは、コマンドを実行する前に、Excel が適切なダイアログ ボックスを表示することを意味します。
  
### <a name="writing-international-dlls"></a>International DLL の作成

**iFunction** の **xlIntl** ビットを設定する場合、その関数またはコマンドは、インターナショナル マクロ シートから呼び出されている場合と同様に実行されます。これは、そのコマンドが国際バージョン (ローカライズされたバージョン) で実行されているとしても、Excel の米国バージョンと同様に動作するという意味です。
  
### <a name="xlretuncalced-or-xlretabort"></a>xlretUncalced または xlretAbort

戻り値の 1 つを受け取った後、DLL は直ちにクリーンアップを行い、制御を Excel に返す必要があります。**xlFree** 以外では、戻り値の 1 つを受け取った後、C API 経由での Excel へのコールバックはできなくなります。
  
## <a name="example"></a>例

次の例は、呼び出し元のセルを選択するために、**Excel12** 関数を使用します。 
  
このコード例は、Excel 2010 XLL SDK で提供されている、より大きな例の一部です。例は、SDK がインストールされている場所の次の位置にあります:
  
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

