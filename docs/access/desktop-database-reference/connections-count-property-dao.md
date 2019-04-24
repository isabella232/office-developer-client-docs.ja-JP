---
title: Count プロパティ (DAO)
TOCTitle: Count Property
ms:assetid: 9b2f0aaa-785a-7fe7-15c3-aea37fdacd12
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198023(v=office.15)
ms:contentKeyID: 48546563
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a286bf992116dc4ddfa71a9be8231e70b717aaa3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295759"
---
# <a name="connectionscount-property-dao"></a><span data-ttu-id="d57ba-102">Count プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="d57ba-102">Connections.Count property (DAO)</span></span>


<span data-ttu-id="d57ba-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="d57ba-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d57ba-104">**[Connections](connection-object-dao.md)** コレクション内の **[Connection](connections-collection-dao.md)** オブジェクトの数を返します。</span><span class="sxs-lookup"><span data-stu-id="d57ba-104">Returns the number of **[Connection](connection-object-dao.md)** objects in the **[Connections](connections-collection-dao.md)** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="d57ba-105">構文</span><span class="sxs-lookup"><span data-stu-id="d57ba-105">Syntax</span></span>

<span data-ttu-id="d57ba-106">*式*。量</span><span class="sxs-lookup"><span data-stu-id="d57ba-106">*expression* .Count</span></span>

<span data-ttu-id="d57ba-107">*式*: **Connections** オブジェクトを表す変数。</span><span class="sxs-lookup"><span data-stu-id="d57ba-107">*expression* A variable that represents a **Connections** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d57ba-108">注釈</span><span class="sxs-lookup"><span data-stu-id="d57ba-108">Remarks</span></span>

<span data-ttu-id="d57ba-p101">コレクションのメンバーは 0 から順に番号が割り当てられるため、ループを使用する場合は常に 0 から始めて、 **Count** プロパティより 1 小さい値で終わらせる必要があります。 **Count** プロパティをチェックせずにコレクションのメンバーをループ処理するには、 **For Each...Next** コマンドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="d57ba-p101">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="d57ba-p102">**Count** プロパティの設定値は、Null になることはありません。値が 0 の場合、そのコレクションにはオブジェクトがありません。</span><span class="sxs-lookup"><span data-stu-id="d57ba-p102">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

