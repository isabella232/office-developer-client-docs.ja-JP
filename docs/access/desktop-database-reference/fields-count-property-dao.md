---
title: Fields プロパティ (DAO)
TOCTitle: Count Property
ms:assetid: 574de1db-2640-159b-7756-28c37acc9f83
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194261(v=office.15)
ms:contentKeyID: 48544969
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 99eb21ba4f4ef13c902fc0d029dba59c30066853
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292546"
---
# <a name="fieldscount-property-dao"></a><span data-ttu-id="aee1c-102">Fields プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="aee1c-102">Fields.Count property (DAO)</span></span>


<span data-ttu-id="aee1c-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="aee1c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="aee1c-104">指定したコレクション内のオブジェクトの数を取得します。</span><span class="sxs-lookup"><span data-stu-id="aee1c-104">Returns the number of objects in the specified collection.</span></span> <span data-ttu-id="aee1c-105">整数型 ( **Integer**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="aee1c-105">Read-only **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="aee1c-106">構文</span><span class="sxs-lookup"><span data-stu-id="aee1c-106">Syntax</span></span>

<span data-ttu-id="aee1c-107">*式*。量</span><span class="sxs-lookup"><span data-stu-id="aee1c-107">*expression* .Count</span></span>

<span data-ttu-id="aee1c-108">\*式\***Fields**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="aee1c-108">*expression* A variable that represents a **Fields** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="aee1c-109">注釈</span><span class="sxs-lookup"><span data-stu-id="aee1c-109">Remarks</span></span>

<span data-ttu-id="aee1c-p102">コレクションのメンバーは 0 から順に番号が割り当てられるため、ループを使用する場合は常に 0 から始めて、 **Count** プロパティより 1 小さい値で終わらせる必要があります。 **Count** プロパティをチェックせずにコレクションのメンバーをループ処理するには、 **For Each...Next** コマンドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="aee1c-p102">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="aee1c-p103">**Count** プロパティの設定値は、Null になることはありません。値が 0 の場合、そのコレクションにはオブジェクトがありません。</span><span class="sxs-lookup"><span data-stu-id="aee1c-p103">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

