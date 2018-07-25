---
title: Office の 32 ビット バージョンと 64 ビット バージョン間の互換性
ms.date: 04/27/2016
ms.audience: ITPro
localization_priority: Normal
ms.assetid: ff49dc9e-daf8-43cf-8802-51c2537ed561
description: 32 ビット バージョンの Office と 64 ビット バージョンの Office の互換性についてご確認ください。
ms.openlocfilehash: 924f7a1aa891addc5841e6cdefc5226dcb056096
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804690"
---
# <a name="compatibility-between-the-32-bit-and-64-bit-versions-of-office"></a>Office の 32 ビット バージョンと 64 ビット バージョン間の互換性

32 ビット バージョンの Office と 64 ビット バージョンの Office の互換性についてご確認ください。
  
Office アプリケーションは、32 ビット バージョンと 64 ビット バージョンでご利用いただけます。 
  
64 ビット バージョンの Office により、Microsoft Excel 2010 で大量のデータを扱う場合など、機能の強化に伴ってより多くのデータを移動させることができるようになりました。32 ビット コードを記述する場合は、変更なしで 64 ビット バージョンの Office を使うことができます。しかし、64 ビット コードを記述する場合は、そのコードに特定のキーワードと条件付きコンパイル定数を含めることで、以前のバーションの Office との下位互換性が確保されるようにし、32 ビット コードと 64 ビット コードを組み合わせて使う場合に正しいコードが実行されるようにする必要があります。
  
Visual Basic for Applications 7.0 (VBA 7) は 64 ビット バージョンの Office でリリースされ、32 ビット バージョンと 64 ビット バージョンのどちらのアプリケーションでも動作します。この記事で説明されている変更は、64 ビット バージョンの Office にのみ適用されます。32 ビット バージョンの Microsoft Office を使うと、追加の変更を加えることなく、以前のバージョンの Office で作成したソリューションを使うことができます。
  
> [!NOTE]
> 既定で、64 ビット バージョンの Office をインストールすると、32 ビット バージョンが 64 ビット システムと共にインストールされます。Microsoft Office 64 ビット バージョンのインストール オプションを明示的に選択する必要があります。 
  
VBA 7 では、既存の Windows API ステートメント (**Declare** ステートメント) を更新して、64 ビット バージョンで動作するようにしなければなりません。 さらに、これらのステートメントで使用されるアドレス ポインターとディスプレイ ウィンドウ ハンドルをユーザー定義型で更新する必要があります。 この点については、32 ビット バージョンと 64 ビット バージョン間の互換性に関する問題と推奨される解決案と共に、この記事で詳しく説明します。 
  
## <a name="comparing-32-bit-and-64-bit-systems"></a>32 ビット システムと 64 ビット システムの比較
<a name="odc_office_Compatibility32bit64bit_Comparing32BitSystemsto64BitSystems"> </a>

64 ビット バージョンの Office で作成されたアプリケーションは、32 ビットバージョンよりも大きいアドレス空間を参照することができます。つまり、以前と比べると、データに対してより多くの物理メモリを使うことができるため、物理メモリでのデータの出入りにかかるオーバーヘッドを軽減できる可能性があります。
  
物理メモリ内の特定の場所への参照 ("ポインター" と呼ばれる) に加えて、表示ウィンドウ識別子 ("ハンドル" と呼ばれる) を参照するアドレスを使うこともできます。32 ビット システムと 64 ビット システムのどちらを使うかに応じて、ポインターやハンドルのサイズ (バイト数) が決まります。 
  
既存のソリューションを 64 ビット バージョンの Office を使って実行する場合は、次の点に注意してください。
  
- Office のネイティブの 64 ビット プロセスは、32 ビット バイナリを読み込むことができません。既存の Microsoft ActiveX コントロールと既存のアドインがある場合、これはよく起こる問題です。
    
- これまで VBA にはポインター データ型がなかったため、ポインターとハンドルを格納する 32 ビットの変数を使う必要がありました。 **Declare** ステートメントを使う場合、API 呼び出しで返される 64 ビット値は、これらの変数で切り詰められるようになりました。 
    
## <a name="vba-7-code-base"></a>VBA 7 コード ベース
<a name="odc_office_Compatibility32bit64bit_IntroducingVBA7CodeBase"> </a>

VBA 7 は、Office 2007 以前のバージョンでの VBA コード ベースを置き換えます。VBA 7 は、Office の 32 ビットと 64 ビットのどちらのバージョンでもご利用いただけます。次の 2 つの条件付きコンパイル定数があります。 
  
- **VBA7** - アプリケーションが VBA 7 を使っているか、以前のバージョンの VBA を使っているかをテストすることによって、コードの下位互換性が確保されます。 
    
- **Win64** 32 ビットと 64 ビットのどちらでコードが実行されているかをテストします。 
    
特定の例外を除き、32 ビット バージョンのアプリケーションで機能しているドキュメント内のマクロは 64 ビット バージョンでも機能します。
  
## <a name="activex-control-and-com-add-in-compatibility"></a>ActiveX コントロールと COM アドインの互換性
<a name="odc_office_Compatibility32bit64bit_ActiveXControlCOMAddinCompatibility"> </a>

既存の 32 ビット ActiveX コントロールは Office の 64 ビット バージョンと互換性がありません。ActiveX コントロールと COM オブジェクトについては、次のようにしてください。
  
- ソース コードがあれば、64 ビット バージョンを自分で生成します。
- ソース コードがなければ、販売元に更新されたバージョンを請求してください。
    
Office のネイティブの 64 ビット プロセスでは 32 ビットのバイナリを読み込むことができません。これには、 **MSComCtl** の一般的なコントロール (TabStrip、Toolbar、StatusBar、ProgressBar、TreeView、ListViews、ImageList、Slider、ImageComboBox) と、 **MSComCt2** のコントロール (Animation、UpDown、MonthView、DateTimePicker、FlatScrollBar) が含まれます。これらのコントロールは、Office 2010 より前の 32 ビット バージョンの Office でインストールされました。64 ビット バージョンの Office にコードを移行するときにこれらのコントロールを使う既存の VBA ソリューションの代替策を見つける必要があります。 
  
## <a name="api-compatibility"></a>API の互換性
<a name="odc_office_Compatibility32bit64bit_ApplicationProgrammingInterfaceCompatibility"> </a>

VBA ライブラリとタイプ ライブラリを組み合わせれば、Office アプリケーションの作成にさまざまな機能を使えるようになります。ただし、コンピューターのオペレーティング システムや他のコンポーネントとの直接のやりとりが必要になることもあります。たとえば、メモリやプロセスの管理、ウィンドウやコントロールなどの UI 要素の操作、Windows レジストリの変更を行うときです。このような状況では、DLL ファイルに組み込まれた外部関数を使うのが最善策です。VBA でこれを行うには、 **Declare** を使って API 呼び出しを行います。 
  
> [!NOTE]
> Microsoft は、1,500 個の Declare ステートメントが含まれている Win32API.txt ファイルと、コードに含める **Declare** ステートメントをコピーするツールを提供しています。 ただし、これらのステートメントは 32 ビット システム用であるため、この記事で後ほど説明する情報に従って 64 ビットに変換する必要があります。 既存の **Declare** ステートメントは、**PtrSafe** 属性を使って 64 ビットに対して安全なステートメントとしてマークするまでは、64 ビットの VBA にコンパイルされません。 この種類の変換の例については、Excel MVP Jan Karel Pieterse の Web サイト ([http://www.jkp-ads.com/articles/apideclarations.asp](http://www.jkp-ads.com/articles/apideclarations.asp)) をご覧ください。 [Office Code Compatibility Inspector ユーザーズ ガイド](http://technet.microsoft.com/ja-JP/library/ee833946%28office.14%29.aspx)は、**PtrSafe** 属性と適切な戻り値の型 (必要に応じて) の API **Declare** ステートメントの構文を検査するのに役立ちます。 
  
**Declare** ステートメントの形式は、サブルーチン (戻り値がない) と関数 (戻り値がある) のどちらを呼び出すのかに応じて、次のどちらかになります。 
  
```vb
Public/Private Declare Sub SubName Lib "LibName" Alias "AliasName" (argument list)
Public/Private Declare Function FunctionName Lib "Libname" alias "aliasname" (argument list) As Type

```

**SubName** 関数または **FunctionName** 関数は、プロシージャを VBA コードから呼び出すときに使用する名前を表しており、DLL ファイル内のプロシージャの実際の名前に置き換えます。プロシージャの名前として **AliasName** 引数を指定することもできます。 **Lib** キーワードの後ろには、呼び出すプロシージャが含まれている DLL ファイルの名前を指定します。引数リストには、プロシージャに渡す必要のあるパラメーターとデータ型を指定します。 
  
次の **Declare** ステートメントは、Windows レジストリ内の*サブキー*を開き、その値を置き換えます。 
  
```vb
Declare Function RegOpenKeyA Lib "advapi32.dll" (ByVal Key As Long, ByVal SubKey As String, NewKey As Long) As Long
```

**RegOpenKeyA** 関数の Windows.h (ウィンドウ ハンドル) エントリは次のようになります。 
  
```vb
LONG RegOpenKeyA ( HKEY hKey, LPCSTR lpSubKey, HKEY *phkResult );
```

Visual C と Microsoft Visual C++ では、上記の例は 32 ビットと 64 ビットのどちらについても正しくコンパイルされます。なぜなら、HKEY がポインターとして定義されており、そのサイズはコードをコンパイルするプラットフォームのメモリ サイズを反映するからです。
  
以前のバージョンの VBA では、特定のポインター データ型がなかったので、 **Long** データ型が使われていました。 **Long** データ型は常に 32 ビットなので、64 ビット メモリのシステムで使用すると問題が起きます。なぜなら、上位の 32 ビットが切り捨てられるか、他のメモリ アドレスに上書きされることがあるからです。どちらの場合も、予測できない動作やシステム クラッシュを引き起こす可能性があります。 
  
この問題を解決するため、VBA には *LongPtr* という真の  **ポインター**  データ型があります。この新しいデータ型を使用すれば、次のように本来の **Declare** ステートメントを正しく書くことができます。 
  
```vb
Declare PtrSafe Function RegOpenKeyA Lib "advapire32.dll" (ByVal hKey as LongPtr, ByVal lpSubKey As String, phkResult As LongPtr) As Long
```

このデータ型と新しい **PtrSafe** 属性を使うと、この **Declare** ステートメントを 32 ビット システムでも 64 ビット システムでも使うことができます。 **PtrSafe** 属性は、 **Declare** ステートメントの対象を 64 ビット バージョンの Office とすることを VBA コンパイラに指示するものです。この属性を指定せずに **Declare** ステートメントを 64 ビット システムで使うと、コンパイル時エラーが発生します。 **PtrSafe** 属性は、32 ビット バージョンの Office ではオプションです。これにより、既存の **Declare** ステートメントは従来どおりに動作します。 
  
次の表では、新しい修飾子とデータ型に加え、1 つのデータ型、2 つの変換演算子、3 つの関数についても説明します。
  
|種類|アイテム|説明|
|:-----|:-----|:-----|
|修飾子  <br/> |**PtrSafe** <br/> |**Declare** ステートメントが 64 ビットと互換性があることを示します。この属性は 64 ビット システムでは必須です。  <br/> |
|データ型  <br/> |**LongPtr** <br/> |変数のデータ型であり、Microsoft Office の 32 ビット バージョンでは 4 バイトのデータ型で、64 ビット バージョンでは 8 バイトのデータ型です。これは新しいコードでポインターやハンドルを宣言するときの推奨方法です。ただし、レガシー コードでも、64 ビット バージョンの Office で実行する場合は、やはりこれが推奨される方法です。これは 32 ビットおよび 64 ビットで VBA 7 ランタイムでのみサポートされます。そこに数値を代入することはできますが、数値型を代入することはできません。  <br/> |
|データ型  <br/> |**LongLong** <br/> |これは 64 ビット バージョンの Microsoft Office でのみ使用できる 8 バイトのデータ型です。数値を代入することはできますが、数値型を代入することはできません (切り詰められるのを避けるためです)。  <br/> |
|変換演算子  <br/> |**CLngPtr** <br/> |単純な式を **LongPtr** データ型に変換します。  <br/> |
|変換演算子  <br/> |**CLngLng** <br/> |単純な式を **LongLong** データ型に変換します。  <br/> |
|職務  <br/> |**VarPtr** <br/> |バリアント コンバーター。64 ビット バージョンでは **LongPtr** を返し、32 ビット バージョンでは **Long** を返します (4 バイト)。  <br/> |
|職務  <br/> |**ObjPtr** <br/> |オブジェクト コンバーター。64 ビット バージョンでは **LongPtr** を返し、32 ビット バージョンでは **Long** を返します (4 バイト)。  <br/> |
|職務  <br/> |**StrPtr** <br/> |文字列コンバーター。64 ビット バージョンでは **LongPtr** を返し、32 ビット バージョンでは **Long** を返します (4 バイト)。  <br/> |
   
次の例は、これらのアイテムのいくつかについて、 **Declare** ステートメントでの使用方法を示したものです。 
  
```vb
Declare PtrSafe Function RegOpenKeyA Lib "advapi32.dll" (ByVal Key As LongPtr, ByVal SubKey As String, NewKey As LongPtr) As Long
```

**Declare** ステートメントで **PtrSafe** を指定しないと、64 ビット バージョンの Office と互換性がないものと見なされます。 
  
**VBA7** と **Win64** という 2 つの条件付きコンパイル定数があります。以前のバージョンの Microsoft Office との下位互換性を確保するには、 **VBA7** 定数を使って (これがより一般的なやり方です)、以前のバージョンの Office で 64 ビット コードが実行されないようにします。32 ビット バージョンと 64 ビット バージョンとでコードが異なる場合は (たとえば、64 ビット バージョンについては **LongLong** を使い、32 ビット バージョンについては **Long** を使う数値演算 API を呼び出す場合など)、 **Win64** 定数を使います。次のコードで、この 2 つの定数の使用例を示します。 
  
```vb
#if Win64 then
   Declare PtrSafe Function MyMathFunc Lib "User32" (ByVal N As LongLong) As LongLong
#else
   Declare Function MyMathFunc Lib "User32" (ByVal N As Long) As Long
#end if
#if VBA7 then
   Declare PtrSafe Sub MessageBeep Lib "User32" (ByVal N AS Long)
#else
   Declare Sub MessageBeep Lib "User32" (ByVal N AS Long)
#end if
```

要約すると次のようになります。64 ビットのコードを書き、それを以前のバージョンの Office で使用する場合は、 **VBA7** 条件付きコンパイル定数を使用する必要があります。しかし、32 ビットのコードを書き、それを Office で使用する場合は、このコンパイル定数を使用しなくても、そのコードは以前のバージョンの Office での動作と同じになります。32 ビット バージョンには間違いなく 32 ビットのステートメントが使われ、64 ビット バージョンには間違いなく 64 ビットのステートメントが使われるようにするには、 **Win64** 条件付きコンパイル定数を使用するのが最善策です。 
  
## <a name="using-conditional-compilation-attributes"></a>条件付きコンパイル属性の使用
<a name="odc_office_Compatibility32bit64bit_UsingConditionalCompilationAttributes"> </a>

次に、更新する必要がある 32 ビット用に記述された VBA コードの例を示します。このレガシー コードのデータ型は、ハンドルやポインターを参照しているため、 **LongPtr** を使うように更新されていることに注意してください。 
  
### <a name="vba-code-written-for-32-bit-versions"></a>32 ビット バージョン用に記述された VBA コード
  
```vb
Declare Function SHBrowseForFolder Lib "shell32.dll" _
  Alias "SHBrowseForFolderA" (lpBrowseInfo As BROWSEINFO) As Long
  
Public Type BROWSEINFO
  hOwner As Long
  pidlRoot As Long
  pszDisplayName As String
  lpszTitle As String
  ulFlags As Long
  lpfn As Long
  lParam As Long
  iImage As Long
End Type
```

### <a name="vba-code-rewritten-for-64-bit-versions"></a>64 ビット バージョン用に記述された VBA コード
  
```vb
#if VBA7 then    ' VBA7 
Declare PtrSafe Function SHBrowseForFolder Lib "shell32.dll" _
  Alias "SHBrowseForFolderA" (lpBrowseInfo As BROWSEINFO) As Long
Public Type BROWSEINFO
  hOwner As LongPtr
  pidlRoot As Long
  pszDisplayName As String
  lpszTitle As String
  ulFlags As Long
  lpfn As LongPtr
  lParam As LongPtr
  iImage As Long
End Type
 
#else    ' Downlevel when using previous version of VBA7
Declare Function SHBrowseForFolder Lib "shell32.dll" _
  Alias "SHBrowseForFolderA" (lpBrowseInfo As BROWSEINFO) As Long
Public Type BROWSEINFO
  hOwner As Long
  pidlRoot As Long
  pszDisplayName As String
  lpszTitle As String
  ulFlags As Long
  lpfn As Long
  lParam As Long
  iImage As Long
End Type
 
#end if
Sub TestSHBrowseForFolder ()
    Dim bInfo As BROWSEINFO
    Dim pidList As Long
    bInfo.pidlRoot = 0&amp;
    bInfo.ulFlags = &amp;H1
    pidList = SHBrowseForFolder(bInfo)
End Sub
```

<a name="odc_office_Compatibility32bit64bit_FrequentlyAskedQuestions"> </a>

## <a name="frequently-asked-questions"></a>よく寄せられる質問

#### <a name="when-should-i-use-the-64-bit-version-of-office"></a>どのような場合に 64 ビット バージョンの Office を使うべきですか。
  
使っているホスト アプリケーション (Excel、Word など) によって異なります。たとえば、Excel を 64 ビット バージョンの Microsoft Office で使うと、より大きなワークシートを処理できます。
  
#### <a name="can-i-install-64-bit-and-32-bit-versions-of-office-side-by-side"></a>64 ビット バージョンと 32 ビット バージョンの Office を同時にインストールできますか。
  
いいえ。
  
#### <a name="when-should-i-convert-long-parameters-to-longptr"></a>どのような場合に Long パラメーターを LongPtr に変換する必要がありますか。
  
呼び出す関数については、Microsoft Developers Network の Windows API ドキュメントを確認する必要があります。ハンドルとポインターは **LongPtr** に変換する必要があります。たとえば、 [RegOpenKeyA](http://msdn.microsoft.com/library/c8a590f2-3249-437f-a320-c7443d42b792.aspx) のドキュメントは、次のシグネチャを提供します。 
  
```cs
LONG WINAPI RegOpenKeyEx(
  __in        HKEY hKey,
  __in_opt    LPCTSTR lpSubKey,
  __reserved  DWORD ulOptions,
  __in        REGSAM samDesired,
  __out       PHKEY phkResult
);
```

パラメーターは次のように定義されます。
  
|パラメーター|説明|
|:-----|:-----|
|hKey [in]  <br/> |レジストリ キーを開く *ハンドル*  。  <br/> |
|lpSubKey [in, optional]  <br/> |開くレジストリ サブキーの名前。  <br/> |
|ulOptions  <br/> |このパラメーターは予約済みで、0 にする必要があります。  <br/> |
|samDesired [in]  <br/> |キーに対する必要なアクセス権を指定するマスク。  <br/> |
|phkResult [out]  <br/> |キーを開くハンドルを受け取る変数への *ポインター*  。  <br/> |
   
[Win32API_PtrSafe.txt](http://www.microsoft.com/downloads/details.aspx?displaylang=en&amp;FamilyID=035b72a5-eef9-4baf-8dbc-63fbd2dd982b) では、**Declare** ステートメントが次のように定義されています。 
  
```vb
Declare PtrSafe Function RegOpenKeyEx Lib "advapi32.dll" Alias "RegOpenKeyExA" (ByVal hKey As LongPtr , ByVal lpSubKey As String, ByVal ulOptions As Long, ByVal samDesired As Long, phkResult As LongPtr ) As Long
```

#### <a name="should-i-convert-pointers-and-handles-in-structures"></a>構造体のポインターとハンドルを変換する必要がありますか。
  
はい。Win32API_PtrSafe.txt の **MSG** 型をご覧ください。 
  
```vb
Type MSG
    hwnd As LongPtr 
    message As Long
    wParam As LongPtr 
    lParam As LongPtr 
    time As Long
    pt As POINTAPI
End TypeF
```

#### <a name="when-should-i-use-strptr-varpt-and-objptr"></a>strptr、varpt、objptr は、どのような場合に使用すべきですか。
  
これらの関数は、文字列、変数、オブジェクトへのポインターを取得するために使う必要があります。64 ビット バージョンの Office では、これらの関数は 64 ビットの **LongPtr** を返します。これは **Declare** ステートメントに渡すことができます。これらの関数の使い方は、以前のバージョンの VBA と変わっていません。唯一の違いは、 **LongPtr** を返すことです。
  
## <a name="see-also"></a>関連項目
<a name="odc_office_Compatibility32bit64bit_AdditionalResources"> </a>

- [Anatomy of a Declare Statement](https://msdn.microsoft.com/ja-JP/library/office/aa671659.aspx)
    

