---
title: TableDefs.Count プロパティ (DAO)
TOCTitle: Count Property
ms:assetid: 6e2cf3e5-524f-a643-b1dc-99a4b2bb2e63
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195561(v=office.15)
ms:contentKeyID: 48545508
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 88a38180973b83232c324d052db0548cb308740a
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923771"
---
# <a name="tabledefscount-property-dao"></a><span data-ttu-id="fe5f8-102">TableDefs.Count プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="fe5f8-102">TableDefs.Count property (DAO)</span></span>


<span data-ttu-id="fe5f8-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="fe5f8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fe5f8-p101">指定したコレクション内のオブジェクトの数を取得します。値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="fe5f8-p101">Returns the number of objects in the specified collection. Read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe5f8-106">構文</span><span class="sxs-lookup"><span data-stu-id="fe5f8-106">Syntax</span></span>

<span data-ttu-id="fe5f8-107">*式*です。カウント</span><span class="sxs-lookup"><span data-stu-id="fe5f8-107">*expression* .Count</span></span>

<span data-ttu-id="fe5f8-108">\*式\***テーブル定義**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="fe5f8-108">*expression* A variable that represents a **TableDefs** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe5f8-109">注釈</span><span class="sxs-lookup"><span data-stu-id="fe5f8-109">Remarks</span></span>

<span data-ttu-id="fe5f8-p102">コレクションのメンバーは 0 から順に番号が割り当てられるため、ループを使用する場合は常に 0 から始めて、 **Count** プロパティより 1 小さい値で終わらせる必要があります。 **Count** プロパティをチェックせずにコレクションのメンバーをループ処理するには、 **For Each...Next** コマンドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="fe5f8-p102">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="fe5f8-p103">**Count** プロパティの設定値は、Null になることはありません。値が 0 の場合、そのコレクションにはオブジェクトがありません。</span><span class="sxs-lookup"><span data-stu-id="fe5f8-p103">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

