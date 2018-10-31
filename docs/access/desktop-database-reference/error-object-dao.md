---
title: エラー オブジェクトのデータ アクセス オブジェクトの (DAO)
TOCTitle: Error Object
ms:assetid: e2608bc9-bece-9b47-4562-7a2689601f75
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835711(v=office.15)
ms:contentKeyID: 48548289
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 526498ee22bc82735eb3b98e633aa3d1b4cfb610
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25864103"
---
# <a name="error-object-dao"></a>Error オブジェクト (DAO)


**適用されます**Access 2013 |。Office 2013

**Error** オブジェクトにはデータ アクセス エラーに関する詳細が含まれ、各オブジェクトが DAO を扱う 1 回の操作に対応しています。

## <a name="remarks"></a>注釈

DAO を扱うすべての操作では、1 つまたは複数のエラーが生成される可能性があります。たとえば、ODBC サーバーを呼び出すと、データベース サーバーのエラー、ODBC のエラー、および DAO エラーが発生する可能性があります。このようなエラーが発生するたびに、 **DBEngine** オブジェクトの **Errors** コレクションに 1 つの **Error** オブジェクトが追加されます。したがって、単一のイベントで **Errors** コレクションに複数の **Error** オブジェクトが格納される可能性があります。

後続の DAO 操作によってエラーが生成されると、 **Errors** コレクションがクリアされ、1 つ以上の新しい **Error** オブジェクトが **Errors** コレクションに追加されます。エラーを生成しない DAO 操作は、 **Errors** コレクションには影響しません。

**Errors** コレクションの **Error** オブジェクトのセットにより、1 つのエラーが記述されます。最初の **Error** オブジェクトが最も低いレベルのエラー (作成元エラー)、2 番目が次に高いレベルのエラーで、以降同様です。たとえば、 **[Recordset](recordset-object-dao.md)** オブジェクトを開こうとしたときに ODBC エラーが発生した場合、最初の **Error** オブジェクト ( **Errors**(0)) には最も低いレベルの ODBC エラーが含まれ、後続のエラーには ODBC のさまざまなレイヤーによって返された ODBC エラーが含まれます。この場合、ODBC ドライバー マネージャー、さらに場合によってはドライバー自体が別々の **Error** オブジェクトを返します。最後の **Error** オブジェクト ( **Errors.Count-** 1) には、オブジェクトが開かれなかったことを示す DAO エラーが含まれます。

**Errors** コレクションの特定のエラーを列挙すると、エラー処理ルーチンでエラーの原因と発生源をより正確に特定し、適切な修復処理を実行できます。 **Error** オブジェクトのプロパティを参照すると、各エラーに関する次のような詳細を取得できます。

  - エラーがトラップされない場合に画面に表示されるエラー メッセージのテキストを含む **[Description](error-description-property-dao.md)** プロパティ。

  - エラー定数の長整数型 (Long integer) の値を含む **[Number](error-number-property-dao.md)** プロパティ。

  - エラーを発生させたオブジェクトを識別する **[Source](error-source-property-dao.md)** プロパティ。これは特に、ODBC データ ソースへの要求に対応する **Errors** コレクションに複数の **Error** オブジェクトがある場合に便利です。

  - エラーが発生した場合に、そのエラーについて Microsoft Windows の適切なヘルプ ファイルを示す (ある場合) **HelpFile** プロパティおよび Microsoft Windows の適切なヘルプ トピックを示す (ある場合) **HelpContext** プロパティ。
    

    > [!NOTE]
    > [!メモ] Microsoft Visual Basic for Applications (VBA) でプログラミングするときに、 **New** キーワードを使用して、オブジェクトがコレクションに追加される前にエラーが発生するオブジェクトを作成すると、新しいオブジェクトは **DBEngine** オブジェクトに関連付けられていないため、 **DBEngine** オブジェクトの **Errors** コレクションに、そのオブジェクト エラーのエントリが追加されません。 ただし、VBA の **Err** オブジェクトでエラー情報を使用できます。 データ アクセス エラーが発生する可能性がある場合、VBA エラー処理コードで **Errors** コレクションを確認する必要があります。 集中化したエラー ハンドラーを記述している場合は、VBA の **Err** オブジェクトをテストして、 **Errors** コレクションのエラー情報が該当するかどうかを調べます。 場合の**Number**プロパティ (DBEngine.Errors.Count - 1)**エラー**のコレクションの最後の要素の**Err**オブジェクトに一致する値をすることができますをクリックして一連の**Select Case**ステートメント特定の DAO エラーを識別するか、エラーが発生しました。 これらの値が一致しない場合は、 [Errors](errors-refresh-method-dao.md) コレクションに対して **Refresh** メソッドを使用します。



## <a name="example"></a>例

この例では、エラーを発生させてトラップし、 **Error** オブジェクトの **Description**、 **Number**、 **Source**、 **HelpContext**、および **HelpFile** の各プロパティを表示します。

```vb 
Sub DescriptionX() 
 
   Dim dbsTest As Database 
 
   On Error GoTo ErrorHandler 
 
   ' Intentionally trigger an error. 
   Set dbsTest = OpenDatabase("NoDatabase") 
 
   Exit Sub 
 
ErrorHandler: 
   Dim strError As String 
   Dim errLoop As Error 
 
   ' Enumerate Errors collection and display properties of  
   ' each Error object. 
   For Each errLoop In Errors 
      With errLoop 
         strError = _ 
            "Error #" & .Number & vbCr 
         strError = strError & _ 
            "  " & .Description & vbCr 
         strError = strError & _ 
            "  (Source: " & .Source & ")" & vbCr 
         strError = strError & _ 
            "Press F1 to see topic " & .HelpContext & vbCr 
         strError = strError & _ 
            "  in the file " & .HelpFile & "." 
      End With 
      MsgBox strError 
   Next 
 
   Resume Next 
 
End Sub 
 
```

