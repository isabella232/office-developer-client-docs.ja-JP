---
title: Errors コレクション (DAO)
TOCTitle: Errors Collection
ms:assetid: d42007b5-6410-14e9-baf9-9306fdef38f9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834805(v=office.15)
ms:contentKeyID: 48547929
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cf8e891936d4f8bd03535fa199026bc4ad8ff9ba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293414"
---
# <a name="errors-collection-dao"></a>Errors コレクション (DAO)


**適用先:** Access 2013、Office 2013

**Errors** コレクションには、格納されているすべての **Error** オブジェクトが含まれ、それぞれが DAO に関する単一の操作に対応しています。

## <a name="remarks"></a>注釈

DAO オブジェクトに関係するすべての操作では、1 つ以上のエラーが発生する場合があります。 エラーが発生するたびに、1 つ以上の **Error** オブジェクトが **DBEngine** オブジェクトの **Errors** コレクションに追加されます。 別の DAO 操作によってエラーが発生すると、 **Errors** コレクションがクリアされ、 **Errors** コレクションに **Error** オブジェクトの新しいセットが配置されます。 **Errors** コレクションの最高値のオブジェクト (DBEngine.Errors.Count - 1) は、Microsoft Visual Basic for Applications (VBA) の **Err** オブジェクトがレポートするエラーに対応します。

エラーを生成しない DAO 操作が **Errors** コレクションに影響を及ぼすことはありません。

**Errors** コレクションの要素は、一般に他のコレクション内にあるので、追加されません。したがって、 **Errors** コレクションでは、 **Append** メソッドと **Delete** メソッドはサポートされません。

**Errors** コレクションの **Error** オブジェクトのセットは、単一のエラーを表します。最初の **Error** オブジェクトが最低レベルのエラーで、2 番目のエラーが次に高いレベルのエラーになり、その後も同様です。たとえば、 **[Recordset](recordset-object-dao.md)** オブジェクトを開く際に ODBC エラーが発生すると、最初のエラー オブジェクトに最低レベルの ODBC エラーが含まれ、その後のエラーに ODBC のさまざまなレイヤーが返す ODBC エラーが含まれます。この場合、ODBC ドライバー マネージャーおよびドライバー自体も個別の **Error** オブジェクトを返します。最後の **Error** オブジェクトには、オブジェクトを開くことができなかったことを示す DAO エラーが含まれます。

**Errors** コレクションの特定のエラーを列挙することにより、エラー処理ルーチンは、エラーの原因、発生源、および適切な回復手順をより正確に特定できます。


> [!NOTE]
> [!メモ] **New** キーワードを使用してオブジェクトを作成し、 **Errors** コレクションに追加される前またはその最中にエラーが発生した場合、新しいオブジェクトは **DBEngine** オブジェクトに関連付けられていないので、このオブジェクトに関するエラー情報はコレクションに追加されません。ただし、このエラー情報は、VBA の **Err** オブジェクトで参照できます。

## <a name="example"></a>例

次の使用例は、エラーを強制的に発生させ、トラップし、生成された **Error** オブジェクトの **Description**、 **Number**、 **Source**、 **HelpContext**、および **HelpFile** の各プロパティを表示します。

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
 " " & .Description & vbCr 
 strError = strError & _ 
 " (Source: " & .Source & ")" & vbCr 
 strError = strError & _ 
 "Press F1 to see topic " & .HelpContext & vbCr 
 strError = strError & _ 
 " in the file " & .HelpFile & "." 
 End With 
 MsgBox strError 
 Next 
 
 Resume Next 
 
End Sub 
 
```

