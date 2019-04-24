---
title: DLL または XLL から Excel に呼び出す
manager: soliver
ms.date: 08/22/2018
ms.audience: Developer
ms.topic: overview
keywords:
- ダイアログ ボックス [excel 2007]、excel コマンドの呼び出し、DLL [Excel 2007]、Excel への呼び出し、C API 関数への引数の引き渡し [Excel 2007]、コマンド [Excel 2007]、ダイアログ ボックスでの呼び出し、コマンド [Excel 2007]、DLL/XLL からアクセス可能、Excel4 関数 [Excel 2007]、Excel12 関数 [Excel 2007]、XLCallVer 関数 [Excel 2007]、operRes 引数 [Excel 2007]、関数 [Excel 2007]、DLL/XLL からアクセス可能、Excel12v 関数 [Excel 2007]、DLL 専用関数 [Excel 2007]、C API [Excel 2007]、引数の引き渡し、引数の数 [Excel 2007]、コマンド [Excel 2007]、インターナショナル バージョンでの呼び出し、DLL 専用コマンド [Excel 2007]、インターナショナル バージョン [Excel 2007]、関数およびコマンドの呼び出し、XLL [Excel 2007]、Excel への呼び出し、Excel 4v 関数 [Excel 2007]、xlfn 引数 [Excel 2007]、関数 [Excel 2007]、インターナショナル バージョンでの呼び出し
ms.assetid: 616e3def-e4ec-4f3c-bc65-3b92710da1e6
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: 8f2b63ba84b0a78bbf317c284913a8ec0986436f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304159"
---
# <a name="calling-into-excel-from-the-dll-or-xll"></a>DLL または XLL から Excel に呼び出す

**適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Excel を使用すると、DLL は組み込みの Excel コマンド、ワークシート関数、マクロ シート関数にアクセスできます。こうしたコマンドや関数は、Visual Basic for Applications (VBA) で呼び出される DLL コマンドと関数から、および Excel によって直接呼び出される登録済み XLL コマンドと関数から使用できます。
  
## <a name="excel4-excel4v-excel12-and-excel12v-functions"></a>Excel4、Excel4v、Excel12、Excel12v 関数

Excel を使用すると、DLL はコールバック関数 [Excel4](excel4-excel12.md)、[Excel4v](excel4v-excel12v.md)、[Excel12](excel4-excel12.md)、[Excel12v](excel4v-excel12v.md) を介してコマンドや関数にアクセスできます。
  
**Excel4** 関数と **Excel4v** 関数は、Excel バージョン 4 で導入されました。 これらは **XLOPER** データ構造で動作します。 Excel 2007 では、新しいコールバック関数である **Excel12** と **Excel12v** が導入されました。これらは **XLOPER12** データ構造で動作します。 **Excel4** 関数と **Excel4v** 関数は、ライブラリ Xlcall32.lib によってエクスポートされ、DLL または XLL プロジェクトに含める必要があります。 **Excel12** と **Excel12v** はプロジェクト内の SDK C++ source ファイル Xlcall.cpp に含めます。**XLOPER12** 構造を使用して Excel 機能にアクセスする場合は、これらの関数をプロジェクトに含める必要があります。 
  
以下のコードは、これら 4 つの関数の関数プロトタイプを示しています。 最初の 3 つの引数は同じですが、2 番目の引数が最初のペアでは **XLOPER** へのポインターで、次のペアでは **XLOPER12** へのポインターである点が異なります。 呼び出し規約は、**Excel4** と **Excel12** では **_cdecl** で、可変の引数リストが許可されます。 省略記号は、**Excel4** の **XLOPER** 値、および **Excel12** の **XLOPER12** 値へのポインターを表します。 ポインターの数は、_count_ パラメーターの値と等しくなります。 
  
**すべてのバージョンの Excel**
  
 `int _cdecl Excel4(int xlfn, LPXLOPER operRes, int count,... );`
  
 `int pascal Excel4v(int xlfn, LPXLOPER operRes, int count, LPXLOPER opers[]);`
  
**Excel 2007 以降**
  
 `int _cdecl Excel12(int xlfn, LPXLOPER12 operRes, int count,... );`
  
 `int pascal Excel12v(int xlfn, LPXLOPER12 operRes, int count, LPXLOPER12 opers[]);`
  
DLL で **Excel4**、**Excel4v**、**Excel12**、または **Excel12v** を呼び出すことができるようにするには、Excel が DLL に制御を渡す必要があります。つまり、こうした C API コールバックは、次のシナリオでのみ呼び出すことができます。
  
- Excel が直接または VBA を介して呼び出した XLL コマンドから。
    
- Excel が直接または VBA を介して呼び出した XLL ワークシート関数またはマクロ シート関数から。
    
次のシナリオでは、Excel C API を呼び出すことはできません。
  
- オペレーティング システム イベントから (たとえば、[DllMain](https://docs.microsoft.com/windows/desktop/dlls/dllmain) 関数から)。 
    
- DLL が作成したバックグラウンド スレッドから。
    
### <a name="return-values"></a>戻り値

これら 4 つの関数はいずれも整数値を返します。この値によって、呼び出し元に対して、関数またはコマンドが正常に呼び出されたかどうかが知らされます。次のいずれかの値が返されます。
  
|**戻り値**|**Xlcall.h での定義**|**説明**|
|:-----|:-----|:-----|
|0  <br/> |**xlretSuccess** <br/> |関数またはコマンドが正常に実行されました。これは、エラーなく実行されたことを意味するわけではありません。たとえば、**Excel4** は、**FIND** 関数を呼び出して検索テキストが見つからないために **#VALUE!** に評価される場合であっても、**xlretSuccess** を返すことがあります。返される **XLOPER/XLOPER12** の型と値についてはこの可能性を考慮して検証しなければなりません。<br/> |
|1  <br/> |**xlretAbort** <br/> |コマンド マクロは、ユーザーが **[キャンセル]** ボタンをクリックしたか、Esc キーを押したために停止しました。  <br/> |
|2  <br/> |**xlretInvXlfn** <br/> |指定された関数コードまたはコマンド コードが無効です。このエラーは、呼び出し元の関数に関数またはコマンドを呼び出すアクセス許可がない場合に生じます。たとえば、ワークシート関数は、マクロ シート情報関数またはコマンド関数を呼び出すことはできません。  <br/> |
|4  <br/> |**xlretInvCount** <br/> |呼び出しで指定した引数の数が正しくありません。  <br/> |
|8  <br/> |**xlretInvXloper** <br/> |1 つ以上の引数の **XLOPER** 値または **XLOPER12** 値の形式が正しくないか、誤って入力されています。  <br/> |
|16  <br/> |**xlretStackOvfl** <br/> |Excel によって、操作でスタックがオーバーフローするリスクが検出され、関数が呼び出されませんでした。  <br/> |
|32  <br/> |**xlretFailed** <br/> |コマンドまたは関数が、他のいずれの戻り値によっても記述されていない理由によって失敗しました。たとえば、あまりにも大量のメモリを必要とする操作はこのエラーで失敗します。[xlCoerce](xlcoerce.md) 関数を使用して、**xltypeMulti** 配列にとても大きな参照を変換しようとすると生じる場合があります。<br/> |
|64  <br/> |**xlretUncalced** <br/> |計算されていないセルの値を取得しようとする操作が行われました。Excel で再計算整合性を保持するため、ワークシート関数ではこれを行うことができません。ただし、マクロ シート関数として登録された XLL コマンドおよび関数は、計算されていないセル値にアクセスできます。  <br/> |
|128  <br/> |**xlretNotThreadSafe** <br/> |(Excel 2007 以降) スレッド セーフとして登録されている XLL ワークシート関数が、スレッド セーフではない C API 関数を呼び出そうとしました。 たとえば、スレッド セーフ関数が XLM 関数 **xlfGetCell** を呼び出すことはできません。  <br/> |
|256  <br/> |**xlRetInvAsynchronousContext** <br/> |(Excel 2010 以降) 非同期関数ハンドルが無効です。  <br/> |
|512  <br/> |**xlretNotClusterSafe** <br/> |(Excel 2010 以降) クラスターでは、呼び出しはサポートされていません。  <br/> |
   
関数がこの表のいずれかのエラー値を返す場合 (つまり、**xlretSuccess** を返さない場合)、**XLOPER** または **XLOPER12** 戻り値も **#VALUE!** に設定されます。場合によっては、この値をチェックするだけで成功を十分に確認できますが、呼び出しでは **xlretSuccess** と **#VALUE!** の両方が返る可能性を銘記しておく必要があります。
  
C API への呼び出し結果が **xlretUncalced** または **xlretAbort** となる場合、DLL コードまたは XLL コードは、他の C API 呼び出し ([xlfree](xlfree.md) 関数を呼び出して、**XLOPER** 値と **XLOPER12** 値で Excel によって割り当てられたメモリ リソースをリリースする場合以外) を行う前に制御を Excel に返さなければなりません。 
  
### <a name="command-or-function-enumeration-argument-xlfn"></a>コマンドまたは関数の列挙型引数: xlfn

_xlfn_ 引数は、コールバック関数への最初の引数で、32 ビット符号付き整数です。 値は、以下の例に示されているように、SDK ヘッダー ファイル Xlcall.h で定義されている関数またはコマンドの列挙型のいずれかでなければなりません。 
  
```cs
// Excel function numbers. 
#define xlfCount 0
#define xlfIsna 2
#define xlfIserror 3
#define xlfSum 4
#define xlfAverage 5
#define xlfMin 6
#define xlfMax 7
#define xlfRow 8
#define xlfColumn 9
#define xlfNa 10
...
// Excel command numbers. 
#define xlcBeep (0 | xlCommand)
#define xlcOpen (1 | xlCommand)
#define xlcOpenLinks (2 | xlCommand)
#define xlcCloseAll (3 | xlCommand)
#define xlcSave (4 | xlCommand)
#define xlcSaveAs (5 | xlCommand)
#define xlcFileDelete (6 | xlCommand)
#define xlcPageSetup (7 | xlCommand)
#define xlcPrint (8 | xlCommand)
#define xlcPrinterSetup (9 | xlCommand)
...
```

すべてのワークシート関数とマクロ シート関数は、0 (**xlfCount**) から 0x0fff 16 進数までの範囲内です。Excel 2013 で割り当てられている最大値は 547 (10 進数)、0x0223 (16 進数) (**xlfFloor_precise**) です。
  
すべてのコマンド関数は、0x8000 の 16 進数 (**xlcBeep**) から 0x8fff の 16 進数までの範囲内です。Excel 2013 で割り当てられている最大値は 0x8328 の 16 進数 (**xlcHideallInkannots**) です。 これらは、ヘッダー ファイルで `(n | xlCommand)` として定義されます。`n` は 0 以上の 10 進数で、**xlCommand** は 0x8000 の 16 進数として定義されます。 
  
### <a name="invoking-excel-commands-that-use-dialog-boxes"></a>ダイアログ ボックスを使用した Excel コマンドの起動

一部のコマンド コードは、ダイアログ ボックスを使用する Excel での操作に対応しています。たとえば、**xlcFileDelete** は 1 つの引数 (ファイル名またはマスク) を取ります。ダイアログ ボックスを使用して起動し、ユーザーが削除操作をキャンセルしたり変更したりする機会を提供できます。また、ダイアログ ボックスを使用せずに呼び出すこともできます。その場合には、ファイルの削除が、ファイルが存在し、呼び出し元にアクセス許可があるという前提で、追加のやり取りなしで行われます。こうしたコマンドをダイアログ ボックス形式で呼び出すには、コマンド列挙型を、0x1000 のビット単位の OR 演算で結合する必要があります (**xlPrompt**)。
  
次のコード例では、マスク my_data\*.bak に一致する現在のディレクトリ内のファイルを削除します。その際、引数が true の場合にのみダイアログ ボックスを表示します。
  
```cs
bool delete_my_backup_files(bool show_dialog)
{
    XLOPER12 xResult, xFilter;
    xFilter.xltype = xltypeStr;
    xFilter.val.str = L"\014my_data*.bak"; // String length: 14 octal
    int cmd;
    if(show_dialog)
        cmd = xlcFileDelete | xlPrompt;
    else
        cmd = xlcFileDelete;
// xResult should be Boolean TRUE if successful, in which
// case return true; otherwise, false.
    return (Excel12(cmd, &xResult, 1, &xFilter) == xlretSuccess
        && xResult.xltype == xltypeBool
        && xResult.val.xbool == 1);
}
```

### <a name="calling-functions-and-commands-in-international-versions"></a>インターナショナル バージョンの関数およびコマンドの呼び出し

関数名および XLM コマンド名をさまざまな言語で表示するように Excel を設定できます。一部の C API コマンドおよび関数は、関数名やコマンド名として解釈される文字列を操作します。たとえば、**xlcFormula** は、指定のセルに配置される文字列引数を取ります。アドインがあらゆる言語設定で動作するためには、英語の文字列名を指定し、関数またはコマンドの列挙体にビット 0x2000 (**xlIntl**) を設定できます。
  
次のコード例では、作業中のワークシートのセル A2 に `=SUM(X1:X100)` と同等の働きをするものを配置します。 一時的な外部参照 **XLOPER** を作成するために、フレームワーク関数 **TempActiveRef** が使用されている点に注目してください。 この数式は A2 に適切なロケールに基づく言語 (たとえば、言語がフランス語の場合には `=SOMME(X1:X100)`) で表示されます。 
  
```cs
int WINAPI InternationlExample(void)
{
    XLOPER12 xSum, xResult;
    xSum.xltype = xltypeStr;
    xSum.val.str = L"\015=SUM(X1:X100)";
    Excel12(xlcFormula | xlIntl, &xResult, 2,
        &xSum, TempActiveRef(2,2,1,1));
    return 1;
}

```

> [!NOTE]
> **Excel12** の呼び出し結果は必須ではないため、**xResult** のアドレスの代わりに 0 (NULL) が 2 番目の引数として渡される可能性があります。これについては次のセクションで詳しく説明します。 
  
### <a name="dll-only-functions-and-commands"></a>DLL 専用の関数とコマンド

Excel では、DLL や XLL からのみアクセスできる関数が少数サポートされています。 これらは、ヘッダー ファイルで `(n | xlSpecial)` として定義されます。`n` は 0 以上の 10 進数で、`xlSpecial` は 0x4000 の 16 進数として定義されます。 これらの関数は以下の表にまとめられ、[API 関数リファレンス](excel-xll-sdk-api-function-reference.md)に記されています。
  
||||
|:-----|:-----|:-----|
|[xlFree](xlfree.md) <br/> |0 | xlSpecial  <br/> |Excel によって割り当てられたメモリ リソースを解放します。  <br/> |
|[xlStack](xlstack.md) <br/> |1 | xlSpecial  <br/> |Excel スタック上の空き領域を返します。  <br/> |
|[xlCoerce](xlcoerce.md) <br/> |2 | xlSpecial  <br/> |**XLOPER** と **XLOPER12** の種類の間で変換します  <br/> |
|[xlSet](xlset.md) <br/> |3 | xlSpecial  <br/> |セル値の設定のための高速なメソッドを提供します。  <br/> |
|[xlSheetId](xlsheetid.md) <br/> |4 | xlSpecial  <br/> |内部 ID からワークシート名を取得します。  <br/> |
|[xlSheetNm](xlsheetnm.md) <br/> |5 | xlSpecial  <br/> |名前から、ワークシートの内部 ID を取得します。  <br/> |
|[xlAbort](xlabort.md) <br/> |6 | xlSpecial  <br/> |ユーザーが **[キャンセル]** ボタンをクリックしたか、Esc キーを押したかを検証します。  <br/> |
|[xlGetInst](xlgetinst.md) <br/> |7 | xlSpecial  <br/> |Excel インスタンス ハンドルを取得します。  <br/> |
|[xlGetHwnd](xlgethwnd.md) <br/> |8 | xlSpecial  <br/> |Excel のメイン ウィンドウ ハンドルを取得します。  <br/> |
|[xlGetName](xlgetname.md) <br/> |9 | xlSpecial  <br/> |DLL のパスとファイル名を取得します。  <br/> |
|[xlEnableXLMsgs](xlenablexlmsgs.md) <br/> |10 | xlSpecial  <br/> |この関数は廃止されており、呼び出される必要もなくなりました。  <br/> |
|[xlDisableXLMsgs](xldisablexlmsgs.md) <br/> |11 | xlSpecial  <br/> |この関数は廃止されており、呼び出される必要もなくなりました。  <br/> |
|[xlDefineBinaryName](xldefinebinaryname.md) <br/> |12 | xlSpecial  <br/> |永続バイナリ ストレージ名を定義します。  <br/> |
|[xlGetBinaryName](xlgetbinaryname.md) <br/> |13 | xlSpecial  <br/> |永続バイナリ ストレージ名のデータを取得します。  <br/> |
   
## <a name="return-value-xloperxloper12-operres"></a>戻り値 XLOPER/XLOPER12: operRes

_operRes_ 引数は、コールバックへの 2 番目の引数であり、**XLOPER** (**Excel4** および **Excel4v**) または **XLOPER12** (**Excel12** および **Excel12v**) へのポインターでもあります。 呼び出しが正常に行われると、関数またはコマンドの戻り値が引数に含まれます。 戻り値が必要ない場合は、**operRes** を 0 (Null ポインター) に設定します。 **operRes** の以前のコンテンツは上書きされるので、以前にポイントされていたメモリは、呼び出し前に解放してメモリ リークを回避しなければなりません。 
  
関数やコマンドを呼び出すことができない場合 (たとえば、引数が正しくない場合)、**operRes** はエラー **#VALUE!** に設定されます。コマンドが成功する場合には常に **Boolean** **TRUE** を返します。失敗した場合、またはユーザーがキャンセルした場合には **FALSE** を返します。 
  
## <a name="number-of-subsequent-arguments-count"></a>2 回目以降の引数の数: count

_count_ 引数は、コールバック関数への 3 番目の引数で、32 ビット符号付き整数です。 これは、2 番目以降の引数の数に設定する必要があります。この数は 1 から始まります。 関数やコマンドが引数を取らない場合は、0 に設定してください。 Microsoft Office Excel 2003 では、任意の関数で取ることができる引数の最大数は 30 です。ただし、多くの場合に実際に取る数はそれより少なくなります。 Excel 2007 以降、任意の関数で取ることができる引数の最大数は 255 に拡張されました。 
  
**Excel4** と **Excel12** の場合、_count_ は、渡される **XLOPER** 値または **XLOPER12** 値へのポインターの数です。 _count_ が設定されている値よりも少ない数の引数を渡すことがないように十分に注意してください。 少ない数にすると、Excel はスタックを先読みし、無効な **XLOPER** 値または **XLOPER12** 値を処理しようとするため、アプリケーション クラッシュが発生する可能性があります。 
  
**Excel4v** と **Excel12v**の場合、_count_ は、次の引数と最後の引数として渡される **XLOPER** 値または **XLOPER12** 値へのポインターの配列のサイズです。 この場合も、_count_ 要素よりも小さいサイズの配列を渡すことがないように十分に注意してください。そうした配列を渡すと、配列の境界がオーバーランしてしまうことになります。 
  
## <a name="passing-arguments-to-c-api-functions"></a>C API 関数への引数の引き渡し

**Excel4** と **Excel12** は _count_ の後に可変長引数リストを受け取り、それぞれが **XLOPER** 値および **XLOPER12** 値へのポインターとして解釈されます。 **Excel4v** と **Excel12v** は _count_ の後に 1 つの引数を受け取ります。これは、**Excel4v** では **XLOPER** 値への、**Excel12v** では **XLOPER12** 値へのポインター配列へのポインターとなります。
  
配列フォーム **Excel4v** および **Excel12v** を使用すると、引数の数が可変の場合に C API への呼び出しを分かりやすくコーディングできます。次の例は、数値の可変サイズの配列を取り、C API を介して合計、平均、最小、最大を計算する Excel ワークシート関数を使用する関数について示しています。  
  
```cs
void Excel12v_example(double *dbl_array, int size, double &sum, double &average, double &min, double &max)
{
// 30 is the limit in Excel 2003. 255 is the limit in Excel 2007.
// Use the lower limit to be safe, although it is better to make
// the function version-aware and use the correct limit.
    if(size < 1 || size > 30)
        return;
// Create an array of XLOPER12 values.
    XLOPER12 *xOpArray = (XLOPER12 *)malloc(size * sizeof(XLOPER12));
// Create an array of pointers to XLOPER12 values.
    LPXLOPER12 *xPtrArray =
        (LPXLOPER12 *)malloc(size * sizeof(LPXLOPER12));
// Initialize and populate the array of XLOPER12 values
// and set up the pointers in the pointer array.
    for(int i = 0; i < size; i++)
    {
        xOpArray[i].xltype = xltypeNum;
        xOpArray[i].val.num = dbl_array[i];
        xPtrArray[i] = xOpArray + i;
    }
    XLOPER12 xResult;
    int retval;
    int fn[4] = {xlfSum, xlfAverage, xlfMin, xlfMax};
    double *result_ptr[4] = {&sum, &average, &min, &max};
    for(i = 0; i < 4; i++)
    {
        retval = Excel12v(fn[i], &xResult, size, xPtrArray);
        if(retval == xlretSuccess && xResult.xltype == xltypeNum)
            *result_ptr[i] = xResult.val.num;
    }
    free(xPtrArray);
    free(xOpArray);
}

```

前述のコードで **XLOPER12** 値への参照を **XLOPER** に、**Excel12v** への参照を **Excel4v** に置き換えると、あらゆるバージョンの Excel で動作する関数になります。Excel 関数の **SUM**、**AVERAGE**、**MIN**、**MAX** のこの操作は単純で、C におけるコーディングの効率を向上させると同時に、引数の準備や Excel への呼び出しのオーバーヘッドを回避できます。ただし、Excel に入っている関数の多くはより複雑ですが、この方法が役立つ場合もあります。 
  
[xlfRegister](xlfregister-form-1.md) のトピックには、**Excel4v** と **Excel12v** を使用した別の処理例が記されています。XLL ワークシート関数を登録すると、**[関数貼り付け]** ダイアログ ボックスで使用されている各引数の説明文字列を提供できます。そのため、**xlfRegister** に指定する引数の合計数は XLL 関数が取る引数の数に依存し、関数ごとに異なります。 
  
常に引数の数が同じ C API 関数またはコマンドを呼び出す場合には、こうした引数のポインター配列を作成するという追加手順を回避したいことがあります。その場合、**Excel4** と **Excel12** を使用する方が単純かつ分かりやすくなります。たとえば、XLL 関数とコマンドを登録するときに、DLL または XLL の完全なパスとファイル名を提供する必要があります。次の **Excel4** と **Excel12** の例に示されているように、**xlfGetName** への呼び出しでファイル名を取得し、それを **xlFree** を呼び出してリリースします。
  
```cs
XLOPER xDllName;
if(Excel4(xlfGetName, &xDllName, 0) == xlretSuccess)
{
    // Use the name, and 
    // then free the memory that Excel allocated for the string.
    Excel4(xlFree, 0, 1, &xDllName);
}
XLOPER12 xDllName;
if(Excel12(xlfGetName, &xDllName, 0) == xlretSuccess)
{
    // Use the name, and
    // then free the memory that Excel allocated for the string.
    Excel12(xlFree, 0, 1, &xDllName);
}

```

実際には、関数 **Excel12v_example** はより効率的にコーディングできます。そのためには、1 つの **xltypeMulti** **XLOPER12** 引数を作成し、**Excel12** を使用して C API を呼び出します。その例を次に示します。
  
```cs
void Excel12_example(double *dbl_array, int size, double &sum, double &average, double &min, double &max)
{
// In this implementation, the upper limit is the largest
// single column array (equals 2^20, or 1048576, rows in Excel 2007).
    if(size < 1 || size > 1048576)
        return;
// Create an array of XLOPER12 values.
    XLOPER12 *xOpArray = (XLOPER12 *)malloc(size * sizeof(XLOPER12));
// Create and initialize an xltypeMulti array
// that represents a one-column array.
    XLOPER12 xOpMulti;
    xOpMulti.xltype = xltypeMulti;
    xOpMulti.val.array.lparray = xOpArray;
    xOpMulti.val.array.columns = 1;
    xOpMulti.val.array.rows = size;
// Initialize and populate the array of XLOPER12 values.
    for(int i = 0; i < size; i++)
    {
        xOpArray[i].xltype = xltypeNum;
        xOpArray[i].val.num = dbl_array[i];
    }
    XLOPER12 xResult;
    int fn[4] = {xlfSum, xlfAverage, xlfMin, xlfMax};
    double *result_ptr[4] = {&sum, &average, &min, &max};
    for(i = 0; i < 4; i++)
    {
        Excel12(fn[i], &xResult, 1, &xOpMulti);
        if(xResult.xltype == xltypeNum)
            *result_ptr[i] = xResult.val.num;
    }
    free(xOpArray);
}

```

> [!NOTE]
> この場合、**Excel12** の戻り値は無視されます。代わりにコードによって、返された **XLOPER12** が **xltypeNum** であるかをチェックして、呼び出しが成功したかどうかを判別します。 
  
## <a name="xlcallver"></a>XLCallVer

コールバック **Excel4**、**Excel4v**、**Excel12**、**Excel12v** に加え、Excel は関数 **XLCallVer** をエクスポートします。この関数は、現在実行している C API のバージョンを返します。
  
関数プロトタイプを次に示します。
  
 `int pascal XLCallVer(void);`
  
スレッド セーフなこの関数は、あらゆる XLL コマンドまたは関数から呼び出せます。
  
Excel 97 から Excel 2003 までの場合、**XLCallVer** は 1280 = 0x0500 hex = 5 x 256 を返します。これは、Excel バージョン 5 を示します。 Excel 2007 以降では、3072 = 0x0c00 hex = 12 x 256 を返し、バージョン 12 を示します。
  
この関数を使用して実行時に新しい C API を利用できるかどうかを判断できますが、`Excel4(xlfGetWorkspace, &version, 1, &arg)` を使用して Excel の実行バージョンを検出することもできます。`arg` は、2 に設定された数値の **XLOPER** です。 この関数は、文字列 **XLOPER** を返すので、強制的に整数にすることができます。 C API バージョンではなく Excel バージョンに依存するのは、ご使用のアドインでも検出しなければならない相違が Excel 2000、Excel 2002、Excel 2003 の間にあるためです。 たとえば、一部の統計関数の精度に変更が加えられました。
  
## <a name="see-also"></a>関連項目

- [XLL を作成する](creating-xlls.md)  
- [Excel での XLL コードへのアクセス](accessing-xll-code-in-excel.md)  
- [Excel XLL SDK API 関数リファレンス](excel-xll-sdk-api-function-reference.md)  
- [C API コールバック関数 Excel4、Excel12](c-api-callback-functions-excel4-excel12.md)  
- [Excel XLL の開発](developing-excel-xlls.md)

