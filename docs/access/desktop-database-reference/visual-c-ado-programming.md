---
title: Visual C++ での ADO プログラミング
TOCTitle: Visual C++ ADO Programming
ms:assetid: 117c4fad-8c11-5e3a-ea0c-18811e87475f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248878(v=office.15)
ms:contentKeyID: 48543319
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7478a90e3c6242c68a1325b08e998f4c76a62f3d
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944663"
---
# <a name="visual-c-ado-programming"></a>Visual C++ の ADO プログラミング


**適用されます**Access 2013、Office 2013。

「ADO API リファレンス」では、Microsoft Visual Basic に似た構文を使用して ADO アプリケーション プログラミング インターフェイス (API) の機能を説明しています。 対象がすべてのユーザーは、ADO プログラマは Visual Basic、Visual C++ などの多様な言語を採用して (しなくても、**\#インポート**ディレクティブ)、および Visual j (ADO/WFC クラス パッケージ) を持つ。

この多様性に対応するため、「[ADO を Visual C++ と共に使用する](using-ado-with-microsoft-visual-c.md)」では、「ADO API リファレンス」内の機能、パラメーター、例外的な動作などの共通の説明にリンクしている Visual C++ 言語固有の構文が用意されています。

ADO は COM (コンポーネント オブジェクト モデル) インターフェイスで実装されています。プログラマにとって、COM の操作は言語によって簡単である場合とそうでない場合があります。たとえば、Visual Basic のプログラマの場合は COM のほとんどの処理が暗黙的に実行されますが、Visual C++ プログラマの場合はそれらの処理を自分で行う必要があります。

次のセクションの概要を C および C++ のプログラマが ADO を使用して、**\#インポート**ディレクティブです。 COM (**バリアント**、 **BSTR**、および**safearray 型**)、およびエラー処理に固有のデータ型に重点を置いています (\_com\_エラー)。

## <a name="using-the-import-compiler-directive"></a>使用して、\#コンパイラ ディレクティブのインポート

**\#インポート**Visual C++ コンパイラ ディレクティブは、ADO のメソッドとプロパティの使用を簡略化します。 このディレクティブは、タイプ ライブラリを含んでいる ADO .dll (Msado15.dll) などのファイルの名前を取得し、typedef 宣言、インターフェイスのスマート ポインター、および列挙定数を含むヘッダー ファイルを生成します。 各インターフェイスはクラス内にカプセル化またはラップされます。

クラス内の操作 (メソッドまたはプロパティの呼び出し) ごとに、操作を直接呼び出す宣言 ("raw" 形式の操作) と、raw 操作を呼び出して、操作の実行が失敗したときに COM エラーをスローする宣言があります。プロパティの操作の場合は、通常、その操作に対して Visual Basic に似た構文を持つ代替構文を作成するコンパイラ ディレクティブがあります。

プロパティの値を取得する操作は、フォームの名前を持つ **を取得します。 プロパティ*。 プロパティの値を設定する操作は、フォームの名前を持つ **配置。 プロパティ*。 ADO オブジェクトへのポインターを持つプロパティの値を設定する操作は、フォームの名前を持つ **PutRef。 プロパティ*。

プロパティを取得または設定するには、次の形式の呼び出しを行います。

```vb 
 
variable = objectPtr->GetProperty(); // get property value 
objectPtr->PutProperty(value); // set property value 
objectPtr->PutRefProperty(&value); // set property with object pointer 
```

## <a name="using-property-directives"></a>プロパティ ディレクティブの使用

** \_ \_Declspec(property...)** コンパイラ ディレクティブは、マイクロソフト固有の C 言語拡張機能が別の構文を使用してプロパティとして使用される関数を宣言します。 これにより、Visual Basic に似た方法でプロパティの値を設定または取得できるようになります。 たとえば、次のようにしてプロパティを設定または取得できます。

```vb 
 
objectPtr->property = value; // set property value 
variable = objectPtr->property; // get property value 
```

コーディングが不要な点に注意してください。

```vb 
 
objectPtr->PutProperty(value); // set property value 
variable = objectPtr->GetProperty; // get property value 
```

適切なコンパイラが生成されます **Get。-*、**配置**の、または **PutRef。 プロパティ*の呼び出しでは、宣言されたどのような代替の構文と、プロパティがされているかどうかに基づいて読み取りや書き込みをします。

** \_ \_Declspec(property...)** コンパイラ ディレクティブには、**取得**、**配置**、または関数の別の構文を****取得**し、** のみを宣言できます。 読み取り専用操作では **get** 宣言だけを、書き込み専用操作では **put** 宣言だけを、読み取りおよび書き込み操作では **get** 宣言と **put** 宣言の両方を組み込みます。

2 つの宣言は、このディレクティブで実行できます。ただし、各プロパティがプロパティの 3 つの関数を必要があります: **を取得します。 プロパティ*、**配置。 プロパティ*、および **PutRef。 プロパティ*。 その場合、代替構文があるのは 2 つの形式のプロパティだけです。

代替の構文を使用して**Command**オブジェクトの**ActiveConnection**プロパティを宣言するたとえば、**を取得します。 ActiveConnection*と **PutRef。 ActiveConnection*。 **PutRef**での構文をお勧めため実際には、通常このプロパティで開いている**接続**オブジェクト (つまり、**接続**オブジェクト ポインター) を配置します。 **レコード セット**オブジェクトには、その一方で、**取得**、**配置**、および **PutRef。 ActiveConnection*操作が別の構文ではありません。

## <a name="collections-the-getitem-method-and-the-item-property"></a>コレクション、GetItem メソッド、および Item プロパティ

ADO では、**Fields**、**Parameters**、**Properties**、**Errors** など、いくつかのコレクションが定義されています。Visual C++ では、コレクションのメンバーは **GetItem(***index***)** メソッドによって返されます。*Index* はバリアント型 (**Variant**) で、値はコレクションのメンバーの数値インデックスか、またはメンバーの名前を含む文字列です。

** \_ \_Declspec(property...)** コンパイラ ディレクティブは、 **getitem() を実行**メソッドの基本的なコレクションごとに別の構文として**Item**プロパティを宣言しています。 代替構文は角かっこを使用し、配列参照に似ています。 一般に、次のような 2 つの形式になります。

```vb
    collectionPtr->GetItem(index); 
    collectionPtr->Item[index]; 
```

たとえば、 ***rs***、 **pubs**データベースの**authors**テーブルから派生したという名前**のレコード セット**オブジェクトのフィールドに値を割り当てます。 **Item()** プロパティを使用して、 **Recordset**オブジェクトの**Fields**コレクションの 3 番目の**フィールド**にアクセスするのには (コレクションのインデックスは 0 から; 3 番目のフィールドの名前は前提としています***au\_fname***)。 **Field** オブジェクトで **Value()** メソッドを呼び出して、文字列値を代入します。

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

\-または -( **Value**プロパティの代替構文も表示)

```cpp 
 
rs->Fields->Item[long(2)]->Value = "value"; 
rs->Fields->Item["au_fname"]->Value = "value"; 
```

## <a name="com-specific-data-types"></a>COM 固有のデータ型

一般に、「ADO API リファレンス」で使われている Visual Basic のデータ型に対しては、同等のデータ型が Visual C++ にあります。たとえば、Visual Basic のバイト型 ( **Byte** ) に対する **unsigned char** 、整数型 ( **Integer** ) に対する **short** 、長整数型 ( **Long** ) に対する **long** などの標準データ型があります。各メソッドまたはプロパティのオペランドに必要な要素の詳細については、各「構文インデックス」を参照してください。

この規則が当てはまらないのは、COM 固有のデータ型であるバリアント型 ( **Variant** )、 **BSTR** 型、および **SafeArray** 型です。

## <a name="variant"></a>バリアント型 (Variant)

バリアント型 ( **Variant** ) は、値メンバーとデータ型メンバーを格納する構造化データ型です。バリアント型 ( **Variant** ) には、別のバリアント型 (Variant)、BSTR、ブール型 (Boolean)、IDispatch ポインターまたは IUnknown ポインター、通貨、日付など、さまざまなデータ型を格納できます。また、COM には、データ型の変換を簡単に実行できるメソッドが用意されています。

**\_バリアント\_t**クラスは、カプセル化し、**バリアント**データ型を管理します。

場合 ADO API リファレンス」でメソッドまたはプロパティのオペランドが値を受け取り、通常は、値が渡された、**\_バリアント\_t**。

「ADO API リファレンス」のトピックの「 **パラメーター** 」セクションでオペランドがバリアント型 ( **Variant** ) であると記載されている場合は、この規則が明白に当てはまります。例外は、このドキュメントでオペランドが長整数型 ( **Long** ) やバイト型 ( **Byte** ) などの標準データ型である、または列挙型であると明示的に記載されている場合です。また、オペランドが文字列型 ( **String** ) である場合も例外です。

## <a name="bstr"></a>BSTR 型

**BSTR** (**B**asic **STR**ing) は、文字列と文字列長を格納する構造化データ型です。COM には、**BSTR** 型を割り当て、操作、および解放するメソッドが用意されています。

** \_Bstr\_t**クラスは、カプセル化し、 **BSTR**データ型を管理します。

「ADO API リファレンス」でメソッドまたはプロパティが**文字列**値を受け取る、ときにことを意味値の形式で、 ** \_bstr\_t**.

## <a name="casting-variantt-and-bstrt-classes"></a>キャスト\_バリアント\_t と\_bstr\_t クラス

多くの場合、コードでは明示的にする必要はありません、**\_バリアント\_t**または**\_bstr\_t**操作への引数にします。 場合、**\_バリアント\_t**または**\_bstr\_t**クラスには、引数のデータ型に一致するコンス トラクターは、コンパイラが生成されます、適切な**\_バリアント\_t**または**\_bstr\_t**。

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

参照は、暗黙的に**\_バリアント\_t**、接続文字列または開いている**接続**オブジェクトへのポインターとしてコードを作成することがあります。

正しい**\_バリアント\_t**次のように文字列を渡す場合は、暗黙的に作成される"DSN = pubs; uid = sa; pwd =;"、またはようにポインター"(IDispatch \*) pConn」。

明示的にコーディングすることがありますか、**\_バリアント\_t**のポインターを次のように含まれている"\_バリアント\_t ((IDispatch \*) pConn、true を指定)」です。 キャスト (IDispatch \*)、IUnknown インターフェイスへのポインターを取得するもう 1 つのコンス トラクターを持つあいまいさを解決します。

ほとんど言及されませんが、ADO が IDispatch インターフェイスであるということは非常に重要です。ADO オブジェクトへのポインターをバリアント型 ( **Variant** ) として渡す場合は、そのポインターを IDispatch インターフェイスへのポインターとしてキャストする必要があります。

コンス トラクターの 2 番目のブール型の引数のオプションの既定値の true を明示的にコーディングする方法も。 この引数は、**バリアント型**コンス トラクターは、ADO の呼び出しを自動的に補正、 **AddRef**() メソッドを呼び出す、**\_バリアント\_t::Release**() メソッドの ADO のメソッドまたはプロパティの呼び出しが完了するとします。

## <a name="safearray"></a>SafeArray

**SafeArray**は、他のデータ型の配列を含む構造化データ タイプです。 **SafeArray**は各配列の次元、およびそれらの範囲内の配列要素へのアクセス制限の範囲に関する情報が含まれているために、*安全*と呼ばれます。

「ADO API リファレンス」で、メソッドまたはプロパティが配列を取得する、または配列を返すと記載されている場合は、メソッドまたはプロパティが、C/C++ のネイティブ配列ではなく **SafeArray** 型を取得するまたは返すことを意味します。

たとえば、 **Connection** オブジェクトの **OpenSchema** メソッドの 2 番目のパラメーターには、バリアント型 ( **Variant** ) の値の配列が必要です。これらのバリアント型 ( **Variant** ) の値は **SafeArray** 型の要素として渡される必要があり、その **SafeArray** 型は別のバリアント型 ( **Variant** ) の値として設定される必要があります。 **OpenSchema** の 2 番目の引数として渡されるのは、この別のバリアント型 ( **Variant** ) です。

さらに別の例として、 **Find** メソッドの最初の引数がバリアント型 ( **Variant** ) で、その値が 1 次元の **SafeArray** 型である場合、 **AddNew** の最初と 2 番目のオプションの引数はそれぞれ 1 次元の **SafeArray** 型で、 **GetRows** メソッドの戻り値は、値が 2 次元の **SafeArray** 型であるバリアント型 ( **Variant** ) です。

## <a name="missing-and-default-parameters"></a>省略可能なパラメーターと既定のパラメーター

Visual Basic では、メソッドのパラメーターを省略できます。たとえば、 **Recordset** オブジェクトの **Open** メソッドには 5 つのパラメーターがありますが、中間のパラメーターを省略して、後続のパラメーターをそのまま使用できます。省略可能なオペランドのデータ型に応じて、既定の **BSTR** 型またはバリアント型 ( **Variant** ) が代用されます。

C/C++ では、すべてのオペランドを指定する必要があります。 不足しているパラメーターを指定する場合は、データ型の文字列は、指定、 ** \_bstr\_t**は、null 文字列が含まれています。 不足しているパラメーターを指定する場合は、データ型の**バリアント型**は、指定、**\_バリアント\_t**変位の値を持つ\_E\_PARAMNOTFOUND と vt 型\_エラーです。 または、相当するものを指定**\_バリアント\_t**定数、 **vtMissing**が提供する、**\#インポート**ディレクティブです。

**vtMissing** の一般的な使用方法の例外として、3 つのメソッドがあります。それは、 **Connection** オブジェクトおよび **Command** オブジェクトの **Execute** メソッドと、 **Recordset** オブジェクトの **NextRecordset** メソッドです。次に、これらのメソッドを示します。

```vb 
 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthcnnexecute_HV10294345.xml( _bstr_t CommandText, VARIANT * RecordsAffected, 
 long Options ); // Connection 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthcmdexecute_HV10294344.xml( VARIANT * RecordsAffected, VARIANT * Parameters, 
 long Options ); // Command 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthnextrec_HV10294541.xml( VARIANT * RecordsAffected ); // Recordset 
```

*RecordsAffected* パラメーターと *Parameters* パラメーターは、1 つのバリアント型 (**Variant**) へのポインターです。*Parameters* は、実行されるコマンドを変更する 1 つのパラメーターまたはパラメーターの配列を格納するバリアント型 (**Variant**) のアドレスを指定する入力パラメーターです。*RecordsAffected* は、メソッドによって影響を受ける行数を返すバリアント型 (**Variant**) のアドレスを指定する出力パラメーターです。

**コマンド**オブジェクトの**Execute**メソッドで*パラメーター*を設定するか、パラメーターが指定されていないことを示す\&vtMissing (推奨)、または null のポインターを (つまり、 **NULL**またはゼロ (0))。 *パラメーター*は、null ポインターに設定されているメソッドは、 **vtMissing**のと同じでは内部的に、操作が完了します。

すべてのメソッドでことの影響を受けるレコードの数を返すべきでない*RecordsAffected*を null ポインターに設定することでを指定します。 この場合、Null ポインターは省略されたパラメーターではなく、影響を受けるレコードの数を破棄するようにというメソッドへの指示です。

したがって、これらの 3 つのメソッドの場合、次のようなコーディングもできます。

```vb 
 
pConnection->Execute("commandText", NULL, adCmdText); 
pCommand->Execute(NULL, NULL, adCmdText); 
pRecordset->NextRecordset(NULL); 
```

## <a name="error-handling"></a>エラー処理

COM では、ほとんどの操作は、関数が正常に完了したかどうかを示す HRESULT リターン コードを返します。 **\#インポート**ディレクティブは、各「生」のメソッドまたはプロパティをラッパー コードを生成し、返された HRESULT を確認します。 ラッパー コードが呼び出すことによって COM エラーをスローする HRESULT は、エラーを示している場合\_com\_問題\_の errorex() には、引数としてコードが返されます。 **実行してください**COM エラー オブジェクトをキャッチできます-**catch**ブロック。 (効率のためへの参照をキャッチ、 ** \_com\_エラー**オブジェクト)。

これらは ADO エラーであり、ADO 操作の失敗によって生成されます。基になるプロバイダーから返されるエラーは、 **Connection** オブジェクトの **Errors** コレクションに **Error** オブジェクトとして表示されます。

**\#インポート**ディレクティブによって作成のみエラー処理ルーチンでメソッドおよびプロパティは、ADO .dll で宣言されているのです。 ただし、自分でエラー確認マクロやインライン関数を記述すると、同じエラー処理機構を利用できます。 例については、「 [ADO 用の Visual C++ Extensions](visual-c-extensions-for-ado.md)」または、以下に説明するコードを参照してください。

## <a name="visual-c-equivalents-of-visual-basic-conventions"></a>Visual Basic の規則と同等の Visual C++ の規則

Visual Basic および、それと同等の Visual C++ でコーディングされた ADO ドキュメントにおけるいくつかの規則の概要を次に示します。

## <a name="declaring-an-ado-object"></a>ADO オブジェクトの宣言

Visual Basic では、ADO オブジェクト変数 (この場合は **Recordset** オブジェクトの変数) を次のように宣言します。

```vb 
 
Dim rst As ADODB.Recordset 
```

句は"ADODB。レコード セット"は、レジストリで定義されている**レコード セット**オブジェクトの ProgID です。 **Record** オブジェクトの新しいインスタンスは、次のように宣言します。

```vb 
 
Dim rst As New ADODB.Recordset 
```

\-または -

```vb 
 
Dim rst As ADODB.Recordset 
Set rst = New ADODB.Recordset 
```

Visual C++ で、**\#インポート**ディレクティブは、すべての ADO オブジェクトのスマート ポインターの型宣言を生成します。 ポイントする変数などの**\_レコード セット**型のオブジェクトは、 ** \_RecordsetPtr**が次のように宣言されているとします。

```cpp 
 
_RecordsetPtr rs; 
```

新しいインスタンスを指す変数、**\_レコード セット**オブジェクトは次のように宣言します。

```cpp 
 
_RecordsetPtr rs("ADODB.Recordset"); 
```

\-または -

```cpp 
 
_RecordsetPtr rs; 
rs.CreateInstance("ADODB.Recordset"); 
```

\-または -

```cpp 
 
_RecordsetPtr rs; 
rs.CreateInstance(__uuidof(_Recordset)); 
```

**CreateInstance** メソッドの呼び出し後に、この変数を次のように使用できます。

```cpp 
 
rs->Open(...); 
```

1 つのケースでいることを確認、"です。"演算子は、変数が (rs クラスのインスタンスであるかのように使用。CreateInstance) と別のケースで、"-\>"演算子は、変数がインターフェイスへのポインターであるかのように使用 (rs -\>オープン)。

2 つの方法の 1 つの変数を使用できます、"-\>"インターフェイスへのポインターのように動作するクラスのインスタンスを許可する演算子をオーバー ロードします。 インスタンス変数のプライベート クラス メンバーへのポインターを含む、**\_レコード セット**インタ フェースです。"-\>"演算子がそのポインターを返します。返されたポインターのメンバーにアクセスして、**\_レコード セット**オブジェクトです。

## <a name="coding-a-missing-parameter"></a>省略可能なパラメーターのコーディング: バリアント型 (Variant)

Visual Basic で省略可能な文字列型 ( **String** ) のオペランドをコーディングする場合は、単純にそのオペランドを省略します。 Visual C++ では、そのオペランドを指定する必要があります。 コードは**\_bstr\_t**の値として空の文字列を持ちます。

```cpp 
 
_bstr_t strMissing(L""); 
```

## <a name="coding-a-missing-parameter"></a>省略可能なパラメーターのコーディング: バリアント型 (Variant)

Visual Basic で省略可能なバリアント型 ( **Variant** ) のオペランドをコーディングする場合は、単純にそのオペランドを省略します。 Visual C++ では、そのオペランドを指定する必要があります。 コードで不足している**バリアント型**パラメーター、**\_バリアント\_t**変位、特別な値に設定\_E\_PARAMNOTFOUND、および、型の VT\_エラーです。 **VtMissing**同等であるの代わりに、指定によって定義済みの定数が指定された、**\#インポート**ディレクティブです。

```cpp 
 
_variant_t vtMissingYours(DISP_E_PARAMNOTFOUND, VT_ERROR); 
```

\-またはを使用して-

```cpp 
 
...vtMissing...; 
```

## <a name="declaring-a-variant"></a>バリアント型 (Variant) の宣言

Visual Basic では、バリアント型 ( **Variant** ) は次のように **Dim** ステートメントで宣言します。

```vb 
 
Dim VariableName As Variant 
```

Visual C++ の型として変数を宣言**\_バリアント\_t**。 いくつかの回路図**\_バリアント\_t**の宣言を以下に示します。


> [!NOTE]
> <P>[!メモ] これらの宣言では、プログラムでコーディングする内容の概要のみを示しています。詳細については、後の例や Visual C++ のドキュメントを参照してください。</P>



```cpp 
 
_variant_t VariableName(value); 
_variant_t VariableName((data type cast) value); 
_variant_t VariableName(value, VT_DATATYPE); 
_variant_t VariableName(interface * value, bool fAddRef = true); 
```

## <a name="using-arrays-of-variants"></a>バリアント型 (Variant) の配列の使用

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

Visual C++ の例を次に使用される**SafeArray**を使用する、**\_バリアント\_t**。


> [!NOTE]
> <P>[!メモ] 次の注意事項は、コード例のコメント部分に対応しています。</P>



1.  既存のエラー処理機構を利用するために、もう一度、TESTHR() インライン関数を定義します。

2.  必要なのは 1 次元配列のみであるため、汎用の **SAFEARRAYBOUND** 宣言と **SafeArrayCreate** 関数の代わりに **SafeArrayCreateVector** 関数を使用できます。次に、 **SafeArrayCreate** を使用した場合のコードを示します。
    
    ```cpp 
     
     SAFEARRAYBOUND sabound[1]; 
     sabound[0].lLbound = 0; 
     sabound[0].cElements = 4; 
     pSa = SafeArrayCreate(VT_VARIANT, 1, sabound); 
    ```

3.  列挙定数**adSchemaColumns**、によって識別されるスキーマは、次の 4 つの制約列に関連付けられている: テーブル\_カタログ、テーブル\_スキーマ、テーブル\_名、および列\_名です。 したがって、4 つの要素を持つバリアント型 ( **Variant** ) の値の配列が作成されます。 3 番目の列では、テーブルに対応する制約値にし、\_の名前が指定されています。 返される **Recordset** はいくつかの列で構成され、そのサブセットは制約列です。 返される各行に対する制約列の値は、対応する制約値と同じである必要があります。

4.  ご存知の**Safearray**を見て驚かれるかもしれません**SafeArrayDestroy**() が終了する前に呼び出されません。 実際、 **SafeArrayDestroy**() を呼び出してここで例外が発生実行時。 理由は、vtCriteria のデストラクターが**VariantClear**() を呼び出すことと、**\_バリアント\_t** **SafeArray**を開放するには、スコープ外に出る。 **SafeArrayDestroy**を呼び出すことを手動でオフにすることがなく、**\_バリアント\_t**、デストラクターが無効な**SafeArray**ポインターをオフにしようとしていますが発生します。 **SafeArrayDestroy** を呼び出した場合、コードは次のようになります。
    
    ```cpp 
     
     TESTHR(SafeArrayDestroy(pSa)); 
     vtCriteria.vt = VT_EMPTY; 
     vtCriteria.parray = NULL; 
    ```
    
    ただし、ことができるようにした方が簡単、**\_バリアント\_t** **SafeArray**を管理します。

<!-- end list -->

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

## <a name="using-property-getputputref"></a>Get/Put/PutRef プロパティの使用

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

この Visual C++ の例は、**取得**/**に**/**PutRef。 プロパティ*。


> [!NOTE]
> [!メモ] 次の注意事項は、コード例のコメント部分に対応しています。



1.  不足している文字列の引数の 2 つのフォームを使用して、次の使用例: 明示的な定数**strMissing**と一時領域を作成するコンパイラを使用する文字列**\_bstr\_t**の**Open**メソッドのスコープが存在します。

2.  Rs のオペランドをキャストする必要はありません\>に PutRefActiveConnection(cn) (IDispatch \*) のオペランドの型が既にあるため (IDispatch \*)。
    
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

## <a name="using-getitemx-and-itemx"></a>GetItem(x) とアイテムを使用して\[x\]

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

この Visual C++ の例は、 **Item** を示します。


> [!NOTE]
> <P>[!メモ] 次の注意事項は、コード例のコメント部分に対応しています。</P>



1.  コレクションに **Item** を使用してアクセスした場合、適切なコンストラクターが呼び出されるように、インデックス **2** が **long** にキャストされる必要があります。
    
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

## <a name="casting-ado-object-pointers-with-idispatch-"></a>(IDispatch \*) による ADO オブジェクト ポインターのキャスト

次の Visual C++ の例では、(IDispatch \*) を使用した ADO オブジェクト ポイントのキャストを示します。


> [!NOTE]
> <P>[!メモ] 次の注意事項は、コード例のコメント部分に対応しています。</P>



1.  明示的にコーディングされたバリアント型 ( **Variant** ) で、開いている **Connection** オブジェクトを指定します。 キャスト (IDispatch \*)、適切なコンス トラクターが呼び出されるようにします。 また、2 番目を明示的に設定**\_バリアント\_t**パラメーター、既定値**は true**、 **Recordset::Open**操作が終了したときに、オブジェクトの参照カウントが正しくありますので。

2.  式 (\_bstr\_t)、キャストではありませんが、**\_バリアント\_t**を抽出するための演算子、 ** \_bstr\_t** **値**によって返される**バリアント型**の文字列。 式 (char\*)、キャストではありませんが、 ** \_bstr\_t**にカプセル化された文字列へのポインターを抽出するための演算子、 ** \_bstr\_t**オブジェクト。 コードのこのセクションでは、いくつかの便利な動作を示します**\_バリアント\_t**と**\_bstr\_t**演算子です。
    
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

