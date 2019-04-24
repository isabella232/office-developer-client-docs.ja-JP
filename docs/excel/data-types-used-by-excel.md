---
title: Excel で使用されるデータ型
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
keywords:
- 登録データ型 [excel 2007],Excel データ型,文字 [Excel 2007],数字 [Excel 2007],データ構造 [Excel 2007],データ型 [Excel 2007]
ms.assetid: 8740a8fb-ad67-4232-a49b-d78967a786c2
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: c546fc80b212301689744d3279a59733d9cc5524
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310907"
---
# <a name="data-types-used-by-excel"></a>Excel で使用されるデータ型

**適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
Mirosoft Excel は ANSI C/C++ 型と Excel 固有のデータ構造を交換します。 ここでこれらを説明するのは、他のセクションのコンテキスト提供のためです。詳細については、「[xlfRegister (形式 1)](xlfregister-form-1.md)」のトピックを参照してください。 
  
## <a name="ansi-cc-types"></a>ANSI C /C++ 形式

### <a name="numbers"></a>数値

すべてのバージョンの Excel：
  
- 8 バイト倍精度浮動小数点型
    
- [signed] short [int] &ndash; **Boolean** の値および整数に用いられます 
    
- unsigned short [int]
    
- [signed long] int
    
### <a name="strings"></a>文字列

すべてのバージョンの Excel：
  
- [signed] char \* &ndash;: 最大 255 文字のヌル終端文字列
    
- unsigned char \* &ndash; 最大 255 文字の length-counted バイト文字列
    
Excel 2007 以降:
  
- unsigned short \* &ndash; 最大 32,767 文字の Unicode 文字列で、ヌル終端文字列または length-counted 文字列のいずれかの形式
    
Excel のワークシート番号はすべて倍精度小数点として格納されているため、Excel でアドイン関数をこれに代わる整数型として宣言する必要はありません (むしろそうするなら小さな変換オーバーヘッドが発生します) 。
  
整数型を使用している場合、Excel は入力が型の範囲内の値であることを確認します。範囲外の場合は **#NUM!**  で失敗します。 例外は、関数を登録して、short int で実装される **Boolean** 引数を取る場合です。この場合、0 以外の入力はすべて 1 に変換され、0 は直接渡されます。 
  
## <a name="excel-specific-data-structures"></a>Excel 固有のデータ構造

すべてのバージョンの Excel：
  
- **FP**&ndash; 2 次元の浮動小数点型配列構造で、行数は最大 65,356 行、列数は Excel のバージョンでサポートされる最大数をサポートします。 
    
- **XLOPER**&ndash; 複数の型のデータ構造で、ワークシートのデータ型 (エラーを含む)、整数、範囲の参照、XLM マクロ シート フロー コントロールの型、および内部バイナリ ストレージ データの型をすべて表します。  
    
   > [!NOTE]
   > 文字列は最大 255 文字の length-counted 文字列で表されます。 
  
Excel 2007 以降:
  
- **FP12** &ndash; 2 次元の浮動小数点型配列構造で、Excel 2007 以降のすべての行および列をサポートします。 
    
- **XLOPER12**&ndash; 複数の型のデータ構造で、ワークシートのデータ型 (エラーを含む)、整数、範囲の参照、XLM マクロ シート フロー コントロールの型、および内部バイナリ ストレージ データの型をすべて表します。 
    
   > [!NOTE]
   > 文字列は、最大 32,767 文字の length-counted Unicode 文字列で表されます。 
  
## <a name="registration-data-type-codes"></a>登録データ型コード

XLL 関数は、C API 関数 **xlfRegister** を使用して登録されます。この関数は戻り値および引数の型をエンコードする文字列を 3 番目の引数として取ります。 この文字列には、関数が揮発性関数か、スレッド セーフか (Excel 2007 以降)、マクロ シートの同等関数か、また、引数をインプレース変更して結果を返すかどうかということを Excel に指示する情報も含まれています。
  
次の表は、「[xlfRegister (形式 1)](xlfregister-form-1.md)」のトピックで再度取り上げて、詳しく説明します。 ここでは、本セクションの残りのコンテキストを提供する目的で掲載しています。 たとえば、length-counted Unicode 文字列 (Excel 2007 以降) を取る関数は、C% 引数型を取る関数と表現できます。 
  
|データ型|値渡し|参照渡し (ポインター)|コメント|
|:-----|:-----|:-----|:-----|
|ブール型 (Boolean)。  <br/> |A  <br/> |L  <br/> |short (0 = false または 1 = true)  <br/> |
|double  <br/> |B  <br/> |E  <br/> ||
|char \*  <br/> ||C、F  <br/> |Null で終了する ASCII バイト文字列  <br/> |
|unsigned char \*  <br/> ||D、G  <br/> |Length-counted ASCII バイト文字列  <br/> |
|unsigned short \*  (Excel 2007 以降)  <br/> ||C%、F%  <br/> |ヌル終端 Unicode ワイド文字文字列  <br/> |
|unsigned short \*  (Excel 2007 以降)  <br/> ||D%、G%  <br/> |Length-counted Unicode ワイド文字文字列  <br/> |
|unsigned short [int]  <br/> |H  <br/> ||WORD  <br/> |
|[signed] short [int]  <br/> |I  <br/> |M  <br/> |16 ビット  <br/> |
|[signed long] int  <br/> |J  <br/> |N  <br/> |32 ビット  <br/> |
|配列  <br/> ||O  <br/> | 参照により以下の 3 つの引数として渡されます。  <br/>1. short int \*rows  <br/>2. short int \*columns  <br/>3. double \*array  <br/> |
|配列  <br/> (Excel 2007 以降)  <br/> ||O%  <br/> | 参照により以下の 3 つの引数として渡されます。  <br/>1. int \*rows  <br/>2. int \*columns  <br/>3. double \*array  <br/> |
|FP  <br/> ||K  <br/> |浮動小数点配列構造  <br/> |
|FP12  <br/> (Excel 2007 以降)  <br/> ||K%  <br/> |大グリッド浮動小数点配列構造  <br/> |
|XLOPER  <br/> ||P  <br/> |可変型のワークシートの値および配列  <br/> |
|||R  <br/> |値、配列、および範囲の参照  <br/> |
|XLOPER12  <br/> (Excel 2007 以降)  <br/> ||Q  <br/> |可変型のワークシートの値および配列  <br/> |
|||U  <br/> |値、配列、および範囲の参照  <br/> |
   
**C%**、**F%**、**D%**、**G%**、**K%**、**O%**、**Q**、および **U** は Microsoft Office Excel 2007 から登場する新しい型のため、それ以前のバージョンではサポートされません。 文字列型 **F**、**F%**、**G**、および **G%** は、インプレース変更される引数に使用します。 引数 **XLOPER** または **XLOPER12** の引数は、それぞれ **P** または **Q** の型として登録されている場合、Excel は準備段階で単一セル参照を単純数値に、複数セル参照を配列に変換します。 
  
**P** および **Q** の型は常に逆参照されるため、**xltypeRef** または **xltypeSRef** ではなく、必ず **xltypeNum**、**xltypeStr**、**xltypeBool**、**xltypeErr**、**xltypeMulti**、**xltypeMissing** または **xltypeNil** のいずれかとして入力されます。 
  
**O** の型は、スタックの 3 つの引数であり、引数が参照によって渡される Fortran Dll との互換性を確保するために導入されました。 インプレース変更の戻り値として引数を宣言し、結果を参照値に配置する場合以外では、値を返す目的で使用できません。 **O%** の型は、Excel 2007 の **O** の型を拡張したもので、Office Excel 2003 グリッドよりも広い領域をカバーしている配列にアクセスできます。 
  
## <a name="see-also"></a>関連項目

- [xlfRegister (形式 1)](xlfregister-form-1.md)
- [Excel プログラミングの概念](excel-programming-concepts.md)
- [Excel XLL SDK API 関数リファレンス](excel-xll-sdk-api-function-reference.md)

