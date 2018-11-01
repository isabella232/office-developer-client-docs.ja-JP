---
title: Fields コレクション
TOCTitle: The Fields Collection
ms:assetid: 3bda8e5d-eceb-9605-c4d7-c1f4cc00ce6b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249154(v=office.15)
ms:contentKeyID: 48544297
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 67f16c9c4dd27fdbd57a2c082580ead0606298e9
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874875"
---
# <a name="the-fields-collection"></a>Fields コレクション


**適用されます**Access 2013、Office 2013。

**Fields** コレクションは、ADO に組み込まれたコレクションの 1 つです。コレクションは、並べ替えられた項目のセットで、単位と呼ばれることもあります。

**Fields** コレクションには、 **Recordset** 内の各フィールド (列) に対応する **Field** オブジェクトが含まれています。すべての ADO コレクションと同様に、 **Append** メソッドおよび **Refresh** メソッド以外に、 **Count** プロパティおよび **Item** プロパティも使用できます。他の ADO コレクションでは使用できない、 **CancelUpdate** 、 **Delete** 、 **Resync** 、および **Update** の各メソッドも使用できます。

## <a name="examining-the-fields-collection"></a>Fields コレクションを検査する

この章で説明したサンプル **Recordset** の **Fields** コレクションについて考えてみましょう。サンプル **Recordset** は、SQL ステートメントから導出されました。

```sql 
 
SELECT ProductID, ProductName, UnitPrice FROM Products WHERE CategoryID = 7 
```

このように、 **Recordset** **Fields** コレクションには、3 つのフィールドが含まれています。

```vb 
 
'BeginWalkFields 
 Dim objFields As ADODB.Fields 
 
 objRs.Open strSQL, strConnStr, adOpenForwardOnly, adLockReadOnly, adCmdText 
 
 Set objFields = objRs.Fields 
 
 For intLoop = 0 To (objFields.Count - 1) 
 Debug.Print objFields.Item(intLoop).Name 
 Next 
'EndWalkFields 
```

このコードでは、単に **Count** プロパティを使用して **Fields** コレクション内の **Field** オブジェクトの数を調べ、コレクション内をループし、 **Field** オブジェクトごとに **Name** プロパティの値を返します。さらに多くの **Field** プロパティを使用すると、フィールドに関する情報を取得できます。 **Field** の照会の詳細については、「 [Field オブジェクト](the-field-object.md)」を参照してください。

## <a name="counting-columns"></a>列をカウントする

**Count** プロパティは、名前のとおり、 **Fields** コレクション内にある **Field** オブジェクトの実際の数を返します。コレクションのメンバーの番号はゼロから始まるため、常にゼロ番のメンバーからループを開始し、 **Count** プロパティの値から 1 を引いた値で終了するようにコードを記述する必要があります。Microsoft Visual Basic を使用して、 **Count** プロパティをチェックせずにコレクションのメンバーをループする場合は、 **For** **Each...Next** コマンドを使用します。

**Count** プロパティがゼロの場合、コレクション内にはオブジェクトはありません。

## <a name="getting-to-the-field"></a>Field にアクセスする

ADO コレクションと同様に、 **Item** プロパティはコレクションの既定のプロパティです。このプロパティは、渡された名前またはインデックスで指定された個別の **Field** オブジェクトを返します。したがって、次のステートメントは、サンプル **Recordset** と同じになります。

```vb 
 
objField = objRecordset.Fields.Item("ProductID") 
objField = objRecordset.Fields("ProductID") 
objField = objRecordset.Fields.Item(0) 
objField = objRecordset.Fields(0) 
```

これらのメソッドが同等の場合、どのメソッドが最適でしょうか。それは、時と場合によります。インデックスを使用してコレクションから **Field** を取得する方が、文字列検索を実行しなくても **Field** に直接アクセスできるため、高速です。一方、コレクション内の **Fields** の順序を把握しておく必要があり、順序が変わった場合、常に **Field** のインデックスへの参照を変更する必要があります。若干遅くなりますが、 **Field** の名前を使用する方が、コレクション内の **Fields** の順序に依存しないため、柔軟性があります。

## <a name="using-the-refresh-method"></a>Refresh メソッドを使用する

他のいくつかの ADO コレクションと異なり、 **Fields** コレクションで **Refresh** メソッドを使用しても目に見える効果はありません。基になるデータベース構造から変更を取得するには、 **Requery** メソッドを使用するか、 **Recordset** オブジェクトがブックマークをサポートしていない場合は、 **MoveFirst** メソッドを使用する必要があります。このメソッドにより、コマンドがプロバイダーに対して再実行されます。

## <a name="adding-fields-to-a-recordset"></a>Recordset にフィールドを追加する

**Append** メソッドは、 **Recordset** にフィールドを追加するために使用されます。

**Append** メソッドを使用すると、データ ソースへの接続を開かなくても、 **Recordset** をプログラムによって製造できます。開いている **Recordset** 、または **ActiveConnection** プロパティが設定されている **Recordset** の **Fields** コレクションで **Append** メソッドを呼び出すと、実行時エラーが発生します。フィールドを追加できるのは、開いていない状態で、データ ソースにも接続されていない **Recordset** のみです。ただし、新しく追加された **Fields** に値を指定するには、 **Recordset** をまず開く必要があります。

開発者は、データを一時的に保存する場所を必要とすることや、データをサーバーから発生したかのように処理して、ユーザー インターフェイスのデータ バインドに参加できるようにすることがあります。ADO と [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) を組み合わせて使用すると、開発者は、列情報を指定して **Open** を呼び出すことにより、空の **Recordset** オブジェクトを作成できます。次の例では、新しい **Recordset** オブジェクトに 3 つの新規フィールドが追加されます。次に **Recordset** が開かれ、2 つの新規レコードが追加され、 **Recordset** がファイルに保存されます。 **Recordset** の保存の詳細については、「 [5 章: データを更新し、保存する](chapter-5-updating-and-persisting-data.md)」を参照してください。

```vb 
 
 'BeginFabricate 
 Dim objRs As New ADODB.Recordset 
 
 With objRs.Fields 
 .Append "StudentID", adChar, 11, adFldUpdatable 
 .Append "FullName", adVarChar, 50, adFldUpdatable 
 .Append "PhoneNmbr", adVarChar, 20, adFldUpdatable 
 End With 
 
 With objRs 
 .Open 
 
 .AddNew 
 .Fields(0) = "123-45-6789" 
 .Fields(1) = "John Doe" 
 .Fields(2) = "(425) 555-5555" 
 .Update 
 
 .AddNew 
 .Fields(0) = "123-45-6780" 
 .Fields(1) = "Jane Doe" 
 .Fields(2) = "(615) 555-1212" 
 .Update 
 End With 
 
 objRs.Save App.Path & "\FabriTest.adtg", adPersistADTG 
 
 objRs.Close 
 'EndFabricate 
```

**Fields** **Append** メソッドの使用方法は、 **Recordset** オブジェクトの場合と **Record** オブジェクトの場合とで異なります。 **Record** オブジェクトの詳細については、「 [10 章: レコードとストリーム](chapter-10-records-and-streams.md)」を参照してください。

