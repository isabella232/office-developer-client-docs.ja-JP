---
title: Excel の再計算
manager: kelbow
ms.date: 08/22/2018
ms.audience: Developer
ms.topic: overview
keywords:
- forced calculation [excel 2007],selective recalculation [Excel 2007],functions [Excel 2007], volatile,calculation modes,recalculated cells [Excel 2007],dependence [Excel 2007],specified worksheet calculation [Excel 2007],recalculation [Excel 2007],workbook tree rebuild [Excel 2007],range calculation [Excel 2007],Excel recalculation,volatile functions [Excel 2007],functions [Excel 2007], non-volatile,active worksheet calculation [Excel 2007],dirty cells [Excel 2007],non-volatile functions [Excel 2007],forced recalculation [Excel 2007]
ms.assetid: b4c38442-42e6-4fd2-a1b0-97cfa3300379
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.localizationpriority: high
ms.openlocfilehash: ac4078ca77cacc220e1449d4cf28a9b569f4f550
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592964"
---
# <a name="excel-recalculation"></a>Excel の再計算

**適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Excel の再計算は、複数の方法でトリガーできます。次に、その例を挙げます。
  
- 新しいデータを入力する (Excel が、このトピックで説明する自動計算モードの場合)。
    
- ブックの一部またはすべての再計算を Excel に明示的に指示する。
    
- 行または列を削除または挿入する。
    
- **[保存前に再計算]** オプションをオンにしているときにブックを保存する。 
    
- 特定の [オートフィルタ] のアクションを実行する。
    
- 行または列の区切り線をダブルクリックする (自動再計算モード時)。
    
- 定義された名前を追加、編集、または削除する。
    
- ワークシートの名前を変更する。
    
- 別のワークシートとの相対位置を変更する。
    
- 列ではなく、行を非表示または再表示する。
    
> [!NOTE]
> このトピックでは、ユーザーが直接キーを押したりマウスをクリックしたりすることと、コマンドやマクロによって該当するタスクが実行されることを区別しません。ユーザーはコマンドを実行するか、何らかの操作によってコマンドが実行されるようにしますが、これはユーザー アクションと見なされます。そのため、「ユーザー」というフレーズは、「ユーザー、またはユーザーによって開始されたコマンドまたはプロセス」という意味にもなります。 
  
## <a name="dependence-dirty-cells-and-recalculated-cells"></a>依存関係、ダーティ セル、および再計算されるセル

Excel のワークシートの計算は、3 段階のプロセスと見なせます。
  
1. 依存関係ツリーの構築
    
2. 計算チェーンの構築
    
3. セルの再計算
    
依存関係ツリーによって、Excel は、セル間の依存関係または同等性、セル間の参照関係についての情報を得ます。Excel は、このツリーから計算チェーンを構築します。計算チェーンは、数式を格納しているすべてのセルの一覧であり、計算される順序で並べられています。再計算時に、まだ計算されていないセルに依存する数式が見つかると、このチェーンは Excel によって改訂されます。この場合、計算されるセルとそのセルの参照先は、チェーンの末尾方向に移動されます。このため、開いた直後のワークシートでの最初の数回の計算サイクルは、多くの場合、計算時間が向上します。
  
When a structural change is made to a workbook, for example, when a new formula is entered, Excel reconstructs the dependency tree and calculation chain. When new data or new formulas are entered, Excel marks all the cells that depend on that new data as needing recalculation. Cells that are marked in this way are known as  *dirty*  . All direct and indirect dependents are marked as dirty so that if B1 depends on A1, and C1 depends on B1, when A1 is changed, both B1 and C1 are marked as dirty. 
  
あるセルがそのセル自体に直接的または間接的に依存している場合は、Excel によって循環参照が検出され、ユーザーに警告が示されます。これは、通常ユーザーが修正しなければならないエラー状態です。Excel には、ユーザーが循環依存の関係の原因を見つけられるようにする非常に役立つグラフィカルなナビゲーション ツールがあります。場合によっては、この状態を意図的に必要とすることもあります。たとえば、次の繰り返しの開始点が、前の繰り返しの結果になる反復計算の実行を必要とすることがあります。Excel は、[計算方法の設定] ダイアログ ボックスによる反復計算の制御をサポートしています。
  
セルにダーティのマークを付けた後、次回の再計算が実行されるときに、Excel は、それぞれのダーティ セルの内容を計算チェーンで指定された順序で再評価します。前述の例では、最初に B1、次に C1 の順になります。この再計算は、再計算モードが自動になっている場合には、Excel がセルにダーティのマークを付け終わった直後に実行されます。それ以外の場合は、再計算は後で実行されます。
  
Microsoft Excel 2002 以降の Microsoft Visual Basic for Applications (VBA) の **Range** オブジェクトは、セルに計算が必要というマークを付ける **Range.Dirty** メソッドをサポートしています。このメソッドを **Range.Calculate** メソッドと併用すると (次のセクションを参照)、特定の範囲内のセルを強制的に再計算できるようになります。これは、計算モードが手動に設定されているときに、マクロで限定的な計算を実行する際に、そのマクロ関数とは無関係のセルを計算するオーバーヘッドを回避するために役立ちます。範囲計算のメソッドは、C API では使用できません。 
  
Excel 2002 以前のバージョンの Excel では、開いている各ブックのワークシートごとに計算チェーンを構築していました。このため、処理されるワークシート間のリンク方法は複雑になり、効率的な再計算のためには注意が必要でした。特に Excel 2000 では、ワークシート間の依存関係を最小限にして、ワークシートにアルファベット順の名前を付ける必要があります。このようにして、他のシートに依存するシートが、依存先のシートの後に (アルファベット順) なるようにします。
  
In Excel 2007, the logic was improved to enable recalculation on multiple threads so that sections of the calculation chain are not interdependent and can be calculated at the same time. You can configure Excel to use multiple threads on a single processor computer, or a single thread on a multi-processor or multi-core computer. 
  
## <a name="asynchronous-user-defined-functions-udfs"></a>非同期のユーザー定義関数 (UDF)

計算中に非同期の UDF が現れると、現在の数式の状態が保存され、UDF が開始されて、残りのセルの評価が続行されます。計算ですべてのセルの評価が終了したときに、まだ実行中の非同期関数がある場合、Excel は非同期関数が完了するまで待機します。各非同期関数が結果を報告したときに、Excel は数式を終了して、非同期関数への参照を含むセルを使用しているセルの再計算のために新しい計算パスを実行します。
  
## <a name="volatile-and-non-volatile-functions"></a>揮発性関数と非揮発性関数

Excel では、揮発性関数の概念をサポートしています。これは、その関数の引数が変更されていなくても (関数が引数を取る場合)、ある瞬間と次の瞬間では値が異なる可能性があると見なされる関数です。Excel は、再計算のたびに、揮発性関数が含まれているセルをすべての参照先と共に再評価します。このため、揮発性関数に依存しすぎていると、再計算にかかる時間が長くなる可能性があります。控えめに使用するようにしてください。
  
次に示す Excel 関数は揮発性です。
  
- **NOW**
    
- **TODAY**
    
- **RANDBETWEEN**
    
- **OFFSET**
    
- **INDIRECT**
    
- **INFO** (引数によって異なります) 
    
- **CELL** (引数によって異なります) 
    
- **SUMIF** (引数によって異なります) 
    
VBA と C API は、揮発性として処理する必要のあるユーザー定義間数 (UDF) について Excel に通知する手段をサポートしています。VBA を使用する場合は、次のようにすると UDF が揮発性として宣されます。
  
```vba
Function MyUDF(MakeMeVolatile As Boolean) As Double
   ' Good practice to call this on the first line.
   Application.Volatile MakeMeVolatile
   MyUDF = Now
End Function

```

既定では、Excel は VBA の UDF を非揮発性であると見なします。Excel は、UDF の最初の呼び出し時に、その UDF が揮発性であることを認識します。この例のように、揮発性 UDF は非揮発性に戻すことができます。
  
C API を使用する場合は、XLL 関数を最初の呼び出し前に揮発性として登録できます。また、ワークシート関数の揮発性状態のオン/オフを切り替えることもできます。
  
既定では、Excel は範囲引数を受け取り、マクロ シートと同等のものとして宣言された XLL UDF を揮発性として処理します。この既定の状態は、UDF が最初に呼び出されるときに **xlfVolatile** 関数を使用することでオフにできます。 
  
## <a name="calculation-modes-commands-selective-recalculation-and-data-tables"></a>計算モード、コマンド、選択的な再計算、およびデータ テーブル

Excel には 3 つの計算モードがあります。
  
- 自動
    
- テーブル以外自動
    
- Manual
    
計算が自動に設定されていると、データ入力の後に再計算が毎回実行されます。また、前のセクションで例を示したように、特定のイベントの後にも再計算が発生します。非常に巨大なブックの場合、再計算に長い時間がかかるようになり、この事態が発生した場合はユーザーによる制限が必要になります。つまり、再計算は必要なときにのみ行うということです。これを可能にするために、Excel では手動モードをサポートしています。ユーザーは、Excel のメニュー システムからモードを選択することも、VBA、COM、または C API を使用することで、プログラムによってモードを選択することもできます。
  
データ テーブルとは、ワークシート内の特殊な構造のことです。最初に、ユーザーは結果の計算をワークシートにセット アップします。これは、1 つまたは 2 つのキーになる変更可能な入力と、その他のパラメーターによって決まります。次に、ユーザーは一方または両方のキーになる入力の値のセットに対する結果のテーブルを作成します。テーブルの作成には、**データ テーブル ウィザード** を使用します。テーブルのセット アップ後、Excel は入力を 1 つずつ計算に組み込んで、結果の値をテーブルにコピーします。1 つまたは 2 つの入力が使用できるため、データ テーブルは 1 次元または 2 次元になります。 
  
データ テーブルの再計算の処理方法は若干異なります。
  
- 再計算は、通常のブックの再計算とは非同期に処理されます。これは、巨大なテーブルの再計算には、ブックの残りの部分よりも時間がかかることがあるためです。
    
- 循環参照が許容されています。結果を得るために使用される計算がデータ テーブルの 1 つまたは 2 つの値に依存する場合、Excel は循環依存の関係に関するエラーを返しません。 

- データ テーブルでは、マルチスレッド計算を使用しません。
    
Excel がデータ テーブルの再計算を別の方法で処理することと、複雑な計算または非常に長い計算に依存する巨大なテーブルの計算には時間がかかるという事実から、Excel ではデータ テーブルの自動計算を無効化できるようになっています。これを行うには、計算モードを [データ テーブル以外自動] に設定します。計算がこのモードのときには、ユーザーが F9 を押すか、それと同等のプログラムによる操作を実行することで、データ テーブルが再計算されます。
  
Excel は、再計算モードの変更と再計算の制御に利用できるメソッドを公開しています。これに該当するメソッドは、バージョンが進むごとに改善されていて、より細かい制御が可能になっています。これに関連する C API の機能は、Excel バージョン 5 で使用可能だったものを反映しているため、それよりも新しい VBA を使用することで得られるものと同じ制御は得られません。 
  
Excel が手動計算モードのときに最も頻繁に使用されるメソッドは、ブック、ワークシート、および範囲の選択的な計算を可能にするメソッド、開いているすべてのブックの完全な再計算を可能にするメソッド、さらに依存関係ツリーと計算チェーンの完全な再構築を可能にするメソッドです。
  
### <a name="range-calculation"></a>範囲計算

キーボード操作: なし
  
VBA: **Range.Calculate** (Excel 2000 で導入、Excel 2007 で変更) および **Range.CalculateRowMajorOrder** (Excel 2007 で導入) 
  
C API: サポートなし
  
- **[手動] モード**
    
    特定の範囲内のセルのみを再計算します (セルがダーティかどうかは関係ありません)。**Range.Calculate** メソッドの動作は Excel 2007 で変更されています。ただし、以前の動作も **Range.CalculateRowMajorOrder** メソッドでサポートされています。 
    
- **[自動] または [テーブル以外自動] モード**
    
    ブックを再計算しますが、範囲の再計算または範囲に含まれるセルの再計算を強制しません。
    
### <a name="active-worksheet-calculation"></a>アクティブなワークシートの計算

キーボード操作: SHIFT + F9
  
VBA: **ActiveSheet.Calculate**
  
C API: **xlcCalculateDocument**
  
- **すべてのモード**
    
    アクティブなワークシート内でのみ、計算のマークが付けられているセルを再計算します。
    
### <a name="specified-worksheet-calculation"></a>指定されたワークシートの計算

キーボード操作: なし
  
VBA: **Worksheets(** reference **).Calculate**
  
C API: サポートなし
  
- **すべてのモード**
    
    指定されたワークシート内でのみ、ダーティなセルとそのセルの参照先を再計算します。参照は文字列としてのワークシートの名前、または関連するブックのインデックス番号です。
    
    Excel 2000 以降のバージョンでは、**Boolean** ワークシート プロパティである **EnableCalculation** プロパティが公開されています。これを **False** から **True** に設定すると、指定されたワークシート内のすべてのセルがダーティになります。自動モードの場合は、これによりブック全体の再計算もトリガーされます。  
    
    手動モードの場合は、次のコードでアクティブ シートのみの再計算が行われます。
    
  ```vb
  With ActiveSheet
    .EnableCalculation = False
    .EnableCalculation = True
    .Calculate
  End With
  
  ```

### <a name="workbook-tree-rebuild-and-forced-recalculation"></a>ブックのツリーの再構築と再計算の強制

キーボード操作: CTRL + ALT + SHIFT + F9 (Excel 2002 で導入されました)
  
VBA: **Workbooks(** reference **).ForceFullCalculation** (Excel 2007 で導入) 
  
C API: サポートなし
  
- **すべてのモード**
    
    Excel によって特定のブックの依存関係ツリーと計算チェーンが再構築され、数式を含んでいるすべてのセルの再計算を強制します。
    
### <a name="all-open-workbooks"></a>開いているすべてのブック

キーボード操作: F9
  
VBA: **Application.Calculate**
  
C API: **xlcCalculateNow**
  
- **すべてのモード**
    
    Excel によってダーティのマークが付けられたすべてのセル (揮発性データと変更されたデータの参照先、およびプログラムによりダーティのマークが付けられたセル) を再計算します。計算モードが [テーブル以外自動] の場合は、更新を必要とするテーブルに加えて、すべての揮発性関数とその関数の参照先も生産します。
    
### <a name="all-open-workbooks-tree-rebuild-and-forced-calculation"></a>開いているすべてのブックのツリーの再構築と計算の強制

キーボード操作: CTRL + ALT + F9
  
VBA: **Application.CalculateFull**
  
C API: サポートなし
  
- **すべてのモード**
    
    開いているすべてのブックに含まれるすべてのセルを再計算します。計算モードが [テーブル以外自動] の場合は、テーブルの再計算を強制します。
    
## <a name="see-also"></a>関連項目



[Excel でのマルチスレッド再計算](multithreaded-recalculation-in-excel.md)
  
[Excel で使用されるデータ型](data-types-used-by-excel.md)
  
[Excel のメモリ管理](memory-management-in-excel.md)
  
[Excel プログラミングの概念](excel-programming-concepts.md)

