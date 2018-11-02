---
title: Connections.Count プロパティ (DAO)
TOCTitle: Count Property
ms:assetid: 9b2f0aaa-785a-7fe7-15c3-aea37fdacd12
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198023(v=office.15)
ms:contentKeyID: 48546563
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 572fed8afa9eb0f40a2b4938a31e866824147c83
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25924470"
---
# <a name="connectionscount-property-dao"></a><span data-ttu-id="38ca3-102">Connections.Count プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="38ca3-102">Connections.Count property (DAO)</span></span>


<span data-ttu-id="38ca3-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="38ca3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="38ca3-104">**[Connections](connection-object-dao.md)** コレクション内の **[Connection](connections-collection-dao.md)** オブジェクトの数を返します。</span><span class="sxs-lookup"><span data-stu-id="38ca3-104">Returns the number of **[Connection](connection-object-dao.md)** objects in the **[Connections](connections-collection-dao.md)** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="38ca3-105">構文</span><span class="sxs-lookup"><span data-stu-id="38ca3-105">Syntax</span></span>

<span data-ttu-id="38ca3-106">*式*です。カウント</span><span class="sxs-lookup"><span data-stu-id="38ca3-106">*expression* .Count</span></span>

<span data-ttu-id="38ca3-107">\*式\***接続**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="38ca3-107">*expression* A variable that represents a **Connections** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="38ca3-108">注釈</span><span class="sxs-lookup"><span data-stu-id="38ca3-108">Remarks</span></span>

<span data-ttu-id="38ca3-p101">コレクションのメンバーは 0 から順に番号が割り当てられるため、ループを使用する場合は常に 0 から始めて、 **Count** プロパティより 1 小さい値で終わらせる必要があります。 **Count** プロパティをチェックせずにコレクションのメンバーをループ処理するには、 **For Each...Next** コマンドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="38ca3-p101">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="38ca3-p102">**Count** プロパティの設定値は、Null になることはありません。値が 0 の場合、そのコレクションにはオブジェクトがありません。</span><span class="sxs-lookup"><span data-stu-id="38ca3-p102">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

