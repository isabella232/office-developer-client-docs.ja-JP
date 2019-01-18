---
title: QueryDef.Updatable プロパティ (DAO)
TOCTitle: Updatable Property
ms:assetid: 9b978b7d-1d76-ff27-a032-dd94660fb088
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198056(v=office.15)
ms:contentKeyID: 48546575
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c5321e834f1dd5ed663033cacb530962d7beeb5a
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28713367"
---
# <a name="querydefupdatable-property-dao"></a><span data-ttu-id="eb941-102">QueryDef.Updatable プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="eb941-102">QueryDef.Updatable property (DAO)</span></span>


<span data-ttu-id="eb941-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="eb941-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="eb941-p101">DAO オブジェクトを変更できるかどうかを示す値を取得します。値の取得のみ可能です。ブール型 ( **Boolean**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="eb941-p101">Returns a value that indicates whether you can change a DAO object. Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb941-106">構文</span><span class="sxs-lookup"><span data-stu-id="eb941-106">Syntax</span></span>

<span data-ttu-id="eb941-107">*式*です。更新可能です</span><span class="sxs-lookup"><span data-stu-id="eb941-107">*expression* .Updatable</span></span>

<span data-ttu-id="eb941-108">\*式\***クエリ定義**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="eb941-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb941-109">注釈</span><span class="sxs-lookup"><span data-stu-id="eb941-109">Remarks</span></span>

<span data-ttu-id="eb941-110">クエリ結果の \*\*\*\*Recordset\*\*\*\* オブジェクトを更新できないときでも、クエリ定義を更新できる場合、 **QueryDef** オブジェクトの [Updatable](recordset-object-dao.md) プロパティは **True** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="eb941-110">The **Updatable** property of a **QueryDef** object is set to **True** if the query definition can be updated, even if the resulting **[Recordset](recordset-object-dao.md)** object isn't updatable.</span></span>

