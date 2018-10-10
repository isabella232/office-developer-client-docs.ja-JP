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
# <a name="documentcontainer-property-dao"></a><span data-ttu-id="c9586-102">Document.Container プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="c9586-102">Document.Container Property (DAO)</span></span>


<span data-ttu-id="c9586-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="c9586-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c9586-p101">[Document](container-object-dao.md) オブジェクトが属する \*\*\*\*Container\*\*\*\* オブジェクトの名前を返します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="c9586-p101">Returns the name of the **[Container](container-object-dao.md)** object to which a **Document** object belongs (Microsoft Access workspaces only). .</span></span>

## <a name="syntax"></a><span data-ttu-id="c9586-106">構文</span><span class="sxs-lookup"><span data-stu-id="c9586-106">Syntax</span></span>

<span data-ttu-id="c9586-107">*式*です。コンテナー</span><span class="sxs-lookup"><span data-stu-id="c9586-107">*expression* .Container</span></span>

<span data-ttu-id="c9586-108">\*式\***ドキュメント**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="c9586-108">*expression* A variable that represents a **Document** object.</span></span>

## <a name="example"></a><span data-ttu-id="c9586-109">例</span><span class="sxs-lookup"><span data-stu-id="c9586-109">Example</span></span>

<span data-ttu-id="c9586-110">次の使用例は、さまざまな **Document** オブジェクトの **Container** プロパティを表示します。</span><span class="sxs-lookup"><span data-stu-id="c9586-110">This example displays the **Container** property for a variety of **Document** objects.</span></span>

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

