---
title: ParentRow プロパティ (ADO)
TOCTitle: ParentRow property (ADO)
ms:assetid: c7520353-9428-9c8f-9d21-ff42e30e1193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249971(v=office.15)
ms:contentKeyID: 48547638
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 28f0d1c7dbc0e062ff133b9f9997f1a737c3262e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25872131"
---
# <a name="parentrow-property-ado"></a><span data-ttu-id="c94d2-102">ParentRow プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="c94d2-102">ParentRow property (ADO)</span></span>


<span data-ttu-id="c94d2-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="c94d2-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="c94d2-104">OLE DB **Row** オブジェクトのコンテナーを **ADORecordConstruction** オブジェクトに設定し、行の親が ADO **Record** オブジェクトに変換されるようにします。</span><span class="sxs-lookup"><span data-stu-id="c94d2-104">Sets the container of an OLE DB **Row** object on an **ADORecordConstruction** object, so that the parent of the row is turned into an ADO **Record** object.</span></span>

<span data-ttu-id="c94d2-105">値の設定のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="c94d2-105">Write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c94d2-106">構文</span><span class="sxs-lookup"><span data-stu-id="c94d2-106">Syntax</span></span>

<span data-ttu-id="c94d2-107">HRESULT に\_ParentRow (\[の\]IUnknown\* pParent)。</span><span class="sxs-lookup"><span data-stu-id="c94d2-107">HRESULT put\_ParentRow(\[in\] IUnknown\* pParent);</span></span>

## <a name="parameters"></a><span data-ttu-id="c94d2-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c94d2-108">Parameters</span></span>

  - <span data-ttu-id="c94d2-109">*pParent*</span><span class="sxs-lookup"><span data-stu-id="c94d2-109">*pParent*</span></span>

  - <span data-ttu-id="c94d2-110">行のコンテナー。</span><span class="sxs-lookup"><span data-stu-id="c94d2-110">A container of a row.</span></span>

## <a name="return-values"></a><span data-ttu-id="c94d2-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="c94d2-111">Return values</span></span>

<span data-ttu-id="c94d2-112">このプロパティのメソッドなどの標準の HRESULT 値を返します。\_[ok] および E\_は失敗します。</span><span class="sxs-lookup"><span data-stu-id="c94d2-112">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="c94d2-113">対象</span><span class="sxs-lookup"><span data-stu-id="c94d2-113">Applies To</span></span>

[<span data-ttu-id="c94d2-114">ADORecordConstruction</span><span class="sxs-lookup"><span data-stu-id="c94d2-114">ADORecordConstruction</span></span>](adorecordconstruction-interface-ado.md)

