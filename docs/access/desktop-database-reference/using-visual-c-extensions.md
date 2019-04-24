---
title: Visual C++ Extensions を使用する
TOCTitle: Using Visual C++ Extensions
ms:assetid: 0fb1014c-7ab6-6add-d09f-e5e48b2b32cb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248866(v=office.15)
ms:contentKeyID: 48543270
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8bf2234e5935c2a1a13871e7e45c980fb9f33109
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32312062"
---
# <a name="using-visual-c-extensions"></a>Visual C++ Extensions の使用


**適用先:** Access 2013、Office 2013

## <a name="the-iadorecordbinding-interface"></a>IADORecordBinding インターフェイス

ADO 用 Microsoft Visual C++ Extensions は、[Recordset](recordset-object-ado.md) オブジェクトのフィールドを C/C++ の変数に関連付け (つまりバインドし) ます。バインドされた **Recordset** の現在の行が変更されると、 **Recordset** 内のバインドされたすべてのフィールドが C/C++ 変数にコピーされます。コピーされるデータは、必要に応じて、C/C++ 変数の宣言データ型に変換されます。

**IADORecordBinding** インターフェイスの **BindToRecordset** メソッドは、フィールドを C/C++ の変数にバインドします。 **AddNew** メソッドは、バインドされた **Recordset** に新しい行を追加します。 **Update** メソッドは、C/C++ 変数の値で、 **Recordset** の新しい行のフィールドを設定したり、既存の行のフィールドを更新したりします。

**IADORecordBinding** インターフェイスは、 **Recordset** オブジェクトによって実装されます。ユーザー自身が実装をコーディングする必要はありません。

## <a name="binding-entries"></a>バインディング エントリ

The Visual C++ Extensions for ADO map fields of a [Recordset](recordset-object-ado.md) object to C/C++ variables. フィールドと変数の間のマッピングの定義を*バインドエントリ*と呼びます。 Macros provide binding entries for numeric, fixed-length, and variable-length data. The binding entries and C/C++ variables are declared in a class derived from the Visual C++ Extensions class, **CADORecordBinding**. The **CADORecordBinding** class is defined internally by the binding entry macros.

ADO internally maps the parameters in these macros to an OLE DB **DBBINDING** structure and creates an OLE DB **Accessor** object to manage the movement and conversion of data between fields and variables. OLE DB は、データが格納される*バッファー*の3つの部分で構成されるデータを定義します。フィールドがバッファーに正常に格納されたかどうか、または変数をフィールドに復元する方法を示す*状態*。データの*長さ*。 (詳細については、「 *OLE DB プログラマリファレンス*」、「6章: データの取得と設定」を参照してください)。

## <a name="header-file"></a>ヘッダー ファイル

ADO 用 Visual C++ Extensions を使用するには、アプリケーションに次のファイルをインクルードします。

```cpp 
 
#include <icrsint.h> 
```

## <a name="binding-recordset-fields"></a>Recordset のフィールドのバインド

**Recordset のフィールドを C/C++ の変数にバインドするには**

1.  **CADORecordBinding** クラスから派生するクラスを作成します。

2.  バインディング エントリおよび対応する C/C++ 変数を派生クラスで指定します。 ado バインドマクロと**\_END ado\_バインド**マクロの間のバインドエントリをブラケットにします。 **\_\_** マクロの末尾にコンマまたはセミコロンを使用しないでください。 適切な区切り文字がマクロによって自動的に指定されます。 C/C++ 変数にマップするフィールドごとに、バインディング エントリを 1 つ指定します。 **ado\_\_の固定長\_エントリ**、ado **\_の数値\_** エントリ、または ado **\_\_の可変長\_エントリ**ファミリのマクロの適切なメンバーを使用します。

3.  アプリケーションで、 **CADORecordBinding** から派生したクラスのインスタンスを作成します。 **Recordset** から **IADORecordBinding** インターフェイスを取得します。その後、 **BindToRecordset** メソッドを呼び出して、 **Recordset** のフィールドを C/C++ 変数にバインドします。

詳細については、「[Visual C++ Extensions の例](visual-c-extensions-example.md)」を参照してください。

## <a name="interface-methods"></a>インターフェイスのメソッド

**IADORecordBinding** インターフェイスには、3 つのメソッド **BindToRecordset** 、 **AddNew** 、および **Update** があります。各メソッドに対する唯一の引数は、 **CADORecordBinding** から派生したクラスのインスタンスへのポインターです。したがって、 **AddNew** メソッドおよび **Update** メソッドでは、同名の ADO メソッドのパラメーターは指定できません。

**構文**

**BindToRecordset** メソッドは、 **Recordset** のフィールドを C/C++ の変数に関連付けます。

`BindToRecordset(CADORecordBinding *binding)` 

**AddNew** メソッドは、ADO の同名の [AddNew](addnew-method-ado.md) メソッドを呼び出して、 **Recordset** に新しい行を追加します。

`AddNew(CADORecordBinding *binding)` 

**Update** メソッドは、ADO の同名の [Update](update-method-ado.md) メソッドを呼び出して、**Recordset** を更新します。

`Update(CADORecordBinding *binding)` 

## <a name="binding-entry-macros"></a>バインディング エントリ マクロ

バインディング エントリ マクロは、 **Recordset** のフィールドと変数の関連付けを定義します。開始および終了のマクロで、バインディング エントリのセットを区切ります。

**adDate** や **adBoolean** などの固定長データ、 **adTinyInt** 、 **adInteger** 、 **adDouble** などの数値データ、および **adChar** 、 **adVarChar** 、 **adVarBinary** などの可変長データに対し、マクロ ファミリが用意されています。 **adVarNumeric** を除くすべての数値型は、固定長型でもあります。各マクロ ファミリは、それぞれ異なるパラメーター セットを持っているので、必要のないバインディング情報を除外できます。

追加情報については、「OLE DB プログラマ リファレンス」の「付録 A データ型」を参照してください。

_**バインドエントリの開始**_

**\_ADO\_バインドの開始**(*クラス*)

_**固定長のデータ**_

**ADO\_の\_固定\_長のエントリ**(*序数、データ型、バッファー、状態、変更*)  
**ADO\_固定\_長\_ENTRY2**(*序数、データ型、バッファー、変更*)

_**数値データ**_

**ADO\_の\_数値エントリ**(*序数、データ型、バッファー、精度、規模、状態、変更*)  
**ADO\_の\_数値 ENTRY2**(*序数、データ型、バッファー、精度、小数点以下の桁数、変更*)

_**可変長データ**_

**ADO\_の\_可変長\_エントリ**(*序数、データ型、バッファー、サイズ、状態、長さ、変更*)  
**ADO\_の\_可変長\_ENTRY2**(*序数、データ型、バッファー、サイズ、状態、変更*)  
**ADO\_\_可変長\_ENTRY3**(*序数、データ型、バッファー、サイズ、長さ、変更*)  
**ADO\_\_可変長\_ENTRY4**(*序数、データ型、バッファー、サイズ、変更*)

_**バインディングエントリの終了**_

**\_ADO\_バインドを終了**する()

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>パラメーター</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Class</em></p></td>
<td><p>バインディング エントリおよび C/C++ 変数を定義するクラスです。</p></td>
</tr>
<tr class="even">
<td><p><em>Ordinal</em></p></td>
<td><p>C/C++ 変数に対応する <strong>Recordset</strong> フィールドの、1 から始まるインデックスです。</p></td>
</tr>
<tr class="odd">
<td><p><em>DataType</em></p></td>
<td><p>C/C++ 変数に対する ADO での等価のデータ型です (有効なデータ型の一覧については、<a href="datatypeenum.md">DataTypeEnum</a> のトピックを参照)。<strong>Recordset</strong> フィールドの値は、必要に応じてこのデータ型に変換されます。</p></td>
</tr>
<tr class="even">
<td><p><em>Buffer</em></p></td>
<td><p><strong>Recordset</strong> フィールドを格納する C/C++ 変数の名前です。</p></td>
</tr>
<tr class="odd">
<td><p><em>Size</em></p></td>
<td><p>バイト数で示す <em>Buffer</em> の最大サイズです。 <em>Buffer</em> に可変長文字列を格納する場合は、末尾のゼロを含んだサイズになります。</p></td>
</tr>
<tr class="even">
<td><p><em>状態</em></p></td>
<td><p><em>Buffer</em> の内容が有効かどうか、および <em>DataType</em> へのフィールドの変換が成功したかどうかを示す変数の名前です。 この変数で最も重要な 2 つの値は、変換が成功したことを示す <strong>adFldOK</strong> と、フィールドの値が VT_NULL 型の VARIANT であって単なる空ではないことを示す <strong>adFldNull</strong> です。 <em>status</em>に指定できる値は、 &quot;次の表の状態値で示されます。&quot;</p></td>
</tr>
<tr class="odd">
<td><p><em>Modify</em></p></td>
<td><p>ブール型のフラグです。TRUE の場合は、ADO が対応する <strong>Recordset</strong> フィールドを <em>Buffer</em> の値で更新できることを示します。
 バインドされたフィールドを ADO が更新できるようにするには、ブール型の <em>modify</em> パラメーターを TRUE に設定します。確認だけでフィールドを変更しない場合は FALSE に設定します。</p></td>
</tr>
<tr class="even">
<td><p><em>精度</em></p></td>
<td><p>数値変数で表すことのできる桁数です。</p></td>
</tr>
<tr class="odd">
<td><p><em>Scale</em></p></td>
<td><p>数値変数での小数点以下の桁数です。</p></td>
</tr>
<tr class="even">
<td><p><em>Length</em></p></td>
<td><p><em>Buffer</em> 内のデータの実際の長さを格納する 4 バイト変数の名前です。</p></td>
</tr>
</tbody>
</table>


## <a name="status-values"></a>Status の値

*Status* 変数の値は、フィールドが変数に正常にコピーされたかどうかを示します。

データを設定するときは、*Status* を **adFldNull** に設定することで、**Recordset** フィールドを Null に設定する必要があることを示すことができます。

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>定数</p></th>
<th><p>値</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adfldok</strong></p></td>
<td><p>.0</p></td>
<td><p>Null ではないフィールド値が返されました。</p></td>
</tr>
<tr class="even">
<td><p><strong>adfldbadaccessor</strong></p></td>
<td><p>1-d</p></td>
<td><p>バインディングが無効です。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adfldcantconvertvalue</strong></p></td>
<td><p>pbm-2</p></td>
<td><p>符号の不一致またはデータのオーバーフロー以外の理由で、値を変換できませんでした。</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldNull</strong></p></td>
<td><p>1/3</p></td>
<td><p>フィールドを取得するときは、Null 値が返されたことを示します。 フィールドを設定するときは、フィールドが <strong>NULL</strong> そのものをエンコードできない場合 (文字配列または整数など)、フィールドを <strong>NULL</strong> に設定する必要があることを示します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adfldtruncated</strong></p></td>
<td><p>2/4</p></td>
<td><p>可変長データまたは数値の桁が切り捨てられました。</p></td>
</tr>
<tr class="even">
<td><p><strong>adfldsignmismatch</strong></p></td>
<td><p>5</p></td>
<td><p>値は符号付きですが、変数のデータ型は符号なしです。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adflddataoverflow</strong></p></td>
<td><p>シックス</p></td>
<td><p>変数のデータ型に格納できる値を超えています。</p></td>
</tr>
<tr class="even">
<td><p><strong>adfldcantcreate</strong></p></td>
<td><p>7</p></td>
<td><p>未知の列の型であり、フィールドは既に開かれています。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adfldunavailable 不可</strong></p></td>
<td><p>~</p></td>
<td><p>フィールド値を特定できませんでした。たとえば、新規の未割り当てフィールドで既定値が設定されていません。</p></td>
</tr>
<tr class="even">
<td><p><strong>adfldpermissiondenied</strong></p></td>
<td><p>i-9</p></td>
<td><p>更新時に、データの書き込み権限が与えられていませんでした。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldIntegrityViolation</strong></p></td>
<td><p>個</p></td>
<td><p>更新時に、フィールド値が列の整合性に違反していました。</p></td>
</tr>
<tr class="even">
<td><p><strong>adfldschemaviolation</strong></p></td>
<td><p>#</p></td>
<td><p>更新時に、フィールド値が列のスキーマに違反していました。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adfldbadadstatus</strong></p></td>
<td><p>個</p></td>
<td><p>更新時に、無効なステータス パラメーターがありました。</p></td>
</tr>
<tr class="even">
<td><p><strong>adflddefault</strong></p></td>
<td><p>スリー</p></td>
<td><p>更新時に、既定値が使用されました。</p></td>
</tr>
</tbody>
</table>

