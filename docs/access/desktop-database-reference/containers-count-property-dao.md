---
title: Containers.Count プロパティ (DAO)
TOCTitle: Count Property
ms:assetid: 3b0bf865-a4d5-82bb-c1a9-9957f110db4c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192657(v=office.15)
ms:contentKeyID: 48544276
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7553b0e7d64e059dfeed50f158f21f48455976d7
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699948"
---
# <a name="containerscount-property-dao"></a><span data-ttu-id="7bc00-102">Containers.Count プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="7bc00-102">Containers.Count property (DAO)</span></span>


<span data-ttu-id="7bc00-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="7bc00-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7bc00-104">**[Connections](connection-object-dao.md)** コレクション内の **[Connection](connections-collection-dao.md)** オブジェクトの数を返します。</span><span class="sxs-lookup"><span data-stu-id="7bc00-104">Returns the number of **[Connection](connection-object-dao.md)** objects in the **[Connections](connections-collection-dao.md)** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="7bc00-105">構文</span><span class="sxs-lookup"><span data-stu-id="7bc00-105">Syntax</span></span>

<span data-ttu-id="7bc00-106">*式*です。カウント</span><span class="sxs-lookup"><span data-stu-id="7bc00-106">*expression* .Count</span></span>

<span data-ttu-id="7bc00-107">*式*: **Connections** オブジェクトを表す変数。</span><span class="sxs-lookup"><span data-stu-id="7bc00-107">*expression* A variable that represents a **Connections** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="7bc00-108">注釈</span><span class="sxs-lookup"><span data-stu-id="7bc00-108">Remarks</span></span>

<span data-ttu-id="7bc00-p101">コレクションのメンバーは 0 から順に番号が割り当てられるため、ループを使用する場合は常に 0 から始めて、 **Count** プロパティより 1 小さい値で終わらせる必要があります。 **Count** プロパティをチェックせずにコレクションのメンバーをループ処理するには、 **For Each...Next** コマンドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="7bc00-p101">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="7bc00-p102">**Count** プロパティの設定値は、Null になることはありません。値が 0 の場合、そのコレクションにはオブジェクトがありません。</span><span class="sxs-lookup"><span data-stu-id="7bc00-p102">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

