---
title: レコードセットを使用する
TOCTitle: Working with Recordsets
ms:assetid: 9cd52866-2738-8150-381c-eee0b8a6cd36
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249711(v=office.15)
ms:contentKeyID: 48546608
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0d4b877b680c80a10067e19065facd4ce9e4819d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32305974"
---
# <a name="working-with-recordsets"></a>レコードセットの利用

**適用先:** Access 2013、Office 2013 

**Recordset** オブジェクトには、結果セット内のデータ順序の並べ替え、指定した基準に基づく特定のレコードの検索、さらにインデックスを使用した検索操作の最適化を実行できる機能が組み込まれています。これらの機能を使用できるかどうかは、プロバイダーによって異なり、 [Index](index-property-ado.md) プロパティなどの場合には、データ ソース自体の構造によっても異なります。

## <a name="arranging-data"></a>データの配置

通常、 **Recordset** 内のデータを最も効率的に並べ替えるには、SQL コマンドで ORDER BY 句を指定して結果が返されるようにします。ただし、場合によっては、既に作成した **Recordset** のデータ順序を変更する必要があります。 **Sort** プロパティを使用すると、 **Recordset** の行をスキャンする順序を指定できます。さらに、 **Filter** プロパティを使用して、行のスキャン中にアクセスできる行を指定することもできます。

**Sort** プロパティは、並べ替える **Recordset** のフィールド名を示す **String** 値を設定または返します。それぞれの名前はコンマで区切ります。名前の後には、スペース、およびキーワードとしてフィールドを昇順で並べ替える **ASC** または降順で並べ替える **DESC** を指定することもできます。既定では、キーワードを指定しない場合、フィールドは昇順で並べ替えられます。

データは物理的に並べ替えられるわけではなく、インデックスで指定された順序でアクセスされるだけなので、並べ替え操作は効率的に行われます。

**Sort** プロパティでは、 [CursorLocation](cursorlocation-property-ado.md) プロパティを **adUseClient** に設定する必要があります。インデックスがない場合、 **Sort** プロパティに指定されたフィールドごとに一時インデックスが作成されます。

**Sort** プロパティを空の文字列に設定すると、行は元の順序にリセットされ、一時インデックスが削除されます。既存のインデックスは削除されません。

**Recordset** に、*firstName* (名)、*middleInitial* (ミドルネームのイニシャル)、および *lastName* (姓) という名前の 3 つのフィールドがあるとします。 並べ替えプロパティを文字列 "" に設定します。これにより、**レコードセット**は姓で降順に並べ替えられ、次に名によって昇順で**並べ替え**られます。 ミドル ネームは無視されます。

並べ替え条件で参照するフィールド名に "ASC" または "DESC" を使用することはできません。これは、キーワード **ASC** および **DESC** と競合するためです。 **Recordset** を返すクエリで **AS** キーワードを使用して、競合する名前のフィールドにエイリアスを指定してください。

**Recordset** のフィルターの詳細については、「結果のフィルター処理」を参照してください。

## <a name="finding-a-specific-record"></a>特定のレコードを検索する

ADO には、 [Recordset](find-method-ado.md) 内の特定のレコードを検索するための [Find](seek-method-ado.md) メソッドと **Seek** メソッドがあります。 **Find** メソッドはさまざまなプロバイダーでサポートされていますが、検索基準は 1 つしか設定できません。 **Seek** メソッドでは複数の検索基準を設定できますが、サポートするプロバイダーが限られます。

フィールドのインデックスを使用すると、 **Recordset** オブジェクトの **Find** メソッド、 **Sort** プロパティ、および **Filter** プロパティのパフォーマンスを大幅に向上できます。 **Field** オブジェクトの内部インデックスを作成するには、動的な [Optimize](optimize-property-dynamic-ado.md) プロパティを設定します。この動的プロパティは、 **CursorLocation** プロパティを **adUseClient** に設定したときに、 [Field](cursorlocation-property-ado.md) オブジェクトの **Properties** コレクションに追加されます。ただし、このインデックスは ADO 内部でのみ使用でき、外部からアクセスしたり、他の目的で使用することはできません。また、このインデックスは、 **Recordset** オブジェクトの [Index](index-property-ado.md) プロパティとは異なります。

**Find** メソッドは、 **Recordset** の列 (フィールド) 内をすばやく検索します。 **Optimize** プロパティを使用して列のインデックスを作成すると、通常は **Find** メソッドの動作の速度が向上します。

**Find** メソッドでは、1 つのフィールドの内容しか検索できません。 **Seek** メソッドではインデックスが必要であり、その他の制限もあります。インデックスのベースではない複数のフィールドを検索する必要がある場合、またはプロバイダーがインデックスをサポートしていない場合は、 **Recordset** オブジェクトの **Filter** プロパティを使用して結果を絞り込む必要があります。

### <a name="find"></a>Find

**Find** メソッドでは、指定した条件を満たす行の **Recordset** を検索します。必要に応じて、検索の方向、開始行、および開始行からのオフセットを指定できます。条件が一致すると、カレント行の位置は、検出されたレコードに設定されます。条件を満たす行がない場合、カレント行の位置は、検索する方向によって、**Recordset** の最後または最初に設定されます。

基準に指定できるのは、単一列の名前のみです。つまり、このメソッドでは複数列の検索はサポートしていません。

条件の比較演算子に**\>** は、"" (より大きい)、"**\<**" (より小さい)、"=" (等しい)、"\>=" (より大きいまたは等しい)、"\<=" (以下)\<\>、"" (等しくない)、または "LIKE" (パターンマッチング) のいずれかを指定できます。

抽出条件の値には、文字列、浮動小数点数、または日付を指定できます。 文字列型 (String) の値は、\#一重引用符または "" (シャープ記号) マークで区切られます (たとえば、"state = \#'\#WA '" または "state = WA")。 日付の値は、"\#" (シャープ記号) マークで区切られます (たとえば\_、 \> \#"\#start date 7/22/97")。

比較演算子に "like" を使用する場合、文字列の値にアスタリスク (\*) を含めると、1 つまたは複数の文字または部分文字列を検索できます。たとえば、「state like 'M\*'」と指定すると、Maine や Massachusetts が検索されます。文字列の先頭と末尾にアスタリスクを使用して、その値に含まれる部分文字列を検索することもできます。たとえば、「state like '\*as\*'」と指定すると、Alaska、Arkansas、および Massachusetts が検索されます。

前の例のように、アスタリスクを使用できるのは、基準文字列の末尾、または検索文字列の先頭と末尾の両方の場合のみです。先頭のワイルドカード ('\*str') または文字列中のワイルドカード ('s\*r') としてアスタリスクを使用することはできません。この場合、エラーが発生します。

### <a name="seek-and-index"></a>Seek および Index

基になるプロバイダーが **Recordset** オブジェクトのインデックスをサポートしている場合、**Index** プロパティと共に **Seek** メソッドを使用します。基になるプロバイダーが **Seek** をサポートしているかどうかを判別するには、[Supports](supports-method-ado.md)**(adSeek)** メソッドを使用します。プロバイダーがインデックスをサポートしているかどうかを判別するには、**Supports(adIndex)** メソッドを使用します。たとえば、[OLE DB Provider for Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md) は **Seek** および **Index** をサポートしています。

**Seek** メソッドで目的の行が見つからない場合、エラーは発生せず、行は **Recordset** の末尾に配置されます。このメソッドを実行する前に、 **Index** プロパティを必要なインデックスに設定してください。

このメソッドは、サーバー側のカーソルでのみサポートされます。 **Recordset** オブジェクトの [CursorLocation](cursorlocation-property-ado.md) プロパティの値が **adUseClient** の場合、Seek はサポートされません。

このメソッドは、 **Recordset** オブジェクトが [adCmdTableDirect](commandtypeenum.md) の **CommandTypeEnum** 値で開かれている場合のみ使用できます。

## <a name="filtering-the-results"></a>結果のフィルター処理

**Find** メソッドでは、1 つのフィールドの内容しか検索できません。 **Seek** メソッドではインデックスが必要であり、その他の制限もあります。インデックスのベースではない複数のフィールドを検索する必要がある場合、またはプロバイダーがインデックスをサポートしていない場合は、 **Recordset** オブジェクトの **Filter** プロパティを使用して結果を絞り込む必要があります。

**Filter** プロパティを使用すると、 **Recordset** オブジェクト内の特定のレコードを抽出できます。フィルター処理後の **Recordset** は現在のカーソルになり、 **Filter** 基準を満たさないレコードは、 **Filter** が削除されるまで **Recordset** では使用できなくなります。 **AbsolutePosition** 、 **AbsolutePage** 、 **RecordCount** 、 **PageCount** など、現在のカーソルに基づいて値を返すその他のプロパティが影響を受けます。これは、 **Filter** プロパティを特定の値に設定すると、現在のレコードが新しい値を満たす最初のレコードに移動するためです。

**Filter** プロパティには、バリアント型の引数を指定します。この値は、 **Filter** プロパティを使用するための 3 つの方法、つまり検索条件文字列、 **FilterGroupEnum** 定数、ブックマークの配列のうちの 1 つを表します。詳細については、「検索条件文字列によるフィルター処理」、「定数によるフィルター処理」、および「ブックマークによるフィルター処理」を参照してください。

> [!NOTE]
> [!メモ] 選択するデータがわかっている場合は、 **Filter** プロパティを使用するのではなく、結果セットを効果的にフィルター処理する SQL ステートメントを使用して **Recordset** を開く方が効率的です。

**Recordset** からフィルターを削除するには、 **adFilterNone** 定数を使用します。 **Filter** プロパティを長さ 0 の文字列 ("") に設定すると、 **adFilterNone** 定数を使用した場合と同じ結果になります。

### <a name="filtering-with-a-criteria-string"></a>抽出条件文字列を使用してフィルターを適用する

criteria 文字列は、"フォーム*名" 演算子の値*(たとえば、"LastName = ' Smith '") 内の句で構成されます。 複合句を作成するには、and (たとえば、"LastName = ' Smith ' および FirstName = ' John '") と or (など) を使用して、個別の句を連結します。 複合句を作成するには、and (たとえば、"lastname = ' smith ' と FirstName = ' John '") や OR (たとえば、"lastname = ' smith ' OR LastName = ' Jones '") を使用して、個別の句を連結します。 検索条件文字列を指定する際は、次の点に注意してください。

- *FieldName* には、**Recordset** の有効なフィールド名を指定する必要があります。フィールド名にスペースを含める場合は、名前を角かっこで囲みます。

- *Operator* \<には、、 \>、 \<=、 \>=、 \< \>、=、または LIKE のいずれかを指定する必要があります。

- *value*は、フィールド値を比較する値 (たとえば、' Smith '、 \#8/24/95\#、12.345、$50.00) です。 文字列とシャープ記号 (\#) には、日付と共に単一引用符 (') を使用します。 数値の場合、小数点、ドル記号、および指数表記を使用できます。 *Operator* が LIKE の場合、*Value* にワイルドカードを使用できます。 アスタリスク (\*) とパーセント記号 (%) のみワイルドカードを使用でき、文字列内の最後の文字である必要があります。 *Value* に Null を指定することはできません。
    
  > [!NOTE]
  > フィルター *Value* に単一引用符 (') を含めるには、2 つの単一引用符を使用して 1 つの単一引用符を表します。 たとえば、 *O'Malley*にフィルターを適用するには、criteria 文字列を "col1 = ' O ' ' Malley '" にする必要があります。 
  > 
  > フィルター値の先頭と末尾の両方に単一引用符を使用するには、文字列をシャープ記号 (#) で囲みます。 たとえば、 *' 1 '* にフィルターを適用するには、criteria 文字列を "col1 = # ' 1 ' #" にする必要があります。

AND と OR には優先順位はありません。かっこを使用して句をグループ化できます。ただし、次のように OR で結合したグループ句を、AND を使用してさらに別の句に結合することはできません。

```vb 
 
(LastName = 'Smith' OR LastName = 'Jones') AND FirstName = 'John' 
```

この場合は、このフィルターを次のように構成します。

```vb 
 
(LastName = 'Smith' AND FirstName = 'John') OR (LastName = 'Jones' AND FirstName = 'John') 
```

LIKE 句では、パターンの先頭と末尾 (たとえば、lastname など\*\*) でワイルドカードを使用できます。または、パターンの最後 (たとえば、lastname like ' Smit\*') だけでワイルドカードを使用することができます (例:)。

### <a name="filtering-with-a-constant"></a>定数を使用してフィルターを適用する

**Recordsets** のフィルター処理では、次の定数を使用できます。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>定数</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adFilterAffectedRecords</strong></p></td>
<td><p><strong>Delete</strong>、<strong>Resync</strong>、<strong>UpdateBatch</strong>、または <strong>CancelBatch</strong> の最後の呼び出しによって影響を受けたレコードのみを表示するようにフィルター処理します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adFilterConflictingRecords</strong></p></td>
<td><p>最後のバッチ更新が失敗したレコードを表示するようにフィルター処理します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adfilterfetchedrecords</strong></p></td>
<td><p>現在のキャッシュ内のレコード、つまりデータベースからレコードを取得するための最後の呼び出しの結果を表示するようにフィルター処理します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adFilterNone</strong></p></td>
<td><p>現在のフィルターを削除し、すべてのレコードを復元して表示します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adfilterpendingrecords</strong></p></td>
<td><p>変更が行われたが、変更内容がサーバーにまだ送信されていないレコードのみを表示するようにフィルター処理します。 バッチ更新モードの場合のみ使用できます。</p></td>
</tr>
</tbody>
</table>

<br/>

フィルター定数を使用すると、バッチ更新モードでレコードに競合が発生した場合、**UpdateBatch** メソッドの最後の呼び出しで影響を受けたレコードのみを表示するなどの方法で、競合を簡単に解決できます。次に例を示します。

```vb 
 
'BeginDeleteGroup 
    'add some bogus records 
    With objRs1 
        For i = 0 To 8 
            .AddNew 
            .Fields("CompanyName") = "Shipper Number " & i + 1 
            .Fields("Phone") = "(425) 555-000" & (i + 1) 
            .Update 
        Next i 
         
    're-connect & update 
        .ActiveConnection = GetNewConnection 
        .UpdateBatch 
         
    'filter on newly added records 
        .Filter = adFilterAffectedRecords 
        Debug.Print "Deleting the " & .RecordCount & _ 
                    " records you just added." 
         
    'delete the newly added bogus records 
        .Delete adAffectGroup 
        .Filter = adFilterNone 
        Debug.Print .RecordCount & " records remain." 
         
        .Close 
    End With 
'EndDeleteGroup 
```

### <a name="filtering-with-bookmarks"></a>ブックマークを使用したフィルター処理

最後に、バリアント型のブックマークの配列を **Filter** プロパティに渡すことができます。結果カーソルに含まれるのは、ブックマークがプロパティに渡されたレコードのみです。次のコード例では、**Recordset** 内の *ProductName* フィールドに "B" が含まれるレコードからブックマークの配列が作成されます。次に、配列を **Filter** プロパティに渡し、フィルター処理された **Recordset** に関する情報を表示します。

```vb 
 
'BeginFilterBkmk 
    Dim vBkmkArray() As Variant 
    Dim i As Integer 
 
    'Recordset created using "SELECT * FROM Products" as command. 
    'So, we will check to see if ProductName has a capital B, and 
    'if so, add to the array. 
    i = 0 
    Do While Not objRs.EOF 
        If InStr(1, objRs("ProductName"), "B") Then 
            ReDim Preserve vBkmkArray(i) 
            vBkmkArray(i) = objRs.Bookmark 
            i = i + 1 
            Debug.Print objRs("ProductName") 
        End If 
        objRs.MoveNext 
    Loop 
     
    'Filter using the array of bookmarks. 
    objRs.Filter = vBkmkArray 
     
    objRs.MoveFirst 
    Do While Not objRs.EOF 
        Debug.Print objRs("ProductName") 
        objRs.MoveNext 
    Loop 
    'EndFilterBkmk 
```

## <a name="creating-a-clone-of-a-recordset"></a>Recordset の複製の作成

複数の **Recordset** オブジェクトの複製を作成するには、 **Clone** メソッドを使用します。特に、特定のレコードセット内の現在のレコードを複数保持する場合に、このメソッドを使用します。 **Clone** メソッドを使用すると、同じ定義を使用して新規の **Recordset** オブジェクトを作成して開くよりも効率的です。

The current record of a newly created clone is originally set to the first record. The current record pointer in a cloned **Recordset** is not synchronized with the original or vice versa. You can navigate independently in each **Recordset**.

1 つの **Recordset** オブジェクトに加えた変更は、カーソルの種類に関係なく、すべての複製で表示できます。ただし、複製元の [Recordset](requery-method-ado.md) で **Requery** を実行した後は、複製は複製元の Recordset とは同期しなくなります。

複製元の **Recordset** を閉じても、そのコピーは開いたままです。また、コピーを閉じても、複製元またはその他のコピーは開いたままです。

**Recordset** オブジェクトがブックマークをサポートする場合のみ、オブジェクトの複製を作成できます。ブックマークの値は共通です。つまり、1 つの **Recordset** オブジェクトのブックマークで、すべての複製の同じレコードを参照できます。

