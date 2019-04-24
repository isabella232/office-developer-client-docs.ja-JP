---
title: 'エラー: Description プロパティ (DAO)'
TOCTitle: Description Property
ms:assetid: 47a84bec-3258-f2c7-e1af-239da39844dc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193218(v=office.15)
ms:contentKeyID: 48544601
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053358
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 1d7e949771e764c22e93ef56059930ccf39584ab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293505"
---
# <a name="errordescription-property-dao"></a>エラー: Description プロパティ (DAO)


**適用先:** Access 2013、Office 2013
 

エラーについて説明する文字列を取得します。 これは、 **Error** オブジェクトの既定のプロパティです。

## <a name="syntax"></a>構文

*式*。Description

*式*: **Error** オブジェクトを表す変数。

## <a name="remarks"></a>解説

**Description** プロパティは、エラーの簡単な説明で構成されます。プログラムで対処できないエラー、または処理することが望ましくないエラーについては、このプロパティを使用してユーザーに警告します。

## <a name="example"></a>例

次の使用例は、エラーを強制的に発生させ、トラップし、生成された Error オブジェクトの **Description**、 **Number**、 **Source**、 **HelpContext**、および **HelpFile** の各プロパティを表示します。

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

