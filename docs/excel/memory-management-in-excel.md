---
title: Excel のメモリ管理
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- xloper12 メモリ[Excel 2007]、Excel によるメモリ管理、Excel スタック、文字列[Excel 2007]、メモリ管理、Excel によるメモリ管理、XLOPER メモリ[Excel 2007]、メモリ[Excel 2007]、管理ガイドライン
localization_priority: Normal
ms.assetid: 3bf5195b-6235-43cf-8795-0c7b0a63a095
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f129dac2971f01c8ada15f0028958132b1945746
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419542"
---
# <a name="memory-management-in-excel"></a>Excel のメモリ管理

 **適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
効率的で安定した XLL を作成する場合には、メモリ管理が最も重要な課題となります。メモリを管理できないと Microsoft Excel で様々な問題が生じる可能性があります。たとえば、メモリ割り当てや初期化の効率が悪くなったり、小規模なメモリ リークが生じたりするといった比較的小さな問題から、Excel が不安定になるといった大きな問題などが起こる原因となります。
  
メモリの管理ミスは、アドイン関連の深刻な問題の最も一般的な原因です。したがって、メモリ管理に関して一貫性のあるよく考え抜かれた戦略でプロジェクトを構築する必要があります。 
  
Microsoft Office Excel 2007 では、マルチスレッドでのワークブック再計算が導入され、メモリ管理がより複雑になりました。スレッドセーフワークシート関数を作成、エクスポートする場合は、複数のスレッドのアクセスが集中したときに発生する可能性がある競合を管理する必要があります。
  
次の 3 つのデータ構造型に関してメモリの留意事項があります。
  
- **XLOPER**および**XLOPER12**
    
- **XLOPER**または**XLOPER12**にない文字列
    
- **FP**および**FP12**配列 
    
## <a name="xloperxloper12-memory"></a>XLOPER/XLOPER12 メモリ

**XLOPER**/ **XLOPER12**データ構造には、メモリブロックへのポインタを含むサブタイプ、つまり文字列（**xltypeStr**）、配列（**xltypeMulti**）、 および外部参照（**xltypeRef**）があります。 **xltypeMulti**配列には、文字列**XLOPER **/ **XLOPER12s**を含めることができ、これがさらに他のメモリブロックを指すこともできます。 
  
**XLOPER**/ **XLOPER12**は、いくつかの方法によって作成できます。 
  
- Excel によって。XLL 関数に渡される引数を準備するとき
    
- Excel によって。C API 呼び出しで**XLOPER**または**XLOPER12**を返すとき 
    
- DLL によって。C API 呼び出しに渡される引数を作成するとき
    
- DLL によって。XLL 関数の戻り値を作成するとき
    
いずれかのメモリ ポイント型のメモリ ブロックは、次のいくつかの方法で割り当てることができます。
  
- 関数コード外の DLL で静的ブロックとすることができます。この場合、メモリを割り当てたり解放したりする必要はありません。
    
- 関数コード内の DLL で静的ブロックとすることができます。この場合、メモリを割り当てたり解放したりする必要はありません。
    
- DLLによって動的に割り当てられ、解放される方法はいくつかあります。**malloc**と** free**、**new**と**delete**などです。
    
- Excel で動的に割り当てることができます。
    
考えうる**XLOPER**/ **XLOPER12**メモリーの起点数、および**XLOPER**/ ** XLOPER12**がそのメモリーが割り当てている状況の数を踏まえれば、この問題が非常に難しいであろうことに驚きはありません。しかしながら、いくつかの規則やガイドラインに従えば、複雑さは大幅に軽減されます。 
  
### <a name="rules-for-working-with-xloperxloper12"></a>XLOPER/XLOPER12 を扱うときの規則

- XLL 関数に引数として渡される**XLOPER**/ **XLOPER12**のメモリを解放したり、上書きしたりしないでください。そのような引数は読み取り専用として扱います。詳しくは、「[Excel XLL 開発における既知の問題](known-issues-in-excel-xll-development.md)」の「引数をそのまま変更して**XLOPER**または**XLOPER12**を返す」を参照してください。
    
- C API の呼び出しでDLL に返された**XLOPER**/ **XLOPER12**にExcelがメモリを割り当てた場合： 
    
  - [xlFree](xlfree.md)への呼び出しを使用して、**XLOPER**/ **XLOPER12**が不要になったら、メモリーを解放する必要があります。メモリを解放するのに、freeやdeleteなど他の方法を使用しないでください。
    
  - 返された型が**xltypeMulti**の場合、文字列が含まれていたり、また文字列で上書きしようとしている際は特に、配列内の**XLOPER**/ **XLOPER12**を上書きしないでください。
    
  - DLL 関数の戻り値として**XLOPER**/ **XLOPER12**をExcel に返す場合は、完了時に解放する必要があるメモリがあることをExcel に通知する必要があります。 
    
- C API 呼び出しへの戻り値として作成された**XLOPER**/ **XLOPER12**に対してのみ、**xlFree**を呼び出す必要があります。 
    
- DLL が、DLL 関数の戻り値としてExcel に返したい**XLOPER**/ **XLOPER12**にメモリを割り当てている場合は、そのDLL が解放すべきメモリーがあることをExcel に通知する必要があります。 
    
### <a name="guidelines-for-memory-management"></a>メモリ管理のガイドライン

- メモリを割り当てて解放するために使用するメソッドを DLL 内で一貫させます。異なるメソッドが混在しないようにします。メモリ クラスまたは構造体で使用するメソッドをラップし、対象メソッドが使用されている多くの場所でコードを変えなくても変更できるようにすることをお勧めします。
    
- DLL 内に**xltypeMulti**配列を作成するときは、文字列へのメモリ割り当て方法の一貫性を保ってください。常に動的にメモリに割り当てるか、常に静的メモリを使用してください。これによって、メモリを解放するときに、文字列を常に解放する必要があるか、あるいは解放しないべきかがわかります。 
    
- Excel が作成した**XLOPER**/ **XLOPER12**をコピーするときは、Excel に割り当てられたメモリのディープコピーを作成してください。
    
- Excel が割り当てた文字列**XLOPER**/ **XLOPER12**を**xltypeMulti **配列内に配置しないでください。該当の文字列のディープコピーを作成し、そのコピーへのポインタを配列に格納してください。 
    
## <a name="freeing-excel-allocated-xloperxloper12-memory"></a>Excel が割り当てた XLOPER/XLOPER12 メモリを解放する

次のXLL コマンドを考えてみましょう。これは**xlGetName**を使用してDLL のパスとファイル名を含む文字列を取得し、**xlcAlert**を使用して警告ダイアログボックスに表示します。
  
```cs
int WINAPI show_DLL_name(void)
{
    XLOPER12 xDllName;
    if(Excel12(xlfGetName, &xDllName, 0) == xlretSuccess)
    {
        // Display the name.
        Excel12(xlcAlert, 0, 1, &xDllName);
        // Free the memory that Excel allocated for the string.
        Excel12(xlFree, 0, 1, &xDllName);
    }
    return 1;
}

```

関数が**xDllName**が指すメモリーを必要としなくなった場合、DLL専用のC API 関数の1つである[xlFree関数](xlfree.md)への呼び出しを使用して解放できます。 
  
**xlFree**関数は関数参照セクションに全て記述されています（[DLL、またはXLL からのみ呼び出すことができる C API 関数](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)を参照）が、以下の点に注意してください。
  
- **xlFree**への1回の呼び出しで、複数の**XLOPER**/ **XLOPER12**へのポインタを渡すことができます。ただし、実行中のExcelバージョン（Excel 2003では30、Excel 2007以降は255）でサポートされる関数引数の数によってのみ制限されます。
    
- **xlFree**は、既に解放されている**XLOPER**/ **XLOPER12**の解放試行が安全か確かめるため、含まれているポインターを**NULL**に設定します。**xlFree**は、その引数を変更する唯一のC API 関数です。 
    
- C API への呼び出しの戻り値に使用される**XLOPER**/ **XLOPER12**の上には、メモリーへのポインターが含まれているかどうかに関係なく、**xlFree**を安全に呼び出すことができます。 
    
## <a name="returning-xloperxloper12s-to-be-freed-by-excel"></a>Excel で解放される XLOPER/XLOPER12 を返す

事前のセクションのコマンド例を変更し、**Boolean****true**引数、および **#N/A**その他を渡すとDLLパスとファイル名を返すワークシート関数に変更したいとします。 文字列メモリを解放するため、Excel関数に**xlFree**を呼び出すことは明らかにできません。ただし、それがある時点で解放されていない場合、アドインは関数が呼び出されるたびにメモリをリークします。この問題を回避するには、 **XLOPER**/ **XLOPER12**の**xltype**フィールドにxcall.h の**xlbitXLFree**と定義してビットを設定します。 これを設定すると、値のコピーが終了したら、返されたメモリを解放する必要があることがExcelに伝えられます。 
  
### <a name="example"></a>例

次のコード例は、XLL ワークシート関数に変換された、前のセクションの XLL コマンドを示しています。
  
```cs
LPXLOPER12 WINAPI get_DLL_name(int calculation_trigger)
{
    static XLOPER12 xRtnValue; // Not thread-safe
    Excel12(xlfGetName, &xRtnValue, 0);
// If xlfGetName failed, xRtnValue will be #VALUE!
    if(xRtnValue.xltype == xltypeStr)
    {
// Tell Excel to free the string memory after
// it has copied out the return value.
        xRtnValue.xltype |= xlbitXLFree;
    }
    return &xRtnValue;
}
```

**XLOPER**/ **XLOPER12**を使用するXLL 関数は、**XLOPER**/ ** XLOPER12**へのポインタを取得して返すものとして宣言する必要があります。この例の関数内での静的**XLOPER12**の使用は、スレッドセーフではありません。この関数をスレッドセーフとして誤って登録することはできますが、**xRtnValue**が別のスレッドで終了する前に1つのスレッドによって上書きされる危険があります。 
  
それを割り当てるExcel コールバックへの呼び出しの後に**xlbitXLFree**を設定する必要があります。これより前に設定した場合は、上書きされ、必要な効果を発揮しません。ワークシートに返す前に別のC API 関数の呼び出しで引数として値を使用する予定の場合は、そのような呼び出しの後にこのビットを設定する必要があります。そうしないと、**XLOPER**/ **XLLOPER12**型をチェックする前に、このビットをマスクしない関数を混同してしまうでしょう。 
  
## <a name="returning-xloperxloper12s-to-be-freed-by-the-dll"></a>DLL で解放される XLOPER/XLOPER12 を返す

これと同様の問題は、XLL が**XLOPER**/ **XLOPER12**にメモリを割り当て、それをExcel に返したい場合に発生します。 Excel は、xlcall.hの**xlbitDLLFree**として定義される**XLOPER**/ **XLOPER12**の**xltype**フィールドに設定できる別のビットを認識します。 
  
このビットが設定された**1 XLOPER**/ **XLOPER12**を受け取ると、Excelは[xlAutoFree](xlautofree-xlautofree12.md)という名前の、XLL によってエクスポートされるであろう関数を呼び出そうとします。  （ **XLOPER**） や **xlAutoFree12**の場合、 （**XLOPER12** の場合）。この機能については、関数リファレンス（[アドインマネージャおよびXLL インタフェース関数](add-in-manager-and-xll-interface-functions.md)を参照）で詳細に記載されていますが、ここでは最小限の実装例を示します。その目的は、 **XLOPER**/ **XLOPER12**メモリを、元々割り当てられていた方法と一致する方法で解放することです。 
  
### <a name="examples"></a>例

次の関数例は、DLL名の前に「このDLLのフルパス名は」というテキストが含まれている点を除けば、この前の関数と同じです。
  
```cs
#include <string.h>
LPXLOPER12 WINAPI get_DLL_name_2(int calculation_trigger)
{
    static XLOPER12 xRtnValue; // Not thread-safe
    Excel12(xlfGetName, &xRtnValue, 0);
// If xlfGetName failed, xRtnValue will be #VALUE!
    if(xRtnValue.xltype != xltypeStr)
        return &xRtnValue;
// Make a copy of the DLL path and file name.
    wchar_t *leader = L"The full pathname for this DLL is ";
    size_t leader_len = wcslen(leader);
    size_t dllname_len = xRtnValue.val.str[0];
    size_t msg_len = leader_len + dllname_len;
    wchar_t *msg_text = (wchar_t *)malloc(msg_len + 1);
    wcsncpy_s(msg_text + 1, leader, leader_len);
    wcsncpy_s(msg_text + 1 + leader_len, xRtnValue.val.str + 1,
        dllname_len);
    msg_text[0] = msg_len;
// Now the original string has been copied Excel can free it.
    Excel12(xlFree, 0, 1, &xRtnValue);
// Now reuse the XLOPER12 for the new string.
    xRtnValue.val.str = msg_text;
// Tell Excel to call back into the DLL to free the string
// memory after it has copied out the return value.
    xRtnValue.xltype     = xltypeStr | xlbitDLLFree;
    return &xRtnValue;
}
```

前の関数をエクスポートしたXLLでの**xlAutoFree12**の最低限の実装は次のとおりです。 
  
```cs
void WINAPI xlAutoFree12(LPXLOPER12 p_oper)
{
    if(p_oper->xltype == (xltypeStr | xlbitDLLFree))
        free(p_oper->val.str);
}
```

この実装は、XLL が**XLOPER12**文字列のみを返し、それらの文字列が**malloc**を使用してのみ割り当てられる場合にのみ満たされます。テストは 
  
 ` if(p_oper->xltype == xltypeStr) `
  
**xlbitDLLFree**が設定されている場合、失敗することに注意してください。 
  
一般に、**xlAutoFree**および**xlAutoFree12**は、XLL で作成された** xltypeMulti**配列および**xltypeRef**外部参照に関連付けられているメモリを解放するように実装する必要があります。 
  
動的に割り当てられた**XLOPER**および**XLOPER12**を返すように、XLL 関数を実装するということもできます。 この場合、サブタイプに関係なく、**xlbitDLLFree**をそのような**XLOPER**および**XLOPER12**すべてに設定する必要があります。 また、**xlAutoFree**および**xlAutoFree12**を実装して、このメモリーが解放され、**XLOPER**/ **XLOPER12**内で指定されているすべてのメモリーを解放する必要もあります。 これは、戻り値をスレッド セーフにする 1 つの方法です。 たとえば、前述の関数を次のように書き換えることができます。
  
```cs
#include <string.h>
LPXLOPER12 WINAPI get_DLL_name_3(int calculation_trigger)
{
// Thread-safe
    LPXLOPER12 pxRtnValue = (LPXLOPER12)malloc(sizeof(XLOPER12));
    Excel12(xlfGetName, pxRtnValue, 0);
// If xlfGetName failed, pxRtnValue will be #VALUE!
    if(pxRtnValue->xltype != xltypeStr)
    {
// Even though an error type does not point to memory,
// Excel needs to pass this oper to xlAutoFree12 to
// free pxRtnValue itself.
        pxRtnValue->xltype |= xlbitDLLFree;
        return pxRtnValue;
    }
// Make a copy of the DLL path and file name.
    wchar_t *leader = L"The full pathname for this DLL is ";
    size_t leader_len = wcslen(leader);
    size_t dllname_len = pxRtnValue->val.str[0];
    size_t msg_len = leader_len + dllname_len;
    wchar_t *msg_text = (wchar_t *)malloc(msg_len + 1);
    wcsncpy_s(msg_text + 1, leader, leader_len);
    wcsncpy_s(msg_text + 1 + leader_len, pxRtnValue->val.str + 1,
        dllname_len);
    msg_text[0] = msg_len;
// Now the original string has been copied Excel can free it.
    Excel12(xlFree, 0, 1, pxRtnValue);
// Now reuse the XLOPER12 for the new string.
    pxRtnValue->val.str = msg_text;
    pxRtnValue->xltype = xltypeStr | xlbitDLLFree;
    return pxRtnValue;
}
void WINAPI xlAutoFree12(LPXLOPER12 p_oper)
{
    if(p_oper->xltype == (xltypeStr | xlbitDLLFree))
        free(p_oper->val.str);
    free(p_oper);
}
```

**xlAutoFree**および**xlAutoFree12**について詳しくは、[xlAutoFree/xlAutoFree12](xlautofree-xlautofree12.md)を参照してください。
  
## <a name="returning-modify-in-place-arguments"></a>変更インプレース引数を返す

Excel では、XLL 関数はインプレースで引数を変更して値を返すことができます。この操作は、ポインターとして渡された引数でのみ行うことができます。このような処理を行うには、関数を登録するときに、変更対象の引数を Excel に通知しなければなりません。 
  
この方法で値を返すことは、ポインターで渡すことができるすべてのデータ型でサポートされていますが、特に以下の型で便利です。
  
- 長さが計測され、null で終了する ASCII バイト文字列
    
- 長さが計測され、null で終了する Unicode ワイド文字列（Excel 2007以降）
    
- **FP** 浮動小数点配列 
    
- **FP12** 浮動小数点配列（Excel 2007以降） 
    
> [!NOTE]
> この方法で**XLOPER**または**XLOPER12**を返さないでください。詳しくは、[Excel XLL開発における既知の問題](known-issues-in-excel-xll-development.md)を参照してください。 
  
単にreturn 文を使用するのではなく、この手法を使用する利点は、Excel が戻り値にメモリを割り当てることです。 Excel が返されたデータの読み取りを終了すると、メモリを解放します。これはXLL の機能からメモリ管理作業を取り除きます。この手法はスレッドセーフです。Excel によって異なるスレッドで同時に呼び出された場合、各スレッドの各関数呼び出しにはそれぞれでバッファーがあります。
  
**XLOPER**/ **XLOPER12**に対して存在するメモリの追返還を解放するためDLL に呼び戻すメカニズムは、単純な文字列および**FP**/ **FP12**配列には存在しないため、特に上記のデータ型の場合に役立ちます。したがって、DLL で作成された文字列または浮動小数点配列を返すときは、次の選択肢があります。 
  
- 永続的ポインタを動的に割り当てられたバッファに設定し、ポインタを返します。次の関数呼び出しでは、（1）ポインタがnull でないことを確認し、（2）事前の呼び出しで割り当てられたリソースを解放し、ポインタをnull にリセットし、（3）新しく割り当てられたメモリブロックへのポインタを再利用します。
    
- 文字列と配列を、解放する必要がない静的バッファーに作成し、そのバッファーへのポインターを返します。
    
- 引数をインプレースで変更します。その際、文字列または配列を Excel 外の領域に直接書き込みます。
    
それ以外の場合は、**XLOPER**/ **XLOPER12**を作成し、リソースを解放するため**xlbitDLLFree**および**xlAutoFree** / **xlAutoFree12 **を使用する必要があります。 
  
最後の選択肢は、戻り値と同じ型の引数が渡される場合には最も簡単な方法です。覚えておきたい重要な点はバッファサイズが限られていることで、オーバーランさせないよう非常に注意しなければなりません。これを誤ると、Excelがクラッシュする可能性があります。文字列と**FP**/ **FP12**配列のバッファサイズについては次に説明します。 
  
## <a name="strings"></a>文字列

文字列のメモリ管理に関する問題が、アプリケーションとアドインが不安定になる最も一般的な原因です。文字列を処理する方法 (null 終了または長さカウント (あるいはその両方)、静的バッファーまたは動的バッファー、固定長またはほぼ無制限の長さ、オペレーティング システム管理メモリ (たとえば、OLE Bstr など)、アンマネージ文字列など) が多様なことを考慮すると、これは理解できないことではありません。
  
C/C++ プログラマは、null で終わる文字列には馴染みが深いです。標準Cライブラリは、そのような文字列を扱うように設計されています。コード内の静的文字列リテラルは、null で終わる文字列にコンパイルされます。別の方法として、Excelは一般的にnull で終了しない長さを数えた文字列を扱います。これらの諸事実から、文字列と文字列メモリの処理方法に関して、DLL / XLL内では明確で一貫したアプローチが必要です。
  
最も一般的な問題を以下に示します。
  
- 有効なポインターを予期し、ポインター自体の妥当性自体を検査しない、または検査できない関数に、null または無効なポインターを渡すこと。
    
- 書き込まれる文字列の長さに対してバッファーの長さをチェックしないまたはできない関数が、文字列バッファーの境界をオーバーランする。
    
- 静的文字列バッファー メモリ、または既に解放された文字列バッファー メモリ、解放する方法と一貫しない方法で割り当てられた文字列バッファー メモリを解放しようとしている。
    
- 割り当てられたものの解放されいない文字列から生じるメモリ リーク。通常、頻繁に呼び出される関数で生じます。
    
### <a name="rules-for-strings"></a>文字列の規則

**XLOPER**/ **XLOPER**と同様に、従う規則とガイドラインがあります。ガイドラインは前のセクションで示したものと同じです。ここでの規則は、特に文字列に関する規則の拡張です。
  
 **規則:**
  
- XLL関数に引数として渡された文字列**XLOPER**/ **XLOPER12**、単純な長さ計測済み文字列またはnull で終わる文字列を、メモリーを解放したり上書きしたりしないでください。そのような引数は読み取り専用として扱います。
    
- ExcelがC API コールバック関数の戻り値に文字列**XLOPER**/ ** XLOPER12**にメモリを割り当てる場合は、**xlFree**を使用して解放するか、XLL関数からExcelに返す場合は**xlbitXLFree**を設定します。 
    
- DLL が**XLOPER**/ **XLOPER12**に文字列バッファを動的に割り当てる場合は、終了時に割り当てた方法と一致する方法で解放するか、XLL関数からExcelに返すならば**xlbitDLLFree**を設定し**xlAutoFree**/ **xlAutoFree12**を開放します。
    
- Excel がC API の呼び出しでDLL に返された**xltypeMulti**配列にメモリを割り当てている場合は、配列内で文字列**XLOPER**/ **XLOPER12**を上書きしないでください。そのような配列は、**xlFree**を使用して解放、またはXLL関数によって返されるならは**xlbitXLFree**を設定することによってのみ解放しなくてはいけません。
    
### <a name="string-types-supported"></a>サポートされる文字列型

**C API xltypeStr XLOPER/XLOPER12s**

|**バイト文字列：** XLOPER ****|**ワイド文字列：** XLOPER12 ****|
|:-----|:-----|
|すべてのバージョンの Excel  <br/> |Excel 2007 以降  <br/> |
|最大長：255拡張ASCIIバイト  <br/> |最大長: 32,767 Unicode 文字  <br/> |
|最初の (符号なし) バイト = 長さ  <br/> |最初の Unicode 文字 = 長さ  <br/> |
   
> [!IMPORTANT]
> **XLOPER**または**XLOPER12**文字列のnull 終了を想定しないでください。 
  
**C / C ++文字列**

|**バイト文字列**|**ワイド文字列**|
|:-----|:-----|
|null 終了（**char** *） "C"最大長：255拡張ASCIIバイト  <br/> |null 終了（**wchar_t** *） "C％"最大長32,767のUnicode文字  <br/> |
|長さ計測済（**unsigned char** *） "D"  <br/> |長さ計測済（**wchar_t ** *） "D％"  <br/> |
   
### <a name="strings-in-xltypemulti-xloperxloper12-arrays"></a>xltypeMulti XLOPER/XLOPER12 配列内の文字列

場合によっては、Excel はDLL / XLL で使用するための**xltypeMulti**配列を作成します。いくつかのXLM 情報関数はそのような配列を返します。たとえば、C API 関数**xlfGetWorkspace**は、引数*44*を渡されると、現在登録されているすべてのDLLプロシージャを記述する文字列を含む配列を返します。C API 関数**xlfDialogBox**は、文字列のディープコピーを含む配列引数の修正コピーを返します。おそらく、XLL で**xltypeMulti**配列に遭遇する最も一般的な状況は、配列がXLL 関数への引数として渡されたか、または範囲参照から強制された場所がこの型となっているかです。後者の場合、Excelはソースセル内の文字列のディープコピーを作成し、配列内でこれらを指します。 
  
DLL 内の文字列を変更したい場合は、そのディープコピーを作成してください。独自の**xltypeMulti**配列を作成しているときは、その中にExcel 割り当て文字列**XLOPER**/ **XLOPER12**を配置しないでください。後でそれらが正しく解放されない、またはまったく解放されないという危険性があります。やはり、文字列のディープコピーを作成し、そのコピーへのポインタを配列に格納してください。
  
 **例**
  
次の関数例は、長さ計測済のUnicode 文字列の動的に割り当てられたコピーを作成します。呼び出し側は、この例で割り当てられたメモリを**delete**[]を使用して最終的に解放する必要があります。また、ソース文字列はnull で終了するとは見なされません。安全のために必要であればコピー文字列は切り捨てられ、それはnull で終了しません。
  
```cs
#include <string.h>
#define MAX_V12_STRBUFFLEN    32678
    
wchar_t * deep_copy_wcs(const wchar_t *p_source)
{
    if(!p_source)
        return NULL;
    size_t source_len = p_source[0];
    bool truncated = false;
    if(source_len >= MAX_V12_STRBUFFLEN)
    {
        source_len = MAX_V12_STRBUFFLEN - 1; // Truncate the copy
        truncated = true;
    }
    wchar_t *p_copy = new wchar_t[source_len + 1];
    wcsncpy_s(p_copy, p_source, source_len + 1);
    if(truncated)
        p_copy[0] = source_len;
    return p_copy;
}
```

引数が文字列の場合、引数のコピーを返す次のエクスポート可能なXLL 関数に示すように、この関数は**XLOPER12**のコピーに安全に使用できます。他のすべての型は長さゼロの文字列として返されます。領域は処理されないことに注意してください 。**#VALUE!** の関数が返されます。この関数は、参照が値として渡されるように、U型の引数を取るものとして登録する必要があります。これは組み込みワークシート関数 **T()** と同じですが、**AsText**もエラーを長さゼロの文字列に変換します。このコード例では、**delete**を使用して、**xlAutoFree12**が渡されたポインターとその内容を解放すると想定しています。
  
```cs
LPXLOPER12 WINAPI AsText(LPXLOPER12 pArg)
{
    LPXLOPER12 pRtnVal = new XLOPER12;
// If the input was an array, only operate on the top-left element.
    LPXLOPER *pTemp;
    if(pArg->xltype == xltypeMulti)
        pTemp = pArg->val.array.lparray;
    else
        pTemp = pArg;
    switch(pTemp->xltype)
    {
        case xltypeErr:
        case xltypeNum:
        case xltypeMissing:
        case xltypeNil:
        case xltypeBool:
            pRtnVal->xltype = xltypeStr | xlbitDLLFree;
            pRtnVal->val.str = deep_copy_wcs(L"\000");
            return pRtnVal;
        case xltypeStr:
            pRtnVal->xltype = xltypeStr | xlbitDLLFree;
            pRtnVal->val.str = deep_copy_wcs(pTemp->val.str);
            return pRtnVal;
        
        default: // xltypeSRef, xltypeRef, xltypeFlow, xltypeInt
            pRtnVal->xltype = xltypeErr | xlbitDLLFree;
            pRtnVal->val.err = xlerrValue;
            return pRtnVal;
    }
}
```

### <a name="returning-modify-in-place-string-arguments"></a>変更インプレース文字列引数を返す

型**F**、**G**、**F％**、および**G％** として登録された引数は、その場で変更ができます。Excelがこれらの型の文字列引数を準備しているとき、最大長バッファを作成します。その後、たとえこの文字列が非常に短くても、引数文字列をその中にコピーします。これにより、XLL関数はその戻り値を同じメモリに直接書き込むことができます。 
  
こうした型のために取り分けられるバッファー サイズは次のとおりです。
  
- **バイト文字列:** 256 バイト (長さカウンター (G 型) または null 終端 (F 型) を含みます)。 
    
- **Unicode 文字列:** 32,768 ワイド文字 (65,536 バイト)(長さカウンター (G% 型) または null 終端 (F% 型) を含みます)。 
    
> [!NOTE]
> バッファが十分な大きさで割り当てられていることは確認できないため、そのような関数をVisual Basic for Applications（VBA）から直接呼び出すことはできません。十分に大きいバッファを明示的に渡した場合にのみ、他のDLLから安全にそのような関数を呼び出すことができます。 
  
これは、標準ライブラリー関数**wcsrev**を使用して、渡されたnull で終わるワイド文字列を元に戻すXLL 関数の例です。この場合の引数は、タイプ{3 F％** として登録されます。
  
```cs
void WINAPI reverse_text_xl12(wchar_t *text)
{
    _wcsrev(text);
}
```

## <a name="persistent-storage-binary-names"></a>永続記憶 (バイナリ名)

バイナリ名は定義され、バイナリのブロック、つまりワークブックと一緒に格納されている非構造化データに関連付けられます。これらは関数[xlDefineBinaryName](xldefinebinaryname.md)を使用して作成され、データは関数[xlGetBinaryName](xlgetbinaryname.md)を使用して取得されます。両方の関数は関数リファレンスにより詳細な説明がありますが（[ DLL またはXLL からしか呼び出せないC API 関数](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)を参照）、また両方とも**xltypeBigData** **XLOPER**/ **XLOPER12**を使用します。 
  
バイナリ名の実用的な適用を制限する既知の問題については、[ Excel XLL開発における既知の問題](known-issues-in-excel-xll-development.md)を参照してください。
  
## <a name="excel-stack"></a>Excel のスタック

Excel は、読み込んだすべての DLL とスタック領域を共有します。通常、スタック領域は普段の使用量よりも多く、次に取り上げるいくつかのガイドラインに従う限りは問題となることはありません。 
  
- 非常に大きな構造体をスタックの値によって関数の引数として渡さないでください。代わりにポインタまたはリファレンスを渡してください。
    
- 大きな構造体をスタックに返さないでください。静的または動的に割り当てられたメモリへのポインタを返すか、またはリファレンスによって渡された引数を使用してください。
    
- 関数コード内で非常に大きな自動変数構造を宣言しないでください。必要な場合は、それらを静的として宣言してください。
    
- 再帰深度が常に浅いことが確実でない限り、関数を再帰的に呼び出さないでください。代わりにループを使ってみてください。
    
DLL がC API を使用してExcel に呼び戻されるとき、Excel は最初に、可能性上最悪の呼び出し方法に対して十分なスペースがスタック上にあるかどうかを確認します。十分なスペースがない可能性があると思われる場合は、たとえ実際にその特定の呼び出しに対する十分なスペースがあったとしても、呼び出しが安全であるとは言えません。この場合、呼び戻しにはコード**xlretFailed**が返されます。 C API とスタックの通常の使用では、これがC API呼び出しの失敗の原因となる可能性は低いです。
  
このエラーが発生する場合、または懸念する場合、あるいは原因不明のエラー発生原因としてのスタック領域の不足を解消する場合、[xlStack](xlstack.md) 関数への呼び出しでスタック領域がどれほどあるかを調べることができます。 
  
## <a name="see-also"></a>関連項目



[Excel でのマルチスレッド再計算](multithreaded-recalculation-in-excel.md)
  
[Excel におけるマルチスレッド処理とメモリ競合](multithreading-and-memory-contention-in-excel.md)
  
[Excel XLL の開発](developing-excel-xlls.md)

