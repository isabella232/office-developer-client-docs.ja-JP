---
title: QueryDef プロパティ (DAO)
TOCTitle: Updatable Property
ms:assetid: 9b978b7d-1d76-ff27-a032-dd94660fb088
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198056(v=office.15)
ms:contentKeyID: 48546575
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c5321e834f1dd5ed663033cacb530962d7beeb5a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303333"
---
# <a name="querydefupdatable-property-dao"></a><span data-ttu-id="ba290-102">QueryDef プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="ba290-102">QueryDef.Updatable property (DAO)</span></span>


<span data-ttu-id="ba290-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="ba290-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ba290-104">DAO オブジェクトを変更できるかどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="ba290-104">Returns a value that indicates whether you can change a DAO object.</span></span> <span data-ttu-id="ba290-105">値の取得のみ可能なブール型 (**Boolean**) の値です。</span><span class="sxs-lookup"><span data-stu-id="ba290-105">Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba290-106">構文</span><span class="sxs-lookup"><span data-stu-id="ba290-106">Syntax</span></span>

<span data-ttu-id="ba290-107">*式*。できる</span><span class="sxs-lookup"><span data-stu-id="ba290-107">*expression* .Updatable</span></span>

<span data-ttu-id="ba290-108">\*式\***QueryDef**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="ba290-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba290-109">注釈</span><span class="sxs-lookup"><span data-stu-id="ba290-109">Remarks</span></span>

<span data-ttu-id="ba290-110">クエリ結果の **[Recordset](recordset-object-dao.md)** オブジェクトを更新できないときでも、クエリ定義を更新できる場合、**QueryDef** オブジェクトの **Updatable** プロパティは **True** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="ba290-110">The **Updatable** property of a **QueryDef** object is set to **True** if the query definition can be updated, even if the resulting **[Recordset](recordset-object-dao.md)** object isn't updatable.</span></span>

