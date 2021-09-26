---
title: Document.Container プロパティ (DAO)
TOCTitle: Container Property
ms:assetid: aa1ace1d-f0b8-e0b0-20b6-d3e296254c51
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821451(v=office.15)
ms:contentKeyID: 48546940
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053320
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: dfb3799221bd8a5bafcc9a2f1d0aa977d00009d4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59632036"
---
# <a name="documentcontainer-property-dao"></a>Document.Container プロパティ (DAO)


**適用先**: Access 2013、Office 2013

**Document** オブジェクトが属する **[Container](container-object-dao.md)** オブジェクトの名前を返します (Microsoft Access ワークスペースのみ)。 .

## <a name="syntax"></a>構文

*式* .コンテナー

*式* Document オブジェクトを表す **変数** 。

## <a name="example"></a>例

次の使用例は、さまざまな **Document** オブジェクトの **Container** プロパティを表示します。

```vb 
Sub ContainerPropertyX() 
 
 Dim dbsNorthwind As Database 
 Dim ctrLoop As Container 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 ' Display the container name for the first Document 
 ' object in each Container object's Documents collection. 
 For Each ctrLoop In dbsNorthwind.Containers 
 Debug.Print "Document: " & ctrLoop.Documents(0).Name 
 Debug.Print " Container = " & _ 
 ctrLoop.Documents(0).Container 
 Next ctrLoop 
 
 dbsNorthwind.Close 
 
End Sub 
 
```

