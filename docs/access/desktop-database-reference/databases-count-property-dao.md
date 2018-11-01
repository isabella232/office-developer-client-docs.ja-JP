---
title: Databases.Count プロパティ (DAO)
TOCTitle: Count Property
ms:assetid: 7c542b17-9806-e00e-8cbd-58d6d17e98c4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196364(v=office.15)
ms:contentKeyID: 48545831
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b1860f1719b4e26ab192450c66d610517f0ca9a6
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868645"
---
# <a name="databasescount-property-dao"></a><span data-ttu-id="7d60b-102">Databases.Count プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="7d60b-102">Databases.Count Property (DAO)</span></span>


<span data-ttu-id="7d60b-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="7d60b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7d60b-p101">指定したコレクション内のオブジェクトの数を取得します。値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="7d60b-p101">Returns the number of objects in the specified collection. Read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d60b-106">構文</span><span class="sxs-lookup"><span data-stu-id="7d60b-106">Syntax</span></span>

<span data-ttu-id="7d60b-107">*式*です。カウント</span><span class="sxs-lookup"><span data-stu-id="7d60b-107">*expression* .Count</span></span>

<span data-ttu-id="7d60b-108">\*式\***データベース**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="7d60b-108">*expression* A variable that represents a **Databases** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d60b-109">注釈</span><span class="sxs-lookup"><span data-stu-id="7d60b-109">Remarks</span></span>

<span data-ttu-id="7d60b-p102">コレクションのメンバーは 0 から順に番号が割り当てられるため、ループを使用する場合は常に 0 から始めて、 **Count** プロパティより 1 小さい値で終わらせる必要があります。 **Count** プロパティをチェックせずにコレクションのメンバーをループ処理するには、 **For Each...Next** コマンドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="7d60b-p102">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="7d60b-p103">**Count** プロパティの設定値は、Null になることはありません。値が 0 の場合、そのコレクションにはオブジェクトがありません。</span><span class="sxs-lookup"><span data-stu-id="7d60b-p103">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

