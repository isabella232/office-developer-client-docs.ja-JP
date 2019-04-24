---
title: Count プロパティ (DAO)
TOCTitle: Count Property
ms:assetid: 6e2cf3e5-524f-a643-b1dc-99a4b2bb2e63
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195561(v=office.15)
ms:contentKeyID: 48545508
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6c997a437cc7a7ae1461e7308899c85dac44fbda
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314267"
---
# <a name="tabledefscount-property-dao"></a><span data-ttu-id="18870-102">Count プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="18870-102">TableDefs.Count property (DAO)</span></span>


<span data-ttu-id="18870-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="18870-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="18870-104">指定したコレクション内のオブジェクトの数を取得します。</span><span class="sxs-lookup"><span data-stu-id="18870-104">Returns the number of objects in the specified collection.</span></span> <span data-ttu-id="18870-105">読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="18870-105">Read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="18870-106">構文</span><span class="sxs-lookup"><span data-stu-id="18870-106">Syntax</span></span>

<span data-ttu-id="18870-107">*式*。量</span><span class="sxs-lookup"><span data-stu-id="18870-107">*expression* .Count</span></span>

<span data-ttu-id="18870-108">\*式\***テーブル定義**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="18870-108">*expression* A variable that represents a **TableDefs** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="18870-109">注釈</span><span class="sxs-lookup"><span data-stu-id="18870-109">Remarks</span></span>

<span data-ttu-id="18870-p102">コレクションのメンバーは 0 から順に番号が割り当てられるため、ループを使用する場合は常に 0 から始めて、 **Count** プロパティより 1 小さい値で終わらせる必要があります。 **Count** プロパティをチェックせずにコレクションのメンバーをループ処理するには、 **For Each...Next** コマンドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="18870-p102">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="18870-p103">**Count** プロパティの設定値は、Null になることはありません。値が 0 の場合、そのコレクションにはオブジェクトがありません。</span><span class="sxs-lookup"><span data-stu-id="18870-p103">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

