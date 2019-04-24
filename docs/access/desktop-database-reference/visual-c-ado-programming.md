---
title: Visual C++ ADO プログラミング
TOCTitle: Visual C++ ADO programming
ms:assetid: 117c4fad-8c11-5e3a-ea0c-18811e87475f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248878(v=office.15)
ms:contentKeyID: 48543319
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2a890b4906fb9f207f12ff17ef0d3ccf1a97a44d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302773"
---
# <a name="visual-c-ado-programming"></a>Visual C++ ADO プログラミング

**適用先:** Access 2013、Office 2013

「ADO API リファレンス」では、Microsoft Visual Basic に似た構文を使用して ADO アプリケーション プログラミング インターフェイス (API) の機能を説明しています。 すべてのユーザーが対象となりますが、ado のプログラマは、visual Basic、visual C++ ( ** \#import**ディレクティブの有無は含む)、visual J++ (ado/WFC クラスパッケージ) など、さまざまな言語を使用します。

この多様性に対応するため、「[ADO を Visual C++ と共に使用する](using-ado-with-microsoft-visual-c.md)」では、「ADO API リファレンス」内の機能、パラメーター、例外的な動作などの共通の説明にリンクしている Visual C++ 言語固有の構文が用意されています。

ADO は COM (コンポーネント オブジェクト モデル) インターフェイスで実装されています。プログラマにとって、COM の操作は言語によって簡単である場合とそうでない場合があります。たとえば、Visual Basic のプログラマの場合は COM のほとんどの処理が暗黙的に実行されますが、Visual C++ プログラマの場合はそれらの処理を自分で行う必要があります。

次のセクションでは、ADO と** \#import**ディレクティブを使用する C および C++ のプログラマの詳細を要約します。 com に固有のデータ型 (**Variant**、 **BSTR**、および**SafeArray**) について、およびエラー処理\_(\_com エラー) を中心に説明します。

## <a name="using-the-import-compiler-directive"></a>import コンパイラ\#ディレクティブの使用

** \#import** Visual C++ コンパイラディレクティブを使用すると、ADO のメソッドとプロパティを簡単に使用できます。 このディレクティブは、タイプ ライブラリを含んでいる ADO .dll (Msado15.dll) などのファイルの名前を取得し、typedef 宣言、インターフェイスのスマート ポインター、および列挙定数を含むヘッダー ファイルを生成します。 各インターフェイスはクラス内にカプセル化またはラップされます。

クラス内の操作 (メソッドまたはプロパティの呼び出し) ごとに、操作を直接呼び出す宣言 ("raw" 形式の操作) と、raw 操作を呼び出して、操作の実行が失敗したときに COM エラーをスローする宣言があります。プロパティの操作の場合は、通常、その操作に対して Visual Basic に似た構文を持つ代替構文を作成するコンパイラ ディレクティブがあります。

プロパティの値を取得する操作には、form の名前 (**Get * ***) があります。 プロパティの値を設定する操作には、form の名前 **Put * * * プロパティ*を指定します。 ADO オブジェクトへのポインターを使用してプロパティの値を設定する操作は、**PutRef * *** * プロパティという形式の名前を持ちます。

プロパティを取得または設定するには、次の形式の呼び出しを行います。

```vb 
 
variable = objectPtr->GetProperty(); // get property value 
objectPtr->PutProperty(value); // set property value 
objectPtr->PutRefProperty(&value); // set property with object pointer 
```

## <a name="using-property-directives"></a>プロパティディレクティブの使用

**declspec (プロパティ...) コンパイラディレクティブは、Microsoft 固有の C 言語拡張機能であり、プロパティとして使用される関数を宣言しています。これは、代替構文を使用します。 \_ \_** これにより、Visual Basic に似た方法でプロパティの値を設定または取得できるようになります。 たとえば、次のようにしてプロパティを設定または取得できます。

```vb 
 
objectPtr->property = value; // set property value 
variable = objectPtr->property; // get property value 
```

コーディングが不要な点に注意してください。

```vb 
 
objectPtr->PutProperty(value); // set property value 
variable = objectPtr->GetProperty; // get property value 
```

コンパイラは、宣言された代替構文と、プロパティが読み取られているか書き込まれているかに基づいて、適切な **Get *** *-、 **Put**-、または **PutRef * ** * * * * * * * * * * * * * * * * * * * * * * * * *

**** **** **** **** ** \_declspec (プロパティ...) コンパイラディレクティブは、関数の get、put、または get および put の代替\_** 構文のみ宣言できます。 読み取り専用操作では **get** 宣言だけを、書き込み専用操作では **put** 宣言だけを、読み取りおよび書き込み操作では **get** 宣言と **put** 宣言の両方を組み込みます。

このディレクティブでは、2つの宣言のみが可能です。ただし、各プロパティには、次の3つのプロパティ関数があります。 **Get * * * * プロパティ*、**Put * ***、**PutRef *** * * その場合、代替構文があるのは 2 つの形式のプロパティだけです。

たとえば、 **Command**オブジェクトの**ActiveConnection**プロパティは、**Get * * * ActiveConnection* and **PutRef *** * ActiveConnection の代替構文を使用して宣言されています。 一般に、このプロパティには開いている **Connection** オブジェクト (つまり **Connection** オブジェクトのポインター) を設定することが多いため、**PutRef**- 構文を選択するのが適切です。 一方、 **Recordset**オブジェクトには、 **Get**、 **Put**、および **PutRef * ** * * * * * * * ActiveConnection 操作がありますが、代替構文はありません。

## <a name="collections-the-getitem-method-and-the-item-property"></a>コレクション、GetItem メソッド、および Item プロパティ

ADO では、 **Fields** 、 **Parameters** 、 **Properties** 、 **Errors** など、いくつかのコレクションが定義されています。 Visual C++ では、 **GetItem (***index***)** メソッドはコレクションのメンバーを返します。 *Index* はバリアント型 (**Variant**) で、値はコレクションのメンバーの数値インデックスか、またはメンバーの名前を含む文字列です。

** \_ \_declspec (プロパティ...)** コンパイラディレクティブは、各コレクションの基本的な**GetItem ()** メソッドに対して、代替構文として**Item**プロパティを宣言します。 代替構文は角かっこを使用し、配列参照に似ています。 一般に、次のような 2 つの形式になります。

```vb
    collectionPtr->GetItem(index); 
    collectionPtr->Item[index]; 
```

たとえば、**Recordset** オブジェクトの ***rs*** という名前のフィールドに、**pubs** データベースの **authors** テーブルの値を代入します。 **Recordset**オブジェクトの**Fields**コレクションの3番目の**フィールド**にアクセスするには、 **Item ()** プロパティを使用します (コレクションには0から始まるインデックスが付けられ、3番目のフィールドの名前は***\_au fname***になると仮定されます)。 **Field** オブジェクトで **Value()** メソッドを呼び出して、文字列値を代入します。

これを Visual Basic で記述するには、次の 4 つの方法があります (最後の 2 つの形式は Visual Basic 固有の形式であり、他の言語には同等の形式はありません)。

```vb 
 
rs.Fields.Item(2).Value = "value" 
rs.Fields.Item("au_fname").Value = "value" 
rs(2) = "value" 
rs!au_fname = "value" 
```

最初の 2 つの形式と同等の Visual C++ の形式は次のとおりです。

```cpp 
 
rs->Fields->GetItem(long(2))->PutValue("value"); 
rs->Fields->GetItem("au_fname")->PutValue("value"); 
```

\-または-( **Value**プロパティの代替構文も示されています)

```cpp 
 
rs->Fields->Item[long(2)]->Value = "value"; 
rs->Fields->Item["au_fname"]->Value = "value"; 
```

## <a name="com-specific-data-types"></a>COM 固有のデータ型

一般に、「ADO API リファレンス」で使われている Visual Basic のデータ型に対しては、同等のデータ型が Visual C++ にあります。たとえば、Visual Basic のバイト型 ( **Byte** ) に対する **unsigned char** 、整数型 ( **Integer** ) に対する **short** 、長整数型 ( **Long** ) に対する **long** などの標準データ型があります。各メソッドまたはプロパティのオペランドに必要な要素の詳細については、各「構文インデックス」を参照してください。

この規則が当てはまらないのは、COM 固有のデータ型であるバリアント型 ( **Variant** )、 **BSTR** 型、および **SafeArray** 型です。

### <a name="variant"></a>バリアント型

バリアント型 (**Variant**) は、値メンバーとデータ型メンバーを格納する構造化データ型です。バリアント型 (**Variant**) には、別のバリアント型 (Variant)、BSTR、ブール型 (Boolean)、IDispatch ポインターまたは IUnknown ポインター、通貨、日付など、さまざまなデータ型を格納できます。また、COM には、データ型の変換を簡単に実行できるメソッドが用意されています。

** \_variant\_t**クラスは、**バリアント型 (variant** ) のデータ型をカプセル化し、管理します。

ADO API リファレンスでメソッドまたはプロパティのオペランドが値を受け取る場合、通常は、値が** \_バリアント型 (variant\_**) で渡されたことを意味します。

「ADO API リファレンス」のトピックの「 **パラメーター** 」セクションでオペランドがバリアント型 ( **Variant** ) であると記載されている場合は、この規則が明白に当てはまります。例外は、このドキュメントでオペランドが長整数型 ( **Long** ) やバイト型 ( **Byte** ) などの標準データ型である、または列挙型であると明示的に記載されている場合です。また、オペランドが文字列型 ( **String** ) である場合も例外です。

### <a name="bstr"></a>BSTR 型

**BSTR** (**B**asic **STR**ing) は、文字列と文字列長を格納する構造化データ型です。COM には、**BSTR** 型を割り当て、操作、および解放するメソッドが用意されています。

** \_bstr\_t**クラスは、 **bstr**データ型をカプセル化し、管理します。

ADO API リファレンスでは、メソッドまたはプロパティが**文字列型 (String** ) の値を受け取ることを示している場合、値は** \_bstr\_t**の形式になっていることを意味します。

#### <a name="casting-variantt-and-bstrt-classes"></a>バリアント\_型\_t および\_bstr\_t クラスのキャスト

多くの場合、 ** \_バリアント型 (\_variant** ) の t または** \_bstr\_** を明示的に指定して操作に引数を指定する必要はありません。 ** \_\_** ** \_\_** ** \_variant\_t**または bstr t クラスに引数のデータ型と一致するコンストラクターがある場合、コンパイラは適切な variant t または** \_を生成します。bstr\_t**。

しかし、引数が不明確である、つまり、引数のデータ型が複数のコンストラクターに対応する場合は、正しいコンストラクターを呼び出すことができるように、引数を適切なデータ型にキャストする必要があります。

たとえば、 **Recordset::Open** メソッドの宣言を次に示します。

```vb 
 
 HRESULT Open ( 
 const _variant_t & Source, 
 const _variant_t & ActiveConnection, 
 enum CursorTypeEnum CursorType, 
 enum LockTypeEnum LockType, 
 long Options ); 
```

ActiveConnection 引数は、 ** \_バリアント型 (variant\_**) への参照を取得します。これは、接続文字列または開いている**connection**オブジェクトへのポインターとしてコーディングすることができます。

"DSN = pubs; uid = sa; pwd =;" などの文字列、または "(IDispatch \*) pconn" などのポインターを渡す場合は、正しい** \_variant\_t**が暗黙的に作成されます。

また、"\_variant\_t ((IDispatch \*) pconn, true)" のようなポインターを含む** \_バリアント型 (variant) の変数\_** を明示的にコーディングすることもできます。 cast (IDispatch \*) は、IUnknown インターフェイスへのポインターを取得する別のコンストラクターとのあいまいさを解決します。

ほとんど言及されませんが、ADO が IDispatch インターフェイスであるということは非常に重要です。ADO オブジェクトへのポインターをバリアント型 ( **Variant** ) として渡す場合は、そのポインターを IDispatch インターフェイスへのポインターとしてキャストする必要があります。

また、コンストラクターの 2 番目のブール型の引数を、オプションの既定値 true に明示的にコーディングする方法もあります。 この引数を指定すると、 **variant**のコンストラクタは**AddRef**() メソッドを呼び出します。このメソッドは、ado のメソッドまたはプロパティの呼び出しが完了すると、 ** \_バリアント型\_の t:: Release**() メソッドが自動的に呼び出されることを補正します。

### <a name="safearray"></a>safearray 型

A **SafeArray** is a structured data type that contains an array of other data types. **SafeArray**は、各配列次元の範囲に関する情報を格納し、それらの範囲内の配列要素へのアクセスを制限するので、*安全*と呼ばれます。

「ADO API リファレンス」で、メソッドまたはプロパティが配列を取得する、または配列を返すと記載されている場合は、メソッドまたはプロパティが、C/C++ のネイティブ配列ではなく **SafeArray** 型を取得するまたは返すことを意味します。

たとえば、 **Connection** オブジェクトの **OpenSchema** メソッドの 2 番目のパラメーターには、バリアント型 ( **Variant** ) の値の配列が必要です。これらのバリアント型 ( **Variant** ) の値は **SafeArray** 型の要素として渡される必要があり、その **SafeArray** 型は別のバリアント型 ( **Variant** ) の値として設定される必要があります。 **OpenSchema** の 2 番目の引数として渡されるのは、この別のバリアント型 ( **Variant** ) です。

さらに別の例として、 **Find** メソッドの最初の引数がバリアント型 ( **Variant** ) で、その値が 1 次元の **SafeArray** 型である場合、 **AddNew** の最初と 2 番目のオプションの引数はそれぞれ 1 次元の **SafeArray** 型で、 **GetRows** メソッドの戻り値は、値が 2 次元の **SafeArray** 型であるバリアント型 ( **Variant** ) です。

## <a name="missing-and-default-parameters"></a>不足している既定のパラメーター

Visual Basic では、メソッドのパラメーターを省略できます。たとえば、 **Recordset** オブジェクトの **Open** メソッドには 5 つのパラメーターがありますが、中間のパラメーターを省略して、後続のパラメーターをそのまま使用できます。省略可能なオペランドのデータ型に応じて、既定の **BSTR** 型またはバリアント型 ( **Variant** ) が代用されます。

C/C++ では、すべてのオペランドを指定する必要があります。 データ型が文字列である不足パラメーターを指定する場合は、null 文字列を** \_含む\_bstr t**を指定します。 データ型が**バリアント**である不足パラメーターを指定する場合は、 ** \_バリアント\_型 t**を指定します。この値\_\_には、////\_///////の種類の VT エラーがあります。 または **、 \#インポート**ディレクティブによって提供される、等価** \_のバリアント型\_t**定数**vtmissing**を指定します。

**vtMissing** の一般的な使用方法の例外として、3 つのメソッドがあります。それは、 **Connection** オブジェクトおよび **Command** オブジェクトの **Execute** メソッドと、 **Recordset** オブジェクトの **NextRecordset** メソッドです。次に、これらのメソッドを示します。

```vb 
 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthcnnexecute_HV10294345.xml( _bstr_t CommandText, VARIANT * RecordsAffected, 
 long Options ); // Connection 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthcmdexecute_HV10294344.xml( VARIANT * RecordsAffected, VARIANT * Parameters, 
 long Options ); // Command 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthnextrec_HV10294541.xml( VARIANT * RecordsAffected ); // Recordset 
```

*RecordsAffected* パラメーターと *Parameters* パラメーターは、1 つのバリアント型 (**Variant**) へのポインターです。*Parameters* は、実行されるコマンドを変更する 1 つのパラメーターまたはパラメーターの配列を格納するバリアント型 (**Variant**) のアドレスを指定する入力パラメーターです。*RecordsAffected* は、メソッドによって影響を受ける行数を返すバリアント型 (**Variant**) のアドレスを指定する出力パラメーターです。

**Command**オブジェクトの**Execute**メソッドで、パラメーターを vtmissing (推奨) また** は null ポインター \&( **null**またはゼロ (0)) のいずれかに設定することによって、パラメーターが指定されていないことを示します。 *Parameters* が Null ポインターに設定された場合、メソッドは同等の **vtMissing** を内部的に代用し、操作を実行します。

どのメソッドでも、*RecordsAffected* を Null ポインターに設定すると、影響を受けるレコードの数を返さないように指定できます。この場合、Null ポインターは省略されたパラメーターではなく、影響を受けるレコードの数を破棄するようにというメソッドへの指示です。

したがって、これらの 3 つのメソッドの場合、次のようなコーディングもできます。

```vb 
 
pConnection->Execute("commandText", NULL, adCmdText); 
pCommand->Execute(NULL, NULL, adCmdText); 
pRecordset->NextRecordset(NULL); 
```

## <a name="error-handling"></a>エラー処理

COM では、ほとんどの操作は、関数が正常に完了したかどうかを示す HRESULT リターンコードを返します。 ** \#import**ディレクティブは、各 "raw" メソッドまたはプロパティの前後にラッパーコードを生成し、返された HRESULT をチェックします。 hresult が失敗を示している場合、ラッパーコードは、hresult リターン\_コード\_を\_引数として com 問題 errorex () を呼び出すことによって com エラーをスローします。 COM エラーオブジェクトは、 **try**-**catch**ブロックでキャッチできます。 (効率を上げるために、 ** \_com\_error**オブジェクトへの参照をキャッチします)。

これらは ADO エラーであり、ADO 操作の失敗によって生成されます。基になるプロバイダーから返されるエラーは、 **Connection** オブジェクトの **Errors** コレクションに **Error** オブジェクトとして表示されます。

** \#import**ディレクティブは、ADO .dll で宣言されているメソッドおよびプロパティに対してエラー処理ルーチンのみを作成します。 ただし、自分でエラー確認マクロやインライン関数を記述すると、同じエラー処理機構を利用できます。 例については、「 [ADO 用の Visual C++ Extensions](visual-c-extensions-for-ado.md)」または、以下に説明するコードを参照してください。

## <a name="visual-c-equivalents-of-visual-basic-conventions"></a>visual Basic の規則と同等の visual C++ の規則

Visual Basic および、それと同等の Visual C++ でコーディングされた ADO ドキュメントにおけるいくつかの規則の概要を次に示します。

### <a name="declaring-an-ado-object"></a>ADO オブジェクトを宣言する

Visual Basic では、ADO オブジェクト変数 (この場合は **Recordset** オブジェクトの変数) を次のように宣言します。

```vb 
 
Dim rst As ADODB.Recordset 
```

句「ADODB」recordset "は、レジストリで定義されている**recordset**オブジェクトの ProgID です。 **Record** オブジェクトの新しいインスタンスは、次のように宣言します。

```vb 
 
Dim rst As New ADODB.Recordset 
```

\-や

```vb 
 
Dim rst As ADODB.Recordset 
Set rst = New ADODB.Recordset 
```

Visual C++ では、 ** \#import**ディレクティブによって、すべての ADO オブジェクトに対するスマートポインター型の宣言が生成されます。 たとえば、 ** \_Recordset**オブジェクトを参照する変数は** \_RecordsetPtr**型であり、次のように宣言されます。

```cpp 
 
_RecordsetPtr rs; 
```

Recordset オブジェクトの新しいインスタンスを指す変数は、次のように宣言されます。 ** \_**

```cpp 
 
_RecordsetPtr rs("ADODB.Recordset"); 
```

\-や

```cpp 
 
_RecordsetPtr rs; 
rs.CreateInstance("ADODB.Recordset"); 
```

\-や

```cpp 
 
_RecordsetPtr rs; 
rs.CreateInstance(__uuidof(_Recordset)); 
```

**CreateInstance** メソッドの呼び出し後に、この変数を次のように使用できます。

```cpp 
 
rs->Open(...); 
```

1つのケースでは、変数がクラスのインスタンスであるかのように "." 演算子が使用されていることに注意してください (rs.CreateInstance) を使用します。別のケースで\>は、変数がインターフェイスへのポインター (rs-\>Open) であった場合と同じように "-" 演算子が使用されます。

1つの変数は2つの方法で使用でき\>ます。 "-" 演算子は、クラスのインスタンスがインターフェイスへのポインターのように動作するようにするためにオーバーロードされています。 インスタンス変数のプライベートクラスメンバーには、 ** \_Recordset**インターフェイスへのポインターが含まれています。"-\>" 演算子はそのポインターを返します。そして、返されるポインターは** \_Recordset**オブジェクトのメンバーにアクセスします。

### <a name="coding-a-missing-parameter"></a>不足しているパラメーターのコーディング

#### <a name="string"></a>String

Visual Basic で省略可能な文字列型 ( **String** ) のオペランドをコーディングする場合は、単純にそのオペランドを省略します。 Visual C++ では、そのオペランドを指定する必要があります。 値として空の文字列を持つ** \_bstr\_t**をコーディングします。

```cpp 
 
_bstr_t strMissing(L""); 
```

#### <a name="variant"></a>バリアント型

Visual Basic で省略可能なバリアント型 ( **Variant** ) のオペランドをコーディングする場合は、単純にそのオペランドを省略します。 Visual C++ では、そのオペランドを指定する必要があります。 PARAMNOTFOUND のバリアント**** 型 (variant) のパラメーターに、特殊な値、/\_変位\_E、type、VT\_エラーが設定されて** \_\_** います。 または、 ** \#import**ディレクティブによって提供される同等の、定義済みの定数である**vtmissing**を指定します。

```cpp 
 
_variant_t vtMissingYours(DISP_E_PARAMNOTFOUND, VT_ERROR); 
```

\-または-

```cpp 
 
...vtMissing...; 
```

### <a name="declaring-a-variant"></a>バリアントの宣言

Visual Basic では、バリアント型 ( **Variant** ) は次のように **Dim** ステートメントで宣言します。

```vb 
 
Dim VariableName As Variant 
```

Visual C++ では、変数を** \_variant\_t**型として宣言します。 以下に、いくつかのスケマティック** \_variant\_t**宣言を示します。

> [!NOTE]
> [!メモ] これらの宣言では、プログラムでコーディングする内容の概要のみを示しています。詳細については、後の例や Visual C++ のドキュメントを参照してください。

```cpp 
 
_variant_t VariableName(value); 
_variant_t VariableName((data type cast) value); 
_variant_t VariableName(value, VT_DATATYPE); 
_variant_t VariableName(interface * value, bool fAddRef = true); 
```

### <a name="using-arrays-of-variants"></a>バリアントの配列を使用する

Visual Basic では、バリアント型 ( **Variant** ) の配列は **Dim** ステートメントを使用するか、または **Array** 関数を使用してコーディングできます。次にコード例を示します。

```vb 
 
Public Sub ArrayOfVariants 
Dim cn As ADODB.Connection 
Dim rs As ADODB.Recordset 
Dim fld As ADODB.Field 
 
cn.Open "DSN=pubs", "sa", "" 
rs = cn.OpenSchema(adSchemaColumns, _ 
 Array(Empty, Empty, "authors", Empty)) 
For Each fld in rs.Fields 
 Debug.Print "Name = "; fld.Name 
Next fld 
rs.Close 
cn.Close 
End Sub 
```

次の Visual C++ の例では、 ** \_バリアント型\_t**で使用される**SafeArray**の使用方法を示します。

> [!NOTE]
> 次の注意事項は、コード例のコメント部分に対応しています。

1. 既存のエラー処理機構を利用するために、もう一度、TESTHR() インライン関数を定義します。

2. 必要なのは 1 次元配列のみであるため、汎用の **SAFEARRAYBOUND** 宣言と **SafeArrayCreate** 関数の代わりに **SafeArrayCreateVector** 関数を使用できます。次に、 **SafeArrayCreate** を使用した場合のコードを示します。
    
   ```cpp 
     
     SAFEARRAYBOUND sabound[1]; 
     sabound[0].lLbound = 0; 
     sabound[0].cElements = 4; 
     pSa = SafeArrayCreate(VT_VARIANT, 1, sabound); 
   ```

3. 列挙定数**adSchemaColumns**によって識別されるスキーマは、table\_CATALOG、\_table スキーマ、table\_name、および COLUMN\_name という4つの制約列に関連付けられています。 したがって、4 つの要素を持つバリアント型 ( **Variant** ) の値の配列が作成されます。 次に、3番目の列の TABLE\_NAME に対応する制約値が指定されます。 返される **Recordset** はいくつかの列で構成され、そのサブセットは制約列です。 返される各行に対する制約列の値は、対応する制約値と同じである必要があります。

4. **SafeArrays** 型に慣れていると、終了前に **SafeArrayDestroy**() が呼び出されないことに驚かれるかもしれません。 実際には、この場合に **SafeArrayDestroy**() を呼び出すと実行時例外が発生します。 理由は、VariantClear () を呼び出すと、その** \_バリアント型\_** のデストラクターがスコープ外になるときに、 **SafeArray**を解放することになるため、vtcriteria のデストラクターは****() を呼び出します。 **バリアント型 (\_variant) を手動でクリアせずに SafeArrayDestroy を呼び出すと、デストラクターは無効な SafeArray ポインターを削除しようとします。 \_** **** **** **SafeArrayDestroy** を呼び出した場合、コードは次のようになります。
    
   ```cpp 
     
     TESTHR(SafeArrayDestroy(pSa)); 
     vtCriteria.vt = VT_EMPTY; 
     vtCriteria.parray = NULL; 
   ```
    
   ただし、 ** \_バリアント型\_** の**SafeArray**を管理する方がはるかに簡単です。


```cpp 
 
    #import "c:\Program Files\Common Files\System\ADO\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
    #include <stdio.h> 
    
    // Note 1 
    inline void TESTHR( HRESULT _hr ) 
    { if FAILED(_hr) _com_issue_error(_hr); } 
    
    void main(void) 
    { 
    CoInitialize(NULL); 
    try 
    { 
    _RecordsetPtr pRs("ADODB.Recordset"); 
    _ConnectionPtr pCn("ADODB.Connection"); 
    _variant_t vtTableName("authors"), 
    vtCriteria; 
    long ix[1]; 
    SAFEARRAY *pSa = NULL; 
    
    pCn->Open("DSN=pubs;User ID=MyUserId;pwd=MyPassword;Provider=MSDASQL;", "", "", 
    adConnectUnspecified); 
    // Note 2, Note 3 
    pSa = SafeArrayCreateVector(VT_VARIANT, 1, 4); 
    if (!pSa) _com_issue_error(E_OUTOFMEMORY); 
    
    // Specify TABLE_NAME in the third array element (index of 2). 
    
    ix[0] = 2; 
    TESTHR(SafeArrayPutElement(pSa, ix, &vtTableName)); 
    
    // There is no Variant constructor for a SafeArray, so manually set the 
    // type (SafeArray of Variant) and value (pointer to a SafeArray). 
    
    vtCriteria.vt = VT_ARRAY | VT_VARIANT; 
    vtCriteria.parray = pSa; 
    
    pRs = pCn->OpenSchema(adSchemaColumns, vtCriteria, vtMissing); 
    
    long limit = pRs->GetFields()->Count; 
    for (long x = 0; x < limit; x++) 
    printf("%d: %s\n", x+1, 
    ((char*) pRs->GetFields()->Item[x]->Name)); 
    // Note 4 
    pRs->Close(); 
    pCn->Close(); 
    } 
    catch (_com_error &e) 
    { 
    printf("Error:\n"); 
    printf("Code = %08lx\n", e.Error()); 
    printf("Code meaning = %s\n", (char*) e.ErrorMessage()); 
    printf("Source = %s\n", (char*) e.Source()); 
    printf("Description = %s\n", (char*) e.Description()); 
    } 
    CoUninitialize(); 
    } 
```

### <a name="using-property-getputputref"></a>プロパティ Get/Put/PutRef を使用する

Visual Basic では、プロパティが取得、割り当て、または参照を割り当てられるかどうかによって、プロパティの名前が修飾されることはありません。

```vb
    Public Sub GetPutPutRef 
    Dim rs As New ADODB.Recordset 
    Dim cn As New ADODB.Connection 
    Dim sz as Integer 
    cn.Open "Provider=sqloledb;Data Source=yourserver;" & _ 
     "Initial Catalog=pubs;Integrated Security=SSPI;" 
    rs.PageSize = 10 
    sz = rs.PageSize 
    rs.ActiveConnection = cn 
    rs.Open "authors",,adOpenStatic 
    ' ... 
    rs.Close 
    cn.Close 
    End Sub
```

この Visual C++ の例では、 **Get**/**Put**/**PutRef * * * プロパティ*を示します。

> [!NOTE]
> [!メモ] 次の注意事項は、コード例のコメント部分に対応しています。

1. この例では、省略可能な文字列引数の2つの形式を使用します。明示的な定数**strmissing**、および**Open**メソッドのスコープに対して存在する一時的** \_な bstr\_t**を作成するためにコンパイラが使用する文字列。

2. オペランドの型が既に (idispatch\> \* \*) になっているため、PutRefActiveConnection (cn) のオペランドを (idispatch) にキャストする必要はありません。
    
   ```cpp 
     
    #import "c:\Program Files\Common Files\System\ADO\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
    #include <stdio.h> 
     
    void main(void) 
    { 
     CoInitialize(NULL); 
     try 
     { 
     _ConnectionPtr cn("ADODB.Connection"); 
     _RecordsetPtr rs("ADODB.Recordset"); 
     _bstr_t strMissing(L""); 
     long oldPgSz = 0, 
     newPgSz = 5; 
     
    // Note 1 
     cn->Open("Provider=sqloledb;Data Source=MyServer;" 
     "Initial Catalog=pubs;Integrated Security=SSPI;", 
     strMissing, "", 
     adConnectUnspecified); 
     
     oldPgSz = rs->GetPageSize(); 
     // -or- 
     oldPgSz = rs->PageSize; 
     
     rs->PutPageSize(newPgSz); 
     // -or- 
     rs->PageSize = newPgSz; 
     
    // Note 2 
     rs->PutRefActiveConnection( cn ); 
     rs->Open("authors", vtMissing, adOpenStatic, adLockReadOnly, 
     adCmdTable); 
     printf("Original pagesize = %d, new pagesize = %d\n", oldPgSz, 
     rs->GetPageSize()); 
     rs->Close(); 
     cn->Close(); 
     } 
     catch (_com_error &e) 
     { 
     printf("Description = %s\n", (char*) e.Description()); 
     } 
     ::CoUninitialize(); 
    } 
   ```

### <a name="using-getitemx-and-itemx"></a>GetItem (x) と Item\[x の使用\]

この Visual Basic の例では、**Item**() の標準構文と代替構文を示します。

```vb 
 
Public Sub GetItemItem 
Dim rs As New ADODB.Recordset 
Dim name as String 
rs = rs.Open "authors", "DSN=pubs;", adOpenDynamic, _ 
 adLockBatchOptimistic, adTable 
name = rs(0) 
' -or- 
name = rs.Fields.Item(0) 
rs(0) = "Test" 
rs.UpdateBatch 
' Restore name 
rs(0) = name 
rs.UpdateBatch 
rs.Close 
End Sub 
```

この Visual C++ の例は、**Item** を示します。

> [!NOTE]
> [!メモ] 次の注意事項は、コード例のコメント部分に対応しています。

1. コレクションに **Item** を使用してアクセスした場合、適切なコンストラクターが呼び出されるように、インデックス **2** が **long** にキャストされる必要があります。
    
   ```cpp 
     
    #import "c:\Program Files\Common Files\System\ADO\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
    #include <stdio.h> 
     
    void main(void) 
    { 
     CoInitialize(NULL); 
     try { 
     _RecordsetPtr rs("ADODB.Recordset"); 
     _variant_t vtFirstName; 
     
     rs->Open("authors", 
     "Provider=sqloledb;Data Source=MyServer;" 
     "Initial Catalog=pubs;Integrated Security=SSPI;", 
     adOpenStatic, adLockOptimistic, adCmdTable); 
     rs->MoveFirst(); 
     
    // Note 1. Get a field. 
     vtFirstName = rs->Fields->GetItem((long)2)->GetValue(); 
     // -or- 
     vtFirstName = rs->Fields->Item[(long)2]->Value; 
     
     printf( "First name = '%s'\n", (char*) ((_bstr_t) vtFirstName)); 
     
     rs->Fields->GetItem((long)2)->Value = L"TEST"; 
     rs->Update(vtMissing, vtMissing); 
     
     // Restore name 
     rs->Fields->GetItem((long)2)->PutValue(vtFirstName); 
     // -or- 
     rs->Fields->GetItem((long)2)->Value = vtFirstName; 
     rs->Update(vtMissing, vtMissing); 
     rs->Close(); 
     } 
     catch (_com_error &e) 
     { 
     printf("Description = '%s'\n", (char*) e.Description()); 
     } 
     ::CoUninitialize(); 
    } 
   ```

### <a name="casting-ado-object-pointers-with-idispatch-"></a>(IDispatch \*) による ADO オブジェクト ポインターのキャスト

次の Visual C++ の例では、(IDispatch \*) を使用した ADO オブジェクト ポイントのキャストを示します。

> [!NOTE]
> [!メモ] 次の注意事項は、コード例のコメント部分に対応しています。

1. 明示的にコーディングされたバリアント型 ( **Variant** ) で、開いている **Connection** オブジェクトを指定します。 適切なコンストラクターが呼び出さ\*れるように、(IDispatch) をキャストします。 また、 **Recordset:: Open**操作の終了時に、2番目** \_の\_variant の t**パラメーターを明示的に既定値の**true**に設定して、オブジェクト参照カウントが正しいことを確認してください。

2. 式 (\_\_bstr t) はキャストではなく、**値**によって返される**variant**から**bstr \_\_t**文字列を抽出する** \_バリアント型\_の t**演算子です。 式 (char\*) はキャストではなく、bstr t オブジェクトの** \_\_** カプセル化された文字列へのポインターを抽出する** \_\_bstr t**演算子です。 このコードセクションでは、 ** \_バリアント型\_の t**演算子と** \_bstr\_の t**演算子の便利な動作をいくつか示します。
    
   ```cpp 
     
    #import "c:\Program Files\Common Files\System\ADO\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
     
    #include <stdio.h> 
     
    void main(void) 
    { 
     CoInitialize(NULL); 
     try 
     { 
     _ConnectionPtr pConn("ADODB.Connection"); 
     _RecordsetPtr pRst("ADODB.Recordset"); 
     
     pConn->Open("Provider=sqloledb;Data Source=MyServer;" 
     "Initial Catalog=pubs;Integrated Security=SSPI;", 
     "", "", adConnectUnspecified); 
    // Note 1. 
     pRst->Open( 
     "authors", 
     _variant_t((IDispatch *) pConn, true), 
     adOpenStatic, 
     adLockReadOnly, 
     adCmdTable); 
     pRst->MoveLast(); 
    // Note 2. 
     printf("Last name is '%s %s'\n", 
     (char*) ((_bstr_t) pRst->GetFields()->GetItem("au_fname")->GetValue()), 
     (char*) ((_bstr_t) pRst->Fields->Item["au_lname"]->Value)); 
     
     pRst->Close(); 
     pConn->Close(); 
     } 
     catch (_com_error &e) 
     { 
     printf("Description = '%s'\n", (char*) e.Description()); 
     } 
    ::CoUninitialize(); 
    } 
   ```

