---
title: Recordsets プロパティ (DAO)
TOCTitle: Count Property
ms:assetid: 4362aa16-c8e9-e517-887e-c4532bd1eef9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192940(v=office.15)
ms:contentKeyID: 48544500
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a81c1ede8a3afb95e39b2c33fb8112119faf8bd8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309291"
---
# <a name="recordsetscount-property-dao"></a><span data-ttu-id="90601-102">Recordsets プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="90601-102">Recordsets.Count property (DAO)</span></span>


<span data-ttu-id="90601-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="90601-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="90601-104">指定したコレクション内のオブジェクトの数を取得します。</span><span class="sxs-lookup"><span data-stu-id="90601-104">Returns the number of objects in the specified collection.</span></span> <span data-ttu-id="90601-105">整数型 ( **Integer**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="90601-105">Read-only **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="90601-106">構文</span><span class="sxs-lookup"><span data-stu-id="90601-106">Syntax</span></span>

<span data-ttu-id="90601-107">*式*。量</span><span class="sxs-lookup"><span data-stu-id="90601-107">*expression* .Count</span></span>

<span data-ttu-id="90601-108">\*式\***recordset**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="90601-108">*expression* A variable that represents a **Recordsets** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="90601-109">注釈</span><span class="sxs-lookup"><span data-stu-id="90601-109">Remarks</span></span>

<span data-ttu-id="90601-p102">コレクションのメンバーは 0 から順に番号が割り当てられるため、ループを使用する場合は常に 0 から始めて、 **Count** プロパティより 1 小さい値で終わらせる必要があります。 **Count** プロパティをチェックせずにコレクションのメンバーをループ処理するには、 **For Each...Next** コマンドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="90601-p102">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="90601-p103">**Count** プロパティの設定値は、Null になることはありません。値が 0 の場合、そのコレクションにはオブジェクトがありません。</span><span class="sxs-lookup"><span data-stu-id="90601-p103">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

