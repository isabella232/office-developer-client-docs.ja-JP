---
title: Databases.Count プロパティ (DAO)
TOCTitle: Count Property
ms:assetid: 7c542b17-9806-e00e-8cbd-58d6d17e98c4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196364(v=office.15)
ms:contentKeyID: 48545831
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 189d34a5ede5965d3c241c742e21faf15f8077c8
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477858"
---
# <a name="databasescount-property-dao"></a><span data-ttu-id="aa75a-102">Databases.Count プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="aa75a-102">Databases.Count Property (DAO)</span></span>


<span data-ttu-id="aa75a-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="aa75a-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="aa75a-p101">指定したコレクション内のオブジェクトの数を取得します。値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="aa75a-p101">Returns the number of objects in the specified collection. Read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa75a-106">構文</span><span class="sxs-lookup"><span data-stu-id="aa75a-106">Syntax</span></span>

<span data-ttu-id="aa75a-107">*式*です。カウント</span><span class="sxs-lookup"><span data-stu-id="aa75a-107">*expression* .Count</span></span>

<span data-ttu-id="aa75a-108">\*式\***データベース**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="aa75a-108">*expression* A variable that represents a **Databases** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa75a-109">注釈</span><span class="sxs-lookup"><span data-stu-id="aa75a-109">Remarks</span></span>

<span data-ttu-id="aa75a-p102">コレクションのメンバーは 0 から順に番号が割り当てられるため、ループを使用する場合は常に 0 から始めて、 **Count** プロパティより 1 小さい値で終わらせる必要があります。 **Count** プロパティをチェックせずにコレクションのメンバーをループ処理するには、 **For Each...Next** コマンドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="aa75a-p102">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="aa75a-p103">**Count** プロパティの設定値は、Null になることはありません。値が 0 の場合、そのコレクションにはオブジェクトがありません。</span><span class="sxs-lookup"><span data-stu-id="aa75a-p103">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

