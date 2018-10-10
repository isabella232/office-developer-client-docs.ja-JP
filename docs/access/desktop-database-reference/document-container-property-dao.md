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
ms.openlocfilehash: 1b943c9668ce03df029eb4a27d4ed594d00300de
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477948"
---
# <a name="documentcontainer-property-dao"></a>Document.Container プロパティ (DAO)


**適用されます**Access 2013 |。Office 2013

[Document](container-object-dao.md) オブジェクトが属する ****Container**** オブジェクトの名前を返します (Microsoft Access ワークスペースのみ)。

## <a name="syntax"></a>構文

*式*です。コンテナー

*式***ドキュメント**オブジェクトを表す変数です。

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

