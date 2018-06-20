---
title: DLL または XLL から Excel に呼び出す
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- ダイアログ ボックス [excel 2007] を呼び出すことは、コマンド、Dll の [Excel 2007]、[Excel 2007] のコマンドを Excel では、[Excel 2007] の C API 関数に引数を渡す方法を呼び出すことを excel のダイアログ ボックスを呼び出すと、コマンド [Excel 2007] では、DLL または xll ファイル、Excel4 からアクセスできる機能 [Excel 2007] Excel12 関数 [Excel 2007] XLCallVer [Excel 2007] の [Excel 2007] は、operRes 引数を関数、関数 [Excel 2007] では、DLL または xll ファイル、Excel12v からアクセス可能な機能の [Excel 2007]、DLL のみ [Excel 2007]、[Excel 2007] c 言語の API に渡す機能引数、引数 [Excel 2007]、コマンド [Excel 2007] では、他の言語バージョンを呼び出す、DLL 専用のコマンド [Excel 2007]、[Excel 2007] の各国語版、関数を呼び出すとカウント コマンド、Xll [Excel 2007] では、Excel 4 v 関数 [Excel への呼び出しExcel 2007]、xlfn の引数 [Excel 2007] では、関数 [Excel 2007] では、他の言語バージョンを呼び出す
localization_priority: Normal
ms.assetid: 616e3def-e4ec-4f3c-bc65-3b92710da1e6
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 3f36d2f59b7f5bef9f9ffdca4d13e95c788bf113
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798820"
---
# <a name="calling-into-excel-from-the-dll-or-xll"></a>DLL または XLL から Excel に呼び出す

**適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
Microsoft Excel を使用すると、DLL は組み込みの Excel コマンド、ワークシート関数、マクロ シート関数にアクセスできます。こうしたコマンドや関数は、Visual Basic for Applications (VBA) で呼び出される DLL コマンドと関数から、および Excel によって直接呼び出される登録済み XLL コマンドと関数から使用できます。
  
## <a name="excel4-excel4v-excel12-and-excel12v-functions"></a>Excel4、Excel4v、Excel12、Excel12v 関数

Excel では、 [Excel4](excel4-excel12.md)、 [Excel4v](excel4v-excel12v.md)、 [Excel12](excel4-excel12.md)、および[Excel12v](excel4v-excel12v.md)のコールバック関数を使用してコマンドや機能にアクセスするのには、DLL を使用できます。
  
**Excel4**と**Excel4v**関数は、Excel バージョン 4 で導入されました。 **XLOPER**データ構造で動作します。 Excel 2007 には、2 つ新しいコールバック関数、 **Excel12**と**Excel12v**、 **XLOPER12**のデータ構造体の使用が導入されています。 **Excel4**と**Excel4v**関数は、ライブラリ、DLL や XLL プロジェクトに含める必要があります Xlcall32.lib でエクスポートされます。 **XLOPER12**構造体を使用して、Excel の機能にアクセスする場合に、プロジェクトに含める必要があります Xlcall.cpp SDK の C++ ソース ファイルには、 **Excel12**と**Excel12v**が含まれます。 
  
次のコードは、これら 4 つの関数の関数プロトタイプを示します。 最初の 3 つの引数は、2 番目の引数は、最初のペアでは、 **XLOPER**へのポインターと 2 番目のペアで、 **XLOPER12**へのポインターが同じです。 呼び出し規約は、可変個引数リストを許可するには、 **Excel4**と**Excel12** **に従って _cdecl**です。 省略記号は、 **Excel4**の**XLOPER**の値と**Excel12**を**XLOPER12**の値へのポインターを表します。 _Count_パラメーターの値をポインターの数に等しくなります。 
  
**Excel のすべてのバージョン**
  
 `int _cdecl Excel4(int xlfn, LPXLOPER operRes, int count,... );`
  
 `int pascal Excel4v(int xlfn, LPXLOPER operRes, int count, LPXLOPER opers[]);`
  
**Excel 2007 の起動**
  
 `int _cdecl Excel12(int xlfn, LPXLOPER12 operRes, int count,... );`
  
 `int pascal Excel12v(int xlfn, LPXLOPER12 operRes, int count, LPXLOPER12 opers[]);`
  
**Excel4**、 **Excel4v**、 **Excel12**、または**Excel12v**を呼び出すことができる DLL、Excel は、DLL に制御を渡す必要があります。 これは、次のシナリオでのみこれらの API のコールバックを呼び出すことができることを意味します。
  
- Excel が直接または VBA を介して呼び出した XLL コマンドから。
    
- Excel が直接または VBA を介して呼び出した XLL ワークシート関数またはマクロ シート関数から。
    
次のシナリオでは、Excel C API を呼び出すことはできません。
  
- ( [DllMain](http://msdn.microsoft.com/library/base.dllmain%28Office.15%29.aspx)関数) からでは、オペレーティング システム イベント。 
    
- DLL が作成したバックグラウンド スレッドから。
    
### <a name="return-values"></a>戻り値

これら 4 つの関数はいずれも整数値を返します。この値によって、呼び出し元に対して、関数またはコマンドが正常に呼び出されたかどうかが知らされます。次のいずれかの値が返されます。
  
|**戻り値**|**として Xlcall.h で定義されています。**|**説明**|
|:-----|:-----|:-----|
|0  <br/> |**xlretSuccess** <br/> |関数やコマンドが正常に実行します。 実行が正常にエラーがないことはありません。 たとえば、 **Excel4**を返す**xlretSuccess** **検索**をには、関数を呼び出すときに評価されることも **#VALUE!** 検索文字列が見つかりませんでした。 種類と返される**XLOPER/XLOPER12**の値を検査する必要がありますこの可能性については。  <br/> |
|1  <br/> |**xlretAbort** <br/> |コマンド マクロは、 **[キャンセル**] ボタンをクリックするか、ESC キーを押すと、ユーザーによって停止されました。  <br/> |
|2  <br/> |**xlretInvXlfn** <br/> |指定された関数コードまたはコマンド コードが無効です。このエラーは、呼び出し元の関数に関数またはコマンドを呼び出すアクセス許可がない場合に生じます。たとえば、ワークシート関数は、マクロ シート情報関数またはコマンド関数を呼び出すことはできません。  <br/> |
|4  <br/> |**xlretInvCount** <br/> |呼び出しで指定した引数の数が正しくありません。  <br/> |
|8  <br/> |**xlretInvXloper** <br/> |**XLOPER**または**XLOPER12**の引数の値の 1 つ以上が正しく形成、または設定します。  <br/> |
|16  <br/> |**xlretStackOvfl** <br/> |Excel によって、操作でスタックがオーバーフローする危険が検出され、関数が呼び出されませんでした。  <br/> |
|32  <br/> |**xlretFailed** <br/> |コマンドまたは関数は、他の戻り値のいずれかで記述されていないため失敗しました。 たとえば、大量のメモリを必要とする操作はこのエラーで失敗します。 [XlCoerce](http://msdn.microsoft.com/library/guid_9d47c16c-a7e7-4998-b594-9cf001827b7b%28Office.15%29.aspx)関数を使用して、非常に大きな配列への参照を**xltypeMulti**に変換しようとしたらこれでした。  <br/> |
|64  <br/> |**xlretUncalced** <br/> |計算されていないセルの値を取得しようとする操作が行われました。Excel で再計算整合性を保持するため、ワークシート関数ではこれを行うことができません。ただし、マクロ シート関数として登録された XLL コマンドおよび関数は、計算されていないセル値にアクセスできます。  <br/> |
|128  <br/> |**xlretNotThreadSafe** <br/> |(Excel 2007 で開始)スレッド セーフとして登録されている XLL ワークシート関数は、スレッド セーフではない C API 関数を呼び出すしようとしました。 たとえば、スレッド セーフでない関数では、XLM 関数**xlfGetCell**を呼び出すことはできません。  <br/> |
|256  <br/> |**xlRetInvAsynchronousContext** <br/> |(Excel 2010 年に開始)非同期関数のハンドルが有効ではありません。  <br/> |
|512  <br/> |**xlretNotClusterSafe** <br/> |(Excel 2010 年に開始)クラスターでは、呼び出しはサポートされていません。  <br/> |
   
返しますエラー値のいずれかのテーブルで (つまり、それを返さない**xlretSuccess**)、 **XLOPER**または**XLOPER12**の戻り値も設定する **#VALUE!** です。 チェックの成功のための十分なテストがありますが、呼び出しが両方の**xlretSuccess**を返すことに注意してください、特定の状況で、 **#VALUE!** です。
  
**XlretUncalced**または**xlretAbort**のいずれかで、C API を呼び出し、DLL や XLL コードはコントロールに戻ります Excel (Excel で割り当てられたメモリを解放する[xlfree](http://msdn.microsoft.com/library/guid_8ce2eef2-0138-495d-b6cb-bbb727a3cda4%28Office.15%29.aspx)関数の呼び出し以外の他の C API の呼び出しを行う前にリソースの**XLOPER**および**XLOPER12**の値)。 
  
### <a name="command-or-function-enumeration-argument-xlfn"></a>コマンドまたは関数の列挙型引数: xlfn

_Xlfn_引数は、コールバックを最初の引数が機能し、32 ビット符号付き整数です。 次の例のようには、その値は Xlcall.h、SDK のヘッダー ファイルで定義されている関数やコマンドの列挙値のいずれかでなければなりません。 
  
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

関数は、0x0fff の 16 進数、0 (**xlfCount**) から最高 Excel 2013 での番号が割り当てられますが、すべてのワークシートとマクロ シートは、547 10 進数、0x0223 16 進数 (**xlfFloor_precise**) です。
  
0x8000 16 進数 (**xlcBeep**) から 0x8fff の 16 進数、使用の範囲のコマンドのすべての機能は、Excel 2013 での最高の割り当てられた番号は、16 進数の 0x8328 (**xlcHideallInkannots**)。 としてヘッダー ファイルでこれらの定義は、 `(n | xlCommand)` 、`n`の 10 進数は 0 以上、および**xlCommand**が 0x8000 を 16 進数として定義されています。 
  
### <a name="invoking-excel-commands-that-use-dialog-boxes"></a>ダイアログ ボックスを使用した Excel コマンドの起動

コマンド コードのいくつかは、ダイアログ ボックスを使用する Excel での操作に対応しています。 たとえば、 **xlcFileDelete**では、1 つの引数: ファイル名またはマスク。 ユーザーがキャンセルまたは削除操作を変更する機会を持ってできるようにダイアログ ボックスを起動できます。 それもなしで呼び出される] ダイアログ ボックスでは、存在して、呼び出し元がアクセス許可を持つと仮定した場合、それ以上の介入なしのファイルまたはファイルを削除する場合。 このようなコマンドを呼び出すと、ダイアログ ボックスの形式で、コマンドの列挙体を 0x1000 (**xlPrompt**) のビットごとの OR 演算を使用して組み合わせる必要があります。
  
マスク my_data に一致する現在のディレクトリ内のファイルを削除するコード例を次に示します\*.bak、引数が true の場合にのみ、ダイアログ ボックスを表示します。
  
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

関数およびコマンド名の XLM をさまざまな言語で表示するのには Excel を設定できます。 いくつかの C API コマンドおよび関数は、関数やコマンド名として解釈される文字列を操作します。 たとえば、 **xlcFormula**では、指定したセルに配置することは意図されている文字列引数を受け取ります。 アドインのすべての言語設定を使用するのには、英語の文字列名を指定し、関数やコマンドの列挙に含まれるビット 0x2000 (**xlIntl**) を設定できます。
  
コード例を次の配置のと同じ`=SUM(X1:X100)`作業中のシートのセル A2 に。 Framework 関数、 **TempActiveRef**を使用して**XLOPER**の一時的な外部参照を作成することに注意してください。 数式は A2 に含まれる適切なロケールが指定した言語で表示されます (たとえば、`=SOMME(X1:X100)`の言語がフランス語の場合)。 
  
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
> **Excel12**への呼び出しの結果が必要ないので、0 (NULL) は**xResult**のアドレスではなく 2 番目の引数として渡すことができます。 これについては次のセクションで詳細説明します。 
  
### <a name="dll-only-functions-and-commands"></a>DLL 専用の関数とコマンド

Excel には、DLL や xll ファイルからアクセスできる機能の数が少ないがサポートされています。 としてヘッダー ファイルで定義されているこれらは`(n | xlSpecial)`、`n`よりも大きい値または 0 に等しい 10 進数では、 `xlSpecial` 0x4000 16 進数として定義されています。 これらの関数は次の表に記載されているし、 [API 関数のリファレンス](excel-xll-sdk-api-function-reference.md)に記載されています。
  
||||
|:-----|:-----|:-----|
|[xlFree](xlfree.md) <br/> |0 | xlSpecial  <br/> |Excel によって割り当てられたメモリ リソースを解放します。  <br/> |
|[xlStack](xlstack.md) <br/> |1 | xlSpecial  <br/> |Excel スタック上の空き領域を返します。  <br/> |
|[xlCoerce](xlcoerce.md) <br/> |2 | xlSpecial  <br/> |**XLOPER**および**XLOPER12**型間の変換します。  <br/> |
|[xlSet](xlset.md) <br/> |3 | xlSpecial  <br/> |セル値の設定のための高速なメソッドを提供します。  <br/> |
|[xlSheetId](xlsheetid.md) <br/> |4 | xlSpecial  <br/> |内部 ID からワークシート名を取得します。  <br/> |
|[xlSheetNm](xlsheetnm.md) <br/> |5 | xlSpecial  <br/> |名前から、ワークシートの内部 ID を取得します。  <br/> |
|[xlAbort](xlabort.md) <br/> |6 | xlSpecial  <br/> |ユーザーが **[キャンセル**] ボタンがクリックされたか、ESC キーが押されたかどうかを確認します。  <br/> |
|[xlGetInst](xlgetinst.md) <br/> |7 | xlSpecial  <br/> |Excel インスタンス ハンドルを取得します。  <br/> |
|[xlGetHwnd](xlgethwnd.md) <br/> |8 | xlSpecial  <br/> |Excel のメイン ウィンドウ ハンドルを取得します。  <br/> |
|[xlGetName](xlgetname.md) <br/> |9 | xlSpecial  <br/> |DLL のパスとファイル名を取得します。  <br/> |
|[xlEnableXLMsgs](xlenablexlmsgs.md) <br/> |10 | xlSpecial  <br/> |���̊֐��͎g�p����Ă��炸�A�Ăяo�����K�v��Ȃ��Ȃ�܂����B  <br/> |
|[xlDisableXLMsgs](xldisablexlmsgs.md) <br/> |11 | xlSpecial  <br/> |���̊֐��͎g�p����Ă��炸�A�Ăяo�����K�v��Ȃ��Ȃ�܂����B  <br/> |
|[xlDefineBinaryName](xldefinebinaryname.md) <br/> |12 | xlSpecial  <br/> |永続バイナリ ストレージ名を定義します。  <br/> |
|[xlGetBinaryName](xlgetbinaryname.md) <br/> |13 | xlSpecial  <br/> |バイナリ ストレージが永続的な名前のデータを取得します。  <br/> |
   
## <a name="return-value-xloperxloper12-operres"></a>XLOPER/XLOPER12 の値を返す: operRes

_OperRes_引数では、コールバックには、2 番目の引数では、 **XLOPER** (**Excel4**および**Excel4v**) または**XLOPER12** (**Excel12**および**Excel12v**) へのポインターします。 呼び出しが成功すると、関数やコマンドの戻り値が含まれます。 **operRes**は、戻り値が必要ない場合、0 (NULL ポインター) に設定できます。 以前が指すメモリは、メモリ リークを回避するのには呼び出しをする前に解放する必要がありますように、 **operRes**の以前の内容が上書きされます。 
  
**OperRes**がエラーに設定されている場合は (たとえば、引数が適切ではありません) 場合は、関数やコマンドを呼び出すことができない、 **#VALUE!** です。 コマンドは、成功すると、 **FALSE**に失敗した場合や、ユーザーのキャンセルにより、または**ブール値****は TRUE**常に返します。 
  
## <a name="number-of-subsequent-arguments-count"></a>2 回目以降の引数の数: count

引数_count_はコールバックには、3 番目の引数では、32 ビット符号付き整数です。 1 から数えて、それ以降の引数の数を設定します。 関数やコマンドの引数をとらない場合は、0 に設定する必要があります。 ほとんどを実行するよりも少ない、Microsoft Office Excel 2003 では、任意の関数が取ることができる引数の最大数、30、です。 Excel 2007 以降では、任意の関数が取ることができる引数の最大数は 255 に増加させました。 
  
**Excel4**と**Excel12**、_カウント_は、渡される**XLOPER**または**XLOPER12**の値へのポインターの数です。 その_数_の値より少ない引数を渡すには十分に注意する必要があります] に設定されています。 Excel スタックに先読みし、無効な**XLOPER**または**XLOPER12**の値、アプリケーション クラッシュが発生する可能性がありますを処理しようとしていますが発生します。 
  
**Excel4v**と**Excel12v**は、_カウント_は、次と最後の引数として渡される**XLOPER**または**XLOPER12**の値へのポインターの配列のサイズです。 もう一度、このオーバーランが発生している配列の境界になります、サイズ、_数_の要素よりも小さく、配列を渡すには十分に注意する必要があります。 
  
## <a name="passing-arguments-to-c-api-functions"></a>C API 関数への引数の引き渡し

両方**Excel4**および**Excel12**を可変長引数リストでは、_カウント_、それぞれ**XLOPER**および**XLOPER12**の値へのポインターとして解釈されます。 **Excel4v**と**Excel12v** _カウント_ポインターの場合は**Excel4v**、 **XLOPER**の値、 **Excel12v**の場合**XLOPER12**の値の配列へのポインターである 1 つの引数がかかります。
  
配列フォーム、 **Excel4v** **Excel12v**では、引数の数が変数の場合、C API への呼び出しを正常にコードを有効にします。 次の例では、数値の可変サイズの配列を受け取るし、c 言語の API を使用して、Excel のワークシート関数を使用して、合計、平均、最小、および最大を計算する関数を示します。 
  
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

**XLOPER12**の値への参照を**XLOPER**、および**Excel4v**と**Excel12v**に置き換えて、上記のコードになりますすべてのバージョンの Excel で動作する関数。 **合計**、**平均**、**最小**、および**最大値**は、Excel の関数には、この操作は、単純に C のコードし、引数を準備して、Excel への呼び出しのオーバーヘッドを回避する方が効率的となります。 ただし、Excel に含まれている関数の多くより複雑なためこの方法をいくつかの場合に便利です。 
  
[XlfRegister](http://msdn.microsoft.com/library/guid_c730124c-1886-4a0f-8f06-79763025537d%28Office.15%29.aspx)トピックには、 **Excel4v**と**Excel12v**の別の例が用意されています。 XLL ワークシート関数を登録するときは、 **[関数貼り付け**] ダイアログ ボックスで使用されている各引数について説明する文字列を指定できます。 したがって、 **xlfRegister**を提供する合計の引数の数は、XLL 関数は、引数の数によって異なりますおり、次に 1 つの関数から異なります。 
  
C API 関数またはコマンドの引数の数が同じで常に呼び出すと、どこに、これらの引数のポインターの配列を作成する余分な手順を避けるためにします。 ような場合は、簡単、 **Excel4**と**Excel12**を使用するクリーナーがあります。 たとえば、XLL 関数とコマンドを登録するときは、DLL または xll ファイルのフル パスとファイル名を指定する必要があります。 **XlfGetName**への呼び出しでファイル名を取得し、元の呼び出しを**xlFree**、 **Excel4**と**Excel12**の両方の例を次に示すようにできます。
  
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

実際には、関数、 **Excel12v_example**、でしたをコーディングするより効率的に、1 つ**xltypeMulti** **XLOPER12**の引数を作成し、次の例のように、 **Excel12**を使用して C API を呼び出します。
  
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
> この例では、 **Excel12**の戻り値は無視されます。 コードは、返される**XLOPER12**では、呼び出しが成功したかどうかを判断するのには**xltypeNum**が、代わりにチェックします。 
  
## <a name="xlcallver"></a>XLCallVer

**Excel4**、 **Excel4v**、 **Excel12**、および**Excel12v**のコールバックだけでなく**XLCallVer**、現在実行されている C API のバージョンを返す関数が Excel にエクスポートします。
  
関数プロトタイプを次に示します。
  
 `int pascal XLCallVer(void);`
  
スレッド セーフなこの関数は、あらゆる XLL コマンドまたは関数から呼び出せます。
  
Excel 2003、Excel 97 では、 **XLCallVer**は 1280 = 値を 0x0500 の 16 進数を返します。 = 5 x 256、Excel バージョン 5 を示します。 3072 と = 場合は 0x0c00。 16 進数を返す Excel 2007 以降では、12 x 256、同様に 12 のバージョンを示します。
  
新しい C API は、実行時に使用できるかどうかを判断するには、これを使用できますが、実行中のバージョンの Excel を使用して検出する方が`Excel4(xlfGetWorkspace, &version, 1, &arg)`、`arg`は、 **XLOPER**を 2 に設定する数値です。 **XLOPER**バージョンは、整数値に強制的に変換する文字列を返します。 C API のバージョンではなく、Excel のバージョンに依存することの理由は、Excel 2000、Excel 2002 および Excel 2003 を追加で必要な場合も検出される間の相違点があること。 などが変更されたいくつかの統計関数の精度です。
  
## <a name="see-also"></a>関連項目



[XLL ��쐬����](creating-xlls.md)
  
[Excel �� XLL �R�[�h�ɃA�N�Z�X����](accessing-xll-code-in-excel.md)
  
[Excel XLL SDK API �֐����t�@�����X](excel-xll-sdk-api-function-reference.md)
  
[C API �R�[���o�b�N�֐� Excel4�AExcel12](c-api-callback-functions-excel4-excel12.md)
  
[Excel XLL �̊J��](developing-excel-xlls.md)

