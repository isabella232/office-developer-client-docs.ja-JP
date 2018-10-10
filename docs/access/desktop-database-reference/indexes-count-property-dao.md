---
title: Indexes.Count プロパティ (DAO)
TOCTitle: Count Property
ms:assetid: 195ede10-f91e-50c6-6af4-b318c476b9ea
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845647(v=office.15)
ms:contentKeyID: 48543499
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f5b4dad3da2c9e6e7b8a5b719687a4b424a61dd7
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477052"
---
# <a name="indexescount-property-dao"></a><span data-ttu-id="20b32-102">Indexes.Count プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="20b32-102">Indexes.Count Property (DAO)</span></span>


<span data-ttu-id="20b32-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="20b32-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="20b32-p101">指定したコレクション内のオブジェクトの数を取得します。値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="20b32-p101">Returns the number of objects in the specified collection. Read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="20b32-106">構文</span><span class="sxs-lookup"><span data-stu-id="20b32-106">Syntax</span></span>

<span data-ttu-id="20b32-107">*式*です。カウント</span><span class="sxs-lookup"><span data-stu-id="20b32-107">*expression* .Count</span></span>

<span data-ttu-id="20b32-108">\*式\***インデックス**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="20b32-108">*expression* A variable that represents an **Indexes** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="20b32-109">注釈</span><span class="sxs-lookup"><span data-stu-id="20b32-109">Remarks</span></span>

<span data-ttu-id="20b32-p102">コレクションのメンバーは 0 から順に番号が割り当てられるため、ループを使用する場合は常に 0 から始めて、 **Count** プロパティより 1 小さい値で終わらせる必要があります。 **Count** プロパティをチェックせずにコレクションのメンバーをループ処理するには、 **For Each...Next** コマンドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="20b32-p102">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="20b32-p103">**Count** プロパティの設定値は、Null になることはありません。値が 0 の場合、そのコレクションにはオブジェクトがありません。</span><span class="sxs-lookup"><span data-stu-id="20b32-p103">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>
