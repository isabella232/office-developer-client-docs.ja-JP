---
title: Excel でのマルチスレッド再計算
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
keywords:
- thread-safe cells [excel 2007],multithreading in Excel,concurrent tasks [Excel 2007],thread-safe functions [Excel 2007],multithreaded recalculation [Excel 2007],MTR [Excel 2007],XLL functions [Excel 2007], registering as thread safe,recalculation [Excel 2007], multithreaded,memory contention [Excel 2007],registering XLL functions as thread safe [Excel 2007],unsafe functions [Excel 2007]
ms.assetid: c6c831f1-4be1-4dcc-a0fa-c26052ec53c9
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: f0b6f3d7310cac6d141fc74652a3333f70bda8e9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310506"
---
# <a name="multithreaded-recalculation-in-excel"></a>Excel でのマルチスレッド再計算

**適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Office Excel 2007は、ワークシートのマルチスレッド再計算（MTR）を使用した最初のバージョンのExcelです。コンピューター上のプロセッサまたはプロセッサコアの数に関係なく、再計算時に最大1024の同時スレッドを使用するようにExcelを構成できます。 
  
> [!NOTE]
> それぞれのスレッドには関連するオペレーティング システムのオーバーヘッドがあるため、必要以上に多くのスレッドを使用するように Excel を構成してはいけません。 
  
コンピューターに複数のプロセッサまたはプロセッサのコアが搭載されている場合は、オペレーティング システムが、最適な方法でプロセッサにスレッドを割り当てます。
  
## <a name="excel-mtr-overview"></a>Excel の MTR の概要

Excelは、別々のスレッドで同時に再計算できる計算チェーンの部位の認識を試みます。以下のごく単純化されたツリー（x←yはyがxにのみ依存することを意味）はこの例を示しています。
  
**図 1. 別々のスレッドでの同時並行計算**

![複数のスレッドでの同時並行計算](media/12b5a52b-6308-420c-b6cf-492bd1f195ce.gif "複数のスレッドでの同時並行計算")
  
A1 の計算が済むと、一方のスレッドでは A2、A3 の順に計算ができるようになり、同時に、もう一方のスレッドでは B1、C1 の順に計算ができるようになります (すべてのセルがスレッド セーフであると仮定しています)。 
  
> [!NOTE]
> スレッドセーフセルとは、スレッドセーフ関数のみを含むセルを意味します。スレッドセーフとは何か、スレッドセーフでないものとは、については、[エクセルがスレッドセーフとみなすもの・みなさないもの](#xl2007xllsdk_threadsafe)に記載されています。 
  
ほとんどの実用的なワークブックには、この例よりはるかに複雑な依存関係ツリーが含まれています。さらに、セルの再計算時間は計算が完了するまで知ることができず、関数の引数によって大きく異なります。最良の結果を得るために、Excelは最適化がそれ以上不可能になるまで各計算の計算順序を改善しようとします。
  
Excel は、次の項目の実行に単一のメイン スレッドを使用します。
  
- 組み込みコマンド
    
- XLL コマンド
    
- アドイン マネージャー インターフェイス関数 (**xlAutoOpen** 関数など) 
    
- Microsoft Visual Basic for Applications (VBA) のユーザー定義コマンド (通常はマクロと呼ばれます)
    
- VBA のユーザー定義関数
    
- 組み込みのスレッド セーフではないワークシート関数 (次のセクションに一覧を示します)
    
- XLM マクロ シートのユーザー定義コマンドとユーザー定義関数
    
- COM アドインのコマンドと関数
    
- 条件付きフォーマット式内の関数と演算子
    
- ワークシートの式で使用された定義済みの名前定義内の関数と演算子
    
- 数式編集ボックス内の式の強制的な評価 (**F9** キーを使用) 
    
関数がスレッドセーフかどうかにかかわらず、すべてのワークシートの数式は、Excelが複数のスレッドを使用するように構成されていない限り、メインスレッドで判断されます。ユーザーが複数のスレッドを使用するように指定した場合、追加のスレッドがスレッドセーフセルに使用されます。メインスレッドは、負荷分散の観点上有用な場合でも、スレッドセーフセルに使用されることがあります。
  
ここでもう一度強調すべきこととして、Excel は一度に複数のコマンドを実行しません。そのため、スレッド ローカル メモリとクリティカル セクションの使用など、スレッド セーフな関数を記述するときと同様の注意を払う必要はありません。
  
## <a name="what-is-and-is-not-considered-thread-safe-by-excel"></a>Excel でスレッド セーフと見なされるもの (見なされないもの)
<a name="xl2007xllsdk_threadsafe"> </a>

Excel では、次のものだけがスレッド セーフと見なされます。
  
- Excel の単項演算子と二項演算子のすべて
    
- Excel 2007以降のほぼすべての組み込みワークシート関数（例外リストを参照）
    
- スレッド セーフとして明示的に登録されている XLL アドイン関数
    
次の組み込みワークシート関数は、スレッド セーフではありません。
  
- **PHONETIC**
    
- "format"または "address"引数が使用されている場合は**CELL** 
    
- **INDIRECT**
    
- **GETPIVOTDATA**
    
- **CUBEMEMBER**
    
- **CUBEVALUE**
    
- **CUBEMEMBERPROPERTY**
    
- **CUBESET**
    
- **CUBERANKEDMEMBER**
    
- **CUBEKPIMEMBER**
    
- **CUBESETCOUNT**
    
- **ADDRESS** (5 番目のパラメーター "sheet_name" が指定されている場合) 
    
- ピボットテーブルを参照するデータベース関数 (**DSUM**、**DAVERAGE** など)
    
- **ERROR.TYPE**
    
- **HYPERLINK**
    
明確にするために、スレッド セーフと見なされないものを挙げます。
  
- VBA のユーザー定義関数
    
- COM アドインのユーザー定義関数
    
- XLM マクロ シートのユーザー定義関数
    
- 明示的にスレッド セーフとして登録されていない XLL アドイン関数
    
次の操作と関数はスレッド セーフとは見なされません。また、スレッド セーフとして登録した XLL 関数から呼び出されると失敗します。
  
- XLM 情報関数 (**xlfGetCell** (**GET.CELL**) など) の呼び出し。
    
- XLL 内部名の定義または削除のための **xlfSetName** (**SET.NAME**) の呼び出し。
    
- スレッド セーフではないユーザー定義関数の **xlUDF** を使用した呼び出し。
    
- スレッド セーフではない関数を含む式、またはスレッド セーフではない関数を含む定義によって定義された名前を含む式に対する [xlfEvaluate](xlfevaluate.md) 関数の呼び出し。 
    
- ブレーク条件をクリアする [xlAbort](xlabort.md) 関数の呼び出し。 
    
- 計算されていないセルの参照の値を取得する [xlCoerce](xlcoerce.md) 関数の呼び出し。 
    
> [!NOTE]
> XLLワークシート関数は、スレッドセーフとして登録されているかどうかにかかわらず、**xlcSave**などのC APIコマンドを呼び出すことはできません。 
  
スレッドセーフとして宣言されたXLL関数がXLM情報関数を呼び出したり、未計算のセルを参照したりすることはできないため、Excelでは、マクロシートに相当するものとして登録されているXLL関数をスレッドセーフとして登録することはできません。したがって、**xlCoerce**を使用して未計算のセル参照の値を取得しようとすると、**xlretUncalced**エラーとなります。 XLM情報関数を呼び出すと、**xlretFailed**エラーとなります。上記のその他の地点では、Excel C APIで導入されたエラーコード**xlretNotThreadSafe**エラーとなります。 
  
C API 専用のコールバック関数は、すべてスレッド セーフです。
  
- **xlCoerce**（未計算のセル参照の強制が失敗した場合を除く） 
    
- **xlFree**
    
- **xlStack**
    
- **xlSheetId**
    
- **xlSheetNm**
    
- **xlAbort**（中断条件をクリアするために使用される場合を除く） 
    
- **xlGetInst**
    
- **xlGetHwnd**
    
- **xlGetBinaryName**
    
- **xlDefineBinaryName**
    
1つの例外は**xlSet**関数です。これは、いずれにせよ、コマンドと同等であるため、どのワークシート関数からも呼び出すことはできません。 
  
XLLワークシート関数はスレッドセーフとしてExcelに登録できます。これはExcelに、その関数が安全かつ同時に複数のスレッドで呼び出されることができると伝達します。ただし、関数の動作を必ずご確認ください。スレッドセーフとして登録された関数が安全に動作しない場合、Excelを不安定にする可能性があります。
  
## <a name="registering-xll-functions-as-thread-safe"></a>XLL 関数をスレッド セーフとして登録する
<a name="xl2007xllsdk_threadsafe"> </a>

スレッド セーフな関数を記述するときに、開発者が従う必要のあるルールは次のとおりです。
  
- スレッド セーフではない可能性のある別の DLL 内のリソースを呼び出さない。
    
- C API または COM を通じてスレッド セーフでない呼び出しを行わない。
    
- クリティカル セクションを使用して、複数のスレッドで同時に使用される可能性のあるリソースを保護する。
    
- スレッド固有のストレージにはスレッド ローカル メモリを使用して、関数内の静的変数はスレッド ローカル変数に置き換える。
    
Excel には、もう 1 つの制限が課せられます。スレッド セーフな関数をマクロ シートと同等なものとして登録することはできません。そのため、XLM 情報関数を呼び出すことや、再計算されていないセルの値を取得することはできません。
  
## <a name="memory-contention"></a>メモリの競合
<a name="xl2007xllsdk_threadsafe"> </a>

マルチスレッド システムは、2 つの基本的な問題に対処する必要があります。
  
- 複数のスレッドが読み書きするメモリの保護方法。
    
- 実行中のスレッドに関連付けられてプライベートになるメモリの作成方法とアクセス方法。
    
WindowsオペレーティングシステムとWindowsソフトウェア開発キット（SDK）には、それぞれ主要領域、およびスレッドローカルストレージ（TLS）APIの両方へのツールが用意されています。詳しくは、[Excelのメモリー管理](memory-management-in-excel.md)を参照してください。
  
まず問題が発生しうる事例として、2つのワークシート関数（または同じ関数を同時に実行している2つのインスタンス）がDLLプロジェクトのグローバル変数にアクセスまたは変更する必要がある場合があります。このようなグローバル変数は、クラスオブジェクトの包括的にアクセス可能なインスタンスに隠される可能性があることに留意してください。
  
2つ目の問題が発生する事例として、ワークシート関数が関数本体コード内で静的変数またはオブジェクトを宣言する場合があります。 C / C ++コンパイラは、すべてのスレッドが使用する単一のコピーのみを作成します。これは、関数の1つのインスタンスが値を変更できる一方で、別のスレッド上の別のインスタンスがその値が以前に設定されたものであると想定している可能性があることを意味します。
  
## <a name="example-applications-of-mtr"></a>MTR のサンプル アプリケーション
<a name="xl2007xllsdk_threadsafe"> </a>

ワークシート関数をエクスポートするすべてのXLLは、Excelのマルチスレッド再計算（MTR）を利用できます。ただし、それらの関数がスレッドセーフでないアクションを実行する必要がない場合です。これにより、Excelはそれらに依存しているワークブックをできるだけ早く再計算することができます。
  
Specifically, MTR has an enormous impact on the recalculation time of workbooks that call user-defined functions (UDFs) that themselves call external processes to obtain the desired result. In particular, consider a UDF that calls a remote server that can process many requests simultaneously and a workbook containing many calls to that function. If recalculation of the workbook is single-threaded, each call to the UDF, and so to the remote server, must complete before the next one can be made. This wastes the server's ability to process many calls at once. If recalculation of the workbook is multithreaded, Excel can make multiple calls at the same time or in rapid succession.
  
Excelがサーバーと同じ数のスレッド（Nと呼称）を使用するように構成されていて、ブックの依存関係ツリーのトポロジーで許可されている場合、合計再計算時間はシングルスレッドの1 / Nにまで減少できる可能性があります。これは、（ワークブックが実行されている）クライアントコンピュータにプロセッサが1つしかない場合、特にサーバーへの呼び出しにかかる時間が、サーバーが呼び出しを処理するのにかかる時間と比べて短い場合でも同様です。 
  
追加スレッドごとにオペレーティングシステムの処理時間があります。そのため、特定のワークブック、特定のサーバーおよびクライアントコンピューターで、Excelに使用するスレッドの最適数を見つけるためには、ある程度の試験が必要になることがあります。 
  
たとえば、Excelを実行しているシングルプロセッサコンピューターと、1,000個のセルを含むブックを考えてみましょう。 UDFを呼び出し、次に1つ以上のリモートサーバーを呼び出します。 Excelが1つ1つの呼び出しが完了するのを待つ必要がないように、1,000のセルが互いに依存していないと仮定します（影響が出ない程度にこの制約から外れる例もあります）。 サーバーが100個の要求を同時に処理でき、Excelが100個のスレッドを使用するように構成されている場合、実行時間は1つのスレッドのみで稼動している場合の100分の1に短縮できます。 各スレッドにコールを割り当てる分の処理時間、および100個のスレッドを管理するオペレーティングシステムというものは、実際には、それほど大きい削減は起きません。ここには、サーバーが適切に拡張され、100個のタスクを同時に処理するように要求しても個々のタスクの完了時間に大きな影響はないという暗黙の前提もあります。
  
この技法が大きなメリットになる実用的アプリケーションとして、モンテカルロ法など、小さなタスクに分割して複数のサーバーに依頼できる数値集約型のタスクが挙げられます。
  
## <a name="excel-services-considerations"></a>Excel Services の考慮事項
<a name="xl2007xllsdk_threadsafe"> </a>

Excel Servicesは、サーバー上のExcelスプレッドシートの読み込み、計算、および表示をサポートしています。その後、ユーザーは標準のブラウザツールを使用して、スプレッドシートにアクセスして運用することができます。
  
Excel ServicesのUDFは、Microsoft .NET Frameworkマネージコードを使用して作成され、.NETアセンブリを通じて使用可能になります。 XLLはExcel Servicesではサポートされていません。マネージコードサーバーのUDFリソースは、その機能にアクセスするためにXLLを呼び出すことができます。そのため、ユーザーは、サーバーで読み込んだワークブックでもクライアントで読み込んだワークブックと同じ機能を使用できます。
  
したがって、XLLの関数をこのように使用できるようにするには、引数と戻り値をネイティブデータ型から.NET Framework管理データ型に変換し、XLL関数を呼び出す.NETアセンブリでそれらを整形する必要があります。 .NETラッパーは、アクセスされているXLL関数ごとに1つのサーバーUDFをエクスポートします。追加の要件は、この方法で呼び出されるXLL関数はすべてスレッドセーフでなければならないということです。 XLL関数はクライアントExcelと同じ方法で登録されていないため、サーバーと.NETラッパーにはスレッドセーフであることを強制する方法がありません。これを確保するのはXLL開発者の管轄です。
  
## <a name="see-also"></a>関連項目

- [Excel の再計算](excel-recalculation.md)  
- [Excel のメモリ管理](memory-management-in-excel.md) 
- [Excel での XLL コードへのアクセス](accessing-xll-code-in-excel.md)  
- [Excel プログラミングの概念](excel-programming-concepts.md)  
- [Excel XLL SDK API 関数リファレンス](excel-xll-sdk-api-function-reference.md)

