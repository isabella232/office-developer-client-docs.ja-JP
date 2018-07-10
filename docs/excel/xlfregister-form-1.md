---
title: xlfRegister (形式 1)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfRegister
keywords:
- xlfregister function [excel 2007]
localization_priority: Normal
ms.assetid: c730124c-1886-4a0f-8f06-79763025537d
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 4fb4e8656b4f27105a30764cdda020849a07645e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798980"
---
# <a name="xlfregister-form-1"></a>xlfRegister (形式 1)

**適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
DLL または xll ファイルのコマンドで、Microsoft Excel で呼び出されました自体から呼び出すことができます。 これは Excel XLM マクロ シートから**登録**を呼び出すことになります。 
  
**xlfRegister**は、2 つの形式で呼び出すことができます。 
  
- xlfRegister (形式 1):1 つのコマンドまたは関数を登録します。
    
- [xlfRegister (2)](xlfregister-form-2.md): 荷重し、xll ファイルをアクティブにします。
    
フォーム 1 で呼び出されると、この関数は DLL の関数またはコマンドを Excel から使用できるように、使用カウントを 1 に設定し、 [xlUDF](xludf.md)または**xlfCall**関数を使用して、後で関数を呼び出すには使用することができる登録 ID を返します。 登録 ID は、 [xlfUnregister (フォーム 1)](xlfunregister-form-1.md)を使用して関数の登録を解除するのにも使用します。 関数が登録されていない場合は**xlfRegister**を再度呼び出すことの使用カウントをインクリメントします。 
  
この形式の関数は、関数やコマンドの登録 ID にも関数の文字列引数、 _pxFunctionText_であるし、評価される非表示の名前を定義します。 関数の登録を解除するには、 [xlfSetName](xlfsetname.md)を使用してこの名前を削除します。 詳細については、 [Excel の XLL の開発での既知の問題点](known-issues-in-excel-xll-development.md)を参照してください。
  
```cs
Excel12(xlfRegister, LPXLOPER12 pxRes, int iCount,
    LPXLOPER12 pxModuleText,   LPXLOPER12 pxProcedure,
    LPXLOPER12 pxTypeText,     LPXLOPER12 pxFunctionText,
    LPXLOPER12 pxArgumentText, LPXLOPER12 pxMacroType,
    LPXLOPER12 pxCategory,     LPXLOPER12 pxShortcutText,
    LPXLOPER12 pxHelpTopic,    LPXLOPER12 pxFunctionHelp,
    LPXLOPER12 pxArgumentHelp1, LPXLOPER12 pxArgumentHelp2,
        ...);
```

## <a name="parameters"></a>�p�����[�^�[

_pxModuleText_(**xltypeStr**)
  
関数を含む DLL の名前です。 これは、登録されている関数が現在実行中の DLL 内でも場合は、xll ファイル専用の関数[xlGetName](xlgetname.md)を呼び出すことによって取得できます。 
  
_pxProcedure_(**xltypeStr**または**xltypeNum**)
  
文字列の場合は、呼び出す関数の名前です (DLL コード内で示された名前)。数字の場合は、呼び出す関数のエクスポートの順序番号です。明確にするために、常に文字列形式を使用します。
  
_pxTypeText_(**xltypeStr**)
  
関数の引数の型と関数の戻り値の型を指定する省略可能な文字列です。 詳細については、「解説」セクションを参照してください。 [XlAutoRegister 関数](xlautoregister-xlautoregister12.md)または**xlAutoRegister12**を含むスタンドアロン DLL (XLL) に、この引数を省略できます。 
  
> [!NOTE]
> **xlAutoRegister12**は、Excel 2007 でのみサポートされます。 
  
この引数が不足するいると**xlfRegister**を呼び出すと、Excel **xlAutoRegister**や**xlAutoRegister12**、いずれかが必要がありますし、正しく関数を登録する、この情報を提供することにより、指定された DLL に存在します。
  
_pxFunctionText_(**xltypeStr**)
  
関数名は、関数ウィザードに表示されます。 この引数は省略可能です。省略すると、関数は、関数ウィザードでは使用できませんし、XLM マクロ シートの関数の登録 ID を使用して**呼び出す**関数を使用してのみ呼び出すことができます。 したがって、通常のワークシートで使用するため必要に応じて、この引数を処理する必要があります。 
  
_pxArgumentText_(**xltypeStr**)
  
関数の引数を記述する省略可能なテキスト文字列です。 ユーザー関数ウィザードで表示されます。 省略すると、Excel は、 _pxTypeText_からの基本的な説明を作成します。
  
_pxMacroType_(**xltypeNum**または**xltypeInt**)
  
XLL のエントリ ポイントの種類を示す、省略可能な引数。既定値 (省略した場合) は 1 です。
  
|||||
|:-----|:-----|:-----|:-----|
| _pxMacroType 値_ <br/> |0  <br/> |1  <br/> |2  <br/> |
|ワークシートから呼び出し可能  <br/> |はい  <br/> |はい  <br/> |いいえ  <br/> |
|マクロ シートから呼び出し可能  <br/> |はい  <br/> |はい  <br/> |はい  <br/> |
|定義済みの名前の定義から呼び出し可能  <br/> |はい  <br/> |はい  <br/> |はい  <br/> |
|条件付き書式の式から呼び出し可能  <br/> |はい  <br/> |はい  <br/> |いいえ  <br/> |
|ワークシート関数の関数ウィザードに表示される  <br/> |いいえ  <br/> |はい  <br/> |いいえ  <br/> |
|マクロ シート関数の関数ウィザードに表示される  <br/> |いいえ  <br/> |はい  <br/> |はい  <br/> |
   
実習では、ワークシート関数をマクロ シートと同等の機能の 1 の 1 を使用する必要があります (タイプとして登録されている**#**) コマンドは、ワークシート、および 2 から呼び出したいです。 
  
> [!NOTE]
> XLL コマンドは隠されているため、実行中のマクロのダイアログ ボックスには表示されません。ただし、有効なコマンド名が必要になる場所では、その名前を入力できます。 
  
_pxCategory_(**xltypeStr**または**xltypeNum**)
  
省略可能な引数。新しい関数またはコマンドが、どのカテゴリに属するかを指定できます。関数ウィザードは、関数を種類 (カテゴリ) ごとに分類します。カテゴリ名または連番を指定できます。この番号は、関数ウィザードに表示されるカテゴリの位置を表します。詳細については、「カテゴリ名」セクションを参照してください。省略すると、ユーザー定義のカテゴリと見なされます。
  
_pxShortcutText_(**xltypeStr**)
  
大文字と小文字が区別される 1 文字の文字列。このコマンドに割り当てるコントロール キーを指定します。たとえば、"A" の場合は、このコマンドを CONTROL + SHIFT + A に割り当てます。この引数は省略可能です。また、コマンド専用です。
  
_pxHelpTopic_(**xltypeStr**)
  
ヘルプ ファイル (.chm ファイルおよび .hlp) 場合、ユーザー定義関数が表示されます)、ユーザーがヘルプ ボタンをクリックしたときに表示するを参照します。 フォームでは、`filepath!HelpContextID`または`http://address/path_to_file_in_site!0`。 前に、と後の両方の部分、"!"が必要。  *ヘルプ コンテキスト Id*は、単一引用符が含まれていない必要があり、Excel を使用して 4 バイト長で、10 進数の符号なし整数に変換されます。 形式の URL を使用している場合のみ参照されているヘルプ ファイルが開かれます。 
  
_pxFunctionHelp_(**xltypeStr**)
  
省略可能な文字列。カスタム関数が選択されたときに関数ウィザードに表示される説明です。
  
_pxArgumentHelp1_(**xltypeStr**)
  
省略可能。 関数が関数ウィザードで選択されている場合は、カスタム関数の引数を記述する文字列の最初の。 Excel 2003 および以前のバージョンでは、 **xlfRegister**は引数を持ち、最大で 30 のみ、関数の引数の最初の 20 にこのヘルプを提供できるようにします。 Excel 2007 以降では、 **xlfRegister**ことができます引数を受け取る最大 255 245 までの関数パラメーターのヘルプを提供できるようにします。 
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

登録が成功した場合、この関数は、 **xlUDF**および**xlfUnregister** dll、または****登録解除**し、** XLM マクロ シート内への呼び出しで使用できる関数 (**xltypeNum**) のレジスタ ID を返します。 それ以外の場合、#VALUE を返します。 エラーです。 
  
## <a name="remarks"></a>備考

### <a name="data-types"></a>データ型

_PxTypeText_引数では、戻り値のデータ型および DLL 関数またはコード リソースのすべての引数のデータ型を指定します。 _PxTypeText_の最初の文字は、戻り値のデータ型を指定します。 残りの文字は、すべての引数のデータ型を示します。 などの浮動小数点数を取得し、整数と浮動小数点数を引数として受け取り、DLL 関数では、 _pxTypeText_引数に"BIB"を必要があります。 
  
XLL とのデータ交換のために Excel で使用されるデータ型と構造体については、次の 2 つの表にまとめています。
  
最初の表は、Excel のすべてのバージョンでサポートされる型を示しています。
  
|**データ型**|**値渡しで渡す**|**参照 (ポインター) を渡す**|**Comments**|
|:-----|:-----|:-----|:-----|
|ブール型 (Boolean)。  <br/> |A  <br/> |L  <br/> |short [int] (0 = false または 1 = true)  <br/> |
|double  <br/> |B  <br/> |E  <br/> ||
|char\*  <br/> ||C、F  <br/> |Null で終了する ASCII バイト文字列  <br/> |
|符号なし char 型\*  <br/> ||D、G  <br/> |カウント付き ASCII バイト文字列  <br/> |
|unsigned short [int]  <br/> |H  <br/> ||16 ビットの Word  <br/> |
|[signed] short [int]  <br/> |I  <br/> |M  <br/> |16 ビットの符号付き整数  <br/> |
|[signed long] int  <br/> |J  <br/> |N  <br/> |32 ビットの符号付き整数  <br/> |
|FP  <br/> ||K  <br/> |浮動小数点配列構造  <br/> |
|配列  <br/> ||O  <br/> |次の 3 つの引数が渡されます。<br/>符号なし短整数\*<br/>符号なし短整数\*<br/>-をダブルクリック  <br/> |
|XLOPER  <br/> ||P  <br/> |可変型のワークシートの値および配列  <br/> |
|||R  <br/> |値、配列、および範囲の参照  <br/> |
   
次のデータ型が導入された Excel 2007 で大規模なグリッドと長の Unicode をサポートするために文字列をします。
  
|**データ型**|**値渡しで渡す**|**参照 (ポインター) を渡す**|**Comments**|
|:-----|:-----|:-----|:-----|
|符号なし短\*  <br/> ||C%、F%  <br/> |Null で終了する Unicode ワイド文字文字列  <br/> |
|符号なし短\*  <br/> ||D%、G%  <br/> |カウント付き Unicode ワイド文字文字列  <br/> |
|FP12  <br/> ||K%  <br/> |大きなグリッドの浮動小数点配列構造  <br/> |
|配列  <br/> ||O%  <br/> |次の 3 つの引数が渡されます。<br/>-int を符号付き\*/RW\*<br/>-int を符号付き\*/段\*<br/>-をダブルクリック  <br/> |
|XLOPER12  <br/> ||Q  <br/> |可変型のワークシートの値および配列  <br/> |
|||U  <br/> |値、配列、および範囲の参照  <br/> |
   
次のデータを Excel 2010 で開始の種類が導入されました。
  
|**データ型**|**値渡しで渡す**|**参照 (ポインター) を渡す**|**Comments**|
|:-----|:-----|:-----|:-----|
|XLOPER12  <br/> ||X  <br/> |非同期ハンドルは、Excel および xll ファイルによって、保留中の非同期関数の呼び出しを追跡するために使用されます。また、文字列型のパラメーターの型の存在は、非同期として関数を指定します。非同期関数の詳細については、 [Asynchronous User-Defined 関数](asynchronous-user-defined-functions.md)を参照してください。  <br/> |
   
**F** **F %** **G**、および**G の %** は、文字列型は、引数には、場所の変更に使用されます。 
  
前の表に示されたデータ型を使用する場合は、次の点に注意してください。
  
- C 言語の宣言では、コンパイラが既定で 8 バイトの double、2 バイトの short integer、4 バイトの long integer を使用すると想定しています。
    
- Dll やコード リソース内のすべての関数は、呼び出し規約 _ **_stdcall**を使用して呼び出されます。 
    
- データ型を参照で返す関数 (何かへのポインターを返す関数) は、安全に NULL ポインターを返せます。Excel は、NULL ポインターを #NUM! エラーと解釈します。
    
## <a name="additional-data-type-information"></a>追加のデータ型情報

このセクションには、 **E**、 **F** **F %**、 **G** **G %**、 **K**、 **O**、 **P**、 **Q** **R**、および**U**のデータ型に関する詳細情報と_の pxTypeText に関するその他の情報が含まれています_引数です。 
  
### <a name="e-data-type"></a>E データ型

Excel は、E データ型を使用する DLL がスタック上の浮動小数点数へのポインターを渡すことを期待します。これは、コプロセッサ エミュレーター スタック上の数値が渡されることを期待する一部の言語 (Borland C++ など) で問題を起こす可能性があります。回避策としては、コプロセッサ スタック上の数値へのポインターを渡します。次の例は、Borland C++ から double が返される方法を示しています。
  
```cpp
typedef double * lpDbl;
extern "C" lpDbl __stdcall AddDbl(double D1,
    double D2, WORD npDbl)
{
    lpDbl Result;
    Result = (lpDbl)MK_FP(_SS, npDbl);
    *Result = D1 + D2;
    return (Result);
}
```

### <a name="f-f-g-and-g-data-types"></a>F、F %、G、および G % のデータ型

**F** **F %** **G**、および**G %** のデータ型、関数は、Excel によって割り当てられた文字列バッファーを変更できます。 戻り値の型コードがこれらの種類のいずれかの場合は、関数によって返される値は無視されます。 代わりに、Excel では、最初の対応するデータ型 (**F** **F %** **G**、または**G %**)、関数の引数のリストを検索し、戻り値として割り当てられた文字列バッファーの現在の内容を実行し、します。 **F**および**G**の ASCII 文字列のすべてのバージョンの Excel が 256 バイトを割り当てるし、Excel 2007 の 65,536年の開始は、割り当てられたバイト数、32,768 の Unicode 文字は、 **% の F**および**G %** の Unicode 文字列を十分です。 バッファーする必要があります含まれている (タイプ**G**と**G %**) の数文字または null 終了文字 ( **F**と**F**型)、実際の最大文字列の長さが 255 から 32,767 になるよう注意してください。 タイプ**F %** と **% の G**の引数と Unicode 文字列を Excel では c 言語の API を通じてのみ利用できます。 
  
### <a name="k-and-k-data-types"></a>K と K % のデータ型

**K**と**K %** のデータ型は、可変サイズの FP と FP12 構造へのポインターをそれぞれ使用します。 XLLCALL では、これらの構造体が定義されています。H. FP12 の構造体と型**K %** 引数では、のみサポートで Excel 2007 を起動します。 
  
### <a name="o-and-o-data-types"></a>O と O % のデータ型

**O**と**O %** のデータ型は、引数に対してのみ使用できますに**O**または**O %** の型引数を変更する、値が返されますが、値を返さない。 3 つの項目を渡す各: 浮動小数点数の 2 次元配列へのポインター、配列の列数へのポインター、配列内の行の数へのポインター。 
  
O または O によって渡される配列を変更するのには % のデータ入力を使って"> O"または"> O %" _pxTypeText_の引数として。 配列を変更する方法の詳細については、このトピックの「変更の場所:: 関数 Void として宣言される」を参照してください。 
  
データ型**O**は引数を参照で渡す Fortran Dll と直接の互換性のために作成されました。 
  
**%O%** は Excel 2007 での起動はサポートされてし、Excel がサポートするロー数の拡大に対応します。 
  
### <a name="p-and-q-data-types"></a>P と Q のデータ型

DLL 関数の引数を使用するか、 **P** XLOPERs の型を受け取るよう登録されて、 **Q** XLOPER12s を入力、Excel は、次の引数を準備する際に単純な値を 1 つのセル参照、配列への複数のセル参照に変換します。 つまり、 **P**と**Q**の種類は、常に到着、関数のこれらの種類の 1 つとして: **xltypeNum**、 **xltypeStr**、 **xltypeBool**、 **xltypeErr**、 **xltypeMulti**、 **xltypeMissing**、**または xltypeNil**がない**xltypeRef**または**xltypeSRef の**ため、これらを常に逆参照します。 **XLOPER12**の s と**Q**の型引数をのみサポートで Excel 2007 を起動します。 
  
戻り値の型の**xltypeMissing**または**xltypeNil**を使用する場合は、数値 0 として Excel を使用して解釈されます。 **xltypeMissing**は、呼び出し側が引数を省略するときに渡されます。 **xltypeNil**は、呼び出し元は、空のセルへの参照を通過するときに渡されます。 セルの範囲は、 **P**または**Q**を入力として渡すことは、 **xltypeMulti**に変換するときに、任意の空白セルの範囲内では、 **xltypeNil**配列の要素に変換されます。 リテラル、配列内の欠落している要素は、同様に**xltypeNil**の要素として渡されます。 
  
### <a name="volatile-functions-and-recalculation"></a>揮発性関数と再計算

ワークシートで、行うことができます DLL 関数またはコード リソース揮発性で、ワークシートを再計算するたびに再計算されるようにします。 これを行うには、 _pxTypeText_の引数の最後の引数のコードの後に感嘆符 (!) を追加します。 
  
> [!NOTE]
> 既定では、関数をタイプ**R** XLOPERs がかかる**U** XLOPER12s の入力やマクロとして登録されているシートの対応する (タイプ**#** は次のセクションを参照してください)、Excel では揮発性として処理されます。 
  
### <a name="functions-declared-as-void"></a>Void として宣言された関数

void を返すように関数を宣言する必要があるケースは 2 つあります。どちらのケースも、関数は別の方法で結果を返します。
  
#### <a name="modifying-in-place"></a>引数の変更

1 桁の数字_n_は、 _n_は 1 から 9 までの数値で_pxTypeText_、戻り値の型コードを使用できます。 戻り値として_pxTypeText_の _n_th の引数で示される場所で変数の値を Excel に指示します。 これは、引数の変更とも呼ばれます。 _N_th 引数は、参照渡しのデータ型 (C、D、E、F、F %、G、G %、K、K %、L、M、N、O、O %、P、Q、R、または U) である必要があります。 また DLL 関数またはコード リソースは、C または C++ 言語 (または、**プロシージャ**にキーワード Pascal 言語) で**void**キーワードを使って宣言する必要もあります。 
  
たとえば、DLL 関数の引数は位置の文字列を変更できますの整数値に null で終わる文字列と 2 つのポインターを受け取る。 _PxTypeText_の引数として"1 fmm"を使用し、関数を void として宣言します。 
  
以前のバージョンの Excel を使用**\>** 関数が void として宣言されていると、最初の引数が場所に変更することを示すために_pxTypeText_の開始時、最初以外の引数を変更する方法はありませんでした。 **\>** は_n_ = 現在のバージョンの Excel での使用はこの 1**\>** 同期機能では、旧バージョンとの互換性を保つのためサポートされています。 
  
#### <a name="asynchronous-functions"></a>非同期関数

**PxTypeText**X の型のパラメーターを使用して表される非同期関数は、最初の関数呼び出しからの結果を返しません。 代わりに、void として非同期の関数を宣言する必要があり、後でアドインでコールバックで結果が返されます。 非同期関数を使用して登録する必要があります**\>** **pxTypeText**の先頭にします。 非同期関数は、**\>** 関数が void として宣言されているが場所の最初の引数が変更されたことを示していないことを意味します。 非同期関数の詳細については、 [Asynchronous User-Defined 関数](asynchronous-user-defined-functions.md)を参照してください。 

### <a name="registering-worksheet-functions-as-macro-sheet-equivalents-handling-uncalculated-cells"></a>ワークシート関数をマクロ シートに対応する (計算されていないセルを処理する) として登録します。

配置すること、**#** 文字の後、 _pxTypeText_で最後のパラメーターのコードはマクロ シートの関数、呼び出し元と同じアクセス許可の機能を提供します。 次のとおり。 
  
- この再計算サイクルでは、まだ計算されていないセルの値を取得できる関数。
    
- 関数は、 **xlfGetCell**など、XLM 情報 (クラス 2) 関数のいずれかを呼び出すことができます。
    
- シャープ記号 (#) が存在しないかどうか: **xlretUncalced**エラー、および現在の関数が計算されないセルの結果を評価する呼び出されますもう一度セルを計算するとします。**xlfCaller**以外の任意の XLM 情報関数を呼び出すことで**xlretInvXlfn**エラーが発生します。 
    
### <a name="registering-worksheet-functions-as-thread-safe"></a>ワークシート関数をスレッド セーフとして登録します。

Excel は、Excel 2007 以降では、マルチ スレッドのブックの再計算を実行できます。 これは、再評価の同時実行スレッドをスレッド セーフでない関数の別のインスタンスを割り当てることができることを意味します。 Excel 2007 以降では、組み込みのワークシート関数のほとんどは、スレッド セーフです。 Excel 2007 以降では、Excel、Xll ワークシート関数をスレッド セーフとして登録できます。 これを行うを含む、 **$** _pxTypeText_の最後のパラメーターのコードの後に文字。 
  
> [!NOTE]
> のみワークシート関数は、スレッド セーフとして宣言できます。 Excel はマクロ シートと同じ関数のスレッド セーフであるように、両方を追加することはできませんを考慮していない**#** と**$** _pxTypeText_の引数の文字です。 
  
スレッド セーフとして関数を登録した場合ことをスレッド セーフな方法で動作するが、Excel は、C API を使用してスレッド セーフな呼び出しを拒否します。 たとえば、スレッド セーフでない関数は、 **xlfGetCell**を呼び出そうとすると、 **xlretNotThreadSafe**エラーが発生した呼び出しは失敗します。 
  
### <a name="registering-worksheet-functions-as-cluster-safe"></a>クラスター セーフとしてワークシート関数を登録します。

Excel は、Excel 2010 以降では、指定された計算クラスターのプロバイダーへの関数呼び出しをオフロードできます。 詳細については、[クラスターの安全な関数](cluster-safe-functions.md)を参照してください。 クラスター セーフとして登録されている任意の XLL ワークシート関数では、クラスターがある場合に割り当てることで参加します。 クラスター セーフな関数を含めることによって登録されている、 **&amp;** _pxTypeText_の引数の最後のパラメーターのコードの後の文字です。 
  
クラスター セーフとして関数を登録した場合、クラスター セーフな方法で動作することを確認する必要があります。 詳細については、[クラスターの安全な関数](cluster-safe-functions.md)を参照してください。
  
> [!NOTE]
> ワークシート関数だけは、クラスター セーフとして宣言することができます。 Excel はマクロ シートと同じ関数を両方を追加することはできませんように、クラスター セーフを考慮していない**#** と**&amp;** _pxTypeText_の引数の文字です。 ワークシート関数は、クラスター セーフとスレッド セーフの両方として宣言することができます。 この例では、Excel によって、これらの関数に参画するマルチ スレッド再計算クラスターのオフロードを無効にするとできます。 
  
### <a name="category-names"></a>カテゴリ名

次のガイドラインを使用して、カスタムの XLL 関数の分類先カテゴリについて判断してください。
  
- 関数は、アドインのユーザー インターフェイスの一部として、ユーザーが行うことがある場合は、[**コマンド**] カテゴリ関数を配置する必要があります。 
    
- 関数には、アドインの状態に関する情報、またはその他の有用な情報が返された場合は、**情報**カテゴリの関数を配置する必要があります。 
    
- アドインを追加する必要があることはありません関数またはコマンド カテゴリに追加**ユーザーが定義されています**。 このカテゴリが、エンド ・ ユーザーが排他的に使用します。 
    
カテゴリを指定するには、 **xlfRegister**、 _pxCategory_パラメーターを使用しています。 数値またはハード コーディングの標準的なカテゴリのいずれかに対応するテキストまたは DLL で指定された新しいカテゴリのテキストを指定できます。 入力した文字列が存在しない場合、Excel はその名前の新しいカテゴリを作成します。
  
ワークシートから [**関数貼り付け**] ダイアログ ボックスを表示するときに表示される標準的なカテゴリを次の表に一覧します。 
  
|**番号**|**Text**|
|:-----|:-----|
|1  <br/> |財務  <br/> |
|2  <br/> |日付&amp;時間  <br/> |
|3  <br/> |数値演算&amp;三角  <br/> |
|4  <br/> |テキスト  <br/> |
|5  <br/> |論理演算子  <br/> |
|6  <br/> |参照&amp;参照  <br/> |
|7  <br/> |データベース  <br/> |
|8  <br/> |統計  <br/> |
|9  <br/> |情報  <br/> |
|14  <br/> |ユーザー定義  <br/> |
||(Excel 2007 の起動) エンジニア リング  <br/> |
||(Excel 2007 の起動) キューブ  <br/> |
   
さらに、これらのカテゴリも表示されているマクロ シート内から、[**関数貼り付け**] ダイアログ ボックスを表示するときです。 
  
|**番号**|**Text**|
|:-----|:-----|
|10  <br/> |コマンド  <br/> |
|11  <br/> |DDE/外部  <br/> |
|12  <br/> |ユーザー設定  <br/> |
|13  <br/> |マクロ制御  <br/> |
   
### <a name="example"></a>例

**XlAutoOpen**関数のコードを参照してください`\SAMPLES\GENERIC\GENERIC.C`。
  
## <a name="see-also"></a>関連項目

- [REGISTER.ID](xlfregisterid.md)
- [UNREGISTER](xlfunregister-form-1.md)
- [�d�v�Ŗ�ɗ��� C API XLM �֐�](essential-and-useful-c-api-xlm-functions.md)
