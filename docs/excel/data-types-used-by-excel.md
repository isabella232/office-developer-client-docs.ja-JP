---
title: Excel で使用されるデータ型
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
keywords:
- 登録データ タイプが [excel 2007]、Excel のデータ型、文字列 [Excel 2007]、[Excel 2007] の数値、データ構造 [Excel 2007]、[Excel 2007] のデータ型
localization_priority: Normal
ms.assetid: 8740a8fb-ad67-4232-a49b-d78967a786c2
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: b32a9beb2f77c12e6b6f2c445672c717a2546386
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798779"
---
# <a name="data-types-used-by-excel"></a>Excel で使用されるデータ型

**適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
Microsoft Excel では、いくつかの ANSI C および C++ の型ともいくつか Excel に固有のデータ構造体を交換します。 他のセクションでは、コンテキストを提供するここではこれらとは、 [xlfRegister (フォーム 1)](xlfregister-form-1.md)のトピックで詳しく説明します。 
  
## <a name="ansi-cc-types"></a>ANSI C と C++ の型

### <a name="numbers"></a>数字

すべてのバージョンの Excel：
  
- 8 バイト倍精度浮動小数点型
    
- [int] の [署名] 短い&ndash;の整数および**ブール**値の使用 
    
- unsigned short [int]
    
- [signed long] int
    
### <a name="strings"></a>文字列

すべてのバージョンの Excel：
  
- [署名] char \* &ndash;を 255 文字以内の文字列を null で終わるバイト
    
- char 型の符号なし\*&ndash;を 255 文字以内の文字列をバイトの長さのカウント
    
Excel 2007 で開始します。
  
- 符号なしの短い\* &ndash; 、null で終わるか、長さのカウントは、最大 32,767 文字の Unicode 文字列
    
Excel のワークシート番号はすべて倍精度小数点として格納されているため、Excel でアドイン関数をこれに代わる整数型として宣言する必要はありません (むしろそうするなら小さな変換オーバーヘッドが発生します) 。
  
整数型を使用している場合 Excel ことを確認、型の範囲内では、入力に失敗した **#NUM!** これら以外の場合。 短い整数を使用して実装、**ブール型**の引数を使用する関数を登録する場合は例外です。この例では、0 以外の任意の入力が 1 に変換し、0 を渡すとストレート。 
  
## <a name="excel-specific-data-structures"></a>Excel に固有のデータ構造体

すべてのバージョンの Excel：
  
- **FP**&ndash;浮動小数点数の 2 次元の配列構造体の特定のバージョンの Excel でサポートされている最大の番号の列で最大 65,356 の行をサポートします。 
    
- **XLOPER**&ndash; (エラーを含む) すべてのワークシートのデータ型、整数、範囲の参照、XLM マクロ シート フロー コントロールの種類、および内部バイナリ ストレージのデータ型を表すことができます複数の種類のデータ構造体です。 
    
   > [!NOTE]
   > 文字列は最大 255 文字の length-counted 文字列で表されます。 
  
Excel 2007 で開始します。
  
- **FP12**&ndash;浮動小数点数の 2 次元の配列構造体のすべての行と列が Excel 2007 の起動をサポートします。 
    
- **XLOPER12**&ndash; (エラーを含む) すべてのワークシートのデータ型、整数、範囲の参照、XLM マクロ シート フロー コントロールの種類、および内部バイナリ ストレージのデータ型を表すことができます複数の種類のデータ構造体です。 
    
   > [!NOTE]
   > 文字列は、最大 32,767 文字の length-counted Unicode 文字列で表されます。 
  
## <a name="registration-data-type-codes"></a>登録データは、コードを入力します。

XLL 関数は、戻り値と引数の型をエンコードする文字の文字列を 3 番目の引数として受け取り、C API 関数**xlfRegister**を使用して登録されます。 この文字列には、関数は揮発性かどうかを Excel に通知はスレッド セーフである (Excel 2007 で開始)、マクロ シートに対応する情報も含まれていて、かどうか、その結果を返します場所引数を変更することによってします。
  
次の表は再現し、 [xlfRegister (フォーム 1)](xlfregister-form-1.md)のトピックで詳しく説明します。 このセクションの残りのコンテキストを提供するためにここでは再現されます。 たとえば、型 C % 引数を受け取るよう (Excel 2007 で始まる) の長さのカウントの Unicode 文字列を受け取る関数を記述する可能性があります。 
  
|データ型|値渡し|参照渡し (ポインター)|コメント|
|:-----|:-----|:-----|:-----|
|ブール型 (Boolean)。  <br/> |A  <br/> |L  <br/> |short (0 = false または 1 = true)  <br/> |
|double  <br/> |B  <br/> |E  <br/> ||
|char\*  <br/> ||C、F  <br/> |Null で終了する ASCII バイト文字列  <br/> |
|符号なし char 型\*  <br/> ||D、G  <br/> |長さのバイトの ASCII 文字列をカウント  <br/> |
|符号なしの短い\*(Excel 2007 で開始)  <br/> ||C%、F%  <br/> |Unicode ワイド文字の null で終わる文字列  <br/> |
|符号なしの短い\*(Excel 2007 で開始)  <br/> ||D%、G%  <br/> |Unicode ワイド文字文字列の長さのカウント  <br/> |
|unsigned short [int]  <br/> |H  <br/> ||WORD  <br/> |
|[signed] short [int]  <br/> |I  <br/> |M  <br/> |16 ビット  <br/> |
|[signed long] int  <br/> |J  <br/> |N  <br/> |32 ビット  <br/> |
|配列  <br/> ||O  <br/> | 参照により以下の 3 つの引数として渡されます。  <br/>1. 短い int\*行  <br/>2. 短い int\*列  <br/>3 倍\*配列  <br/> |
|配列  <br/> (Excel 2007 で開始)  <br/> ||O%  <br/> | 参照により以下の 3 つの引数として渡されます。  <br/>1. int\*行  <br/>2. int\*列  <br/>3 倍\*配列  <br/> |
|FP  <br/> ||K  <br/> |浮動小数点配列構造  <br/> |
|FP12  <br/> (Excel 2007 で開始)  <br/> ||K%  <br/> |浮動小数点配列構造体の大規模なグリッド  <br/> |
|XLOPER  <br/> ||P  <br/> |可変型のワークシートの値および配列  <br/> |
|||R  <br/> |値、配列、および範囲の参照  <br/> |
|XLOPER12  <br/> (Excel 2007 で開始)  <br/> ||Q  <br/> |可変型のワークシートの値および配列  <br/> |
|||U  <br/> |値、配列、および範囲の参照  <br/> |
   
**C %** **F %** **D %** **G %** **K %** **O %** **Q**、 **U**がすべての Microsoft Office Excel 2007 で新しいとは種類は、以前のバージョンでサポートされています。 **F** **F %** **G**、および**G の %** は、文字列型は、引数には、場所の変更に使用されます。 **XLOPER**または**XLOPER12**の引数はそれぞれ**P**または**Q**の種類として登録されている、Excel は準備をするときに単純な値を 1 つのセル参照とアレイへの複数のセル参照を変換します。 
  
**P**と**Q**の種類は常に、関数に次の種類の 1 つとして到着した: **xltypeNum**、 **xltypeStr**、 **xltypeBool**、 **xltypeErr**、 **xltypeMulti**、 **xltypeMissing**、 **xltypeNil**、または、**xltypeRef**または**xltypeSRef**ではないため、これらを常に逆参照します。 
  
引数が参照によって渡される Fortran Dll との互換性のために本当にスタック上の 3 つの引数には、 **O**の種類が導入されました。 変更・ イン ・ プレースの戻り値として引数を宣言して、参照されている値に結果を配置することによって以外の値を取得するには使用できません。 型 **%o%** は、Office Excel 2003 グリッドよりも大きい領域をカバーしているアレイにアクセスできるように、Excel 2007 では**O**型を拡張します。 
  
## <a name="see-also"></a>関連項目

- [xlfRegister (�`�� 1)](xlfregister-form-1.md)
- [Excel �v���O���~���O�̊T�O](excel-programming-concepts.md)
- [Excel XLL SDK API �֐����t�@�����X](excel-xll-sdk-api-function-reference.md)

