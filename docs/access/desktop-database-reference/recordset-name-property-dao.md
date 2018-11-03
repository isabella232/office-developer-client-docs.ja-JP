---
title: Recordset.Name プロパティ (DAO)
TOCTitle: Name Property
ms:assetid: 2a80b994-a135-cd61-3906-17dfa0580110
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192067(v=office.15)
ms:contentKeyID: 48543910
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 36e66bc377846259b1e7279a1563e3862ea9c0eb
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25930904"
---
# <a name="recordsetname-property-dao"></a><span data-ttu-id="9836f-102">Recordset.Name プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="9836f-102">Recordset.Name property (DAO)</span></span>


<span data-ttu-id="9836f-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="9836f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9836f-p101">指定したオブジェクトの名前を取得します。値の取得のみ可能です。文字列型 ( **String**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="9836f-p101">Returns the name of the specified object. Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="9836f-106">構文</span><span class="sxs-lookup"><span data-stu-id="9836f-106">Syntax</span></span>

<span data-ttu-id="9836f-107">*式*です。名</span><span class="sxs-lookup"><span data-stu-id="9836f-107">*expression* .Name</span></span>

<span data-ttu-id="9836f-108">\*式\***レコード セット**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="9836f-108">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9836f-109">注釈</span><span class="sxs-lookup"><span data-stu-id="9836f-109">Remarks</span></span>

<span data-ttu-id="9836f-110">SQL ステートメントを使用して開いた **Recordset** オブジェクトの **Name** プロパティは、その SQL ステートメントの先頭 256 文字となります。</span><span class="sxs-lookup"><span data-stu-id="9836f-110">The **Name** property of a **Recordset** object opened by using an SQL statement is the first 256 characters of the SQL statement.</span></span>

