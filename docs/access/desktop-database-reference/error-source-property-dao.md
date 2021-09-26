---
title: Error.Source プロパティ (DAO)
TOCTitle: Source Property
ms:assetid: 3c101cac-278e-025e-55a4-8a9d1ee7db3c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192677(v=office.15)
ms:contentKeyID: 48544302
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053360
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 6d8b672d20e4bbf82acbe2dd2850c2a5be256e94
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59589576"
---
# <a name="errorsource-property-dao"></a>Error.Source プロパティ (DAO)


**適用先**: Access 2013、Office 2013


エラーの発生源のオブジェクト名またはアプリケーション名を取得します。

## <a name="syntax"></a>構文

*式* .ソース

*式*: **Error** オブジェクトを表す変数。

## <a name="remarks"></a>解説

**Source** プロパティの値は、通常、オブジェクトのクラス名またはプログラム識別子になります。 **Source** プロパティを使用すると、別のアプリケーションのオブジェクトで発生したエラーをコードで処理できない場合、ユーザーにその情報を提供することができます。

たとえば、Microsoft Excel にアクセスして "ゼロによる除算" エラーを生成する場合、Microsoft Excel は **Error.Number** をそのエラーの Microsoft Excel コードに設定し **、Source** プロパティを Excel に設定します。アプリケーション。 エラーが Microsoft Office Excel によって呼び出された別のオブジェクトで発生した場合は、Microsoft Office Excel がそのエラーを解釈し、 **Error.Number** を Microsoft Office Excel コードに設定することに注意してください。 ただし、他の **Error** オブジェクトのプロパティ ( **Source** プロパティを含む) は、エラーの発生源となったオブジェクトが設定した値を保持します。 **Source** プロパティは、常にエラーの発生源となったオブジェクトの名前を格納します。

すべてのエラー情報に基づいて、エラーを適切に処理するためのコードを書くことができます。エラー処理ルーチンが失敗した場合、 **[Error](error-object-dao.md)** オブジェクトの情報を使用してユーザーにエラーに関する説明を提供でき、 **Source** プロパティや他の **Error** プロパティを使用すると、ユーザーにエラーの発生源となったオブジェクトの情報、エラーの説明などを提供することができます。


> [!NOTE]
> 他のオブジェクトへのアクセス時に発生したエラーを処理する場合、**On Error GoTo** より **On Error Resume Next** ステートメントの使用をお勧めします。オブジェクトとの各相互作用の後に **Error** オブジェクトのプロパティを確認すると、エラーの発生時にコードがアクセスしていたオブジェクトを明確にすることができます。このため、**Error.Number** にエラー コードを配置したオブジェクトや、エラーの発生源となったオブジェクト (**Error.Source**) を確認できます。

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
